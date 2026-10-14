
/**
 * ============================================================================
 * PASSONS AU VERT
 * REGISTRE CENTRAL DES FICHIERS ET AUTOMATISATIONS
 * ============================================================================
 *
 * Fichier :
 * 00_REGISTRE_AUTOMATISATIONS_PASSONS_AU_VERT.gs
 *
 * Version : 2.3
 *
 * RÔLE
 * ----
 * - Centraliser l'inventaire des scripts.
 * - Décrire leurs responsabilités et leurs dépendances connues.
 * - Distinguer l'état documenté de l'état réellement vérifié.
 * - Conserver les règles métier importantes.
 * - Documenter les archives et les fonctions manquantes.
 * - Préparer les contrôles futurs sans exécuter la production.
 *
 * SÉCURITÉ
 * --------
 * Ce registre est passif.
 * Il n'appelle aucune API externe.
 * Il ne lit ni n'écrit dans Notion.
 * Il ne crée ni ne supprime de déclencheur.
 * Il ne lance aucune automatisation.
 * Il ne contient aucun token ni secret.
 *
 * IMPORTANT
 * ---------
 * Une fonction déclarée dans le registre n'est pas nécessairement
 * présente dans le code source.
 *
 * Un horaire documenté n'est pas une preuve qu'un déclencheur
 * correspondant est installé.
 *
 * ============================================================================
 */

const REGISTRE_PASSONS_AU_VERT = {

  version: '2.3',

  dernierControle: '2026-10-09',

  projet: 'Passons au Vert',

  nature: 'REGISTRE PASSIF — AUCUNE EXÉCUTION DE PRODUCTION',

  statuts: [
    'ACTIF',
    'A_CONTROLER',
    'A_CONSERVER',
    'A_RECONSTRUIRE',
    'OBSOLETE',
    'TEST'
  ],

  /**
   * États de vérification :
   *
   * DOCUMENTE :
   * Information issue d'un registre ou d'une archive.
   *
   * TESTE_HISTORIQUEMENT :
   * Un test positif a été rapporté, mais pas nécessairement rejoué.
   *
   * A_VERIFIER :
   * Le code ou l'état actuel doit être contrôlé.
   *
   * NON_RETROUVE :
   * La fonction ou la brique n'a pas été retrouvée dans les sources
   * historiques contrôlées.
   */

  fichiers: [

    // ========================================================================
    // 00 — REGISTRE CENTRAL
    // ========================================================================

    {
      id: '00',
      nom: '00_REGISTRE_AUTOMATISATIONS_PASSONS_AU_VERT.gs',
      role: 'Inventaire central des scripts, automatisations et règles métier',
      statut: 'ACTIF',
      verification: 'DOCUMENTE',
      fonctionsPubliques: [
        'afficherRegistrePassonsAuVert',
        'testerRegistrePassonsAuVert',
        'enregistrerFichierPassonsAuVert',
        'enregistrerAutomatisationPassonsAuVert'
      ],
      dependances: [],
      effets: [
        'Journalisation locale'
      ],
      remarques:
        'Registre passif. Ne doit pas déclencher lui-même les scripts inventoriés. ' +
        'Version 2.3 : intégration des informations du moteur documentaire, ' +
        'de l’archive documentaire, des règles du Radar et des incertitudes ' +
        'sur les horaires et les déclencheurs.'
    },

    // ========================================================================
    // 01 — AUTHENTIFICATION ET CONFIGURATION NOTION
    // ========================================================================

    {
      id: '01',
      nom: '01_CONFIG_AUTHENTIFICATION_NOTION.gs',
      role: 'Configuration de l’authentification Notion et des Data Sources',
      statut: 'A_CONSERVER',
      verification: 'A_VERIFIER',
      fonctionsPubliques: [],
      dependances: [
        'Notion API'
      ],
      effets: [
        'Fourniture de la configuration aux scripts dépendants'
      ],
      remarques:
        'Le token Notion est conservé hors du registre. ' +
        'Ne jamais recopier le token dans ce fichier. ' +
        'La migration éventuelle vers les Script Properties reste à étudier. ' +
        'Vérifier les noms et identifiants de configuration dans le code réel.'
    },

    // ========================================================================
    // 02 — MOTEUR DOCUMENTAIRE RADAR / CONTENUS
    // ========================================================================

    {
      id: '02',
      nom: '02_MOTEUR_DOCUMENTAIRE_RADAR_CONTENUS.gs',
      role: 'Moteur documentaire et synchronisation Radar vers Contenus',
      statut: 'ACTIF',
      verification: 'TESTE_HISTORIQUEMENT',
      fonctionsPubliques: [
        'lancerRadarQuotidien',
        'transfert Radar vers Contenus'
      ],
      dependances: [
        'Configuration Notion',
        'Base Radar',
        'Base Contenus',
        'Fonctions utilitaires Notion'
      ],
      effets: [
        'Lecture Notion',
        'Transfert de données vers Contenus selon la fonction exécutée'
      ],
      remarques:
        'Le transfert Radar vers Contenus a été déclaré validé. ' +
        'Selon le registre précédent, lancerRadarQuotidien() est absente ' +
        'et empêche le déclenchement quotidien du Radar. ' +
        'Les noms de fonctions indiqués doivent être confrontés au code réel. ' +
        'Ne pas considérer lancerRadarQuotidien comme présente simplement ' +
        'parce qu’elle figure dans cette fiche.'
    },

    // ========================================================================
    // 03 — GESTIONNAIRE DES DÉCLENCHEURS
    // ========================================================================

    {
      id: '03',
      nom: '03_GESTIONNAIRE_DECLENCHEURS_PASSONS_AU_VERT.gs',
      role: 'Gestion des déclencheurs et audit des automatisations',
      statut: 'ACTIF',
      verification: 'A_VERIFIER',
      fonctionsPubliques: [
        'fonctionExiste_'
      ],
      dependances: [
        'Google Apps Script',
        'Fonctions des automatisations déclenchées'
      ],
      effets: [
        'Gestion ou inspection des déclencheurs selon la fonction exécutée'
      ],
      remarques:
        'La fonction fonctionExiste_() a été déclarée corrigée. ' +
        'Le déclencheur YouTube a été déclaré intact. ' +
        'Le déclencheur quotidien du Radar n’est pas opérationnel ' +
        'tant que sa fonction cible reste absente. ' +
        'Ne pas installer, supprimer ou modifier un déclencheur pendant ' +
        'un simple diagnostic. Vérifier le code et les déclencheurs actuels.'
    },

    // ========================================================================
    // 04 — SIMULATION DU RADAR
    // ========================================================================

    {
      id: '04',
      nom: '04_SIMULATION_RADAR_DETECTION_PASSONS_AU_VERT',
      role: 'Simulation et documentation des règles de détection du Radar',
      statut: 'A_CONSERVER',
      verification: 'A_VERIFIER',
      fonctionsPubliques: [],
      dependances: [
        'Règles métier du Radar',
        'Éventuelles fonctions de simulation définies dans le fichier'
      ],
      effets: [
        'À déterminer par lecture du code réel'
      ],
      reglesDocumentees: {
        horairePrevu: '08:00',
        fuseauHoraire: 'À vérifier dans le code',
        maximumNouveauxSujetsParJour: 20,
        radarCumulatif: true,
        detectionDoublons: true,
        comparaisonAvecRadarExistant: true,
        comparaisonAvecDossiers: true,
        comparaisonAvecContenus: true,
        scoringEditorial: true,
        conservationSujetsRetenus: true,
        purgeApresJours: 61,
        purgeLimiteeAuxSujetsNonRetenus: true,
        idempotenceAttendue: true
      },
      remarques:
        'Fichier identifié par le propriétaire du projet comme référence ' +
        'pour les contraintes horaires. ' +
        'Le plan documentaire retrouvé décrit un départ prévu à 08:00. ' +
        'Cet horaire est une règle documentée, pas une preuve qu’un ' +
        'déclencheur est actuellement installé. ' +
        'Le code exact doit être consulté avant de conclure sur le fuseau, ' +
        'les minutes de déclenchement ou le fonctionnement réel. ' +
        'Ne pas modifier ce fichier sans autorisation explicite.'
    },

    // ========================================================================
    // 05 — GESTIONNAIRE DES IDENTIFIANTS PVV
    // ========================================================================

    {
      id: '05',
      nom: '05_GESTIONNAIRE_ID_PVV.gs',
      role: 'Gestionnaire global des identifiants permanents PVV',
      statut: 'ACTIF',
      verification: 'DOCUMENTE',
      fonctionsPubliques: [],
      dependances: [
        'Script Properties',
        'LockService'
      ],
      effets: [
        'Attribution d’identifiants permanents',
        'Mise à jour du compteur interne'
      ],
      remarques:
        'Format public : PVV-XXXXXXXX. ' +
        'Alphabet : 23456789ABCDEFGHJKMNPQRSTVWXYZ. ' +
        'Base 30. Capacité théorique : 656100000000 identifiants. ' +
        'Compteur stocké dans les Script Properties. ' +
        'LockService sert à prévenir les doublons lors d’exécutions concurrentes. ' +
        'Les identifiants ne sont pas réutilisés. ' +
        'Aucune dépendance fonctionnelle à Notion, YouTube, au Radar, ' +
        'aux titres ou aux noms scientifiques. ' +
        'Des fonctions de test et un diagnostic en lecture seule ont été signalés.'
    },

    // ========================================================================
    // 06 — MOTEUR DOCUMENTAIRE V6
    // ========================================================================

    {
      id: '06',
      nom: '06_AUTOMATISME_DOCUMENTATION_V6.gs',
      role: 'Automatisme documentaire V6 : recherche, contrôles et préparation documentaire',
      statut: 'A_CONTROLER',
      verification: 'TESTE_HISTORIQUEMENT',
      fonctionsPubliques: [
        'executerAutomatismeDocumentaireV6LectureSeule',
        'testerBlocs6a12DocumentationV6'
      ],
      dependances: [
        'Configuration Notion',
        'Radar Data Source',
        'Documentation Data Source',
        'Contenus Data Source',
        'Fonctions de recherche documentaire selon les autorisations'
      ],
      effets: [
        'Lecture Notion si autorisée',
        'Recherches externes si autorisées',
        'Écritures Notion uniquement si explicitement autorisées'
      ],
      configurationDocumentee: {
        notionApiVersion: '2026-03-11',
        radarDataSourceId: '61543e5e-0913-470b-be2f-3eee182320a4',
        documentationDataSourceId: '3f808daf-28d7-46a1-89b1-ca78a1d812e3',
        contenusDataSourceId: 'fa9ee98c-8cad-4ffe-8ca3-73df5ad10ba1',
        checkboxRadar: 'Recherche documentaire'
      },
      remarques:
        'Les autorisations PVV_DOC_V6_EXECUTION avaient été documentées ' +
        'comme toutes désactivées. ' +
        'Un test local de 20 blocs sur 20 a été rapporté comme positif. ' +
        'Cela ne prouve pas que le code actuel est identique ni que les ' +
        'services externes fonctionnent aujourd’hui. ' +
        'La fonction principale retourne DESACTIVE lorsque ' +
        'AUTORISER_LECTURE_RADAR est false. ' +
        'Ne pas activer les autorisations pour un simple contrôle du registre. ' +
        'Comparer le code réel avec l’archive documentaire avant toute intégration.'
    },

    // ========================================================================
    // ARCHIVE DOCUMENTAIRE — BRIQUES RETROUVÉES
    // ========================================================================

    {
      id: 'ARCHIVE_DOC',
      nom: 'NOM DE FICHIER À CONFIRMER — ARCHIVE DES BRIQUES DOCUMENTAIRES RETROUVÉES',
      role: 'Conservation des briques documentaires historiques non intégrées',
      statut: 'A_CONSERVER',
      verification: 'DOCUMENTE',
      fonctionsPubliques: [
        'ARCHIVE_rechercherBibliographieGratuite_',
        'ARCHIVE_searchOpenAlex_',
        'ARCHIVE_searchCrossref_',
        'ARCHIVE_searchWikimedia_',
        'ARCHIVE_searchGbif_',
        'ARCHIVE_buildResearchBlocks_',
        'ARCHIVE_rechercheDocumentaireSurDossiers',
        'ARCHIVE_regleValidationIucn_',
        'ARCHIVE_rapportSysteme_',
        'ARCHIVE_testRechercheDocumentaire_'
      ],
      dependances: [
        'UrlFetchApp',
        'OpenAlex',
        'Crossref',
        'Wikimedia Commons',
        'GBIF',
        'Helpers Notion du moteur principal pour certaines fonctions'
      ],
      effets: [
        'Appels HTTP aux API publiques dans les fonctions de recherche',
        'Construction locale de blocs Notion',
        'Écriture potentielle dans Notion via appendBlocks_ dans la fonction de recherche sur Dossiers'
      ],
      sourcesDocumentaires: [
        'OpenAlex',
        'Crossref',
        'Wikimedia Commons',
        'GBIF',
        'IUCN — principes à réintégrer, fonctions originales non recopiées'
      ],
      reglesDocumentees: {
        validationHumaineObligatoire: true,
        sourcesAutomatiquesNonAssimileesAValidationScientifique: true,
        statutIucnNonDetermineSiTaxonAmbiguOuNonVerifie: true,
        republicationImageNonAutoriseeParDefaut: true
      },
      remarques:
        'Archive explicitement non destinée à la production. ' +
        'Ne pas installer de déclencheur sur cette archive. ' +
        'Ne pas appeler automatiquement ses fonctions depuis la production ' +
        'avant vérification des dépendances et collisions de noms. ' +
        'Le nom réel du fichier doit être confirmé. ' +
        'Attention : ARCHIVE_rechercheDocumentaireSurDossiers() peut écrire ' +
        'dans Notion via appendBlocks_. Son commentaire de lecture seule ' +
        'ne doit pas être interprété comme une garantie pour cette fonction. ' +
        'Les fonctions IUCN historiques ne sont pas présentes dans l’extrait.'
    },

    // ========================================================================
    // 08 — CONTRÔLE ET SIMULATION
    // ========================================================================

    {
      id: '08',
      nom: '08_CONTROLE_HORAIRES_SIMULATION_NOTION.gs',
      role: 'Outil de contrôle proposé pour examiner les horaires et simuler des opérations',
      statut: 'A_CONTROLER',
      verification: 'A_VERIFIER',
      fonctionsPubliques: [
        'PVV08_TEST_COMPLET',
        'PVV08_CONTROLER_CODE_06',
        'PVV08_AUDITER_DECLENCHEURS',
        'PVV08_SIMULER_DEPART_HORAIRE',
        'PVV08_SIMULER_CREATION_PAGE'
      ],
      dependances: [
        'Google Apps Script',
        'Code 06 si présent',
        'Gestionnaire de déclencheurs',
        'Configuration Notion pour les contrôles correspondants'
      ],
      effets: [
        'Diagnostic local attendu',
        'Lecture des déclencheurs attendue pour l’audit',
        'Simulation locale attendue, sans création de page Notion'
      ],
      remarques:
        'Ce nom correspond à l’outil de contrôle proposé pendant le travail. ' +
        'La présence effective du fichier et de ces fonctions dans le projet ' +
        'Apps Script n’a pas été confirmée ici. ' +
        'Ne pas considérer ces fonctions comme installées ou validées sans ' +
        'vérification. Ce fichier ne remplace pas le gestionnaire de ' +
        'déclencheurs 03 et ne doit pas créer de déclencheur de production.'
    },

    // ========================================================================
    // 10 — YOUTUBE VERS NOTION
    // ========================================================================

    {
      id: '10',
      nom: '10_AUTOMATISATION_YOUTUBE_VERS_NOTION.gs',
      role: 'Synchronisation des données YouTube vers Notion',
      statut: 'ACTIF',
      verification: 'TESTE_HISTORIQUEMENT',
      fonctionsPubliques: [
        'synchroniserNotionYouTube'
      ],
      dependances: [
        'YouTube',
        'YouTube Analytics selon les opérations',
        'Configuration Notion',
        'Base Contenus'
      ],
      effets: [
        'Lecture des données YouTube',
        'Synchronisation des données dans Notion'
      ],
      remarques:
        'Synchronisation précédemment déclarée validée sur 56 vidéos uniques. ' +
        'Gestion des vues, variations et abonnés rapportée. ' +
        'Version Notion utilisée : 2026-03-11. ' +
        'Le nombre de vidéos synchronisées doit être réévalué lors d’un contrôle actuel.'
    },

    // ========================================================================
    // 88 — LISTING YOUTUBE
    // ========================================================================

    {
      id: '88',
      nom: '88_OUTIL_LISTING_VIDEOS_YOUTUBE.gs',
      role: 'Listing et contrôle des vidéos de la chaîne YouTube',
      statut: 'ACTIF',
      verification: 'A_VERIFIER',
      fonctionsPubliques: [],
      dependances: [
        'YouTube'
      ],
      effets: [
        'Lecture des données YouTube',
        'Journalisation ou production de listings selon la fonction exécutée'
      ],
      remarques:
        'Outil déclaré actif. Les fonctions exactes et les éventuelles écritures ' +
        'doivent être vérifiées dans le code réel.'
    },

    // ========================================================================
    // 89 — RÉPARATION DES IDENTIFIANTS YOUTUBE / NOTION
    // ========================================================================

    {
      id: '89',
      nom: '89_OUTIL_REPARATION_IDS_YOUTUBE_NOTION.gs',
      role: 'Réparation contrôlée des identifiants YouTube dans Notion',
      statut: 'A_CONSERVER',
      verification: 'A_VERIFIER',
      fonctionsPubliques: [],
      dependances: [
        'YouTube',
        'Notion',
        'Configuration Notion'
      ],
      effets: [
        'À déterminer selon la fonction exécutée ; peut modifier Notion'
      ],
      remarques:
        'Outil ponctuel conservé pour les réparations et contrôles. ' +
        'Les opérations de modification doivent être limitées aux cas démontrables. ' +
        'Ne pas lancer une réparation sans diagnostic préalable et validation explicite.'
    },

    // ========================================================================
    // 90 — TEST DE CONNEXION YOUTUBE
    // ========================================================================

    {
      id: '90',
      nom: '90_TEST_YOUTUBE_CONNEXION.gs',
      role: 'Test de connexion et de lecture des données YouTube',
      statut: 'TEST',
      verification: 'A_VERIFIER',
      fonctionsPubliques: [],
      dependances: [
        'YouTube',
        'Autorisations Google Apps Script'
      ],
      effets: [
        'Lecture de données selon les fonctions de test'
      ],
      remarques:
        'Outil de test indépendant. ' +
        'Vérifier les autorisations demandées avant exécution.'
    }

  ],

  // ==========================================================================
  // AUTOMATISATIONS ET RÈGLES MÉTIER
  // ==========================================================================

  automatisations: [

    {
      id: 'RADAR_08H',
      nom: 'Détection quotidienne des sujets du Radar',
      fonction: 'lancerRadarQuotidien',
      statut: 'A_RECONSTRUIRE',
      verification: 'NON_RETROUVE',
      horairePrevu: '08:00',
      fuseauHoraire: 'À confirmer dans le code 04 et les déclencheurs Apps Script',
      effetsAttendus: [
        'Recherche de sources',
        'Détection de sujets candidats',
        'Analyse et scoring éditorial',
        'Contrôle des doublons',
        'Création de pages Radar après validation des règles'
      ],
      limites: {
        maximumNouveauxSujetsParJour: 20,
        cumulatif: true,
        remplacementDesAnciensSujets: false,
        idempotenceRequise: true
      },
      statutOperationnel: 'NON CONFIRME',
      remarques:
        'Le registre précédent signale que lancerRadarQuotidien() est absente. ' +
        'L’archive confirme que le véritable détecteur quotidien n’a pas été ' +
        'retrouvé dans les sources historiques contrôlées. ' +
        'L’horaire 08:00 est documenté dans le plan de reconstruction, mais ' +
        'aucun déclencheur actif correspondant n’est confirmé.'
    },

    {
      id: 'RADAR_DOUBLONS',
      nom: 'Détection des doublons entre Radar, Dossiers et Contenus',
      fonction: 'À intégrer au véritable détecteur Radar',
      statut: 'A_RECONSTRUIRE',
      verification: 'DOCUMENTE',
      horairePrevu: 'Pendant le traitement quotidien du Radar',
      effetsAttendus: [
        'Comparer le candidat au Radar existant',
        'Comparer le candidat aux Dossiers',
        'Comparer le candidat aux Contenus',
        'Empêcher la création répétée d’un même sujet'
      ],
      remarques:
        'Règle métier documentée dans le plan de reconstruction. ' +
        'La présence d’une fonction complète et opérationnelle reste à vérifier.'
    },

    {
      id: 'RADAR_PURGE_61J',
      nom: 'Purge des sujets Radar anciens non retenus',
      fonction: 'purgeRadar61J_',
      statut: 'A_CONTROLER',
      verification: 'DOCUMENTE',
      horairePrevu: 'À vérifier dans le code de production',
      effetsAttendus: [
        'Supprimer uniquement les sujets non retenus dépassant le seuil défini'
      ],
      limites: {
        ageJours: 61,
        conserverSujetsRetenus: true,
        fonctionProductionAConfirmer: true
      },
      remarques:
        'Le nom purgeRadar61J_ apparaît dans l’archive comme une fonction ' +
        'appartenant à la production, pas à l’archive. ' +
        'Son existence, son déclencheur et ses conditions exactes doivent être vérifiés.'
    },

    {
      id: 'RADAR_VERS_CONTENUS',
      nom: 'Transfert des sujets retenus du Radar vers Contenus',
      fonction: 'Fonction de transfert du code 02 à confirmer',
      statut: 'ACTIF',
      verification: 'TESTE_HISTORIQUEMENT',
      horairePrevu: 'Selon le fonctionnement défini dans le code 02',
      effetsAttendus: [
        'Transférer les sujets retenus vers la base Contenus'
      ],
      remarques:
        'Transfert déclaré validé dans le registre précédent. ' +
        'Ne pas inventer le nom de sa fonction d’entrée ni son horaire.'
    },

    {
      id: 'YOUTUBE_NOTION',
      nom: 'Synchronisation YouTube vers Notion',
      fonction: 'synchroniserNotionYouTube',
      statut: 'ACTIF',
      verification: 'TESTE_HISTORIQUEMENT',
      horairePrevu: 'Déclencheur déclaré intact ; horaire exact à vérifier',
      effetsAttendus: [
        'Synchroniser les données YouTube vers Notion'
      ],
      remarques:
        'Le déclencheur YouTube a été déclaré intact dans le registre. ' +
        'La présence et l’horaire exacts du déclencheur doivent être contrôlés ' +
        'dans Apps Script avant de confirmer l’état actuel.'
    },

    {
      id: 'DOCUMENTATION_V6',
      nom: 'Automatisme documentaire V6',
      fonction: 'executerAutomatismeDocumentaireV6LectureSeule',
      statut: 'A_CONTROLER',
      verification: 'TESTE_HISTORIQUEMENT',
      horairePrevu: 'Aucun horaire confirmé dans le registre',
      effetsAttendus: [
        'Préparer ou exécuter des recherches documentaires selon les autorisations'
      ],
      limites: {
        autorisationsHistoriquementDesactivees: true,
        ecritureNotionAutoriseeParDefaut: false,
        declencheursAutomatiquesConfirmes: false
      },
      remarques:
        'Les tests historiques rapportés ne justifient pas d’activer les ' +
        'autorisations ni d’installer un déclencheur. Vérifier le code réel ' +
        'avant tout raccordement.'
    }

  ]

};


/**
 * ============================================================================
 * ENREGISTRER UN FICHIER
 * ============================================================================
 *
 * Ajoute une entrée en mémoire au registre courant.
 * Ne crée ni ne modifie aucun fichier Apps Script.
 * ============================================================================
 */

function enregistrerFichierPassonsAuVert(
  id,
  nom,
  role,
  statut,
  remarques
) {

  const fichier = {
    id: id,
    nom: nom,
    role: role,
    statut: statut,
    remarques: remarques || '',
    verification: 'A_VERIFIER',
    fonctionsPubliques: [],
    dependances: [],
    effets: []
  };

  REGISTRE_PASSONS_AU_VERT.fichiers.push(fichier);

  return fichier;
}


/**
 * ============================================================================
 * ENREGISTRER UNE AUTOMATISATION
 * ============================================================================
 *
 * Ajoute une entrée en mémoire.
 * Ne crée aucun déclencheur et ne lance aucune fonction.
 * ============================================================================
 */

function enregistrerAutomatisationPassonsAuVert(
  id,
  nom,
  fonction,
  statut,
  remarques
) {

  const automatisation = {
    id: id,
    nom: nom,
    fonction: fonction,
    statut: statut,
    verification: 'A_VERIFIER',
    remarques: remarques || ''
  };

  REGISTRE_PASSONS_AU_VERT.automatisations.push(
    automatisation
  );

  return automatisation;
}


/**
 * ============================================================================
 * AFFICHER LE REGISTRE COMPLET
 * ============================================================================
 *
 * Journalisation uniquement.
 * ============================================================================
 */

function afficherRegistrePassonsAuVert() {

  Logger.log(
    JSON.stringify(
      REGISTRE_PASSONS_AU_VERT,
      null,
      2
    )
  );

}


/**
 * ============================================================================
 * RAPPORT SYNTHÉTIQUE DU REGISTRE
 * ============================================================================
 *
 * Ne contacte aucun service et ne modifie aucune donnée externe.
 * ============================================================================
 */

function rapportSyntheseRegistrePassonsAuVert() {

  const registre = REGISTRE_PASSONS_AU_VERT;

  const lignes = [];

  lignes.push('PASSONS AU VERT — RAPPORT DU REGISTRE');
  lignes.push('Version : ' + registre.version);
  lignes.push('Dernier contrôle déclaré : ' + registre.dernierControle);
  lignes.push('');

  lignes.push('FICHIERS : ' + registre.fichiers.length);

  registre.fichiers.forEach(function(fichier) {

    lignes.push(
      '[' + fichier.statut + '] ' +
      fichier.id + ' — ' +
      fichier.nom +
      ' | Vérification : ' +
      (fichier.verification || 'NON RENSEIGNEE')
    );

  });

  lignes.push('');
  lignes.push('AUTOMATISATIONS : ' + registre.automatisations.length);

  registre.automatisations.forEach(function(automatisation) {

    lignes.push(
      '[' + automatisation.statut + '] ' +
      automatisation.nom +
      ' | Fonction : ' +
      (automatisation.fonction || 'NON RENSEIGNEE') +
      ' | Vérification : ' +
      (automatisation.verification || 'NON RENSEIGNEE')
    );

  });

  lignes.push('');
  lignes.push(
    'Rappel : ce rapport décrit le registre et ne vérifie pas le code réel.'
  );

  const rapport = lignes.join('\n');

  Logger.log(rapport);

  return rapport;

}


/**
 * ============================================================================
 * TEST STRUCTUREL DU REGISTRE
 * ============================================================================
 *
 * Vérifie uniquement la cohérence interne des données.
 *
 * NE teste PAS :
 * - l'existence des fichiers Apps Script ;
 * - l'existence réelle des fonctions ;
 * - l'accès à Notion ;
 * - les déclencheurs installés ;
 * - les API externes.
 * ============================================================================
 */

function testerRegistrePassonsAuVert() {

  const registre = REGISTRE_PASSONS_AU_VERT;

  if (!registre) {
    throw new Error('Le registre Passons au Vert est introuvable.');
  }

  if (!registre.version) {
    throw new Error('La version du registre est absente.');
  }

  if (!Array.isArray(registre.statuts)) {
    throw new Error('La liste des statuts est invalide.');
  }

  if (!Array.isArray(registre.fichiers)) {
    throw new Error('La liste des fichiers est invalide.');
  }

  if (!Array.isArray(registre.automatisations)) {
    throw new Error('La liste des automatisations est invalide.');
  }

  const idsFichiers = {};
  const idsAutomatisations = {};

  registre.fichiers.forEach(function(fichier) {

    if (!fichier.id) {
      throw new Error('Un fichier du registre n’a pas d’identifiant.');
    }

    if (!fichier.nom) {
      throw new Error(
        'Le fichier ' + fichier.id + ' n’a pas de nom.'
      );
    }

    if (!fichier.statut) {
      throw new Error(
        'Le fichier ' + fichier.nom + ' n’a pas de statut.'
      );
    }

    if (registre.statuts.indexOf(fichier.statut) === -1) {
      throw new Error(
        'Statut invalide pour ' + fichier.nom + ' : ' + fichier.statut
      );
    }

    if (idsFichiers[fichier.id]) {
      throw new Error(
        'Identifiant de fichier dupliqué : ' + fichier.id
      );
    }

    idsFichiers[fichier.id] = true;

    if (
      fichier.fonctionsPubliques !== undefined &&
      !Array.isArray(fichier.fonctionsPubliques)
    ) {
      throw new Error(
        'fonctionsPubliques doit être un tableau : ' + fichier.nom
      );
    }

    if (
      fichier.dependances !== undefined &&
      !Array.isArray(fichier.dependances)
    ) {
      throw new Error(
        'dependances doit être un tableau : ' + fichier.nom
      );
    }

  });

  registre.automatisations.forEach(function(automatisation) {

    if (!automatisation.id) {
      throw new Error(
        'Une automatisation du registre n’a pas d’identifiant.'
      );
    }

    if (!automatisation.nom) {
      throw new Error('Une automatisation n’a pas de nom.');
    }

    if (!automatisation.statut) {
      throw new Error(
        'Une automatisation n’a pas de statut : ' +
        automatisation.nom
      );
    }

    if (registre.statuts.indexOf(automatisation.statut) === -1) {
      throw new Error(
        'Statut invalide pour l’automatisation ' +
        automatisation.nom +
        ' : ' +
        automatisation.statut
      );
    }

    if (idsAutomatisations[automatisation.id]) {
      throw new Error(
        'Identifiant d’automatisation dupliqué : ' +
        automatisation.id
      );
    }

    idsAutomatisations[automatisation.id] = true;

  });

  Logger.log('TEST STRUCTUREL DU REGISTRE : OK');
  Logger.log('Version : ' + registre.version);
  Logger.log('Fichiers : ' + registre.fichiers.length);
  Logger.log('Automatisations : ' + registre.automatisations.length);
  Logger.log('Aucune API externe appelée.');
  Logger.log('Aucune écriture Notion effectuée.');
  Logger.log('Aucun déclencheur créé ou modifié.');

  return {
    resultat: 'OK',
    version: registre.version,
    fichiers: registre.fichiers.length,
    automatisations: registre.automatisations.length,
    apiExterne: false,
    ecritureNotion: false,
    modificationDeclencheur: false
  };

}
