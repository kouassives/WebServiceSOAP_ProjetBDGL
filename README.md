# WebServiceSOAP_ProjetBDGL

Ce programme est écrit la comunication entre des clients et un serveur web.

## Utilisation:

1- Clonez le projet https://github.com/kouassives/WebServiceSOAP_ProjetBDGL.git
2- Lancer le web service -> Clic droit sur le fichier classe \src\com\web\service\Taxe.java -> Web Services
-> Create Web Service. Sous « Service implementation », choisir
« Start service » (choix par défaut) et modifier la scroll bar sous
« Client type » pour générer un « Test client »
    NB: Ne pas oublier de cocher « Publish the Web service » & « Monitor the web service »
3-Arrivé à ce stade, Eclipse doit lancer le serveur Tomcat avec votre web service. Il doit aussi générer le client(${PROJET_NAME}Client). Lorsque l’opération est achevée, Eclipse exécute le client.
4-Exporter le client pour les machines clientes -> exporter le package generé dans le client.
    4-1- Implemenet une classe principale pour l'utilisation du package client.
      Les prototypes des services disponibles sur le serveur sont dans la classe *proxy.java
      Exemple de classe principale:
        tatic HelloWorldProxy port;
	      public static void main(String[] args) throws ServiceException, RemoteException {
        // TODO Auto-generated method stub
        HelloWorldProxy z = new HelloWorldProxy();
        java.lang.String chaine =z.toUpper("Bien");
        System.out.println("Resultat de la procédure " +chaine + "\nEndPoint " + z.getEndpoint());
	      }
