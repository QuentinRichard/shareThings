 
	* Activite enfants pour les nounous
# shareThings
## Permet de partager des elements comme :
	* Liste des cources
	* Envoyer des event pour un annive
	* Synchroniser des events pour des organisations (fetes, anniversaire, mariage)
	* Arbre genealogique, amicale, cause a effet
	* Jeux
	
	
## Documents constituant le systéme:
	### Users :
		- DocType
		- Description user
			{FirstName, LastName, Adr, ville, CP, Tel, Mail, Sex, DateNaissance}
		- Agregation de Items
			[Item._Id]
		- Agregation of Collaboration
			[Item._Id]
		- Settings
			{Notification periode:enum; notif:Mail - Push}
		
	### Items:
		- DocType
		- Name ==> Tag or name of plugin
		- Description
			{txt, version, validity, userDesc}
		- Data
			{}
		- Moderator
			{Doc._Id}
		- Collaborateur
			[Doc._Id]
		
## Structure du site
		### Page d'accueil Login
		  *Logger ==> Home page :
				  - Onglet Principal : Liste des Items que l'on a créé et auquel on contribut
				  - Onglet Plus : Cree un Itemm, Rechercher/Retirer une contribution
				  - Page profile : Liste des parametres et des données perso
			### Page Items :
			La page realise la rendu specifique a aux Items, et d'exploiter sa fonction. 
			A chaque save des modifications (*), une requête est envoyé et est suivie de l'envois d'un mail/push (*). (*) Optionnel  
			Le moderateur pourra administrer cette page(cf page cree).
			### Page Cree :
			Cette page permet de creer une instance d'une lbrairie predefinie : en fonction, definir son rendue, d'administrer les parametres de l'Item, et d'rechercher/ajouter un contribueur.
			### Page Rechercher :
			Recherche une personne en fonction du description ou sur des projets ou vis et versa en fonction des collaborateurs
			### Page Parametres :
			Liste toutes les donnees et permet de les modifiers
			Parametre de notification
			
			
		
	
	
	
	
	