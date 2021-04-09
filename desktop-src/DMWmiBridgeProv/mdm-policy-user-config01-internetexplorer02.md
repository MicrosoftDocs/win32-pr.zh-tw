---
title: MDM_Policy_User_Config01_InternetExplorer02 類別
description: MDM \_ Policy \_ User \_ Config01 \_ InternetExplorer02 類別代表可用 Internet Explorer 原則。
ms.assetid: 2b155e65-5a81-4916-815f-23763759bb9a
keywords:
- MDM_Policy_User_Config01_InternetExplorer02 類別
- MDM_Policy_User_Config01_InternetExplorer02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02.InstanceID
- MDM_Policy_User_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f79c00505037508307e93120f9e2545b135678
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025144"
---
# <a name="mdm_policy_user_config01_internetexplorer02-class"></a><span data-ttu-id="ac00d-105">MDM \_ 原則 \_ 使用者 \_ Config01 \_ InternetExplorer02 類別</span><span class="sxs-lookup"><span data-stu-id="ac00d-105">MDM\_Policy\_User\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="ac00d-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ac00d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac00d-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ac00d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac00d-108">MDM \_ Policy \_ User \_ Config01 \_ InternetExplorer02 類別代表可用 Internet Explorer 原則。</span><span class="sxs-lookup"><span data-stu-id="ac00d-108">The MDM\_Policy\_User\_Config01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="ac00d-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ac00d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac00d-110">語法</span><span class="sxs-lookup"><span data-stu-id="ac00d-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowAutoComplete;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
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
  string DisableHomePageChange;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DisableSecuritySettingsCheck;
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

## <a name="members"></a><span data-ttu-id="ac00d-111">成員</span><span class="sxs-lookup"><span data-stu-id="ac00d-111">Members</span></span>

<span data-ttu-id="ac00d-112">**MDM \_ Policy \_ User \_ Config01 \_ InternetExplorer02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ac00d-112">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="ac00d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ac00d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac00d-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ac00d-114">Properties</span></span>

<span data-ttu-id="ac00d-115">**MDM \_ Policy \_ User \_ Config01 \_ InternetExplorer02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ac00d-115">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ac00d-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="ac00d-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="ac00d-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="ac00d-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="ac00d-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="ac00d-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="ac00d-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ac00d-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="ac00d-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="ac00d-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="ac00d-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="ac00d-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="ac00d-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="ac00d-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="ac00d-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ac00d-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="ac00d-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="ac00d-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-196">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ac00d-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="ac00d-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="ac00d-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="ac00d-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="ac00d-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="ac00d-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="ac00d-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="ac00d-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="ac00d-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="ac00d-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="ac00d-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="ac00d-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="ac00d-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="ac00d-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-241">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="ac00d-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ac00d-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="ac00d-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="ac00d-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="ac00d-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="ac00d-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-259">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ac00d-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="ac00d-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-271">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="ac00d-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-274">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac00d-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac00d-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-278">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac00d-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-280">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-281">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-283">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-284">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-287">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="ac00d-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-290">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="ac00d-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-293">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-296">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-299">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="ac00d-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-302">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-305">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-308">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="ac00d-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-311">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-314">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="ac00d-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-317">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-320">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-323">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="ac00d-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-326">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-329">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-332">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-335">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-338">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="ac00d-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-341">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="ac00d-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-344">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="ac00d-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-347">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="ac00d-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-350">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ac00d-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-353">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="ac00d-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-356">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-359">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-360">InternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-362">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="ac00d-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-365">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="ac00d-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-368">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-370">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-371">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="ac00d-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-374">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="ac00d-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-377">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="ac00d-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-380">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="ac00d-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-383">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="ac00d-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-386">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-389">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-392">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-395">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-398">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-401">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-404">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-407">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-409">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-410">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-413">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-416">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-419">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="ac00d-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-422">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-423">IntranetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-425">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-428">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-431">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-434">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-437">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-440">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-443">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-446">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-449">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-451">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-452">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-454">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-455">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-457">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-458">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-460">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-461">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-462">LocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-464">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-466">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-467">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-470">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-472">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-473">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-476">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-478">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-479">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-482">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-484">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-485">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-488">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-490">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-491">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-493">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-494">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-496">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-497">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-498">LockedDownInternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-499">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-500">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-502">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-503">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-505">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-506">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-508">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-509">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-512">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-514">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-515">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-517">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-518">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-521">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-524">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-526">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-527">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-529">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-530">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-532">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-533">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-536">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-538">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-539">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-541">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-542">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-544">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-545">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-547">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-548">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-550">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-551">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-553">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-554">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-556">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-557">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-559">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-560">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-562">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-563">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-565">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-566">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-567">LockedDownLocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-568">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-569">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-571">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-572">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-574">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-575">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-577">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-578">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-580">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-581">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-583">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-584">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-586">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-587">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-590">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-592">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-593">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-595">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-596">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-598">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-599">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-601">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-602">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-603">LockedDownRestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-604">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-605">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-607">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-608">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-610">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-611">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-613">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-614">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-616">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-617">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-619">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-620">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-622">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-623">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-625">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-626">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-628">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-629">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-631">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-632">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-634">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-635">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-637">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-638">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-639">LockedDownTrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-640">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-641">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-643">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-644">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ac00d-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-646">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-647">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ac00d-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-649">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-650">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ac00d-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-652">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-653">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ac00d-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-655">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-656">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac00d-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-657">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac00d-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="ac00d-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-659">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-660">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-662">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-663">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ac00d-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-665">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-666">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-668">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-669">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ac00d-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-671">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-672">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-674">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-675">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="ac00d-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-677">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-678">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-680">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-681">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-683">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-684">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="ac00d-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-686">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-687">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="ac00d-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-689">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-690">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="ac00d-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-692">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-693">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-695">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-696">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-698">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-699">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-701">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-702">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="ac00d-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-704">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-705">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="ac00d-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-707">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-708">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-710">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-711">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-713">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-714">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="ac00d-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-716">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-717">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-719">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-720">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="ac00d-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-722">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-723">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-725">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-726">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-728">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-729">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="ac00d-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-731">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-732">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-734">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-735">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-737">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-738">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-740">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-741">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-743">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-744">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="ac00d-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-746">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-747">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="ac00d-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-749">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-750">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="ac00d-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-752">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-753">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="ac00d-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-755">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-756">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="ac00d-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-758">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-759">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-761">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-762">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-763">RestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-764">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-765">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="ac00d-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-767">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-768">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="ac00d-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-770">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-771">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-773">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-774">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="ac00d-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-776">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-777">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="ac00d-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-779">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-780">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="ac00d-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-782">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-783">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="ac00d-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-785">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-786">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-787">RestrictedSitesZoneScriptingOfJAVAApplets</span><span class="sxs-lookup"><span data-stu-id="ac00d-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-788">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-789">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="ac00d-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-791">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-792">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="ac00d-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-794">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-795">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ac00d-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-797">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-798">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="ac00d-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-800">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-801">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ac00d-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-803">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-804">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ac00d-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-806">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-807">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="ac00d-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-809">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-810">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="ac00d-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-812">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-813">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ac00d-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-815">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-816">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-818">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-819">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-821">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-822">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ac00d-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-824">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-825">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ac00d-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-827">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-828">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ac00d-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-830">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-831">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ac00d-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-833">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-834">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ac00d-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-836">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-837">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ac00d-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-839">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-840">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-842">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-843">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-845">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-846">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ac00d-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-848">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-849">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="ac00d-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-851">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-852">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac00d-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="ac00d-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-854">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-855">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-856">TrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="ac00d-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-857">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-858">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac00d-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ac00d-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac00d-860">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac00d-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac00d-861">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac00d-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac00d-862">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac00d-862">Requirements</span></span>



| <span data-ttu-id="ac00d-863">需求</span><span class="sxs-lookup"><span data-stu-id="ac00d-863">Requirement</span></span> | <span data-ttu-id="ac00d-864">值</span><span class="sxs-lookup"><span data-stu-id="ac00d-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac00d-865">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac00d-865">Minimum supported client</span></span><br/> | <span data-ttu-id="ac00d-866">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac00d-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac00d-867">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac00d-867">Minimum supported server</span></span><br/> | <span data-ttu-id="ac00d-868">都不支援</span><span class="sxs-lookup"><span data-stu-id="ac00d-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ac00d-869">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac00d-869">Namespace</span></span><br/>                | <span data-ttu-id="ac00d-870">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ac00d-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ac00d-871">MOF</span><span class="sxs-lookup"><span data-stu-id="ac00d-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac00d-872"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac00d-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac00d-873">DLL</span><span class="sxs-lookup"><span data-stu-id="ac00d-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac00d-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac00d-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

