
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!-- saved from url=(0024)http://www.hf-relay.com/ -->
<html xmlns="http://www.w3.org/1999/xhtml">
<body id="indexbody">


	{ms:include filename=header.html/}
	<div class="wrapper">
		<div class="iBan">
			<div class="iBanScreen">
				<ul class="ibanImg">
				{ms:arclist size=3 titlelen=45 typeid=167}
				<li
					style="background: url(/mcms/[field.litpic/]) no-repeat center bottom;"></li>
				{/ms:arclist}
				</ul>

				<div class="num">
					<a class="cur"></a> <a class=""></a> <a class=""></a>
				</div>
			</div>
		</div>
		<div class="i_brand PNG">
			<h1 class="head">
				<!--<a href="/">新品推荐</a>-->
			</h1>
			<div class="cont">

				<ul class="brandList"
					style="width: 999999px; position: relative; left: -417px;">
					{ms:arclist typeid=150 size=10 flag=c}
					<li style="float: left; list-style: none; margin-right: 12px;">
						<a
						href="[field.link/]"
						target="_blank"> <img alt="" src="/mcms/[field.litpic/]"
							title=""></a>
					</li> {/ms:arclist}
				</ul>

			</div>
		</div>
		<div class="sycon">
			<!--关于我们-->
			<div class="sy_uang">
				<a
					href="{ms:global.url/}/149/152/index.html"><img
					src="{ms:globalskin.url/}/img/con_img01.jpg" width="318"
					height="125" class="imgtop"></a>
				<div class="bon">
					<div class="tit">关于我们</div>
					<div class="kuangcon2">
						<b>明光万佳联众电子有限公司</b>致力于电力、电能表磁保持继电器的研发、生产与销售，公司凭借几十年的继电器研发和制造经验，现已发展成国内最大的...
						<a
							href="{ms:global.url/}/149/152/index.html">查看全部</a>
					</div>
					<div class="clear"></div>
				</div>
				<div class="clear"></div>
			</div>
			<!--新闻资讯-->
			<div class="sy_uang">
				<a
					href="{ms:global.url/}/151/index.html"><img
					src="{ms:globalskin.url/}/img/con_img02.jpg" width="318"
					height="125" class="imgtop"></a>
				<div class="bon">
					<div class="tit1">
						<span><a
							href="{ms:global.url/}/151/index.html"><img
								src="{ms:globalskin.url/}/img/con_j.jpg" width="19" height="19"
								align="left"></a></span>新闻资讯
					</div>
					<div class="newcon">
						<ul>
						{ms:arclist typeid=151 size=4 titlelen=20} 
							<li><span>[field.date fmt=yyyy-MM-dd/]</span>  <a
								href="[field.link/]"
								target="_blank">[field.title/]</a></li>
						{/ms:arclist}	
						</ul>
					</div>
				</div>
			</div>
			<!--经销商专区-->
			<div class="sy_uang" style="margin-right: 0px;">
				<a
					href="{ms:global.url/}/172/173/index.html"><img
					src="{ms:globalskin.url/}/img/con_img03.jpg" width="318"
					height="125" class="imgtop"></a>
				<div class="bon">
					<div class="tit">企业文化</div>
					<div class="kuangcon3">
						<p>万佳成立三十余年来，坚持以创新求突破、以品牌求信誉、以特色求市场、以营销求活力、以管理求效益、以诚心求发展..</p>
						<p style="text-align: right;">
							<!-- <img src="{ms:globalskin.url/}/img/con_j2.jpg" width="8" height="8"> -->
							<a
								href="{ms:global.url/}/172/173/index.html"
								style="padding-left: 5px; color: #ea4820;"></a>
						</p>
					</div>
				</div>
			</div>
			<div class="clear"></div>
		</div>
	</div>
	<script type="text/javascript">
		$(function() {
			var sw = 0;

			var bannerscount = $(".ibanImg li").length;
			$(".iBanScreen .num a").mouseover(function() {
				sw = $(".num a").index(this);
				myShow(sw);
			});
			function myShow(i) {
				$(".iBanScreen .num a").eq(i).addClass("cur").siblings("a")
						.removeClass("cur");
				$(".iBanScreen ul li").eq(i).stop(true, true).fadeIn(600)
						.siblings("li").fadeOut(600);
			}

			$(".iBanScreen").hover(function() {
				if (myTime) {
					clearInterval(myTime);
				}
			}, function() {
				myTime = setInterval(function() {
					myShow(sw)
					sw++;
					if (sw == bannerscount) {
						sw = 0;
					}
				}, 8000);
			});
			var myTime = setInterval(function() {
				myShow(sw);
				sw++;
				if (sw == bannerscount) {
					sw = 0;
				}
			}, 8000);
			myShow(sw);
			$('.i_brand .brandList').bxCarousel({
				display_num : 6,
				move : 3,
				auto : true,
				prev_image : '{ms:globalskin.url/}/img/icon_arrow_left.gif',
				next_image : '{ms:globalskin.url/}/img/icon_arrow_right.gif',
				margin : 12,
				auto_hover : true
			});
		});
	</script>
	<script type="text/javascript">
		$(function() {
			var len = $("#page_nav td.manu_sub_over").length;
			if (len == 0) {
				$("#page_nav td").eq(0).addClass("manu_sub_over");
			}

		});
	</script>
	{ms:include filename=footer.html/}
</body>
</html>
