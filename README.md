# corewar
Ce projet permet de créer une arène virtuelle et d'y faire s’affronter des programmes codés dans un langage simple type ASM. Il a pour but d'aborder la conception d’une VM (avec les instructions qu’elle reconnait, les registres, etc), et les problématiques de compilation d’un langage assembleur en bytecode. Avec, en bonus, le plaisir de faire s’affronter vos champions sur votre arène !

# La VM

La machine virtuelle se lance de la facon suivante :

./corewar [-v] [-dump nbr_cycles] [[-n number] champion1.cor] ...

-v permet de mettre la VM en mode verbose. Appuyez sur espace pour lancer la partie

-dump nbr_cyclesAu bout denbr_cyclescycles d’exécution, dump la mémoire sur la sortie stan-dard, puis quitte la partie. La mémoire doit être dumpée au format hexadécimal, avec 32 octets par ligne.

-n numberFixe le numéro du prochain joueur. Si absent, le joueur aura le prochain numérolibre dans l’ordre des paramètres. Le dernier joueur aura le premier processus dans l’ordre d’exécution.


# L'assembleur

L'assemble permet de compiler les champions

ex:

./asm champs/gagnant.s

./asm champs/maxidefs.s

vous pouvez ensuite envoyer les champions dans la vm :

./corewar -v champs/gagnant.cor champs/maxidefs.cor
