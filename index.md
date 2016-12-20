
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <script src="http://cdn.bootcss.com/three.js/r83/three.min.js"></script>
</head>

<body>
</body>
<script>

var scene, camera, renderer;
scene = new THREE.Scene();
camera = new THREE.PerspectiveCamera(50, window.innerWidth / window.innerHeight);
camera.position.set(3,4,5);
camera.lookAt(new THREE.Vector3(0,0,0));
scene.add(camera);

var geometry = new THREE.BoxGeometry(1,1,1);
var material = new THREE.MeshNormalMaterial();
var cube = new THREE.Mesh(geometry, material);
scene.add(cube);

renderer = new THREE.WebGLRenderer({ alpha: true });
renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);

function render() {
requestAnimationFrame(render);

    cube.rotation.x += 0.01;
    cube.rotation.y += 0.01;

    renderer.render(scene, camera);
}
render();
</script>

</html>

