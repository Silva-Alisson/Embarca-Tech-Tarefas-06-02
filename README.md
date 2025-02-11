# EmbarcaTech_PWM_ServoMotor

Este projeto faz parte da tarefa do EmbarcaTech, cujo objetivo é implementar um sistema utilizando o Pico SDK para simular o controle do ângulo de um servomotor via PWM no Raspberry Pi Pico W. A simulação é realizada na plataforma Wokwi.

## Vídeo Explicativo
A seguir, um vídeo explicativo sobre o projeto.

https://drive.google.com/file/d/15rD7BBuV_T-r3RrcUC4zkmW8ecmWg2v2/view?usp=sharing

## BitDogLab
Durante a execução do código, o LED RGB conectado ao GPIO 12 apresentou variações na intensidade da luz conforme a modulação do sinal PWM. A luminosidade foi maior com o duty cycle em 2400µs e menor em 500µs. Após a ativação da rotina periódica, ficou evidente que a intensidade do LED variava suavemente conforme o duty cycle aumentava ou diminuía.

## Requisitos e Configuração
Para executar o código, certifique-se de possuir:
- Visual Studio Code com a extensão Wokwi Simulator instalada.
- Acesso à placa BitDogLab para testes com LED RGB.
- Ambiente configurado com o Pico SDK.

## Como Executar
1. Abra o arquivo `diagram.json` no Wokwi Simulator para inicializar a simulação com o Raspberry Pi Pico W e o servomotor.
2. Ao iniciar a simulação, o servomotor seguirá esta sequência:
   - 180° ➝ 90° ➝ 0° (permanecendo 5 segundos em cada posição).
   - Em seguida, o braço realizará um movimento suave e periódico entre 0° e 180°.
3. Para testar o LED na BitDogLab:
   - O LED RGB na GPIO 12 terá sua intensidade variada proporcionalmente ao nível de PWM.

## Estrutura do Repositório
- `PWM_ServoMotor.c` → Código principal do projeto.
- `diagram.json` → Arquivo de configuração do Wokwi.
- `README.md` → Documento com instruções de uso.

Este projeto demonstra a aplicação prática de PWM para controle de servomotores e intensidade de LEDs, integrando simulação e hardware real.