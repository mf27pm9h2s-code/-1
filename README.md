  * {
    box-sizing: border-box;
  }

  body {
    margin: 0;
    font-family: "Noto Sans KR", "Apple SD Gothic Neo", sans-serif;
    background: var(--bg);
    color: #111;
  }

  .story {
    min-height: 100vh;
    display: grid;
    place-items: center;
    padding: 40px 20px;
  }

  .content {
    max-width: 680px;
    width: 100%;
    background: white;
    border-radius: 18px;
    box-shadow: 0 12px 30px rgba(0, 0, 0, 0.06);
    padding: 36px 28px;
  }

  .content h1 {
    margin: 0 0 20px;
    font-size: clamp(28px, 4vw, 42px);
  }

  .content p {
    font-size: 18px;
    line-height: 1.7;
    color: #333;
  }

  .content a {
    color: var(--primary);
    text-decoration: none;
    font-weight: 700;
    cursor: pointer;
  }

  .content a:hover {
    text-decoration: underline;
  }

  .open-phone {
    margin-top: 16px;
    border: none;
    background: var(--primary);
    color: var(--white);
    padding: 14px 22px;
    border-radius: 12px;
    font-size: 16px;
    font-weight: 700;
    cursor: pointer;
  }

  .phone-layer {
    position: fixed;
    inset: 0;
    display: grid;
    place-items: center;
    background: rgba(0, 0, 0, 0.5);
    opacity: 0;
    visibility: hidden;
    pointer-events: none;
    transition: all 0.25s ease;
  }

  .phone-layer.active {
    opacity: 1;
    visibility: visible;
    pointer-events: auto;
  }

  .device {
    position: relative;
    width: min(88vw, 400px);
    height: min(86vh, 760px);
    background: var(--phone-bg);
    border: 10px solid #0d0d0d;
    border-radius: 42px;
    box-shadow: 0 30px 70px rgba(0, 0, 0, 0.4);
    overflow: hidden;
  }

  .device::before {
    content: "";
    position: absolute;
    top: 16px;
    left: 50%;
    transform: translateX(-50%);
    width: 40%;
    height: 26px;
    background: rgba(255,255,255,0.06);
    border-radius: 14px;
    z-index: 4;
  }

  .statusbar {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 56px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 18px 0 22px;
    color: #fff;
    font-size: 14px;
    font-weight: 700;
    z-index: 3;
    background: rgba(0,0,0,0.08);
  }

  .sb-time {
    letter-spacing: 0.04em;
  }

  .sb-icons {
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .signal {
    width: 16px;
    height: 12px;
    display: inline-block;
    position: relative;
  }

  .signal::before,
  .signal::after {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(to right, transparent 0 20%, #fff 20% 100%);
    clip-path: polygon(0 100%, 20% 100%, 20% 55%, 40% 55%, 40% 20%, 60% 20%, 60% 0, 100% 0, 100% 100%);
    opacity: 0.9;
  }

  .battery {
    width: 22px;
    height: 12px;
    border: 2px solid #fff;
    border-radius: 3px;
    position: relative;
  }

  .battery::after {
    content: "";
    position: absolute;
    top: 2px;
    right: -4px;
    width: 2px;
    height: 6px;
    background: #fff;
    border-radius: 0 2px 2px 0;
  }

  .battery::before {
    content: "";
    position: absolute;
    inset: 2px 2px 2px 2px;
    background: #fff;
    border-radius: 1px;
  }

  .screen {
    position: absolute;
    inset: 0;
    background: var(--screen-bg);
    border-radius: 32px;
    overflow: hidden;
  }

  .screen-inner {
    position: absolute;
    inset: 56px 0 0 0;
    padding: 16px 18px;
    background: linear-gradient(180deg, #ececec, #f5f5f5);
  }

  .banner {
    height: 140px;
    border-radius: 20px;
    background: linear-gradient(135deg, #6aa5ff, #87d3ff 48%, #d5ecff);
    position: relative;
    overflow: hidden;
  }

  .banner::before,
  .banner::after {
    content: "";
    position: absolute;
    border-radius: 50%;
    background: rgba(255,255,255,0.15);
  }

  .banner::before {
    width: 180px;
    height: 180px;
    top: -40px;
    left: -30px;
  }

  .banner::after {
    width: 220px;
    height: 220px;
    right: -60px;
    bottom: -70px;
  }

  .banner-text {
    position: absolute;
    left: 22px;
    bottom: 20px;
    color: #fff;
    z-index: 1;
  }

  .banner-text strong {
    display: block;
    font-size: 24px;
  }

  .banner-text span {
    display: block;
    margin-top: 6px;
    font-size: 13px;
    opacity: 0.9;
  }

  .card-list {
    margin-top: 18px;
    display: grid;
    gap: 14px;
  }

  .card {
    background: #fff;
    border-radius: 16px;
    padding: 16px;
    box-shadow: 0 8px 18px rgba(0,0,0,0.04);
  }

  .card h3 {
    margin: 0 0 8px;
    font-size: 18px;
  }

  .card p {
    margin: 0;
    font-size: 14px;
    color: #666;
    line-height: 1.6;
  }

  .close-phone {
    position: absolute;
    top: 18px;
    right: 18px;
    width: 36px;
    height: 36px;
    border: none;
    border-radius: 50%;
    background: rgba(0,0,0,0.06);
    color: #222;
    font-size: 22px;
    cursor: pointer;
    z-index: 10;
  }

  .close-phone:hover {
    background: rgba(0,0,0,0.1);
  }
</style>
