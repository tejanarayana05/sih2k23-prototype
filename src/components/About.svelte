<script>
  // import Group from '../../Components/Group.svg';
</script>

<div class="background absolute">

    
    <div class="relative">
      <div class="about_content_section">
          <div class="first-icon">
            <img src="about_icon2.svg" alt="">
            <div class="first-heading">
              <h1>Lorem, ipsum dolor.</h1>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae rerum temporibus et sunt dolorum quaerat fugit animi voluptatibus, facilis quas?</p>
            </div>
          </div>

          <div class="second-icon">
            <img src="about_icon1.svg" alt="">
            <div class="second-heading">
              <h1 class="">Lorem ipsum dolor sit amet.</h1>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo deserunt, quis fugit enim ratione voluptas laboriosam consectetur dolore nobis dicta, iusto nihil cum minus aperiam praesentium! Magnam, cum quas! Expedita!</p>            </div>
          </div>

        <div class="agenda">
          <h2 class="">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsam quo sunt, magni asperiores molestiae, vitae saepe incidunt est earum aut odio. Minima, praesentium? Nihil nemo obcaecati sed, explicabo accusantium deleniti!</p>
          <ul>
            <li>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto nesciunt natus blanditiis atque cum optio eligendi dolore quis voluptates! Placeat doloribus quas nihil debitis obcaecati necessitatibus earum, quos nam ipsa!</li>
            <li>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Praesentium, accusantium in. Odit aliquid expedita magnam iusto omnis numquam quos saepe ipsa corrupti laudantium, tempore suscipit. Tempora, eaque id. Nesciunt, illo?</li>
            <li>Giving a platform for those building on a truly scalable blockchain and those facilitating the development</li>
            <li>lOREM</li>
            <li>Connecting enterprises and investors to blockchain developers</li>
          </ul>
        </div>
      </div>
    </div>
</div>

<!-- Your Svelte component -->

<!-- Your CSS file -->

<style>
  .background {
    font-family: Space Grotesk;
    background: radial-gradient(70% 50% at 1% -1%, #c7dcec 0%, #65849d 3.06%, #26679D 14.58%, #1C4C73 32.81%, #13344F 52.08%, #10013C 100%);
    position: relative;
    width: 100%;
    overflow: hidden;
  }
  .about_content_section{
    margin: 8%;
  }
  .group-image,
  .vector-image1,
  .vector-image2,
  .vector-image3,
  .curves {
    position: absolute;
    display: inline-block;
    width: 100%;
    height: auto;
    max-width: none;
    max-height: none;
  }

  .group-image{
    bottom: 0;
    height: auto;
  }

  .vector-image1{
    width: 30%;
    height: auto;
    right: -5%;
    top: 0;
  }

  .vector-image2{
    width: 20%;
    height: auto;
    top: 30%;
    right: 10%;
  }
  
  .vector-image3{
    width: 20%;
    height: auto;
    top: 50%;
    right: -8%;
  }
  .curves{
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: auto;
  }

  .first-heading,
  .second-heading{
    margin-bottom: 70px;
    display: flex;
    flex-direction: column;
    width: 70%;
    color: #FFFFFF;
  }

  .first-icon,
  .second-icon{
    display: flex;
    flex-direction: row;
  }

  .first-icon img,
  .second-icon img{
    height: 50%;
    margin-right: 40px;
    /* margin-top: 12px; */
  }

  h1{
    font-size: 20px;
    font-weight: 600;
    /* line-height: 56px; */
    /* letter-spacing: 0em; */
    text-align: left;
    /* height: 56px; */
    background: linear-gradient(274.72deg, #5800FF -33.68%, #0077FF -10.34%, #09FFFF 81.48%);
    -webkit-background-clip: text; 
    -webkit-text-fill-color: transparent; 
    color: #09FFFF;
    font-family: Space Grotesk;
    font-size: 40px;
  }

  .first-heading p,
  .second-heading p{
    height: auto;
    font-family: Rubik;
    font-size: 15px;
    font-weight: 400;
    margin-top: 30px;
  }
  .agenda h2{
    font-weight: 500;
    font-size: 40px;
    margin-bottom: 20px;
    color: #FFFFFF;
  }
  .agenda{
    color: #FFFFFF;
    width: 70%;
    margin-left: 70px;
    margin-top: 50px;
  }
  .agenda p{
    font-size: 15px;
  }
  .agenda ul{
    margin-top: 20px;
    list-style-type: disc;
    font-size: 15px;
    margin-left: 30px;
  }
  .agenda li{
    margin-left: 2px;
  }

  /* Media Queries */

  @media only screen and (max-width: 480px) {
    .first-icon img,
    .second-icon img{
      height: 35px;
      margin-right: 20px;
    }
    .first-heading,
    .second-heading{
      width: 100%;
    }
    .first-heading p,
    .second-heading p{
      /* height: auto; */
      margin-left: 0;
      font-family: Rubik;
      font-size: 15px;
      font-weight: 400;
      margin-top: 20px;
  }
    .first-icon h1,
    .second-icon h1 {
      font-size: 20px;
    }

    .agenda h2 {
      margin-left: 0;
      font-size: 24px;
      margin-bottom: 20px;
    }
    .agenda{
      color: #FFFFFF;
      width: 80%;
      margin-left: 50px;
      margin-top: 0px;
    }
    .agenda p {
      font-size: 14px;
      line-height: 22px;
    }
    .agenda li {
      font-size: 14px;
      margin: 0;
    }
  }
</style>