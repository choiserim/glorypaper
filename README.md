<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> glorypaper| 구름처럼 부드러운 화장지</title>
    <style>
        /* 기본 스타일 */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Pretendard', -apple-system, sans-serif; line-height: 1.6; color: #333; background-color: #f9f9f9; }
        a { text-decoration: none; color: inherit; cursor: pointer; }
        ul { list-style: none; }

        /* 헤더 & 네비게이션 */
        header { background: #fff; padding: 20px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 0; z-index: 1000; border-bottom: 1px solid #eee; }
        .logo { font-size: 24px; font-weight: bold; color: #4A90E2; cursor: pointer; }
        nav ul { display: flex; gap: 30px; }
        nav ul li a { font-weight: 500; transition: 0.3s; }
        nav ul li a: hover, nav ul li a.active { color: #4A90E2; font-weight: bold; }

        /* 섹션 공통 스타일 */
        section { display: none; padding: 80px 5%; min-height: 80vh; }
        section.active { display: block; animation: fadeIn 0.5s ease-in-out; }
        h2 { text-align: center; margin-bottom: 40px; font-size: 2rem; color: #222; }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        /* 홈 섹션 전용 스타일 */
        .hero { background: linear-gradient(135deg, #e0f2ff 0%, #ffffff 100%); text-align: center; padding: 100px 5%; }
        .hero h1 { font-size: 3rem; margin-bottom: 20px; }
        .btn { background: #4A90E2; color: #fff; padding: 15px 40px; border-radius: 30px; display: inline-block; font-weight: bold; margin-top: 20px; }

        /* 제품소개 그리드 */
        .product-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; }
        .product-card { background: #fff; border: 1px solid #eee; border-radius: 15px; overflow: hidden; text-align: center; padding-bottom: 20px; transition: 0.3s; }
        .product-card:hover { transform: translateY(-10px); box-shadow: 0 10px 20px rgba(0,0,0,0.1); }
        .product-img { height: 200px; background: #f0f4f8; margin-bottom: 15px; display: flex; align-items: center; justify-content: center; color: #999; }

        /* 공지사항 테이블 */
        .notice-table { width: 100%; border-collapse: collapse; background: #fff; border-radius: 10px; overflow: hidden; }
        .notice-table th, .notice-table td { padding: 15px; border-bottom: 1px solid #eee; text-align: left; }
        .notice-table th { background: #f4f7fa; color: #555; }
        .notice-table tr:hover { background: #fdfdfd; }

        /* 고객지원 폼 */
        .support-container { max-width: 600px; margin: 0 auto; background: #fff; padding: 40px; border-radius: 15px; box-shadow: 0 5px 15px rgba(0,0,0,0.05); }
        .form-group { margin-bottom: 20px; }
        .form-group label { display: block; margin-bottom: 5px; font-weight: bold; }
        .form-group input, .form-group textarea { width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 5px; }
        .submit-btn { width: 100%; background: #4A90E2; color: #fff; border: none; padding: 15px; border-radius: 5px; font-size: 1rem; cursor: pointer; }

        /* 푸터 */
        footer { background: #333; color: #fff; padding: 50px 5%; text-align: center; font-size: 0.9rem; }
    </style>
</head>
<body>

    <header>
        <div class="logo" onclick="showSection('home')">SoftCloud</div>
        <nav>
            <ul>
                <li><a onclick="showSection('home')" id="nav-home" class="active">홈</a></li>
                <li><a onclick="showSection('products')" id="nav-products">제품소개</a></li>
                <li><a onclick="showSection('notice')" id="nav-notice">공지사항</a></li>
                <li><a onclick="showSection('support')" id="nav-support">고객지원</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="active">
        <div class="hero">
            <h1>구름처럼 부드러운<br>우리 집 안심 화장지</h1>
            <p>100% 천연 펄프로 완성한 프리미엄의 차이를 느껴보세요.</p>
            <a onclick="showSection('products')" class="btn">제품 보러가기</a>
        </div>
    </section>

    <section id="products">
        <h2>제품소개</h2>
        <div class="product-grid">
            <div class="product-card">
                <div class="product-img">3겹 클래식 이미지</div>
                <h3>클래식 3겹 30롤</h3>
                <p>매일 쓰는 실속형 타입</p>
                <p style="color:#4A90E2; font-weight:bold;">25,900원</p>
            </div>
            <div class="product-card">
                <div class="product-img">프리미엄 코튼 이미지</div>
                <h3>프리미엄 소프트 코튼</h3>
                <p>먼지 없는 극강의 부드러움</p>
                <p style="color:#4A90E2; font-weight:bold;">32,000원</p>
            </div>
            <div class="product-card">
                <div class="product-img">친환경 뱀부 이미지</div>
                <h3>에코 뱀부(대나무)</h3>
                <p>자연에서 온 무표백 화장지</p>
                <p style="color:#4A90E2; font-weight:bold;">29,800원</p>
            </div>
        </div>
    </section>

    <section id="notice">
        <h2>공지사항</h2>
        <table class="notice-table">
            <thead>
                <tr>
                    <th width="10%">번호</th>
                    <th>제목</th>
                    <th width="20%">날짜</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>3</td>
                    <td>[이벤트] 신규 가입 시 3,000원 할인 쿠폰 증정</td>
                    <td>2024-05-20</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>설 연휴 배송 일정 안내</td>
                    <td>2024-02-05</td>
                </tr>
                <tr>
                    <td>1</td>
                    <td>SoftCloud 공식 홈페이지 오픈 안내</td>
                    <td>2024-01-01</td>
                </tr>
            </tbody>
        </table>
    </section>

    <section id="support">
        <h2>고객지원</h2>
        <div class="support-container">
            <div class="form-group">
                <label>이름</label>
                <input type="text" placeholder="성함을 입력하세요">
            </div>
            <div class="form-group">
                <label>문의유형</label>
                <select style="width:100%; padding:12px; border:1px solid #ddd; border-radius:5px;">
                    <option>배송문의</option>
                    <option>제품문의</option>
                    <option>교환/반품문의</option>
                    <option>기타</option>
                </select>
            </div>
            <div class="form-group">
                <label>문의내용</label>
                <textarea rows="5" placeholder="문의하실 내용을 상세히 적어주세요"></textarea>
            </div>
            <button class="submit-btn">문의하기 접수</button>
        </div>
    </section>

    <footer>
        <p>(주)소프트클라우드 | 사업자등록번호: 123-45-67890</p>
        <p>고객센터: 1588-0000 (평일 09:00 ~ 18:00)</p>
        <div style="margin-top:10px; opacity:0.6;">© 2024 SoftCloud. All rights reserved.</div>
    </footer>

    <script>
        function showSection(sectionId) {
            // 모든 섹션 숨기기
            const sections = document.querySelectorAll('section');
            sections.forEach(sec => sec.classList.remove('active'));

            // 모든 네비게이션 링크 비활성화
            const navLinks = document.querySelectorAll('nav ul li a');
            navLinks.forEach(link => link.classList.remove('active'));

            // 선택한 섹션 보여주기
            document.getElementById(sectionId).classList.add('active');

            // 선택한 네비게이션 활성화
            document.getElementById('nav-' + sectionId).classList.add('active');

            // 페이지 상단으로 스크롤 이동
            window.scrollTo(0, 0);
        }
    </script>
</body>
</html>
