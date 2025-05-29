#include <stdio.h>

int main() {
    int opcao, quantidade;
    float subtotal = 0.0, preco;
    int tipoCliente, formaPagamento;
    float descontoCliente = 0.0, descontoPagamento = 0.0;
    float valorFinal;

    // Menu de produtos com preços
    do {
        printf("\n---------------- Papelaria & Arte --------------\n");
        printf("1 - Caderno espiral .......... R$ 25.90\n");
        printf("2 - Caneta gel ............... R$ 4.50\n");
        printf("3 - Bloco de desenho ......... R$ 22.00\n");
        printf("4 - Pincel artístico .......... R$ 10.00\n");
        printf("5 - Tinta acrílica ............ R$ 18.75\n");
        printf("6 - Lápis de cor (12 cores) ... R$ 25.90\n");
        printf("7 - Finalizar pedido\n");
        printf("8 - Sair da aplicação\n");
        printf("----------------------------------\n");
        printf("Escolha um produto (1-8): ");
        scanf("%d", &opcao);

        switch(opcao) {
            case 1: preco = 25.90; break;
            case 2: preco = 4.50; break;
            case 3: preco = 22.00; break;
            case 4: preco = 10.00; break;
            case 5: preco = 18.75; break;
            case 6: preco = 25.90; break;
            case 7: break; // Finalizar pedido
            case 8: 
    
                printf("Saindo da aplicação.\n");
                return 0;
            default:
                printf("Opção inválida! Tente novamente.\n");
                continue;
        }

        if (opcao >= 1 && opcao <= 6) {
            printf("Digite a quantidade: ");
            scanf("%d", &quantidade);
            subtotal += preco * quantidade;
            printf("Subtotal atual: R$ %.2f\n", subtotal);
        }

    } while(opcao != 7);

    // Finalizar pedido
    if (subtotal == 0.0) {
        printf("Nenhum produto selecionado. Encerrando aplicação.\n");
        return 0;
    }

    // Solicita o tipo de cliente
    printf("\nTipo de cliente:\n");
    printf("1 - Cliente CLUBE (10%% de desconto)\n");
    printf("2 - Cliente comum (sem desconto)\n");
    printf("Informe o tipo de cliente (1 ou 2): ");
    scanf("%d", &tipoCliente);

    if (tipoCliente == 1) {
        descontoCliente = 0.10;
    }

    // Solicita a forma de pagamento
    printf("\nForma de pagamento:\n");
    printf("1 - À vista (10%% de desconto adicional)\n");
    printf("2 - A prazo (sem desconto)\n");
    printf("Informe a forma de pagamento (1 ou 2): ");
    scanf("%d", &formaPagamento);

    if (formaPagamento == 1) {
        descontoPagamento = 0.10;
    }

    // Cálculo dos descontos
    valorFinal = subtotal;
    valorFinal -= valorFinal * descontoCliente;
    valorFinal -= valorFinal * descontoPagamento;

    // Exibe o resumo final
    printf("\n---------------- RESUMO DO PEDIDO -------------\n");
    printf("Subtotal: R$ %.2f\n", subtotal);
    printf("Desconto (cliente): %.0f%%\n", descontoCliente * 100);
    printf("Desconto (pagamento): %.0f%%\n", descontoPagamento * 100);
    printf("Valor final a pagar: R$ %.2f\n", valorFinal);

    return 0;
}
