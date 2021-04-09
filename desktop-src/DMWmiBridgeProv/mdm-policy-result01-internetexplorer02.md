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
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="b3306-105">MDM \_ 原則 \_ Result01 \_ InternetExplorer02 類別</span><span class="sxs-lookup"><span data-stu-id="b3306-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="b3306-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b3306-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b3306-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b3306-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b3306-108">[MDM \_ 原則 \_ Result01] \_ InternetExplorer02 代表 Internet Explorer 原則。</span><span class="sxs-lookup"><span data-stu-id="b3306-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="b3306-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3306-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3306-110">語法</span><span class="sxs-lookup"><span data-stu-id="b3306-110">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b3306-111">成員</span><span class="sxs-lookup"><span data-stu-id="b3306-111">Members</span></span>

<span data-ttu-id="b3306-112">**MDM \_ Policy \_ Result01 \_ InternetExplorer02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b3306-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="b3306-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b3306-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3306-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b3306-114">Properties</span></span>

<span data-ttu-id="b3306-115">**MDM \_ Policy \_ Result01 \_ InternetExplorer02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b3306-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b3306-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="b3306-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="b3306-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="b3306-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="b3306-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="b3306-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="b3306-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="b3306-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="b3306-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="b3306-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="b3306-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="b3306-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="b3306-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="b3306-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="b3306-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="b3306-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="b3306-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="b3306-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-196">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="b3306-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="b3306-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="b3306-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="b3306-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="b3306-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="b3306-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="b3306-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="b3306-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="b3306-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="b3306-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="b3306-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="b3306-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="b3306-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="b3306-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-241">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="b3306-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="b3306-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="b3306-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="b3306-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="b3306-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="b3306-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-259">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="b3306-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="b3306-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="b3306-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-271">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="b3306-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-274">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="b3306-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-277">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="b3306-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-280">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b3306-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3306-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3306-284">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3306-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-287">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-290">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-293">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="b3306-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-296">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="b3306-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-299">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-302">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-305">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="b3306-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-308">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-311">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-314">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="b3306-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-317">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="b3306-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-320">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="b3306-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-323">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-326">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-329">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="b3306-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-332">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-335">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-338">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-341">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-344">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="b3306-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-347">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="b3306-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-350">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="b3306-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-353">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="b3306-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-356">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="b3306-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-359">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="b3306-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-362">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-365">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-366">InternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-368">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="b3306-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-370">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-371">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="b3306-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-374">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-377">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="b3306-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-380">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="b3306-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-383">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="b3306-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-386">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="b3306-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-389">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="b3306-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-392">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-395">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-398">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-401">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-404">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-407">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-409">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-410">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-413">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-416">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-419">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-422">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-425">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="b3306-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-428">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-429">IntranetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-431">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-434">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-437">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-440">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-443">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-446">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-449">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-451">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-452">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-454">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-455">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-457">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-458">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-460">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-461">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-464">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-466">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-467">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-468">LocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-470">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-472">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-473">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-476">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-478">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-479">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-482">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-484">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-485">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-488">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-490">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-491">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-493">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-494">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-496">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-497">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-499">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-500">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-502">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-503">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-504">LockedDownInternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-505">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-506">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-508">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-509">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-512">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-514">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-515">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-517">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-518">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-521">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-524">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-526">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-527">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-529">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-530">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-532">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-533">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-536">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-538">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-539">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-541">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-542">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-544">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-545">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-547">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-548">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-550">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-551">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-553">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-554">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-556">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-557">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-559">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-560">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-562">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-563">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-565">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-566">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-568">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-569">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-571">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-572">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-573">LockedDownLocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-574">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-575">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-577">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-578">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-580">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-581">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-583">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-584">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-586">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-587">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-590">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-592">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-593">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-595">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-596">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-598">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-599">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-601">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-602">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-604">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-605">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-607">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-608">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-609">LockedDownRestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-610">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-611">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-613">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-614">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-616">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-617">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-619">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-620">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-622">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-623">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-625">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-626">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-628">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-629">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-631">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-632">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-634">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-635">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-637">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-638">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-640">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-641">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-643">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-644">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-645">LockedDownTrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-646">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-647">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-649">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-650">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="b3306-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-652">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-653">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="b3306-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-655">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-656">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="b3306-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-658">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-659">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b3306-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-661">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-662">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3306-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3306-663">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3306-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="b3306-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-665">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-666">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-668">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-669">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="b3306-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-671">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-672">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-674">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-675">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="b3306-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-677">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-678">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-680">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-681">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="b3306-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-683">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-684">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-686">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-687">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-689">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-690">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="b3306-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-692">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-693">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="b3306-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-695">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-696">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="b3306-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-698">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-699">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-701">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-702">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-704">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-705">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-707">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-708">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="b3306-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-710">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-711">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="b3306-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-713">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-714">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-716">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-717">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-719">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-720">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="b3306-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-722">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-723">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="b3306-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-725">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-726">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="b3306-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-728">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-729">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-731">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-732">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-734">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-735">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="b3306-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-737">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-738">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-740">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-741">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-743">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-744">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-746">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-747">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-749">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-750">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="b3306-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-752">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-753">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="b3306-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-755">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-756">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="b3306-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-758">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-759">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="b3306-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-761">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-762">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="b3306-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-764">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-765">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-767">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-768">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-769">RestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-770">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-771">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="b3306-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-773">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-774">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="b3306-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-776">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-777">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-779">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-780">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="b3306-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-782">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-783">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="b3306-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-785">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-786">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="b3306-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-788">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-789">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="b3306-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-791">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-792">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-793">RestrictedSitesZoneScriptingOfJAVAApplets</span><span class="sxs-lookup"><span data-stu-id="b3306-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-794">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-795">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="b3306-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-797">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-798">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="b3306-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-800">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-801">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="b3306-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-803">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-804">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="b3306-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-806">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-807">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="b3306-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-809">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-810">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="b3306-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-812">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-813">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="b3306-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-815">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-816">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="b3306-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-818">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-819">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="b3306-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-821">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-822">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="b3306-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-824">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-825">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-827">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-828">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-830">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-831">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="b3306-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-833">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-834">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="b3306-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-836">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-837">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="b3306-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-839">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-840">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="b3306-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-842">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-843">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="b3306-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-845">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-846">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="b3306-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-848">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-849">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-851">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-852">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-854">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-855">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="b3306-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-857">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-858">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="b3306-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-860">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-861">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3306-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="b3306-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-863">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-864">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-865">TrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="b3306-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-866">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-867">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3306-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="b3306-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3306-869">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3306-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3306-870">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3306-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3306-871">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3306-871">Requirements</span></span>



| <span data-ttu-id="b3306-872">需求</span><span class="sxs-lookup"><span data-stu-id="b3306-872">Requirement</span></span> | <span data-ttu-id="b3306-873">值</span><span class="sxs-lookup"><span data-stu-id="b3306-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3306-874">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3306-874">Minimum supported client</span></span><br/> | <span data-ttu-id="b3306-875">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3306-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3306-876">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3306-876">Minimum supported server</span></span><br/> | <span data-ttu-id="b3306-877">都不支援</span><span class="sxs-lookup"><span data-stu-id="b3306-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b3306-878">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3306-878">Namespace</span></span><br/>                | <span data-ttu-id="b3306-879">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b3306-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b3306-880">MOF</span><span class="sxs-lookup"><span data-stu-id="b3306-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3306-881"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3306-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3306-882">DLL</span><span class="sxs-lookup"><span data-stu-id="b3306-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3306-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3306-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

