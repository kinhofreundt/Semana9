# Todas dependencias baixadas e rodando em localhost:3000
 ![Rodando](rodando_api.png)


# Smoke Tests
Verificam se o sistema funciona corretamente com baixa carga.
 ![Rodando](smoke_test.png)


# Load Tests
Avaliam o desempenho do sistema sob carga normal de uso.
 ![Rodando](load_test.png)


 # Stress Tests
Avaliam o desempenho do sistema sob carga alta de uso.
 ![Rodando](stress_test.png)

  # Spike Tests
Avaliam o desempenho do sistema sob carga alta inicial de uso.
 ![Rodando](spike_test.png)

## Testes que ficam inviaveis de testar na pratica, por conta do tempo

  # Breakpoint  Tests
Avaliam o desempenho maximo que o sistema suporta.
 ```
 import http from 'k6/http';
import { sleep } from 'k6';

export const options = {
    stages: [
        {
            duration: '2h',
            target: 100000
        }
    ]
}

export default function () {
    http.get('http://192.168.68.108:3000');
    sleep(1);
}
```

