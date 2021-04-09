---
title: MDM_Policy_Result01_InternetExplorer02 類別
description: '[MDM \_ 原則 \_ Result01] \_ InternetExplorer02 代表 Internet Explorer 原則。'
ms.assetid: 4b14c9ea-2f4d-4e5a-8aab-3741f15b0b1e
keywords:
- MDM_Policy_Result01_InternetExplorer02 類別
- MDM_Policy_Result01_InternetExplorer02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02.InstanceID
- MDM_Policy_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63308b6100d6bd4ec924307a9dcd3892096fc0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934263"
---
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="0b708-105">MDM \_ 原則 \_ Result01 \_ InternetExplorer02 類別</span><span class="sxs-lookup"><span data-stu-id="0b708-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="0b708-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="0b708-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b708-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="0b708-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b708-108">[MDM \_ 原則 \_ Result01] \_ InternetExplorer02 代表 Internet Explorer 原則。</span><span class="sxs-lookup"><span data-stu-id="0b708-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="0b708-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b708-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b708-110">語法</span><span class="sxs-lookup"><span data-stu-id="0b708-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="0b708-111">成員</span><span class="sxs-lookup"><span data-stu-id="0b708-111">Members</span></span>

<span data-ttu-id="0b708-112">**MDM \_ Policy \_ Result01 \_ InternetExplorer02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0b708-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="0b708-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0b708-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b708-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0b708-114">Properties</span></span>

<span data-ttu-id="0b708-115">**MDM \_ Policy \_ Result01 \_ InternetExplorer02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0b708-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0b708-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="0b708-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="0b708-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="0b708-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="0b708-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="0b708-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0b708-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="0b708-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="0b708-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="0b708-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="0b708-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="0b708-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="0b708-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="0b708-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="0b708-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0b708-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="0b708-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="0b708-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-196">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0b708-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="0b708-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="0b708-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="0b708-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="0b708-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="0b708-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="0b708-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="0b708-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="0b708-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="0b708-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="0b708-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="0b708-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="0b708-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="0b708-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-241">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0b708-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="0b708-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="0b708-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="0b708-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="0b708-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="0b708-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-259">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0b708-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="0b708-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="0b708-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-271">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="0b708-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-274">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="0b708-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-277">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="0b708-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-280">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b708-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b708-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b708-284">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b708-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-287">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-290">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-293">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="0b708-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-296">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="0b708-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-299">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-302">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-305">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="0b708-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-308">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-311">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-314">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="0b708-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-317">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="0b708-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-320">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="0b708-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-323">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-326">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-329">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="0b708-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-332">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-335">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-338">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-341">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-344">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0b708-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-347">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="0b708-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-350">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="0b708-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-353">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="0b708-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-356">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0b708-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-359">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="0b708-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-362">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-365">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-366">InternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-368">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="0b708-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-370">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-371">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="0b708-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-374">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-377">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0b708-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-380">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0b708-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-383">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="0b708-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-386">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="0b708-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-389">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="0b708-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-392">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-395">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-398">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-401">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-404">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-407">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-409">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-410">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-413">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-416">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-419">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-422">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-425">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="0b708-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-428">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-429">IntranetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-431">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-434">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-437">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-440">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-443">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-446">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-449">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-451">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-452">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-454">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-455">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-457">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-458">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-460">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-461">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-464">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-466">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-467">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-468">LocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-470">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-472">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-473">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-476">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-478">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-479">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-482">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-484">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-485">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-488">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-490">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-491">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-493">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-494">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-496">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-497">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-499">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-500">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-502">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-503">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-504">LockedDownInternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-505">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-506">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-508">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-509">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-512">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-514">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-515">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-517">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-518">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-521">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-524">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-526">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-527">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-529">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-530">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-532">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-533">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-536">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-538">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-539">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-541">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-542">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-544">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-545">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-547">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-548">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-550">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-551">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-553">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-554">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-556">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-557">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-559">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-560">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-562">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-563">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-565">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-566">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-568">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-569">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-571">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-572">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-573">LockedDownLocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-574">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-575">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-577">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-578">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-580">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-581">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-583">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-584">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-586">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-587">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-590">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-592">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-593">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-595">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-596">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-598">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-599">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-601">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-602">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-604">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-605">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-607">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-608">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-609">LockedDownRestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-610">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-611">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-613">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-614">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-616">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-617">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-619">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-620">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-622">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-623">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-625">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-626">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-628">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-629">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-631">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-632">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-634">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-635">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-637">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-638">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-640">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-641">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-643">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-644">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-645">LockedDownTrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-646">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-647">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-649">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-650">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0b708-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-652">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-653">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0b708-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-655">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-656">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0b708-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-658">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-659">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b708-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-661">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-662">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b708-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b708-663">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b708-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="0b708-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-665">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-666">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-668">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-669">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0b708-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-671">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-672">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-674">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-675">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0b708-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-677">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-678">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-680">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-681">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="0b708-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-683">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-684">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-686">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-687">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-689">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-690">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="0b708-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-692">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-693">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="0b708-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-695">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-696">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="0b708-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-698">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-699">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-701">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-702">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-704">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-705">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-707">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-708">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="0b708-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-710">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-711">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="0b708-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-713">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-714">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-716">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-717">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-719">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-720">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="0b708-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-722">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-723">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="0b708-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-725">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-726">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="0b708-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-728">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-729">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-731">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-732">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-734">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-735">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="0b708-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-737">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-738">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-740">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-741">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-743">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-744">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-746">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-747">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-749">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-750">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0b708-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-752">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-753">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="0b708-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-755">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-756">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="0b708-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-758">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-759">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="0b708-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-761">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-762">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="0b708-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-764">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-765">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-767">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-768">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-769">RestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-770">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-771">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="0b708-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-773">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-774">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="0b708-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-776">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-777">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-779">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-780">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="0b708-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-782">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-783">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="0b708-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-785">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-786">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0b708-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-788">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-789">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="0b708-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-791">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-792">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-793">RestrictedSitesZoneScriptingOfJAVAApplets</span><span class="sxs-lookup"><span data-stu-id="0b708-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-794">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-795">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="0b708-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-797">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-798">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0b708-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-800">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-801">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0b708-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-803">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-804">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="0b708-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-806">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-807">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0b708-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-809">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-810">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0b708-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-812">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-813">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="0b708-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-815">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-816">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="0b708-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-818">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-819">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="0b708-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-821">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-822">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0b708-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-824">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-825">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-827">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-828">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-830">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-831">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0b708-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-833">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-834">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0b708-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-836">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-837">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0b708-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-839">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-840">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0b708-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-842">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-843">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0b708-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-845">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-846">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0b708-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-848">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-849">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-851">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-852">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-854">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-855">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0b708-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-857">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-858">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="0b708-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-860">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-861">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b708-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="0b708-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-863">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-864">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-865">TrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="0b708-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-866">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-867">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b708-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0b708-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b708-869">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b708-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b708-870">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0b708-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b708-871">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b708-871">Requirements</span></span>



| <span data-ttu-id="0b708-872">需求</span><span class="sxs-lookup"><span data-stu-id="0b708-872">Requirement</span></span> | <span data-ttu-id="0b708-873">值</span><span class="sxs-lookup"><span data-stu-id="0b708-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b708-874">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b708-874">Minimum supported client</span></span><br/> | <span data-ttu-id="0b708-875">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b708-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b708-876">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b708-876">Minimum supported server</span></span><br/> | <span data-ttu-id="0b708-877">都不支援</span><span class="sxs-lookup"><span data-stu-id="0b708-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b708-878">命名空間</span><span class="sxs-lookup"><span data-stu-id="0b708-878">Namespace</span></span><br/>                | <span data-ttu-id="0b708-879">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0b708-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0b708-880">MOF</span><span class="sxs-lookup"><span data-stu-id="0b708-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b708-881"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b708-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b708-882">DLL</span><span class="sxs-lookup"><span data-stu-id="0b708-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b708-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b708-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

