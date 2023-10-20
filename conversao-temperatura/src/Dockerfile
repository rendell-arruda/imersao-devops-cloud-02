# Imagem base - Inicializa o build de uma imagem a partir de uma imagem base
FROM node:18.18.2
# diretório de trabalho - Define o diretório de trabalho para o diretório corrente
WORKDIR /app
# copia o arquivo package.json para o diretório de trabalho - Copia o arquivo ou diretórios e add ao sistema de arq da imagem
COPY package*.json .
# baixar/instala as dependências - executa comandos dentro do container
RUN npm install
# copia o restante dos arquivos
COPY . .
# expõe a porta 8080 - Define que o container precisa exportar a porta em questão
EXPOSE 8080
# comando para executar a aplicação - define o comando e/ou os parametros que serão executados quando o container for iniciado
CMD [ "node", "server.js" ]

# LABEL - add metadados a imagem
# ENV - define variáveis de ambiente
# ADD - copia arquivos ou diretórios ou arquivos remotos para o sistema de arquivos da imagem
# ARG - define variáveis que podem ser passadas ao build da imagem
# VOLUME - cria um ponto de montagem para uso com um container . define volumes 
# USER - define o usuário que será usado para executar os comandos RUN, CMD e ENTRYPOINT
# ENTRYPOINT - Ajuda voce a configurar um container que pode ser executado como um executável