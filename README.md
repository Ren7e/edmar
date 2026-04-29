# edmar
Casamento Edmar
[convite.html](https://github.com/user-attachments/files/27205590/convite.html)
<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Casamento Edmar & Natutonda</title>

<style>
body {
  font-family: 'Segoe UI', sans-serif;
  background: #f8f5f2;
  text-align: center;
  padding: 20px;
  animation: fadeIn 1.5s ease-in;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.container {
  max-width: 420px;
  margin: auto;
  background: #fff;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  animation: slideUp 1s ease;
}

@keyframes slideUp {
  from { transform: translateY(30px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

h1 {
  color: #b08d57;
  margin-bottom: 5px;
}

.section {
  margin-top: 20px;
  padding-top: 10px;
  border-top: 1px solid #eee;
}

a {
  display: block;
  margin: 8px 0;
  padding: 10px;
  border-radius: 6px;
  text-decoration: none;
  color: white;
  font-size: 14px;
}

.map { background: #3b82f6; }
.rsvp { background: #10b981; }
.whatsapp { background: #25D366; }
.call { background: #6b7280; }

small { color: #666; }

/* FOTO */
.photo {
  width: 100%;
  border-radius: 10px;
  margin-bottom: 15px;
}

/* CONTADOR */
.countdown {
  font-size: 16px;
  margin-top: 10px;
  color: #b08d57;
  font-weight: bold;
}
</style>
</head>

<body>

<div class="container">

  <!-- FOTO DO CASAL -->
  <img src="https://via.placeholder.com/400x250" class="photo" alt="Foto do casal">

  <h1>💍 Edmar & Natutonda</h1>
  <p>29 de Maio de 2026</p>

  <!-- CONTADOR -->
  <div class="countdown" id="countdown"></div>

  <!-- CONSERVATÓRIA -->
  <div class="section">
    <strong>📍 Conservatória</strong>
    <p>Conservatória do Registo Civil de Luanda</p>
    <p>⏰ 08h00</p>
    <a class="map" href="#" onclick="alert('GPS em atualização')">
      Ver localização
    </a>
  </div>

  <!-- IGREJA -->
  <div class="section">
    <strong>⛪ Cerimónia Religiosa</strong>
    <p>Igreja Evangélica de Angola</p>
    <p>⏰ 15h30</p>
    <a class="map" href="#" onclick="alert('GPS em atualização')">
      Ver localização
    </a>
  </div>

  <!-- FESTA -->
  <div class="section">
    <strong>🥂 Copo d’Água</strong>
    <p>Salão de Festas Meury Inglês</p>
    <p><small>Camama, frente ao comité do MPLA</small></p>
    <p>⏰ 20h00</p>
    <a class="map" href="#" onclick="alert('GPS em atualização')">
      Ver localização
    </a>
  </div>

  <!-- RSVP -->
  <div class="section">
    <a class="rsvp" href="https://wa.me/244945218101?text=Confirmo%20presen%C3%A7a%20no%20casamento%20de%20Edmar%20e%20Natutonda">
      ✅ Confirmar presença
    </a>
  </div>

  <!-- CONTACTOS -->
  <div class="section">
    <a class="whatsapp" href="https://wa.me/244945218101">
      💬 945 218 101
    </a>
    <a class="whatsapp" href="https://wa.me/244924456252">
      💬 924 456 252
    </a>
    <a class="call" href="tel:+244945218101">
      📞 Ligar
    </a>
  </div>

</div>

<script>
// CONTADOR REGRESSIVO
const eventDate = new Date("May 29, 2026 00:00:00").getTime();

const countdownFunction = setInterval(function() {
  const now = new Date().getTime();
  const distance = eventDate - now;

  const days = Math.floor(distance / (1000 * 60 * 60 * 24));
  const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));

  document.getElementById("countdown").innerHTML =
    "Faltam " + days + " dias, " + hours + "h " + minutes + "min";

  if (distance < 0) {
    clearInterval(countdownFunction);
    document.getElementById("countdown").innerHTML = "Hoje é o grande dia! 🎉";
  }
}, 1000);
</script>

</body>
</html>
