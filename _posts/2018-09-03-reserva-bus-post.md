---
layout: post
title: Reserva-Bus
categories: misc
---
### INTRODUÇÃO
Olá,nesse primeiro post irei mostrar um projeto desenvolvido por mim durante a disciplina de Linguagem de Programação.
O projeto consiste na construção de um sistema de reserva de passagem de onibus, o mesmo foi implementado em c++ puro e foi inspirado em um sistema já existente concebido pela empresa Gontijo de transportes, a aplicação conta com muitas opções de destinos e horários e
apresenta uma interatividade bem grande com o cliente.Tomando como base esse sistema,tive a oportunidade de desenvolver algo bem perecido, porém com menos opções de horários e destinos.
![Bem-vindo]({{ "/assets/images/bemvindo.png" | absolute_url }})
### LÓGICA DO PROGRAMA
A lógica do programa é baseada na biblioteca **fstream** e na utilização do tipo **struct**.basicamente no começo do programa há uma leitura dos arquivos .txt referentes a cada destido;dentro de cada arquivo entá contido informaçôes como: nome,RG,numero do assento e se o mesmo esta ocupado ou não,esses dados são carregadas para as structs no inicio da implementação;Com este processo feito, o usuário poderá escolher tranquilamente seu destino e assento. Ao final do programa as informações geradas pelo usuário(essas foram armazenadas nas structs em quanto o cliente fazia suas escolhas) são carregadas para os arquivos .txt referentes a cada destino.
### BIBLIOTECAS UTILIZADAS
---
	#include<iostream>
	#include<cstring>
	#include<cstdlib>
	#include<stdio.h>
	#include<time.h>
	#include<unistd.h>
	#include<fstream>
---

### IMPLEMENTAÇÃO DAS STRUCTS
---

	struct Cadeira //estrutura para pegar a fileira e o numero da poltrona
	{
    	string lugar;
    	string ocupado;
	};

	struct Pessoa // estrutura do cadastro do passageiro
	{
    	string nome,rg;
    	Cadeira assento;
	};

	struct Onibus //estrutura para ver se está ocupado ou nao o lugar
	{
    	Pessoa ocupantes[MAXL];
	};
---
### INICIO DO PROGRAMA



