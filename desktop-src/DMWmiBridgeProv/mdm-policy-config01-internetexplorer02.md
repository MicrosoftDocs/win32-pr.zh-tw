---
title: MDM_Policy_Config01_InternetExplorer02 類別
description: MDM \_ Policy \_ Config01 InternetExplorer02 類別會設定 \_ Internet Explorer 原則。
ms.assetid: 32cc6a64-3008-4add-96e8-33b31beb207f
keywords:
- MDM_Policy_Config01_InternetExplorer02 類別
- MDM_Policy_Config01_InternetExplorer02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_InternetExplorer02
- MDM_Policy_Config01_InternetExplorer02.InstanceID
- MDM_Policy_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a448b0034e3f4658f1c13b238abf455bf413a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465241"
---
# <a name="mdm_policy_config01_internetexplorer02-class"></a><span data-ttu-id="76e50-105">MDM \_ 原則 \_ Config01 \_ InternetExplorer02 類別</span><span class="sxs-lookup"><span data-stu-id="76e50-105">MDM\_Policy\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="76e50-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="76e50-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="76e50-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="76e50-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="76e50-108">MDM \_ Policy \_ Config01 InternetExplorer02 類別會設定 \_ Internet Explorer 原則。</span><span class="sxs-lookup"><span data-stu-id="76e50-108">The MDM\_Policy\_Config01\_InternetExplorer02 class configures the Internet Explorer policies.</span></span>

<span data-ttu-id="76e50-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="76e50-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76e50-110">語法</span><span class="sxs-lookup"><span data-stu-id="76e50-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowFallbackToSSL3;
  string AllowInternetExplorer7PolicyList;
  string AllowInternetExplorerStandardsMode;
  string AllowInternetZoneTemplate;
  string AllowIntranetZoneTemplate;
  string AllowLocalMachineZoneTemplate;
  string AllowLockedDownInternetZoneTemplate;
  string AllowLockedDownIntranetZoneTemplate;
  string AllowLockedDownLocalMachineZoneTemplate;
  string AllowLockedDownRestrictedSitesZoneTemplate;
  string AllowOneWordEntry;
  string AllowSiteToZoneAssignmentList;
  string AllowsLockedDownTrustedSitesZoneTemplate;
  string AllowSoftwareWhenSignatureIsInvalid;
  string AllowsRestrictedSitesZoneTemplate;
  string AllowSuggestedSites;
  string AllowTrustedSitesZoneTemplate;
  string ConsistentMimeHandlingInternetExplorerProcesses;
  string CheckSignaturesOnDownloadedPrograms;
  string CheckServerCertificateRevocation;
  string DisableAdobeFlash;
  string DisableBlockingOfOutdatedActiveXControls;
  string DisableBypassOfSmartScreenWarnings;
  string DisableBypassOfSmartScreenWarningsAboutUncommonFiles;
  string DisableCrashDetection;
  string DisableConfiguringHistory;
  string DisableCustomerExperienceImprovementProgramParticipation;
  string DisableDeletingUserVisitedWebsites;
  string DisableEnclosureDownloading;
  string DisableEncryptionSupport;
  string DisableFirstRunWizard;
  string DisableFlipAheadFeature;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DisableSecuritySettingsCheck;
  string DisableUpdateCheck;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DoNotAllowUsersToAddSites;
  string DoNotAllowUsersToChangePolicies;
  string DoNotBlockOutdatedActiveXControls;
  string DoNotBlockOutdatedActiveXControlsOnSpecificDomains;
  string IncludeAllLocalSites;
  string IncludeAllNetworkPaths;
  string InternetZoneAllowAccessToDataSources;
  string InternetZoneAllowAutomaticPromptingForActiveXControls;
  string InternetZoneAllowAutomaticPromptingForFileDownloads;
  string InternetZoneAllowDragAndDropCopyAndPasteFiles;
  string InternetZoneAllowCopyPasteViaScript;
  string InternetZoneAllowFontDownloads;
  string InternetZoneAllowLessPrivilegedSites;
  string InternetZoneAllowLoadingOfXAMLFiles;
  string InternetZoneAllowNETFrameworkReliantComponents;
  string InternetZoneAllowScriptInitiatedWindows;
  string InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string InternetZoneAllowScriptlets;
  string InternetZoneAllowSmartScreenIE;
  string InternetZoneAllowUpdatesToStatusBarViaScript;
  string InternetZoneAllowUserDataPersistence;
  string InternetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string InternetZoneIncludeLocalPathWhenUploadingFilesToServer;
  string InternetZoneEnableProtectedMode;
  string InternetZoneEnableMIMESniffing;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string InternetZoneEnableCrossSiteScriptingFilter;
  string InternetZoneDownloadUnsignedActiveXControls;
  string InternetZoneDownloadSignedActiveXControls;
  string InternetZoneInitializeAndScriptActiveXControls;
  string InternetZoneJavaPermissions;
  string InternetZoneLogonOptions;
  string InternetZoneLaunchingApplicationsAndFilesInIFRAME;
  string InternetZoneNavigateWindowsAndFrames;
  string InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone;
  string InternetZoneUsePopupBlocker;
  string InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode;
  string IntranetZoneAllowAccessToDataSources;
  string IntranetZoneAllowAutomaticPromptingForActiveXControls;
  string IntranetZoneAllowAutomaticPromptingForFileDownloads;
  string IntranetZoneAllowFontDownloads;
  string IntranetZoneAllowLessPrivilegedSites;
  string IntranetZoneAllowNETFrameworkReliantComponents;
  string IntranetZoneAllowScriptlets;
  string IntranetZoneAllowSmartScreenIE;
  string IntranetZoneAllowUserDataPersistence;
  string IntranetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string IntranetZoneInitializeAndScriptActiveXControls;
  string IntranetZoneJavaPermissions;
  string IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string IntranetZoneNavigateWindowsAndFrames;
  string LocalMachineZoneAllowAccessToDataSources;
  string LocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LocalMachineZoneAllowFontDownloads;
  string LocalMachineZoneAllowLessPrivilegedSites;
  string LocalMachineZoneAllowNETFrameworkReliantComponents;
  string LocalMachineZoneAllowScriptlets;
  string LocalMachineZoneAllowSmartScreenIE;
  string LocalMachineZoneAllowUserDataPersistence;
  string LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls;
  string LocalMachineZoneInitializeAndScriptActiveXControls;
  string LocalMachineZoneJavaPermissions;
  string LocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownInternetZoneAllowAccessToDataSources;
  string LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownInternetZoneAllowFontDownloads;
  string LockedDownInternetZoneAllowLessPrivilegedSites;
  string LockedDownInternetZoneAllowNETFrameworkReliantComponents;
  string LockedDownInternetZoneAllowScriptlets;
  string LockedDownInternetZoneAllowSmartScreenIE;
  string LockedDownInternetZoneAllowUserDataPersistence;
  string LockedDownInternetZoneInitializeAndScriptActiveXControls;
  string LockedDownInternetZoneJavaPermissions;
  string LockedDownInternetZoneNavigateWindowsAndFrames;
  string LockedDownIntranetZoneAllowAccessToDataSources;
  string LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownIntranetZoneAllowFontDownloads;
  string LockedDownIntranetZoneAllowLessPrivilegedSites;
  string LockedDownIntranetZoneAllowNETFrameworkReliantComponents;
  string LockedDownIntranetZoneAllowScriptlets;
  string LockedDownIntranetZoneAllowSmartScreenIE;
  string LockedDownIntranetZoneAllowUserDataPersistence;
  string LockedDownIntranetZoneInitializeAndScriptActiveXControls;
  string LockedDownIntranetZoneNavigateWindowsAndFrames;
  string LockedDownLocalMachineZoneAllowAccessToDataSources;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownLocalMachineZoneAllowFontDownloads;
  string LockedDownLocalMachineZoneAllowLessPrivilegedSites;
  string LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents;
  string LockedDownLocalMachineZoneAllowScriptlets;
  string LockedDownLocalMachineZoneAllowSmartScreenIE;
  string LockedDownLocalMachineZoneAllowUserDataPersistence;
  string LockedDownLocalMachineZoneInitializeAndScriptActiveXControls;
  string LockedDownLocalMachineZoneJavaPermissions;
  string LockedDownLocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownRestrictedSitesZoneAllowAccessToDataSources;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownRestrictedSitesZoneAllowFontDownloads;
  string LockedDownRestrictedSitesZoneAllowLessPrivilegedSites;
  string LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownRestrictedSitesZoneAllowScriptlets;
  string LockedDownRestrictedSitesZoneAllowSmartScreenIE;
  string LockedDownRestrictedSitesZoneAllowUserDataPersistence;
  string LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownRestrictedSitesZoneJavaPermissions;
  string LockedDownRestrictedSitesZoneNavigateWindowsAndFrames;
  string LockedDownTrustedSitesZoneAllowAccessToDataSources;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownTrustedSitesZoneAllowFontDownloads;
  string LockedDownTrustedSitesZoneAllowLessPrivilegedSites;
  string LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownTrustedSitesZoneAllowScriptlets;
  string LockedDownTrustedSitesZoneAllowSmartScreenIE;
  string LockedDownTrustedSitesZoneAllowUserDataPersistence;
  string LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownTrustedSitesZoneJavaPermissions;
  string LockedDownTrustedSitesZoneNavigateWindowsAndFrames;
  string RestrictActiveXInstallInternetExplorerProcesses;
  string RemoveRunThisTimeButtonForOutdatedActiveXControls;
  string ProtectionFromZoneElevationInternetExplorerProcesses;
  string PreventPerUserInstallationOfActiveXControls;
  string PreventManagingSmartScreenFilter;
  string NotificationBarInternetExplorerProcesses;
  string MKProtocolSecurityRestrictionInternetExplorerProcesses;
  string MimeSniffingSafetyFeatureInternetExplorerProcesses;
  string RestrictedSitesZoneAllowAccessToDataSources;
  string RestrictedSitesZoneAllowActiveScripting;
  string RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string RestrictedSitesZoneAllowFileDownloads;
  string RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles;
  string RestrictedSitesZoneAllowCopyPasteViaScript;
  string RestrictedSitesZoneAllowBinaryAndScriptBehaviors;
  string RestrictedSitesZoneAllowFontDownloads;
  string RestrictedSitesZoneAllowLessPrivilegedSites;
  string RestrictedSitesZoneAllowMETAREFRESH;
  string RestrictedSitesZoneAllowLoadingOfXAMLFiles;
  string RestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string RestrictedSitesZoneAllowScriptInitiatedWindows;
  string RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string RestrictedSitesZoneAllowScriptlets;
  string RestrictedSitesZoneAllowSmartScreenIE;
  string RestrictedSitesZoneAllowUpdatesToStatusBarViaScript;
  string RestrictedSitesZoneAllowUserDataPersistence;
  string RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer;
  string RestrictedSitesZoneEnableMIMESniffing;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string RestrictedSitesZoneDownloadUnsignedActiveXControls;
  string RestrictedSitesZoneEnableCrossSiteScriptingFilter;
  string RestrictedSitesZoneDownloadSignedActiveXControls;
  string RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string RestrictedSitesZoneInitializeAndScriptActiveXControls;
  string RestrictedSitesZoneLogonOptions;
  string RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME;
  string RestrictedSitesZoneJavaPermissions;
  string RestrictedSitesZoneNavigateWindowsAndFrames;
  string ScriptedWindowSecurityRestrictionsInternetExplorerProcesses;
  string RestrictFileDownloadInternetExplorerProcesses;
  string RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting;
  string RestrictedSitesZoneUsePopupBlocker;
  string RestrictedSitesZoneTurnOnProtectedMode;
  string RestrictedSitesZoneTurnOnCrossSiteScriptingFilter;
  string RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string RestrictedSitesZoneScriptingOfJavaApplets;
  string RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string RestrictedSitesZoneRunActiveXControlsAndPlugins;
  string RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains;
  string SearchProviderList;
  string SpecifyUseOfActiveXInstallerService;
  string SecurityZonesUseOnlyMachineSettings;
  string TrustedSitesZoneAllowAccessToDataSources;
  string TrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string TrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string TrustedSitesZoneAllowFontDownloads;
  string TrustedSitesZoneAllowLessPrivilegedSites;
  string TrustedSitesZoneAllowNETFrameworkReliantComponents;
  string TrustedSitesZoneAllowScriptlets;
  string TrustedSitesZoneAllowSmartScreenIE;
  string TrustedSitesZoneAllowUserDataPersistence;
  string TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls;
  string TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe;
  string TrustedSitesZoneJavaPermissions;
  string TrustedSitesZoneNavigateWindowsAndFrames;
};
```

## <a name="members"></a><span data-ttu-id="76e50-111">成員</span><span class="sxs-lookup"><span data-stu-id="76e50-111">Members</span></span>

<span data-ttu-id="76e50-112">**MDM \_ Policy \_ Config01 \_ InternetExplorer02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="76e50-112">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="76e50-113">屬性</span><span class="sxs-lookup"><span data-stu-id="76e50-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76e50-114">屬性</span><span class="sxs-lookup"><span data-stu-id="76e50-114">Properties</span></span>

<span data-ttu-id="76e50-115">**MDM \_ Policy \_ Config01 \_ InternetExplorer02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="76e50-115">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="76e50-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="76e50-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="76e50-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="76e50-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="76e50-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="76e50-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="76e50-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="76e50-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="76e50-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="76e50-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="76e50-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="76e50-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="76e50-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="76e50-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="76e50-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="76e50-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="76e50-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="76e50-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-196">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="76e50-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="76e50-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="76e50-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="76e50-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="76e50-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="76e50-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="76e50-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="76e50-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="76e50-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="76e50-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="76e50-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="76e50-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="76e50-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="76e50-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-241">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="76e50-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="76e50-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="76e50-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="76e50-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="76e50-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="76e50-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-259">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="76e50-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="76e50-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="76e50-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-271">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="76e50-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-274">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="76e50-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-277">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="76e50-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-280">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="76e50-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="76e50-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76e50-284">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="76e50-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-287">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-290">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-293">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="76e50-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-296">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="76e50-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-299">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-302">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-305">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="76e50-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-308">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-311">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-314">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="76e50-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-317">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="76e50-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-320">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="76e50-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-323">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-326">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-329">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="76e50-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-332">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-335">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-338">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-341">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-344">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="76e50-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-347">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="76e50-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-350">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="76e50-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-353">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="76e50-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-356">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="76e50-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-359">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="76e50-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-362">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-365">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-366">InternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-368">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="76e50-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-370">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-371">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="76e50-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-374">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-377">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="76e50-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-380">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="76e50-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-383">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="76e50-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-386">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="76e50-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-389">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="76e50-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-392">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-395">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-398">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-401">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-404">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-407">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-409">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-410">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-413">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-416">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-419">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-422">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-425">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="76e50-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-428">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-429">IntranetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-431">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-434">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-437">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-440">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-443">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-446">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-449">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-451">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-452">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-454">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-455">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-457">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-458">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-460">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-461">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-464">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-466">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-467">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-468">LocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-470">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-472">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-473">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-476">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-478">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-479">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-482">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-484">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-485">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-488">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-490">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-491">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-493">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-494">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-496">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-497">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-499">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-500">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-502">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-503">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-504">LockedDownInternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-505">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-506">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-508">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-509">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-512">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-514">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-515">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-517">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-518">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-521">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-524">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-526">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-527">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-529">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-530">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-532">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-533">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-536">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-538">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-539">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-541">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-542">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-544">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-545">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-547">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-548">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-550">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-551">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-553">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-554">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-556">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-557">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-559">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-560">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-562">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-563">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-565">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-566">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-568">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-569">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-571">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-572">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-573">LockedDownLocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-574">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-575">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-577">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-578">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-580">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-581">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-583">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-584">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-586">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-587">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-590">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-592">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-593">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-595">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-596">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-598">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-599">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-601">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-602">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-604">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-605">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-607">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-608">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-609">LockedDownRestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-610">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-611">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-613">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-614">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-616">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-617">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-619">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-620">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-622">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-623">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-625">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-626">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-628">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-629">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-631">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-632">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-634">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-635">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-637">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-638">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-640">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-641">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-643">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-644">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-645">LockedDownTrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-646">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-647">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-649">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-650">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="76e50-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-652">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-653">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="76e50-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-655">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-656">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="76e50-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-658">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-659">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="76e50-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-661">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-662">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="76e50-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76e50-663">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="76e50-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="76e50-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-665">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-666">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-668">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-669">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="76e50-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-671">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-672">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-674">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-675">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="76e50-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-677">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-678">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-680">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-681">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="76e50-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-683">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-684">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-686">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-687">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-689">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-690">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="76e50-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-692">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-693">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="76e50-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-695">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-696">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="76e50-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-698">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-699">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-701">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-702">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-704">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-705">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-707">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-708">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="76e50-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-710">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-711">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="76e50-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-713">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-714">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-716">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-717">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-719">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-720">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="76e50-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-722">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-723">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="76e50-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-725">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-726">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="76e50-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-728">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-729">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-731">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-732">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-734">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-735">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="76e50-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-737">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-738">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-740">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-741">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-743">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-744">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-746">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-747">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-749">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-750">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="76e50-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-752">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-753">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="76e50-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-755">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-756">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="76e50-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-758">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-759">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="76e50-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-761">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-762">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="76e50-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-764">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-765">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-767">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-768">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-769">RestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-770">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-771">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="76e50-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-773">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-774">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="76e50-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-776">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-777">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-779">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-780">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="76e50-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-782">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-783">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="76e50-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-785">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-786">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="76e50-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-788">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-789">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="76e50-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-791">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-792">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-793">RestrictedSitesZoneScriptingOfJAVAApplets</span><span class="sxs-lookup"><span data-stu-id="76e50-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-794">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-795">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="76e50-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-797">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-798">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="76e50-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-800">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-801">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="76e50-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-803">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-804">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="76e50-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-806">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-807">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="76e50-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-809">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-810">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="76e50-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-812">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-813">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="76e50-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-815">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-816">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="76e50-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-818">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-819">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="76e50-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-821">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-822">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="76e50-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-824">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-825">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-827">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-828">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-830">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-831">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="76e50-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-833">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-834">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="76e50-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-836">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-837">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="76e50-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-839">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-840">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="76e50-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-842">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-843">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="76e50-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-845">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-846">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="76e50-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-848">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-849">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-851">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-852">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-854">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-855">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="76e50-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-857">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-858">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="76e50-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-860">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-861">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e50-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="76e50-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-863">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-864">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-865">TrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="76e50-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-866">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-867">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e50-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="76e50-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e50-869">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76e50-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e50-870">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76e50-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76e50-871">規格需求</span><span class="sxs-lookup"><span data-stu-id="76e50-871">Requirements</span></span>



| <span data-ttu-id="76e50-872">需求</span><span class="sxs-lookup"><span data-stu-id="76e50-872">Requirement</span></span> | <span data-ttu-id="76e50-873">值</span><span class="sxs-lookup"><span data-stu-id="76e50-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76e50-874">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76e50-874">Minimum supported client</span></span><br/> | <span data-ttu-id="76e50-875">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76e50-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76e50-876">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76e50-876">Minimum supported server</span></span><br/> | <span data-ttu-id="76e50-877">都不支援</span><span class="sxs-lookup"><span data-stu-id="76e50-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="76e50-878">命名空間</span><span class="sxs-lookup"><span data-stu-id="76e50-878">Namespace</span></span><br/>                | <span data-ttu-id="76e50-879">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="76e50-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="76e50-880">MOF</span><span class="sxs-lookup"><span data-stu-id="76e50-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76e50-881"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="76e50-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="76e50-882">DLL</span><span class="sxs-lookup"><span data-stu-id="76e50-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76e50-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76e50-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

