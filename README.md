# onchain
fullnode bitcoin (tor + bitcoind)

architettura: x86_64

ssh: 1 TB (consigliato 2TB)






# istruzioni
- creare le immagini docker

      cd dockerfile/tor
      docker build -t tor .
      cd ../..
      cd dockerfile/bitcoin
      docker build -t bitcoin . 
      cd ../..
  
- creare il file bitcoin.conf in bitcoin

      cp bitcoin/bitcoin.conf.sample bitcoin/bitcoin.conf
  
- creare il file torrc in tor
  
      cp tor/torrc.sample tor/toorc
  
- far partire il nodo

  dalla cartella dove è presente il cocker compose

      docker-compose up -d
  
  


  
 
