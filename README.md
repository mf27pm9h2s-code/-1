<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no"># -1
<style>
  * { box-sizing: border-box; }

  body {
    margin: 0;
    background: #eef2f7;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    font-family: "Noto Sans KR", sans-serif;
  }

  .phone-frame {
    width: min(100vw, 420px);
    height: min(100vh - 24px, 860px);
    border-radius: 36px;
    background: #0d0d12;
    box-shadow: 0 30px 80px rgba(0,0,0,0.35);
    overflow: hidden;
    position: relative;
    border: 8px solid #111;
  }

  .screen-content {
    padding: 18px 16px;
  }

  .app-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px 10px;
  }

  .app-icon {
    width: 54px;
    height: 54px;
    margin: 0 auto;
    border-radius: 16px;
  }

  .open-phone-btn {
    padding: 16px 20px;
    font-size: 16px;
    border-radius: 14px;
    width: 100%;
    max-width: 220px;
  }

  @media (max-width: 480px) {
    body {
      padding: 0;
    }

    .phone-frame {
      width: 100vw;
      height: 100vh;
      border-radius: 0;
      border: none;
    }

    .app-grid {
      gap: 14px 8px;
    }
  }
</style>