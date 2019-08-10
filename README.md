# helpers_codeigniter

Esse repositório será detinado a helpers para auxiliar programadores no desnevolvimento com com o framework Codeigniter.

## TEMPLATE HELPER

helper para carregamento simplicado de views.
  ### INSTALAÇÃO:
    
    1 - Insira o arquivo dentro na pasta 'application/helpers'
    2 - Carregue o helper você pode fazer de 2 maneiras, porém como será usado contantemente sugiro o primeiro método.
      - Vár em 'application/config/autoload.php' e em carrgue template dessa forma: $autoload['helper'] = array('template');
      - Ou use na sua classe $this->load->helpers('template');
      Obs: das duas formas funcionam, porém da primeira maneira você só precisará fazer uma ver, e todo seu projeto terá acesso.
  
  ### USO:
    
    #### INSTANCIA
    * no construtor da sua classe intancie a classe da seguinte forma $this->template = new Template('templates', 'param');
      o primeiro parâmetro é referente ao caminho arquivos de template, exemplo: header, aside e footer ouseja arquivos que não mudam.
        no exemplo acima é como se os arquivos estivessem dentro de uma pasta chamada templates que estão dentro de views.
        
      O segundo é o local onde estão os demais arquivos ex: home, sobre e etc... Não é obrigatório mas se for deixado vazio o classe entende 
      que seus arquivos estão soltos na pasta views.
      Caso todo o suas views estaja separadas em subpastas como proexemplo: frontend/ e backend/ então você intancia com o segundo parametro
      apontando para a pasta em questão.
      
    #### CARREGANDO ARQUIVOS
    
    Depois de instanciado você pode carregar seu template usando o método load(), esse método recebe 2 parâmetros, o primeiro com os dados
    que suas views vão acessas como títulos e conteúdos vindos da banco de dados. O segundo parâmetro é com o(s) arquivo(s) que você quer carregar
    o segundo parâmetro carrega apenas um arquivo 'home' ou vários se você passa um array ex:
    
    primeira forma:
    $this->template->load($data, 'home');
    
    segunda forma:
    $this->template->load($data, ['sobre', 'home', newslater']);
    
    
      
