<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  
</head>
<body>

<h1>Relógio e Informações do Sistema</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Swing-GUI-blue?style=for-the-badge" alt="Swing">
  <img src="https://img.shields.io/badge/Status-Concluído-brightgreen?style=for-the-badge" alt="Status">
</p>

<h2>Sobre o Projeto</h2>

<p>
Aplicação desktop desenvolvida em <strong>Java</strong> com interface gráfica
<strong>Swing JFrame</strong> que exibe informações completas do sistema,
incluindo <strong>data atual</strong>, <strong>hora</strong>,
<strong>ano</strong> e <strong>fuso horário</strong>, utilizando as APIs
nativas de data e tempo do Java.
</p>

<hr>

<h2>Origem do Projeto</h2>

<blockquote>
Este projeto foi desenvolvido durante o <strong>Curso de Java - 40 Horas</strong>
ministrado pelo professor <strong>Gustavo Guanabara</strong> no
<a href="https://www.cursoemvideo.com/" target="_blank">Curso em Vídeo</a>.
</blockquote>

<p>
O curso tem como objetivo ensinar os fundamentos da linguagem Java e a criação
de aplicações desktop com interface gráfica utilizando Swing.
</p>

<hr>

<h2>Conceitos Utilizados</h2>

<h3>Data e Hora no Java</h3>

<p>
O Java oferece classes robustas para manipulação de data e hora, permitindo
capturar informações precisas do sistema operacional.
</p>

<ul>
  <li>Data atual</li>
  <li>Hora atual</li>
  <li>Ano</li>
  <li>Fuso horário do sistema</li>
  <li>Formatação de data e hora</li>
</ul>

<h3>Principais Classes Utilizadas</h3>

<table border="1" cellpadding="6">
  <tr>
    <th>Classe</th>
    <th>Função</th>
  </tr>
  <tr>
    <td>Date</td>
    <td>Representa data e hora atuais</td>
  </tr>
  <tr>
    <td>Calendar</td>
    <td>Manipula campos de data e hora</td>
  </tr>
  <tr>
    <td>LocalDateTime</td>
    <td>Trabalha com data e hora modernas</td>
  </tr>
  <tr>
    <td>ZoneId</td>
    <td>Identifica o fuso horário</td>
  </tr>
  <tr>
    <td>DateTimeFormatter</td>
    <td>Formata data e hora</td>
  </tr>
</table>

<hr>

<h2>Como Funciona</h2>

<pre>
1. A aplicação é iniciada
2. O sistema captura a data e hora atuais
3. Obtém o ano corrente
4. Identifica o fuso horário do sistema
5. Exibe todas as informações na interface gráfica
</pre>

<hr>

<h2>Funcionalidades</h2>

<ul>
  <li>[x] Exibição da data atual</li>
  <li>[x] Exibição da hora atual</li>
  <li>[x] Identificação do ano corrente</li>
  <li>[x] Detecção automática do fuso horário</li>
  <li>[x] Interface gráfica simples e intuitiva</li>
  <li>[x] Atualização das informações via botão</li>
</ul>

<hr>

<h2>Screenshot</h2>

<pre>
+-----------------------------------------------+
|        RELÓGIO E INFORMAÇÕES DO SISTEMA       |
+-----------------------------------------------+
|                                               |
|   Data Atual:        18/01/2026                |
|   Hora Atual:        14:35:22                  |
|   Ano:               2026                      |
|   Fuso Horário:      America/Sao_Paulo        |
|                                               |
+-----------------------------------------------+
|            [ ATUALIZAR ]                      |
+-----------------------------------------------+
</pre>

<hr>

<h2>Pré-requisitos</h2>

<ul>
  <li><strong>Java JDK 8</strong> ou superior</li>
  <li>IDE Java (NetBeans, Eclipse, IntelliJ IDEA ou VS Code)</li>
</ul>

<hr>

<h2>Como Executar</h2>

<pre>
git clone https://github.com/seu-usuario/relogio-sistema-java.git
cd relogio-sistema-java
javac Main.java
java Main
</pre>

<p>
<strong>Dica:</strong> Se estiver usando NetBeans ou Eclipse, basta abrir o
projeto e clicar em <strong>Run</strong>.
</p>

<hr>

<h2>Estrutura do Projeto</h2>

<pre>
relogio-sistema-java/
|
+-- src/
|   +-- Main.java
|   +-- TelaRelogio.java
|
+-- README.md
</pre>

<hr>

<h2>Tecnologias Utilizadas</h2>

<ul>
  <li>Java SE</li>
  <li>Swing</li>
  <li>JFrame</li>
  <li>JLabel</li>
  <li>JButton</li>
  <li>Date / Calendar</li>
  <li>LocalDateTime</li>
  <li>ZoneId</li>
</ul>

<hr>

<h2>Lógica Principal</h2>

<pre>
import java.time.LocalDateTime;
import java.time.ZoneId;
import java.time.format.DateTimeFormatter;

public class RelogioSistema {

    public static void main(String[] args) {
        LocalDateTime agora = LocalDateTime.now();
        ZoneId fuso = ZoneId.systemDefault();

        DateTimeFormatter data =
            DateTimeFormatter.ofPattern("dd/MM/yyyy");
        DateTimeFormatter hora =
            DateTimeFormatter.ofPattern("HH:mm:ss");

        System.out.println("Data: " + agora.format(data));
        System.out.println("Hora: " + agora.format(hora));
        System.out.println("Ano: " + agora.getYear());
        System.out.println("Fuso Horário: " + fuso);
    }
}
</pre>

<hr>

<h2>Aprendizados</h2>

<ul>
  <li>Manipulação de data e hora em Java</li>
  <li>Uso da API java.time</li>
  <li>Criação de interfaces gráficas com Swing</li>
  <li>Integração entre lógica e interface</li>
  <li>Boas práticas de organização de código</li>
</ul>

<hr>

<h2>Possíveis Melhorias</h2>

<ul>
  <li>[ ] Atualização automática em tempo real</li>
  <li>[ ] Suporte a múltiplos fusos horários</li>
  <li>[ ] Tema claro/escuro</li>
  <li>[ ] Internacionalização da interface</li>
</ul>

<hr>

<h2>Autor</h2>

<p>
Desenvolvido durante o <strong>Curso de Java 40 Horas</strong> do
<a href="https://www.cursoemvideo.com/" target="_blank">Curso em Vídeo</a><br>
<strong>Professor:</strong> Gustavo Guanabara
</p>

<hr>

<h2>Links Úteis</h2>

<ul>
  <li><a href="https://docs.oracle.com/en/java/" target="_blank">Documentação Java</a></li>
  <li><a href="https://docs.oracle.com/javase/8/docs/api/java/time/package-summary.html" target="_blank">Java Time API</a></li>
  <li><a href="https://docs.oracle.com/javase/tutorial/uiswing/" target="_blank">Tutorial Swing</a></li>
  <li><a href="https://www.cursoemvideo.com/curso/java-basico/" target="_blank">Curso em Vídeo - Java</a></li>
</ul>

<p align="center">
  Se este projeto te ajudou, considere dar uma estrela ⭐
</p>

</body>
</html>
