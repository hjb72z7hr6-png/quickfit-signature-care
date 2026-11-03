# quickfit-signature-care
Quick Fit Signature Care App
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>QUICK FIT SIGNATURE CARE</title>
<style>
:root {
  --navy: #0b1228;
  --gold: #d6b33f;
  --gold-light: #f0dda0;
  --white: #f4f5fa;
  --muted: #9aa5bb;
  --panel: #151f38;
}
* {
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 25px 15px;
  color: var(--white);
  font-family: Arial, sans-serif;
  background-color: var(--navy);
  background-image:
    linear-gradient(rgba(133,153,190,.05) 1px, transparent 1px),
    linear-gradient(90deg, rgba(133,153,190,.05) 1px, transparent 1px);
  background-size: 40px 40px;
}
.page {
  width: 100%;
  max-width: 920px;
  min-height: 1250px;
  margin: auto;
  display: flex;
  flex-direction: column;
}
header {
  text-align: center;
  padding: 15px 0 20px;
}
.eyebrow {
  color: #aab5ca;
  font-size: 14px;
  font-weight: bold;
  letter-spacing: 3px;
}
.badge {
  display: inline-block;
  margin-top: 12px;
  padding: 6px 15px;
  border: 1px solid var(--gold);
  color: var(--gold-light);
  border-radius: 4px;
  font-size: 12px;
  font-weight: bold;
  letter-spacing: 2px;
}
h1 {
  margin: 18px 0 5px;
  font-size: clamp(27px, 4vw, 39px);
}
h1 span {
  color: var(--gold);
}
.subtitle {
  color: var(--gold-light);
  font-weight: bold;
  letter-spacing: 4px;
  font-size: 16px;
}
.gold-rule {
  height: 2px;
  background: var(--gold);
  margin-bottom: 20px;
}
.plan-card {
  border: 1px solid var(--gold);
  border-radius: 12px;
  background: rgba(11,18,40,.95);
  padding: 22px;
}
.plan-heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
  padding-bottom: 17px;
  border-bottom: 1px solid #343b4b;
}
.plan-heading h2 {
  font-size: 21px;
  letter-spacing: 1px;
}
.total-wrap {
  text-align: right;
}
.total-wrap label {
  display: block;
  color: var(--muted);
  font-size: 13px;
  font-weight: bold;
  letter-spacing: 1px;
}
.amount-entry {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 8px;
}
.currency {
  color: var(--gold);
  font-weight: bold;
  font-size: 20px;
}
#totalAmount {
  width: 180px;
  padding: 7px;
  border: 1px solid var(--gold);
  border-radius: 5px;
  background: #080f21;
  color: var(--gold);
  font-size: 25px;
  font-weight: bold;
  text-align: right;
}
.installments {
  display: grid;
  gap: 11px;
  padding-top: 17px;
}
.installment {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  padding: 13px 16px;
  border: 1px solid #343b4b;
  border-left: 5px solid var(--gold);
  border-radius: 5px;
  background: var(--panel);
}
.month-title {
  color: var(--gold-light);
  font-size: 16px;
  font-weight: bold;
  text-transform: uppercase;
}
.due-date {
  margin-top: 6px;
  color: var(--muted);
  font-size: 14px;
}
.payment {
  min-width: 175px;
  padding: 10px;
  border: 1px solid rgba(214,179,63,.3);
  border-radius: 6px;
  background: #252c3b;
  color: white;
  text-align: center;
  font-size: 21px;
  font-weight: bold;
}
.section-title {
  display: flex;
  align-items: center;
  gap: 12px;
  margin: 22px 0 12px;
  color: var(--gold);
  font-size: 17px;
  font-weight: bold;
  letter-spacing: 2px;
}
.section-title::after {
  content: "";
  flex: 1;
  height: 1px;
  background: rgba(214,179,63,.5);
}
.payment-options {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 12px;
}
.option {
  padding: 15px;
  border: 1px solid #343b4b;
  border-radius: 7px;
  background: #111a31;
}
.option h3 {
  margin: 0 0 8px;
  font-size: 15px;
}
.option p {
  margin: 0;
  color: var(--muted);
  font-size: 13px;
  line-height: 1.5;
}
.clarification {
  margin-top: 18px;
  padding: 15px;
  border: 1px dashed var(--gold);
  border-radius: 7px;
  background: rgba(214,179,63,.04);
}
.clarification h3 {
  margin: 0 0 7px;
  color: var(--gold-light);
  font-size: 15px;
  letter-spacing: 1px;
}
.clarification p {
  margin: 0;
  color: #b6bfd0;
  font-size: 13px;
  line-height: 1.5;
}
.actions {
  text-align: center;
  margin: 20px 0;
}
button {
  padding: 11px 22px;
  border: none;
  border-radius: 5px;
  background: var(--gold);
  color: var(--navy);
  font-weight: bold;
  cursor: pointer;
}
footer {
  margin-top: auto;
  padding-top: 30px;
}
.footer-line {
  height: 1px;
  background: rgba(214,179,63,.4);
  margin-bottom: 13px;
}
.footer-content {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
  color: var(--muted);
  font-size: 12px;
  font-weight: bold;
}
.footer-content strong {
  color: var(--gold);
}
@media(max-width:640px) {
  .plan-heading {
    flex-direction: column;
    align-items: flex-start;
  }
  .total-wrap {
    text-align: left;
    width: 100%;
  }
  .amount-entry {
    justify-content: flex-start;
  }
  .payment-options {
    grid-template-columns: 1fr;
  }
  .installment {
    padding: 11px 8px;
  }
  .month-title {
    font-size: 12px;
  }
  .payment {
    min-width: 120px;
    font-size: 15px;
  }
}
@media print {
  @page {
    size: A4;
    margin: 10mm;
  }
  body {
    padding: 0;
    print-color-adjust: exact;
    -webkit-print-color-adjust: exact;
  }
  .page {
    min-height: 277mm;
  }
  .actions {
    display: none;
  }
  #totalAmount {
    border: none;
  }
}
</style>
</head>
<body>
<main class="page">
<header>
  <div class="eyebrow">
    QUICK FIT AUTO CENTER — EXCELLENCE IN AUTOMOTIVE CARE
  </div>
  <div class="badge">
    EXCLUSIVE VEHICLE MAINTENANCE & ROADside ASSISTANCE
  </div>
  <h1>QUICK FIT <span>SIGNATURE CARE</span></h1>
  <div class="subtitle">
    PREMIUM FOUR-MONTH PAYMENT PLAN
  </div>
</header>
<div class="gold-rule"></div>
<section class="plan-card">
  <div class="plan-heading">
    <h2>VEHICLE PACKAGE INSTALLMENT PLAN</h2>
    <div class="total-wrap">
      <label for="totalAmount">TOTAL PACKAGE PRICE</label>
      <div class="amount-entry">
        <span class="currency">AED</span>
        <input
          id="totalAmount"
          type="number"
          min="0"
          step="0.01"
          value="5724"
        >
      </div>
    </div>
  </div>
  <div class="installments" id="installments"></div>
</section>
<div class="section-title">
  APPROVED PAYMENT OPTIONS
</div>
<section class="payment-options">
  <div class="option">
    <h3>CASH / CARD / ONLINE</h3>
    <p>
      Direct payment with 0% interest or additional
      charges from 800QuickFit.
    </p>
  </div>
  <div class="option">
    <h3>TABBY</h3>
    <p>
      4 monthly installments with no interest or
      additional charges from Tabby. Subject to approval.
    </p>
  </div>
  <div class="option">
    <h3>TAMARA</h3>
    <p>
      4 monthly installments. A third-party processing
      fee may apply based on Tamara's terms.
    </p>
  </div>
</section>
<section class="clarification">
  <h3>IMPORTANT PAYMENT CLARIFICATION</h3>
  <p>
    All package prices are as listed above. There are no
    additional fees or hidden charges added by 800QuickFit
    for the listed package price. Any applicable third-party
    financing processing fees will be communicated
    transparently prior to payment confirmation.
  </p>
</section>
<div class="actions">
  <button onclick="window.print()">
    PRINT / SAVE AS PDF
  </button>
</div>
<footer>
  <div class="footer-line"></div>
  <div class="footer-content">
    <strong>800QUICKFIT AUTO SERVICES</strong>
    <span>
      800QUICKFIT | +971 4 665 1445 | 800quickfit.ae
    </span>
    <span>Page 1 of 1</span>
  </div>
</footer>
</main>
<script>
(function() {
  const input = document.getElementById("totalAmount");
  const container = document.getElementById("installments");
  const months = ["1st", "2nd", "3rd", "4th"];
  function formatAED(value) {
    return new Intl.NumberFormat("en-AE", {
      minimumFractionDigits: 2,
      maximumFractionDigits: 2
    }).format(value);
  }
  function formatDate(date) {
    return new Intl.DateTimeFormat("en-GB", {
      day: "2-digit",
      month: "short",
      year: "numeric"
    }).format(date);
  }
  function calculate() {
    const total = Math.max(0, Number(input.value) || 0);
    const totalFils = Math.round(total * 100);
    const base = Math.floor(totalFils / 4);
    const remainder = totalFils % 4;
    const today = new Date();
    today.setHours(12, 0, 0, 0);
    container.innerHTML = "";
    for (let i = 0; i < 4; i++) {
      const due = new Date(today);
      due.setDate(today.getDate() + i * 30);
      const amountFils = base + (i < remainder ? 1 : 0);
      const amount = amountFils / 100;
      const row = document.createElement("div");
      row.className = "installment";
      const details = document.createElement("div");
      const title = document.createElement("div");
      title.className = "month-title";
      title.textContent = months[i] + " Month Installment";
      const date = document.createElement("div");
      date.className = "due-date";
      if (i === 0) {
        date.innerHTML = "Due Date: <strong>Today</strong> (" +
          formatDate(due) + ")";
      } else {
        date.textContent = "Due Date: " + formatDate(due);
      }
      details.appendChild(title);
      details.appendChild(date);
      const payment = document.createElement("div");
      payment.className = "payment";
      payment.textContent = "AED " + formatAED(amount);
      row.appendChild(details);
      row.appendChild(payment);
      container.appendChild(row);
    }
  }
  input.addEventListener("input", calculate);
  calculate();
})();
</script>
</body>
</html>