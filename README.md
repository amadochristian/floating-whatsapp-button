<h1>Botão WhatsApp Flutuante com Mensagem Personalizada de Produto</h1>
<p>Feito para E-commerce ou lojas virtuais</p>
<h2>Análise do Código de Botão do WhatsApp</h2>
<p>Este código implementa um botão flutuante do WhatsApp que aparece no canto inferior direito da página e tem comportamento inteligente dependendo se o usuário está em uma página de produto ou não.</p>
Componentes principais:<br>
1. Estilo e Ícone
<ul> <li>Usa Font Awesome para o ícone do WhatsApp</li> <li>O botão é posicionado fixo na tela com estilo circular verde (cor do WhatsApp)</li> </ul>
2. Funcionalidade JavaScript
<ul> <li>O código só executa após o DOM estar completamente carregado (DOMContentLoaded)</li> <li>Captura o clique no botão e previne o comportamento padrão do link</li> </ul>
3. Lógica Inteligente
<ul> <li>Verifica se está em uma página de produto procurando por um elemento com classe .product-sku</li> </ul><h4>Se for página de produto:</h4> <ul> <li>Pega o nome do produto (do SKU)</li> <li>Pega o preço do produto (do elemento #variacaoPreco)</li> <li>Pega a URL atual</li> <li>Monta uma mensagem estruturada com estas informações</li> </ul><h4>Se não for página de produto:</h4> <ul> <li>Usa uma mensagem genérica</li> </ul>
4. Redirecionamento
<ul> <li>Codifica a mensagem para URL</li> <li>Abre o link do WhatsApp em nova aba com a mensagem formatada</li> </ul>

Você pode alterar a classe que busca se é uma página de produto ou não:<br>
var productNameElement = document.querySelector(".product-sku");
