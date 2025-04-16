document.addEventListener('DOMContentLoaded', function() {
    // Menu mobile
    const menuToggle = document.querySelector('.menu-toggle');
    const navMenu = document.querySelector('.nav-menu');

    menuToggle.addEventListener('click', function() {
        navMenu.classList.toggle('active');
    });

    // Fechar menu ao clicar em um link
    const navLinks = document.querySelectorAll('.nav-menu a');
    navLinks.forEach(link => {
        link.addEventListener('click', () => {
            navMenu.classList.remove('active');
        });
    });

    // Formulário de contato
    const contatoForm = document.getElementById('contatoForm');
    if (contatoForm) {
        contatoForm.addEventListener('submit', function(e) {
            e.preventDefault();

            const nome = this.querySelector('#nome').value;
            const telefone = this.querySelector('#telefone').value;
            const endereco = this.querySelector('#endereco').value;
            const servico = this.querySelector('#servico').value;
            const descricao = this.querySelector('#descricao').value;

            const mensagem = `*NOVO PEDIDO DE SERVIÇO*\n\n` +
                            `*Cliente:* ${nome}\n` +
                            `*Telefone:* ${telefone}\n` +
                            `*Endereço:* ${endereco}\n` +
                            `*Serviço Solicitado:* ${servico}\n` +
                            `*Detalhes do Serviço:*\n${descricao}\n\n` +
                            `*Data do Pedido:* ${new Date().toLocaleDateString('pt-BR')}\n` +
                            `*Hora do Pedido:* ${new Date().toLocaleTimeString('pt-BR')}`;

            const whatsappUrl = `https://wa.me/5524981044713?text=${encodeURIComponent(mensagem)}`;
            window.open(whatsappUrl, '_blank');
        });
    }

    // Máscara para o campo de telefone
    const telefoneInput = document.getElementById('telefone');
    if (telefoneInput) {
        telefoneInput.addEventListener('input', function(e) {
            let value = e.target.value.replace(/\D/g, '');
            if (value.length > 0) {
                value = value.replace(/^(\d{2})(\d)/g, '($1) $2');
                if (value.length > 10) {
                    value = value.replace(/(\d{5})(\d)/, '$1-$2');
                }
            }
            e.target.value = value;
        });
    }

    // Smooth scroll para links internos
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            }
        });
    });
}); 