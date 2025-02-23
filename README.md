<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ganhe Seguidores no Instagram</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; padding: 50px; }
        .container { max-width: 500px; margin: auto; padding: 20px; border: 1px solid #ccc; border-radius: 10px; }
        button { padding: 10px 20px; margin: 10px; cursor: pointer; }
    </style>
</head>
<body>
    <h1>Ganhe Seguidores no Instagram</h1>
    <div class="container">
        <p>Escolha um pacote e pague via PIX para receber seguidores automaticamente!</p>
        <select id="package">
            <option value="100">100 Seguidores - R$5,00</option>
            <option value="500">500 Seguidores - R$20,00</option>
            <option value="1000">1000 Seguidores - R$35,00</option>
        </select><br>
        <button onclick="generatePix()">Pagar com PIX</button>
        <p id="payment-info"></p>
    </div>

    <script>
        function generatePix() {
            const package = document.getElementById("package").value;
            let amount;

            if (package === "100") {
                amount = 5.00;
            } else if (package === "500") {
                amount = 20.00;
            } else {
                amount = 35.00;
            }

            // Usando seu nome de usuário do PicPay
            const pixQRCodeUrl = `https://www.qrpay.com.br/api/pix?valor=${amount}&chave=crismayra.campos.costa&descricao=Compra%20de%20Seguidores`;

            // Gerar o QR Code com o valor calculado
            document.getElementById("payment-info").innerHTML = `
                <p>Escaneie o QR Code para pagar:</p>
                <img src="${pixQRCodeUrl}" width="200">
                <p>Valor: R$${amount}</p>
            `;
        }
    </script>
</body>
</html>
