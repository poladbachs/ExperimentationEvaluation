<template>
  <div class="main-container">
    <header class="header">
      <h1 class="header-title">🚀 Welcome to the Experiment</h1>
    </header>

    <section class="cards-section">
      <div class="card">
        <h3 class="card-title">📝 Experiment Explanation</h3>
        <p>
          The purpose of the experiment is to determine if there's a difference
          in reading natural language between <b>camelCase</b> and
          <b>kebab-case</b>.
        </p>
      </div>

      <div class="card">
        <h3 class="card-title">🔍 Difference Between Fonts</h3>
        <div class="list-item">
          <span class="list-title">camelCase:</span> Words start with lowercase, subsequent words capitalize the first
          letter (e.g., <code>doSomething</code>).
        </div>
        <div class="list-item">
          <span class="list-title">kebab-case:</span> Words are separated by dashes (e.g., <code>do-something</code>).
        </div>
      </div>

      <div class="card">
        <h3 class="card-title">🎯 Purpose of the Experiment</h3>
        <p>
          You'll choose the correct transformation between camelCase and
          kebab-case. The goal is to measure which is faster to read and
          understand.
        </p>
      </div>

      <div class="card">
        <h3 class="card-title">💡 What is Expected?</h3>
        <div class="list-item"><span class="list-title">Focus:</span> Stay attentive, as this will only take a few
          minutes.</div>
        <div class="list-item"><span class="list-title">First Instinct:</span> Rely on your initial impressions.</div>
        <div class="list-item"><span class="list-title">Honesty:</span> Complete the experiment independently.</div>
        <div class="list-item"><span class="list-title">Completeness:</span> Finish the quiz to contribute valuable
          data.</div>
      </div>

      <div class="card">
        <h3 class="card-title">🔒 Use of Data</h3>
        <div class="list-item"><span class="list-title">Data Management:</span> The collected data will be used for the
          experiment only.</div>
        <div class="list-item"><span class="list-title">Confidentiality:</span> No personal identifiers will be stored.
        </div>
      </div>
    </section>

    <div class="button-container">
      <button @click="$emit('proceed')" class="proceed-button">Start the Experiment</button>
    </div>

    <footer class="footer">
      <p>Created with ❤️ for research purposes.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: "ExperimentPage",
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: "Roboto", sans-serif;
  background-color: #1e1e2f;
  color: #ffffff;
}

.main-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
}

.header {
  width: 100%;
  background-color: #ff6363;
  padding: 20px;
  text-align: center;
  border-radius: 8px;
  margin-bottom: 30px;
}

.header-title {
  color: #ffffff;
  font-size: 28px;
  font-weight: bold;
  margin: 0;
  text-transform: uppercase;
  animation: pulse 2s infinite;
}

.cards-section {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  width: 100%;
}

.card {
  background-color: #2e2e3e;
  padding: 20px;
  border-radius: 10px;
  border: 1px solid #ff6363;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.list-item {
  background-color: rgba(255, 255, 255, 0.1);
  color: #ffffff;
  padding: 10px;
  border-radius: 6px;
  margin-bottom: 10px;
  font-size: 16px;
  line-height: 1.6;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.list-title {
  color: #ff6363;
  font-weight: bold;
}


.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.5);
}

.card-title {
  font-size: 20px;
  color: #ff6363;
  margin-bottom: 10px;
}

.card p {
  color: #cfcfcf;
  font-size: 16px;
  line-height: 1.5;
}

.card ul li,
.card ol li {
  background-color: rgba(255, 255, 255, 0.1);
  color: #ffffff;
  padding: 10px;
  border-radius: 6px;
  margin-bottom: 10px;
  font-size: 16px;
  line-height: 1.6;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.card ul li b,
.card ol li b {
  color: #ff6363;
}


.button-container {
  margin-top: 20px;
}

.proceed-button {
  background-color: #ff6363;
  color: #ffffff;
  font-size: 18px;
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.proceed-button:hover {
  background-color: #ff4747;
  transform: scale(1.05);
}

.footer {
  margin-top: 40px;
  padding: 10px;
  text-align: center;
  color: #cfcfcf;
  font-size: 14px;
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }

  50% {
    transform: scale(1.05);
  }

  100% {
    transform: scale(1);
  }
}

@media (max-width: 768px) {
  .header-title {
    font-size: 24px;
  }

  .card-title {
    font-size: 18px;
  }
}
</style>
