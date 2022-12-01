Thanks for downloading this template!

Template Name: Yummy
Template URL: https://bootstrapmade.com/yummy-bootstrap-restaurant-website-template/
Author: BootstrapMade.com
License: https://bootstrapmade.com/license/

anlysist table for Food Website
banner header
    tbl_banner_header{
        id,
        name,
        title,
        thumbnail,
        url
    }
    tbl_about {
        id,
        banner,
        text1,
        text2,
        text3,
        text4,
        b_vdo,
        url
    }
our menu
    tbl_starter{
        id,
        starters_name,
        thumbnail,
        food_name,
        title,
        price
    }
    tbl_breakfast{
        id,
        breakfast_name,
        thumbnail,
        food_name,
        title,
        price
    }
     tbl_lunch{
        id,
        lunch_name,
        thumbnail,
        food_name,
        title,
        price
    }
    tbl_dinner{
        id,
        dinner_name,
        thumbnail,
        food_name,
        title,
        price
    }
Event
    tbl_event{
        id,
        thumbnail,
        event_name,
        price,
        title
    }
chefs
    tbl_chefts{
        id,
        chefts_name,
        thumbnail,
        position,
        title
    }
gallerry
    tbl_gallery{
        id,
        thumbnails
    }
Address
    tbl_address{
        id,
        address,
        email,
        number_phone,
        Op_hours
    }
Contact 
    tbl_contact{
        id,
        name,
        email,
        subject,
        message
    }
our social
    tbl_socail{
        id,
        twitter,
        facebook,
        intragram,
        in
   }
Book a table
    tbl_book{
        id,
        thumbnail,
        name,
        email,
        phone,
        date,
        time,
        people,
        message
    }
Testimonials Section
    tbl_Testimonials{
        id,
        name,
        thumbnail,
        title,
        skill,
    }


     <?php
    $sql_select = " SELECT * FROM `tbl_banner_header` ";
    $sql_result = $conn->query($sql_select);
    while($row = mysqli_fetch_assoc($sql_result)){
      echo '
      <section id="hero" class="hero d-flex align-items-center section-bg">
      <div class="container">
        <div class="row justify-content-between gy-5">
          <div
            class="col-lg-5 order-2 order-lg-1 d-flex flex-column justify-content-center align-items-center align-items-lg-start text-center text-lg-start">
            <h2 data-aos="fade-up">'.$row['name'].'</h2>
            <p data-aos="fade-up" data-aos-delay="100">'.$row['title'].'</p>
            <div class="d-flex" data-aos="fade-up" data-aos-delay="200">
              <a href="#book-a-table" class="btn-book-a-table">Book a Table</a>
              <a href="'.$row['url'].'"
                class="glightbox btn-watch-video d-flex align-items-center"><i class="bi bi-play-circle"></i><span>Watch
                  Video</span></a>
            </div>
          </div>
          <div class="col-lg-5 order-1 order-lg-2 text-center text-lg-start">
            <img src="assets/img/'.$row['thumbnail'].'" class="img-fluid" alt="" data-aos="zoom-out" data-aos-delay="300">
          </div>
        </div>
      </div>
    </section><!-- End Hero Section -->
      ';
    }
  ?>