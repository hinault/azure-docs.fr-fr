---
title: "Didacticiel : Intégration d’Azure Active Directory à Zscaler | Microsoft Docs"
description: "Découvrez comment configurer l’authentification unique entre Azure Active Directory et Zscaler."
services: active-directory
documentationCenter: na
author: jeevansd
manager: femila
ms.assetid: 68c453f7-aff1-4614-92d3-9b86f3ad99dc
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 07/08/2017
ms.author: jeedes
ms.translationtype: HT
ms.sourcegitcommit: f76de4efe3d4328a37f86f986287092c808ea537
ms.openlocfilehash: 73c81691b68ee820e1d905a17b4f2ab6b6ceb5fd
ms.contentlocale: fr-fr
ms.lasthandoff: 07/11/2017


---
# <a name="tutorial-azure-active-directory-integration-with-zscaler"></a>Didacticiel : Intégration d’Azure AD à Zscaler

L’objectif de ce didacticiel est de montrer comment intégrer Zscaler à Azure Active Directory (Azure AD).

Intégrer Zscaler à Azure AD vous offre les avantages suivants :

- Dans Azure AD, vous pouvez contrôler l’accès à Zscaler.
- Vous pouvez autoriser les utilisateurs à être automatiquement connectés à Zscaler (via l’authentification unique) avec leurs comptes Azure AD
- Vous pouvez gérer vos comptes à partir d’un emplacement central : le portail Azure

Pour en savoir plus sur l’intégration des applications SaaS avec Azure AD, consultez [Qu’est-ce que l’accès aux applications et l’authentification unique avec Azure Active Directory ?](active-directory-appssoaccess-whatis.md).

## <a name="prerequisites"></a>Composants requis

Pour configurer l’intégration d’Azure AD à Zscaler, vous avez besoin des éléments suivants :

- Un abonnement Azure AD
- Un abonnement Zscaler pour lequel l’authentification unique est activée

> [!NOTE]
> Pour tester les étapes de ce didacticiel, nous déconseillons l’utilisation d’un environnement de production.

Vous devez en outre suivre les recommandations ci-dessous :

- N’utilisez pas votre environnement de production, sauf si cela est nécessaire.
- Si vous n’avez pas d’environnement d’essai Azure AD, vous pouvez obtenir un essai d’un mois [ici](https://azure.microsoft.com/pricing/free-trial/).

## <a name="scenario-description"></a>Description du scénario
Dans ce didacticiel, vous testez l’authentification unique Azure AD dans un environnement de test. Le scénario décrit dans ce didacticiel se compose des deux sections principales suivantes :

1. Ajouter Zscaler à partir de la galerie
2. Configuration et test de l’authentification unique Azure AD

## <a name="adding-zscaler-from-the-gallery"></a>Ajouter Zscaler à partir de la galerie
Pour configurer l’intégration de Zscaler à Azure AD, vous devez ajouter Zscaler, disponible dans la galerie, à votre liste d’applications SaaS gérées.

**Pour ajouter Zscaler à partir de la galerie, effectuez les étapes suivantes :**

1. Dans le volet de navigation gauche du **[portail Azure](https://portal.azure.com)**, cliquez sur l’icône **Azure Active Directory**. 

    ![Active Directory][1]

2. Accédez à **Applications d’entreprise**. Accédez ensuite à **Toutes les applications**.

    ![Applications][2]
    
3. Pour ajouter l’application, cliquez sur le bouton **Nouvelle application** en haut de la boîte de dialogue.

    ![Applications][3]

4. Dans la zone de recherche, tapez **Zscaler**.

    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-zscaler-tutorial/tutorial_zscaler_search.png)

5. Dans le panneau de résultats, sélectionnez **Zscaler**, puis cliquez sur le bouton **Ajouter** pour ajouter l’application.

    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-zscaler-tutorial/tutorial_zscaler_addfromgallery.png)

##  <a name="configuring-and-testing-azure-ad-single-sign-on"></a>Configuration et test de l’authentification unique Azure AD
Dans cette section, vous allez configurer et tester l’authentification unique Azure AD avec Zscaler grâce à un utilisateur de test appelé « Britta Simon ».

Pour que l’authentification unique fonctionne, Azure AD doit connaître l’utilisateur Zscaler correspondant à l’utilisateur Azure AD. En d’autres termes, il faut établir une relation entre l’utilisateur Azure AD et l’utilisateur Zscaler qui lui est associé.

Dans Zscaler, assignez la valeur de **nom d’utilisateur** dans Azure AD comme valeur de **nom d’utilisateur** pour établir la relation.

Pour configurer et tester l’authentification unique Azure AD avec Zscaler, vous devez suivre les indications des sections suivantes :

1. **[Configuring Azure AD Single Sign-On](#configuring-azure-ad-single-sign-on)** pour permettre à vos utilisateurs d’utiliser cette fonctionnalité.
2. **[Configuration des paramètres de proxy](#configuring-proxy-settings)** pour configurer les paramètres de proxy dans Internet Explorer
3. **[Création d’un utilisateur de test Azure AD](#creating-an-azure-ad-test-user)** pour tester l’authentification unique Azure AD avec Britta Simon.
4. **[Création d’un utilisateur de test Zscaler](#creating-a-zscaler-test-user)** pour avoir un équivalent de Britta Simon dans Zscaler qui est lié à la représentation de l’utilisateur Azure AD.
5. **[Affectation de l’utilisateur de test Azure AD](#assigning-the-azure-ad-test-user)** pour permettre à Britta Simon d’utiliser l’authentification unique Azure AD.
6. **[Testing Single Sign-On](#testing-single-sign-on)** pour vérifier si la configuration fonctionne.

### <a name="configuring-azure-ad-single-sign-on"></a>Configuration de l’authentification unique Azure AD

Dans cette section, vous allez activer l’authentification unique Azure AD dans le portail Azure et configurer l’authentification unique dans votre application Zscaler.

**Pour configurer l’authentification unique Azure AD avec Zscaler, effectuez les étapes suivantes :**

1. Dans le portail Azure, dans la page d’intégration de l’application **Zscaler**, cliquez sur **Authentification unique**.

    ![Configurer l’authentification unique][4]

2. Dans la boîte de dialogue **Authentification unique**, pour le **Mode**, sélectionnez **Authentification basée sur SAML** pour activer l’authentification unique.
 
    ![Configurer l’authentification unique](./media/active-directory-saas-zscaler-tutorial/tutorial_zscaler_samlbase.png)

3. Dans la section **Domaine et URL Zscaler**, effectuez les étapes suivantes :

    ![Configurer l’authentification unique](./media/active-directory-saas-zscaler-tutorial/tutorial_zscaler_url.png)

    Dans la zone de texte **URL de connexion**, tapez une URL au format suivant : `https://<companyname>.zsclaer.net`

    > [!NOTE] 
    > Cette valeur n’est pas la valeur réelle. Mettez à jour cette valeur avec l’URL de connexion réelle. Pour obtenir cette valeur, contactez [l’équipe du support Zscaler](https://www.zscaler.com/company/contact). 

4. Dans la section **Certificat de signature SAML**, cliquez sur **Téléchargez le certificat (Base64)** puis enregistrez le fichier du certificat sur votre ordinateur.

    ![Configurer l’authentification unique](./media/active-directory-saas-zscaler-tutorial/tutorial_zscaler_certificate.png) 

5. Cliquez sur le bouton **Enregistrer** .

    ![Configurer l’authentification unique](./media/active-directory-saas-zscaler-tutorial/tutorial_general_400.png)

6. Pour ouvrir la fenêtre **Configurer l’authentification**, dans la section **Configuration de Zscaler**, cliquez sur **Configurer Zscaler**. Copiez l**’URL du service d’authentification unique SAML** à partir de la **section Référence rapide.**

    ![Configurer l’authentification unique](./media/active-directory-saas-zscaler-tutorial/tutorial_zscaler_configure.png) 

7. Dans une autre fenêtre de navigateur web, connectez-vous à votre site d’entreprise Zscaler en tant qu’administrateur.

8. Dans le menu situé dans la partie supérieure, cliquez sur **Administration**.
   
    ![Administration](./media/active-directory-saas-zscaler-tutorial/ic800206.png "Administration")

9. Sous **Manage Administrators & Roles**, cliquez sur **Manage Users & Authentication**.   
            
    ![Gérer les utilisateurs et l’authentification](./media/active-directory-saas-zscaler-tutorial/ic800207.png "Gérer les utilisateurs et l’authentification")

10. Dans la section **Choose Authentication Options for your Organization** , procédez comme suit :   
                
    ![Authentication](./media/active-directory-saas-zscaler-tutorial/ic800208.png "Authentication")
   
    a. Sélectionnez **Authenticate using SAML Single Sign-On**.

    b. Cliquez sur **Configure SAML Single Sign-On Parameters**.

11. Dans la boîte de dialogue **Configure SAML Single Sign-On Parameters** (Configurer les paramètres d’authentification unique SAML), effectuez les étapes suivantes, puis cliquez sur **Done** (Terminé).

    ![Authentification unique](./media/active-directory-saas-zscaler-tutorial/ic800209.png "Authentification unique")
    
    a. Collez **l’URL du service d’authentification unique SAML** que vous avez copiée à partir du portail Azure dans la zone de texte **URL of the SAML Portal to which users are sent for authentication** (URL du portail SAML vers lequel les utilisateurs sont redirigés afin de s’authentifier).
    
    b. Dans la zone de texte **Attribute containing Login Name**, tapez **NameID**.
    
    c. Pour charger le certificat téléchargé, cliquez sur **Zscaler pem**.
    
    d. Sélectionnez **Enable SAML Auto-Provisioning**.

12. Dans la page **Configure User Authentication** , procédez comme suit :

    ![Administration](./media/active-directory-saas-zscaler-tutorial/ic800210.png "Administration")
    
    a. Cliquez sur **Enregistrer**.

    b. Cliquez sur **Activate Now**.

## <a name="configuring-proxy-settings"></a>Configuration des paramètres de proxy
### <a name="to-configure-the-proxy-settings-in-internet-explorer"></a>Pour configurer les paramètres de proxy dans Internet Explorer

1. Démarrez **Internet Explorer**.

2. Pour ouvrir la boîte de dialogue **Options Internet**, sélectionnez **Options Internet** dans le menu **Outils**.   
    
     ![Options Internet](./media/active-directory-saas-zscaler-tutorial/ic769492.png "Options Internet")

3. Cliquez sur l’onglet **Connexions** .   
  
     ![Connexions](./media/active-directory-saas-zscaler-tutorial/ic769493.png "Connexions")

4. Cliquez sur **Paramètres réseau** pour ouvrir la boîte de dialogue **Paramètres réseau**.

5. Dans la section Serveur proxy, procédez comme suit :   
   
    ![Serveur proxy](./media/active-directory-saas-zscaler-tutorial/ic769494.png "Serveur proxy")

    a. Sélectionnez **Utiliser un serveur proxy pour le réseau local**.

    b. Dans la zone de texte Adresse, tapez **gateway.zscaler.net**.

    c. Dans la zone de texte Port, tapez **80**.

    d. Sélectionnez **Ne pas utiliser de serveur proxy pour les adresses locales**.

    e. Cliquez sur **OK** pour fermer la boîte de dialogue **Paramètres du réseau local**.

6. Cliquez sur **OK** pour fermer la boîte de dialogue **Options Internet**.

> [!TIP]
> Vous pouvez maintenant lire une version concise de ces instructions dans le [portail Azure](https://portal.azure.com), pendant que vous configurez l’application.  Après avoir ajouté cette application à partir de la section **Active Directory > Applications d’entreprise**, cliquez simplement sur l’onglet **Authentification unique** et accédez à la documentation incorporée par le biais de la section **Configuration** en bas. Vous pouvez en savoir plus sur la fonctionnalité de documentation incorporée ici : [Documentation incorporée Azure AD]( https://go.microsoft.com/fwlink/?linkid=845985)
> 

### <a name="creating-an-azure-ad-test-user"></a>Création d’un utilisateur de test Azure AD
L’objectif de cette section est de créer un utilisateur de test appelé Britta Simon dans le portail Azure.

![Créer un utilisateur Azure AD][100]

**Pour créer un utilisateur de test dans Azure AD, procédez comme suit :**

1. Dans le panneau de navigation gauche du **portail Azure**, cliquez sur l’icône **Azure Active Directory**.

    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-zscaler-tutorial/create_aaduser_01.png) 

2. Pour afficher la liste des utilisateurs, accédez à **Utilisateurs et groupes**, puis cliquez sur **Tous les utilisateurs**.
    
    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-zscaler-tutorial/create_aaduser_02.png) 

3. Pour ouvrir la boîte de dialogue **Utilisateur**, cliquez sur **Ajouter** en haut de la boîte de dialogue.
 
    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-zscaler-tutorial/create_aaduser_03.png) 

4. Dans la boîte de dialogue **Utilisateur**, procédez comme suit :
 
    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-zscaler-tutorial/create_aaduser_04.png) 

    a. Dans la zone de texte **Nom**, entrez **BrittaSimon**.

    b. Dans la zone de texte **Nom d’utilisateur**, tapez **l’adresse e-mail** de Britta Simon.

    c. Sélectionnez **Afficher le mot de passe** et notez la valeur du **mot de passe**.

    d. Cliquez sur **Create**.
 
### <a name="creating-a-zscaler-test-user"></a>Création d’un utilisateur de test Zscaler

Pour se connecter à Zscaler, les utilisateurs d’Azure AD doivent être attribués dans Zscaler.  
Dans le cas de Zscaler, l’approvisionnement est une tâche manuelle.

### <a name="to-configure-user-provisioning-perform-the-following-steps"></a>Pour configurer l'approvisionnement des utilisateurs, procédez comme suit :

1. Connectez-vous au locataire **Zscaler** .

2. Cliquez sur **Administration**.   
   
    ![Administration](./media/active-directory-saas-zscaler-tutorial/ic781035.png "Administration")

3. Cliquez sur **User Management**.   
        
     ![Ajouter](./media/active-directory-saas-zscaler-tutorial/ic781036.png "Ajouter")

4. Sous l’onglet **Utilisateurs**, cliquez sur **Ajouter**.
      
    ![Ajouter](./media/active-directory-saas-zscaler-tutorial/ic781037.png "Ajouter")

5. Dans la section Add User, procédez comme suit :
        
    ![Ajouter un utilisateur](./media/active-directory-saas-zscaler-tutorial/ic781038.png "Ajouter un utilisateur")
   
    a. Renseignez les zones de texte **UserID**, **Nom d’affichage de l’utilisateur**, **Mot de passe** et **Confirmer le mot de passe**, puis sélectionnez **Groupes** ainsi que l’attribut **Département** du compte AAD valide que vous souhaitez approvisionner.

    b. Cliquez sur **Enregistrer**.

> [!NOTE]
> Vous pouvez utiliser tout autre outil ou n’importe quelle API de création de compte d’utilisateur fournis par Zscaler pour approvisionner des comptes d’utilisateur Azure AD.

### <a name="assigning-the-azure-ad-test-user"></a>Affectation de l’utilisateur de test Azure AD

Dans cette section, vous allez autoriser Britta Simon à utiliser l’authentification unique Azure en lui accordant l’accès à Zscaler.

![Affecter des utilisateurs][200] 

**Pour attribuer Britta Simon à Zscaler, effectuez les étapes suivantes :**

1. Dans le portail Azure, ouvrez la vue des applications, accédez à la vue des répertoires, accédez à **Applications d’entreprise**, puis cliquez sur **Toutes les applications**.

    ![Affecter des utilisateurs][201] 

2. Dans la liste des applications, sélectionnez **Zscaler**.

    ![Configurer l’authentification unique](./media/active-directory-saas-zscaler-tutorial/tutorial_zscaler_app.png) 

3. Dans le menu de gauche, cliquez sur **Utilisateurs et groupes**.

    ![Affecter des utilisateurs][202] 

4. Cliquez sur le bouton **Ajouter**. Ensuite, sélectionnez **Utilisateurs et groupes** dans la boîte de dialogue **Ajouter une affectation**.

    ![Affecter des utilisateurs][203]

5. Dans la boîte de dialogue **Utilisateurs et groupes**, sélectionnez **Britta Simon** dans la liste des utilisateurs.

6. Cliquez sur le bouton **Sélectionner** dans la boîte de dialogue **Utilisateurs et groupes**.

7. Cliquez sur le bouton **Affecter** dans la boîte de dialogue **Ajouter une affectation**.
    
### <a name="testing-single-sign-on"></a>Test de l’authentification unique

Dans cette section, vous allez tester la configuration de l’authentification unique Azure AD à l’aide du volet d’accès.

En cliquant sur la vignette Zscaler dans le Panneau d’accès, vous allez en principe être connecté automatiquement à votre application Zscaler.
Pour plus d’informations sur le panneau d’accès, consultez [Présentation du panneau d’accès](active-directory-saas-access-panel-introduction.md).

## <a name="additional-resources"></a>Ressources supplémentaires

* [Liste de didacticiels sur l’intégration d’applications SaaS avec Azure Active Directory](active-directory-saas-tutorial-list.md)
* [Qu’est-ce que l’accès aux applications et l’authentification unique avec Azure Active Directory ?](active-directory-appssoaccess-whatis.md)

<!--Image references-->

[1]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_04.png

[100]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_201.png
[202]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_202.png
[203]: ./media/active-directory-saas-zscaler-tutorial/tutorial_general_203.png


