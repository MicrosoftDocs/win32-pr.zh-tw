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
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="18b47-105">MDM \_ 原則 \_ Result01 \_ InternetExplorer02 類別</span><span class="sxs-lookup"><span data-stu-id="18b47-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="18b47-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="18b47-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="18b47-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="18b47-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="18b47-108">[MDM \_ 原則 \_ Result01] \_ InternetExplorer02 代表 Internet Explorer 原則。</span><span class="sxs-lookup"><span data-stu-id="18b47-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="18b47-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b47-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b47-110">語法</span><span class="sxs-lookup"><span data-stu-id="18b47-110">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="18b47-111">成員</span><span class="sxs-lookup"><span data-stu-id="18b47-111">Members</span></span>

<span data-ttu-id="18b47-112">**MDM \_ Policy \_ Result01 \_ InternetExplorer02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18b47-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="18b47-113">屬性</span><span class="sxs-lookup"><span data-stu-id="18b47-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18b47-114">屬性</span><span class="sxs-lookup"><span data-stu-id="18b47-114">Properties</span></span>

<span data-ttu-id="18b47-115">**MDM \_ Policy \_ Result01 \_ InternetExplorer02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="18b47-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="18b47-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="18b47-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="18b47-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="18b47-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="18b47-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="18b47-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="18b47-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="18b47-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="18b47-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="18b47-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="18b47-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="18b47-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="18b47-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="18b47-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="18b47-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="18b47-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="18b47-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="18b47-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-196">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="18b47-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="18b47-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="18b47-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="18b47-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="18b47-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="18b47-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="18b47-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="18b47-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="18b47-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="18b47-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="18b47-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="18b47-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="18b47-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="18b47-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-241">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="18b47-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="18b47-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="18b47-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="18b47-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="18b47-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="18b47-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-259">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="18b47-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="18b47-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="18b47-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-271">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="18b47-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-274">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="18b47-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-277">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="18b47-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-280">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18b47-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b47-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18b47-284">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18b47-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-287">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-290">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-293">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="18b47-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-296">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="18b47-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-299">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-302">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-305">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="18b47-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-308">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-311">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-314">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="18b47-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-317">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="18b47-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-320">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="18b47-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-323">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-326">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-329">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="18b47-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-332">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-335">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-338">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-341">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-344">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="18b47-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-347">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="18b47-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-350">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="18b47-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-353">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="18b47-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-356">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="18b47-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-359">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="18b47-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-362">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-365">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-366">InternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-368">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="18b47-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-370">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-371">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="18b47-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-374">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-377">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="18b47-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-380">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="18b47-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-383">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="18b47-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-386">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="18b47-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-389">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="18b47-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-392">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-395">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-398">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-401">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-404">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-407">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-409">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-410">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-413">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-416">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-419">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-422">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-425">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="18b47-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-428">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-429">IntranetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-431">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-434">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-437">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-440">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-443">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-446">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-449">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-451">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-452">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-454">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-455">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-457">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-458">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-460">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-461">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-464">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-466">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-467">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-468">LocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-470">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-472">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-473">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-476">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-478">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-479">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-482">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-484">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-485">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-488">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-490">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-491">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-493">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-494">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-496">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-497">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-499">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-500">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-502">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-503">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-504">LockedDownInternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-505">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-506">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-508">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-509">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-512">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-514">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-515">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-517">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-518">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-521">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-524">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-526">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-527">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-529">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-530">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-532">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-533">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-536">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-538">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-539">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-541">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-542">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-544">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-545">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-547">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-548">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-550">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-551">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-553">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-554">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-556">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-557">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-559">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-560">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-562">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-563">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-565">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-566">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-568">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-569">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-571">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-572">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-573">LockedDownLocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-574">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-575">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-577">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-578">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-580">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-581">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-583">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-584">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-586">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-587">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-590">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-592">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-593">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-595">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-596">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-598">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-599">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-601">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-602">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-604">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-605">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-607">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-608">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-609">LockedDownRestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-610">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-611">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-613">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-614">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-616">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-617">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-619">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-620">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-622">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-623">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-625">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-626">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-628">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-629">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-631">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-632">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-634">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-635">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-637">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-638">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-640">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-641">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-643">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-644">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-645">LockedDownTrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-646">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-647">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-649">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-650">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="18b47-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-652">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-653">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="18b47-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-655">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-656">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="18b47-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-658">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-659">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="18b47-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-661">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-662">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b47-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18b47-663">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18b47-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="18b47-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-665">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-666">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-668">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-669">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="18b47-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-671">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-672">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-674">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-675">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="18b47-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-677">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-678">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-680">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-681">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="18b47-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-683">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-684">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-686">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-687">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-689">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-690">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="18b47-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-692">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-693">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="18b47-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-695">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-696">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="18b47-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-698">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-699">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-701">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-702">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-704">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-705">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-707">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-708">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="18b47-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-710">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-711">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="18b47-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-713">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-714">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-716">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-717">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-719">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-720">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="18b47-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-722">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-723">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="18b47-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-725">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-726">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="18b47-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-728">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-729">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-731">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-732">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-734">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-735">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="18b47-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-737">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-738">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-740">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-741">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-743">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-744">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-746">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-747">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-749">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-750">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="18b47-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-752">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-753">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="18b47-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-755">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-756">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="18b47-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-758">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-759">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="18b47-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-761">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-762">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="18b47-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-764">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-765">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-767">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-768">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-769">RestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-770">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-771">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="18b47-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-773">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-774">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="18b47-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-776">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-777">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-779">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-780">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="18b47-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-782">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-783">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="18b47-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-785">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-786">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="18b47-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-788">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-789">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="18b47-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-791">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-792">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-793">RestrictedSitesZoneScriptingOfJAVAApplets</span><span class="sxs-lookup"><span data-stu-id="18b47-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-794">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-795">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="18b47-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-797">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-798">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="18b47-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-800">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-801">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="18b47-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-803">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-804">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="18b47-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-806">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-807">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="18b47-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-809">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-810">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="18b47-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-812">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-813">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="18b47-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-815">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-816">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="18b47-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-818">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-819">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="18b47-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-821">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-822">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="18b47-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-824">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-825">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-827">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-828">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-830">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-831">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="18b47-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-833">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-834">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="18b47-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-836">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-837">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="18b47-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-839">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-840">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="18b47-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-842">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-843">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="18b47-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-845">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-846">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="18b47-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-848">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-849">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-851">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-852">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-854">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-855">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="18b47-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-857">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-858">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="18b47-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-860">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-861">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18b47-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="18b47-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-863">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-864">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-865">TrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="18b47-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-866">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-867">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18b47-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="18b47-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b47-869">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b47-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b47-870">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18b47-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18b47-871">規格需求</span><span class="sxs-lookup"><span data-stu-id="18b47-871">Requirements</span></span>



| <span data-ttu-id="18b47-872">需求</span><span class="sxs-lookup"><span data-stu-id="18b47-872">Requirement</span></span> | <span data-ttu-id="18b47-873">值</span><span class="sxs-lookup"><span data-stu-id="18b47-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b47-874">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18b47-874">Minimum supported client</span></span><br/> | <span data-ttu-id="18b47-875">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18b47-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18b47-876">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18b47-876">Minimum supported server</span></span><br/> | <span data-ttu-id="18b47-877">都不支援</span><span class="sxs-lookup"><span data-stu-id="18b47-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="18b47-878">命名空間</span><span class="sxs-lookup"><span data-stu-id="18b47-878">Namespace</span></span><br/>                | <span data-ttu-id="18b47-879">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="18b47-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="18b47-880">MOF</span><span class="sxs-lookup"><span data-stu-id="18b47-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18b47-881"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="18b47-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="18b47-882">DLL</span><span class="sxs-lookup"><span data-stu-id="18b47-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18b47-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18b47-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

