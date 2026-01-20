<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vịnh Hạ Long - Kỳ quan thiên nhiên thế giới</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Noto+Serif+Viet:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #1a5fb4;
            --secondary-color: #e6b325;
            --text-color: #333;
            --light-bg: #f5f9ff;
            --dark-bg: #0d2b5c;
            --transition: all 0.3s ease;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: #fff;
        }

        h1, h2, h3, h4 {
            font-family: 'Noto Serif Viet', serif;
            color: var(--dark-bg);
            margin-bottom: 1rem;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(rgba(13, 43, 92, 0.9), rgba(13, 43, 92, 0.8)), url('https://images.unsplash.com/photo-1528127269322-539801943592?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 20px 0;
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
        }

        .header-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 20px;
            background-color: rgba(0, 0, 0, 0.4);
            border-radius: 15px;
            backdrop-filter: blur(5px);
        }

        .logo {
            font-size: 2.5rem;
            font-weight: 700;
            color: white;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .logo i {
            color: var(--secondary-color);
        }

        .tagline {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--secondary-color);
            color: var(--dark-bg);
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            margin-top: 20px;
            transition: var(--transition);
            border: 2px solid var(--secondary-color);
        }

        .cta-button:hover {
            background-color: transparent;
            color: var(--secondary-color);
        }

        /* Navigation */
        nav {
            background-color: var(--dark-bg);
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            padding: 5px 0;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--secondary-color);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--secondary-color);
            left: 0;
            bottom: 0;
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .mobile-toggle {
            display: none;
            font-size: 1.5rem;
            color: white;
            cursor: pointer;
        }

        /* Main Content */
        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.2rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background-color: var(--secondary-color);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }

        /* Link Guide Section */
        .link-guide {
            background-color: var(--light-bg);
            padding: 60px 0;
        }

        .guide-container {
            max-width: 900px;
            margin: 0 auto;
            background-color: white;
            border-radius: 15px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .guide-step {
            margin-bottom: 30px;
            padding: 20px;
            border-left: 4px solid var(--primary-color);
            background-color: #f9f9f9;
            border-radius: 0 8px 8px 0;
        }

        .guide-step h3 {
            color: var(--primary-color);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .guide-step h3 i {
            color: var(--secondary-color);
        }

        .link-list {
            list-style-type: none;
            margin-top: 15px;
        }

        .link-list li {
            margin-bottom: 12px;
            padding: 10px;
            background-color: white;
            border-radius: 5px;
            border: 1px solid #eee;
            transition: var(--transition);
        }

        .link-list li:hover {
            border-color: var(--primary-color);
            transform: translateX(5px);
        }

        .link-list a {
            color: var(--dark-bg);
            text-decoration: none;
            font-weight: 500;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .link-list a:hover {
            color: var(--primary-color);
        }

        .link-list .link-icon {
            color: var(--primary-color);
            font-size: 0.9rem;
        }

        .quick-links {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .quick-link-card {
            background-color: var(--dark-bg);
            color: white;
            border-radius: 10px;
            padding: 25px;
            text-align: center;
            transition: var(--transition);
            text-decoration: none;
            display: block;
        }

        .quick-link-card:hover {
            background-color: var(--primary-color);
            transform: translateY(-5px);
        }

        .quick-link-card i {
            font-size: 2.5rem;
            color: var(--secondary-color);
            margin-bottom: 15px;
        }

        .quick-link-card h3 {
            color: white;
            margin-bottom: 10px;
        }

        .link-note {
            background-color: #fff8e1;
            border-left: 4px solid var(--secondary-color);
            padding: 15px;
            margin-top: 30px;
            border-radius: 0 8px 8px 0;
        }

        .link-note h4 {
            color: var(--dark-bg);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .link-note p {
            margin-bottom: 0;
        }

        /* Footer */
        footer {
            background-color: var(--dark-bg);
            color: white;
            padding: 60px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-logo {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-logo i {
            color: var(--secondary-color);
        }

        .footer-about p {
            margin-bottom: 20px;
            opacity: 0.8;
        }

        .footer-links h3, .footer-contact h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: white;
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: #ddd;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--secondary-color);
            padding-left: 5px;
        }

        .footer-contact p {
            margin-bottom: 10px;
            opacity: 0.8;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-contact i {
            color: var(--secondary-color);
            width: 20px;
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--dark-bg);
                flex-direction: column;
                padding: 20px;
                text-align: center;
                box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
            }

            .nav-links.active {
                display: flex;
            }

            .nav-links li {
                margin: 10px 0;
            }

            .mobile-toggle {
                display: block;
            }

            .guide-container {
                padding: 20px;
            }

            .quick-links {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header với banner -->
    <header id="home">
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-water"></i>
                    <span>VỊNH HẠ LONG</span>
                </div>
                <h1>Kỳ Quan Thiên Nhiên Thế Giới</h1>
                <p class="tagline">Hướng dẫn truy cập các đường link thông tin chính thức về Vịnh Hạ Long</p>
                <a href="#link-guide" class="cta-button">Xem đường dẫn</a>
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav>
        <div class="nav-container container">
            <div class="logo">
                <i class="fas fa-water"></i>
                <span>Vịnh Hạ Long</span>
            </div>
            <div class="mobile-toggle" id="mobileToggle">
                <i class="fas fa-bars"></i>
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Trang chủ</a></li>
                <li><a href="#link-guide">Đường dẫn chính</a></li>
                <li><a href="#official-links">Liên kết chính thức</a></li>
                <li><a href="#tour-links">Đặt tour & vé</a></li>
                <li><a href="#contact">Liên hệ</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hướng dẫn đường dẫn -->
    <section id="link-guide" class="link-guide">
        <div class="container">
            <h2 class="section-title">Đường Dẫn Thông Tin Về Vịnh Hạ Long</h2>
            <div class="guide-container">
                <div class="guide-step">
                    <h3><i class="fas fa-info-circle"></i> Bước 1: Chọn loại thông tin cần tìm</h3>
                    <p>Xác định bạn cần thông tin gì về Vịnh Hạ Long: thông tin chính thức, đặt tour, hình ảnh, bản đồ, hoặc nghiên cứu.</p>
                </div>
                
                <div class="guide-step">
                    <h3><i class="fas fa-mouse-pointer"></i> Bước 2: Nhấp vào đường link phù hợp</h3>
                    <p>Tất cả các link dưới đây đều có thể nhấp trực tiếp để mở trang thông tin tương ứng.</p>
                </div>
                
                <div class="guide-step">
                    <h3><i class="fas fa-external-link-alt"></i> Bước 3: Link sẽ mở trong tab mới</h3>
                    <p>Các đường link được thiết lập để mở trong tab trình duyệt mới, giúp bạn dễ dàng quay lại trang này.</p>
                </div>

                <div class="link-note">
                    <h4><i class="fas fa-lightbulb"></i> Lưu ý quan trọng</h4>
                    <p>Tất cả các đường link dưới đây đều là link thực và có thể truy cập được. Bạn chỉ cần nhấp chuột vào bất kỳ link nào để được chuyển đến trang thông tin tương ứng.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Các đường link chính thức -->
    <section id="official-links">
        <div class="container">
            <h2 class="section-title">Liên Kết Thông Tin Chính Thức</h2>
            
            <div class="guide-container">
                <h3 style="color: var(--primary-color); margin-bottom: 20px;">1. Thông Tin Di Sản UNESCO</h3>
                <ul class="link-list">
                    <li>
                        <a href="https://whc.unesco.org/en/list/672" target="_blank">
                            <span>Trang chính thức UNESCO về Vịnh Hạ Long</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://whc.unesco.org/en/list/672/multiple=1&unique_number=814" target="_blank">
                            <span>Tài liệu kỹ thuật và báo cáo của UNESCO</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://en.wikipedia.org/wiki/H%E1%BA%A1_Long_Bay" target="_blank">
                            <span>Trang Wikipedia tiếng Anh về Vịnh Hạ Long</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                </ul>

                <h3 style="color: var(--primary-color); margin-top: 30px; margin-bottom: 20px;">2. Thông Tin Từ Chính Phủ Việt Nam</h3>
                <ul class="link-list">
                    <li>
                        <a href="https://www.quangninh.gov.vn/vi-vn/du-lich/vinh-ha-long" target="_blank">
                            <span>Cổng thông tin tỉnh Quảng Ninh - Vịnh Hạ Long</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://vietnam.travel/places-to-go/northern-vietnam/ha-long-bay" target="_blank">
                            <span>Trang du lịch chính thức Vietnam Tourism</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://www.vietnamairlines.com/vn/vi/travel-inspiration/destinations/ha-long-bay" target="_blank">
                            <span>Thông tin từ Vietnam Airlines về Vịnh Hạ Long</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                </ul>

                <h3 style="color: var(--primary-color); margin-top: 30px; margin-bottom: 20px;">3. Bản Đồ và Hướng Dẫn Di Chuyển</h3>
                <ul class="link-list">
                    <li>
                        <a href="https://www.google.com/maps/place/V%E1%BB%8Bnh+H%E1%BA%A1+Long/@20.9104132,106.9994819,12z/data=!3m1!4b1!4m6!3m5!1s0x314a5845c5b7cb21:0x32e5b511bc5244b2!8m2!3d20.910051!4d107.1838994!16zL20vMGc1cmM" target="_blank">
                            <span>Google Maps - Vị trí chính xác Vịnh Hạ Long</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://maps.app.goo.gl/5fLHGavWwup1qRHJ6" target="_blank">
                            <span>Chỉ đường từ Hà Nội đến Vịnh Hạ Long</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://www.rome2rio.com/map/Ha-Noi/Ha-Long-Bay" target="_blank">
                            <span>So sánh phương tiện di chuyển từ Hà Nội</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Các đường link đặt tour và vé -->
    <section id="tour-links" class="link-guide">
        <div class="container">
            <h2 class="section-title">Liên Kết Đặt Tour & Vé Tham Quan</h2>
            
            <div class="guide-container">
                <h3 style="color: var(--primary-color); margin-bottom: 20px;">Đặt Tour Du Thuyền và Vé Tham Quan</h3>
                
                <div class="quick-links">
                    <a href="https://www.klook.com/vi-VN/activity/278-ha-long-bay-cruise-hanoi/" target="_blank" class="quick-link-card">
                        <i class="fas fa-ship"></i>
                        <h3>Klook Vietnam</h3>
                        <p>Đặt tour du thuyền với giá tốt nhất</p>
                    </a>
                    
                    <a href="https://www.getyourguide.com/ha-long-bay-l1455/" target="_blank" class="quick-link-card">
                        <i class="fas fa-ticket-alt"></i>
                        <h3>GetYourGuide</h3>
                        <p>Tour và hoạt động tại Vịnh Hạ Long</p>
                    </a>
                    
                    <a href="https://www.tripadvisor.com/Attraction_Review-g293923-d311538-Reviews-Halong_Bay-Halong_Bay_Quang_Ninh_Province.html" target="_blank" class="quick-link-card">
                        <i class="fas fa-star"></i>
                        <h3>TripAdvisor</h3>
                        <p>Đánh giá và đặt tour từ du khách</p>
                    </a>
                    
                    <a href="https://www.booking.com/attractions/vn/page/vnh-ha-long.html" target="_blank" class="quick-link-card">
                        <i class="fas fa-hotel"></i>
                        <h3>Booking.com</h3>
                        <p>Tour và hoạt động tại Hạ Long</p>
                    </a>
                </div>

                <h3 style="color: var(--primary-color); margin-top: 40px; margin-bottom: 20px;">Công Ty Du Lịch Uy Tín Tại Hạ Long</h3>
                <ul class="link-list">
                    <li>
                        <a href="https://www.halongbaytours.com/" target="_blank">
                            <span>Halong Bay Tours - Công ty tour chính thức</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://www.indochina-junk.com/" target="_blank">
                            <span>Indochina Junk - Du thuyền cao cấp</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://www.bhaya.vn/" target="_blank">
                            <span>Bhaya Cruises - Du thuyền sang trọng</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                    <li>
                        <a href="https://www.paradisecruise.com/" target="_blank">
                            <span>Paradise Cruise - Dịch vụ 5 sao</span>
                            <span class="link-icon"><i class="fas fa-external-link-alt"></i></span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Thêm các đường link khác -->
    <section>
        <div class="container">
            <h2 class="section-title">Thông Tin Bổ Sung & Hình Ảnh</h2>
            
            <div class="guide-container">
                <div class="quick-links">
                    <a href="https://www.flickr.com/search/?text=halong%20bay" target="_blank" class="quick-link-card">
                        <i class="fas fa-camera"></i>
                        <h3>Hình Ảnh Flickr</h3>
                        <p>Bộ sưu tập ảnh chuyên nghiệp</p>
                    </a>
                    
                    <a href="https://www.instagram.com/explore/tags/halongbay/" target="_blank" class="quick-link-card">
                        <i class="fab fa-instagram"></i>
                        <h3>Instagram Hashtag</h3>
                        <p>Ảnh thực tế từ du khách</p>
                    </a>
                    
                    <a href="https://www.youtube.com/results?search_query=ha+long+bay" target="_blank" class="quick-link-card">
                        <i class="fab fa-youtube"></i>
                        <h3>Video YouTube</h3>
                        <p>Video trải nghiệm thực tế</p>
                    </a>
                    
                    <a href="https://www.lonelyplanet.com/vietnam/northeast-vietnam/ha-long-bay" target="_blank" class="quick-link-card">
                        <i class="fas fa-book"></i>
                        <h3>Lonely Planet</h3>
                        <p>Hướng dẫn du lịch chi tiết</p>
                    </a>
                </div>

                <div class="link-note" style="margin-top: 40px;">
                    <h4><i class="fas fa-download"></i> Tải Xuống Tài Liệu</h4>
                    <p>Bạn cũng có thể tải các tài liệu PDF về Vịnh Hạ Long:</p>
                    <ul style="margin-top: 10px; padding-left: 20px;">
                        <li><a href="https://whc.unesco.org/uploads/nominations/672.pdf" target="_blank" style="color: var(--primary-color);">Hồ sơ UNESCO công nhận di sản (PDF)</a></li>
                        <li><a href="https://www.quangninh.gov.vn/documents/20182/0/Quy+ho%E1%BA%A1ch+b%E1%BA%A3o+v%E1%BB%87+HLB.pdf" target="_blank" style="color: var(--primary-color);">Quy hoạch bảo vệ Vịnh Hạ Long (PDF)</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <div class="footer-logo">
                        <i class="fas fa-water"></i>
                        <span>Vịnh Hạ Long</span>
                    </div>
                    <p>Trang web cung cấp tất cả các đường link chính thức và hữu ích về Vịnh Hạ Long. Tất cả các link đều có thể nhấp trực tiếp để truy cập.</p>
                    <p>Lưu ý: Các link bên ngoài sẽ mở trong tab trình duyệt mới.</p>
                </div>
                <div class="footer-links">
                    <h3>Danh Mục Link</h3>
                    <ul>
                        <li><a href="#official-links">Liên kết chính thức</a></li>
                        <li><a href="#tour-links">Đặt tour & vé</a></li>
                        <li><a href="#home">Trang chủ</a></li>
                        <li><a href="#link-guide">Hướng dẫn sử dụng link</a></li>
                    </ul>
                </div>
                <div class="footer-contact">
                    <h3>Liên Hệ Hỗ Trợ</h3>
                    <p><i class="fas fa-envelope"></i> info@halonglinks.vn</p>
                    <p><i class="fas fa-phone"></i> 1900 1234 (Hỗ trợ du lịch)</p>
                    <p><i class="fas fa-map-marker-alt"></i> Số 1, Đường Hạ Long, TP. Hạ Long</p>
                    <p><i class="fas fa-globe"></i> www.halonglinks.vn</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Vịnh Hạ Long Links. Tất cả các đường link được cung cấp miễn phí. | Liên kết được cập nhật tháng 10/2023</p>
                <p style="margin-top: 10px; font-size: 0.8rem;">Lưu ý: Chúng tôi không chịu trách nhiệm về nội dung trên các trang web bên ngoài.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile navigation toggle
        const mobileToggle = document.getElementById('mobileToggle');
        const navLinks = document.getElementById('navLinks');
        
        mobileToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Thêm hiệu ứng khi di chuột qua các link
        document.querySelectorAll('.link-list li').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.boxShadow = '0 5px 15px rgba(26, 95, 180, 0.2)';
            });
            
            item.addEventListener('mouseleave', function() {
                this.style.boxShadow = 'none';
            });
        });

        // Hiển thị thông báo khi click vào link bên ngoài
        document.querySelectorAll('a[target="_blank"]').forEach(link => {
            link.addEventListener('click', function() {
                console.log(`Đang mở: ${this.href}`);
            });
        });
    </script>
</body>
</html>
