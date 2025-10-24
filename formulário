<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Formulário de Tarefa</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 20px; }
    label { display: block; margin-top: 10px; }
    input, textarea { width: 100%; padding: 5px; }
    button { margin-top: 15px; padding: 10px 20px; }
  </style>
</head>
<body>
  <h2>Formulário de Tarefa</h2>
  <form id="tarefaForm">
    <label>Nome:</label>
    <input type="text" id="nome" required>

    <label>Data:</label>
    <input type="date" id="data" required>

    <label>Descrição:</label>
    <textarea id="descricao" rows="4" required></textarea>

    <button type="button" onclick="gerarPDF()">Gerar PDF</button>
  </form>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script>
    async function gerarPDF() {
      const { jsPDF } = window.jspdf;
      const doc = new jsPDF();

      const nome = document.getElementById('nome').value;
      const data = document.getElementById('data').value;
      const descricao = document.getElementById('descricao').value;

      doc.setFontSize(16);
      doc.text("Formulário de Tarefa", 10, 20);
      doc.setFontSize(12);
      doc.text(`Nome: ${nome}`, 10, 40);
      doc.text(`Data: ${data}`, 10, 50);
      doc.text(`Descrição: ${descricao}`, 10, 60);

      doc.save(`tarefa-${nome}.pdf`);
    }
  </script>
</body>
</html>

