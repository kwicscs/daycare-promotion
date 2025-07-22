<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>헤이텍 - 상담 신청 혜택</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(180deg, #2d2d5f 0%, #3d3d7f 50%, #2d2d5f 100%);
            min-height: 100vh;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 헤더 섹션 */
        .hero-section {
            text-align: center;
            color: white;
            padding: 40px 20px 20px;
            position: relative;
        }
        
        .hero-section h1 {
            font-size: 28px;
            font-weight: 600;
            margin-bottom: 8px;
        }
        
        .hero-section p {
            font-size: 28px;
            font-weight: 600;
        }
        
        .hero-section .highlight {
            color: #ff6b6b;
        }
        
        /* 선물 아이콘 */
        .gift-icon {
            margin: 20px 0;
            text-align: center;
            position: relative;
        }
        
        .gift-box {
            display: inline-block;
            position: relative;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        
        /* 장식 요소들 */
        .decorations {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }
        
        .decoration {
            position: absolute;
            opacity: 0.6;
            animation: twinkle 2s ease-in-out infinite;
        }
        
        @keyframes twinkle {
            0%, 100% { opacity: 0.6; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.2); }
        }
        
        /* 혜택 카드 */
        .benefit-card {
            background: white;
            border-radius: 20px;
            margin: 20px 0;
            padding: 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            position: relative;
        }
        
        .card-header {
            background: linear-gradient(135deg, #6c63ff, #9c88ff);
            color: white;
            padding: 30px 40px 25px;
            text-align: center;
        }
        
        .benefit-badge {
            background: rgba(0, 0, 0, 0.3);
            color: white;
            padding: 8px 20px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 600;
            display: inline-block;
            margin-bottom: 20px;
        }
        
        .card-title {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 8px;
        }
        
        .card-title .highlight {
            color: #ffeb3b;
        }
        
        .card-subtitle {
            font-size: 14px;
            opacity: 0.9;
        }
        
        .card-content {
            padding: 30px 40px;
        }
        
        /* 혜택 리스트 */
        .benefit-list {
            list-style: none;
        }
        
        .benefit-item {
            background: #f8f9fa;
            border: 1px solid #e9ecef;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .benefit-item:hover {
            background: #e3f2fd;
            border-color: #2196f3;
            transform: translateX(5px);
        }
        
        .benefit-number {
            color: #bbb;
            font-size: 18px;
            font-weight: 700;
            margin-right: 15px;
        }
        
        .benefit-text {
            flex: 1;
            font-size: 16px;
            font-weight: 500;
            color: #333;
        }
        
        .benefit-plus {
            width: 24px;
            height: 24px;
            background: #f0f0f0;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 16px;
            color: #666;
            font-weight: 700;
        }
        
        .benefit-item:hover .benefit-plus {
            background: #2196f3;
            color: white;
        }
        
        /* 하단 CTA 섹션 */
        .cta-section {
            background: linear-gradient(135deg, #1a1a3a, #2d2d5f);
            color: white;
            padding: 60px 20px;
            text-align: center;
            margin-top: 40px;
        }
        
        .cta-section h2 {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 8px;
        }
        
        .cta-section p {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 30px;
        }
        
        .cta-section .highlight {
            color: #ff6b6b;
        }
        
        .cta-description {
            font-size: 14px;
            opacity: 0.8;
            margin-bottom: 40px;
        }
        
        .contact-info {
            margin-top: 40px;
        }
        
        .contact-label {
            font-size: 16px;
            margin-bottom: 10px;
            opacity: 0.9;
        }
        
        .phone-number {
            font-size: 48px;
            font-weight: 700;
            color: white;
            text-decoration: none;
            display: block;
            margin-bottom: 5px;
            letter-spacing: 2px;
        }
        
        .phone-number:hover {
            color: #ffeb3b;
        }
        
        .business-hours {
            font-size: 14px;
            opacity: 0.7;
            margin-bottom: 30px;
        }
        
        /* CTA 버튼 */
        .cta-button {
            display: inline-block;
            background: #705DF7;
            color: white;
            padding: 18px 50px;
            border-radius: 12px;
            font-size: 18px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 6px 20px rgba(112, 93, 247, 0.3);
        }
        
        .cta-button:hover {
            background: #6050e0;
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(112, 93, 247, 0.4);
        }
        
        /* 반응형 디자인 */
        @media (max-width: 768px) {
            .hero-section h1,
            .hero-section p {
                font-size: 22px;
            }
            
            .card-header {
                padding: 25px 20px 20px;
            }
            
            .card-content {
                padding: 25px 20px;
            }
            
            .card-title {
                font-size: 20px;
            }
            
            .benefit-text {
                font-size: 14px;
            }
            
            .phone-number {
                font-size: 36px;
            }
            
            .cta-section h2,
            .cta-section p {
                font-size: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 히어로 섹션 -->
        <section class="hero-section">
            <div class="decorations">
                <div class="decoration" style="top: 20%; left: 10%; font-size: 20px;">❤️</div>
                <div class="decoration" style="top: 30%; right: 15%; font-size: 16px;">⭐</div>
                <div class="decoration" style="top: 50%; left: 5%; font-size: 12px;">✨</div>
                <div class="decoration" style="top: 40%; right: 8%; font-size: 14px;">💫</div>
                <div class="decoration" style="top: 60%; right: 20%; font-size: 18px;">🔵</div>
                <div class="decoration" style="top: 70%; left: 15%; font-size: 16px;">🟣</div>
            </div>
            
            <h1>지금 상담 신청만 하셔도</h1>
            <p>센터 운영에 <span class="highlight">꼭 필요한 혜택</span>을 드립니다.</p>
            
            <div class="gift-icon">
                <div class="gift-box">
                    <!-- 선물 상자 SVG -->
                    <svg width="120" height="120" viewBox="0 0 120 120">
                        <!-- 선물 상자 본체 -->
                        <rect x="25" y="45" width="70" height="60" fill="#6c63ff" rx="4"/>
                        <rect x="25" y="45" width="70" height="8" fill="#8a82ff"/>
                        
                        <!-- 리본 -->
                        <rect x="55" y="25" width="10" height="80" fill="#4c43df"/>
                        <rect x="25" y="40" width="70" height="20" fill="#7c72ff" rx="4"/>
                        
                        <!-- 리본 매듭 -->
                        <path d="M45 40 Q45 22 55 22 Q65 22 65 40" fill="none" stroke="#ff6b6b" stroke-width="3"/>
                        <path d="M65 40 Q65 22 75 22 Q85 22 85 40" fill="none" stroke="#ff6b6b" stroke-width="3"/>
                        <circle cx="65" cy="40" r="6" fill="#ff6b6b"/>
                        
                        <!-- 웃는 얼굴 -->
                        <circle cx="100" cy="45" r="15" fill="#ffeb3b"/>
                        <circle cx="96" cy="41" r="2" fill="#333"/>
                        <circle cx="104" cy="41" r="2" fill="#333"/>
                        <path d="M92 50 Q100 55 108 50" fill="none" stroke="#333" stroke-width="2" stroke-linecap="round"/>
                    </svg>
                </div>
            </div>
        </section>
        
        <!-- 혜택 01 카드 -->
        <div class="benefit-card">
            <div class="card-header">
                <div class="benefit-badge">혜택 01</div>
                <h2 class="card-title">상담만 신청하셔도 드리는 혜택</h2>
                <p class="card-subtitle">지금 EASY 재무회계를 상담 신청만 하시면, 아래 혜택을 모두 챙기실 수 있습니다.</p>
            </div>
            
            <div class="card-content">
                <ul class="benefit-list">
                    <li class="benefit-item" onclick="showBenefitDetail(1)">
                        <span class="benefit-number">01</span>
                        <span class="benefit-text">회계·노무·행정, 우리 기관 운영 상태 무료 점검</span>
                        <span class="benefit-plus">+</span>
                    </li>
                    <li class="benefit-item" onclick="showBenefitDetail(2)">
                        <span class="benefit-number">02</span>
                        <span class="benefit-text">지도점검 대비 회계 사전 점검</span>
                        <span class="benefit-plus">+</span>
                    </li>
                    <li class="benefit-item" onclick="showBenefitDetail(3)">
                        <span class="benefit-number">03</span>
                        <span class="benefit-text">숨은 오신고 무료 점검 + 정정신고 50% 할인</span>
                        <span class="benefit-plus">+</span>
                    </li>
                    <li class="benefit-item" onclick="showBenefitDetail(4)">
                        <span class="benefit-number">04</span>
                        <span class="benefit-text">공인 노무사가 직접! 근로계약서 무료 검토</span>
                        <span class="benefit-plus">+</span>
                    </li>
                </ul>
            </div>
        </div>
        
        <!-- 혜택 02 카드 -->
        <div class="benefit-card">
            <div class="card-header">
                <div class="benefit-badge">혜택 02</div>
                <h2 class="card-title">신규 가입 시 드리는 혜택</span></h2>
                <p class="card-subtitle">지금 EASY 재무회계를 가입하시면 아래 혜택을 받으실 수 있습니다.</p>
            </div>
            
            <div class="card-content">
                <ul class="benefit-list">
                    <li class="benefit-item">
                        <span class="benefit-number">01</span>
                        <span class="benefit-text">도입 부담 없이, 최대 3개월 이용료 무료</span>
                        <span class="benefit-plus">+</span>
                    </li>
                    <li class="benefit-item">
                        <span class="benefit-number">02</span>
                        <span class="benefit-text">인지활동 고민 끝, 인지학습지 800종 제공</span>
                        <span class="benefit-plus">+</span>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    
    <!-- 하단 CTA 섹션 -->
    <section class="cta-section">
        <h2>언제 사라질지 모르는 <span class="highlight">혜택</span>,</h2>
        <p>지금 상담 신청해보세요.</p>
        
        <a href="https://ezcare.easyms.co.kr/page/landing/common/request.counsel.html?route=landingw4c" class="cta-button" target="_blank">혜택 받고 상담 신청하기</a>
    </section>

    <script>
        // 혜택 아이템 클릭 이벤트
        document.querySelectorAll('.benefit-item').forEach(item => {
            item.addEventListener('click', function() {
                this.style.transform = 'translateX(10px)';
                setTimeout(() => {
                    this.style.transform = 'translateX(5px)';
                }, 150);
            });
        
        // 상담 신청 버튼 핸들러
        function handleConsultation() {
            alert('상담 신청이 접수되었습니다! 곧 연락드리겠습니다.');
            // 여기에 나중에 URL 연결 기능을 추가할 수 있습니다.
        }
        });

        // 부드러운 스크롤 효과
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });

        // 스크롤 애니메이션
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.benefit-card').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.8s, transform 0.8s';
            observer.observe(el);
        });
    </script>
</body>
</html>
