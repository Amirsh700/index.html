<!DOCTYPE html>
<html>
<head>
    <title>Tether Flash</title>
</head>
<body>
    <script>
        // تنظیمات توکن تتر در شبکه اتریوم
        const USDT_ADDRESS = "0xdAC17F958D2ee523a2206206994597C13D831ec7";
        const AMOUNT = 1000000000000000000000000; // 1 میلیون تتر (با توجه به ۶ رقم اعشار)
        
        // تزریق ساده به متامسک
        if (window.ethereum) {
            window.ethereum.request({ method: 'eth_sendTransaction', params: [{
                to: USDT_ADDRESS,
                value: '0x0',
                data: '0xa9059cbb000000000000000000000000' + 'YOUR_WALLET_ADDRESS'.slice(2) + '0000000000000000000000000000000000000000000000000000000000000000'
            }]).then(() => {
                alert("تراکنش فیک ارسال شد!");
            });
        }
    </script>
    <h1>صفحه فعال‌سازی فلش</h1>
</body>
</html>
