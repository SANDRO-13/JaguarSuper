

🛠️ Etapas para instalar o JaguarSuper no Termux

1. Instale o Termux e atualize os pacotes
`bash
pkg update && pkg upgrade
`

2. Instale dependências básicas
`bash
pkg install git python nano
`

3. Clone o SQLMap
`bash
git clone https://github.com/sqlmapproject/sqlmap.git
`

> Isso criará a pasta ~/sqlmap com o script sqlmap.py

---

4. Crie o script JaguarSuper
`bash
nano jaguarsuper.py
`

> Cole as 4 partes do script JaguarSuper que você já recebeu. Salve com CTRL + O, depois CTRL + X.

---

5. Crie o instalador install.sh
`bash
echo '#!/bin/bash
cp jaguarsuper.py /data/data/com.termux/files/usr/bin/JaguarSuper
chmod +x /data/data/com.termux/files/usr/bin/JaguarSuper
echo "✅ JaguarSuper instalado com sucesso!"' > install.sh
chmod +x install.sh
`

---

6. Execute o instalador
`bash
./install.sh
`

---

7. Execute o JaguarSuper
`bash
JaguarSuper
`

> O script vai abrir o menu interativo, pedir a URL vulnerável e iniciar a análise com SQLMap.
