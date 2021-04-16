---
title: MDM_Policy_User_Result01_InternetExplorer02 類別
description: MDM \_ Policy \_ User \_ Result01 \_ InternetExplorer02 類別代表可用 Internet Explorer 原則。
ms.assetid: efd999aa-4aa8-486d-82d4-20af7e2005fe
keywords:
- MDM_Policy_User_Result01_InternetExplorer02 類別
- MDM_Policy_User_Result01_InternetExplorer02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02.InstanceID
- MDM_Policy_User_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8693720c7a973cc6bc689abbf76a4674f185e23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464369"
---
# <a name="mdm_policy_user_result01_internetexplorer02-class"></a><span data-ttu-id="1472b-105">MDM \_ 原則 \_ 使用者 \_ Result01 \_ InternetExplorer02 類別</span><span class="sxs-lookup"><span data-stu-id="1472b-105">MDM\_Policy\_User\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="1472b-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="1472b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1472b-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="1472b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1472b-108">MDM \_ Policy \_ User \_ Result01 \_ InternetExplorer02 類別代表可用 Internet Explorer 原則。</span><span class="sxs-lookup"><span data-stu-id="1472b-108">The MDM\_Policy\_User\_Result01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="1472b-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1472b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1472b-110">語法</span><span class="sxs-lookup"><span data-stu-id="1472b-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="1472b-111">成員</span><span class="sxs-lookup"><span data-stu-id="1472b-111">Members</span></span>

<span data-ttu-id="1472b-112">**MDM \_ Policy \_ User \_ Result01 \_ InternetExplorer02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1472b-112">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="1472b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1472b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1472b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1472b-114">Properties</span></span>

<span data-ttu-id="1472b-115">**MDM \_ Policy \_ User \_ Result01 \_ InternetExplorer02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1472b-115">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1472b-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="1472b-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="1472b-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="1472b-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="1472b-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="1472b-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="1472b-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="1472b-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="1472b-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="1472b-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="1472b-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="1472b-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="1472b-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="1472b-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="1472b-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="1472b-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="1472b-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="1472b-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-196">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="1472b-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="1472b-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="1472b-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="1472b-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="1472b-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="1472b-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="1472b-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="1472b-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="1472b-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="1472b-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="1472b-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="1472b-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="1472b-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="1472b-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-241">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="1472b-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="1472b-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="1472b-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="1472b-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="1472b-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="1472b-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-259">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="1472b-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="1472b-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="1472b-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-271">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="1472b-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-274">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1472b-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1472b-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1472b-278">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1472b-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-280">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-281">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-283">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-284">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-287">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="1472b-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-290">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="1472b-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-293">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-296">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-299">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="1472b-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-302">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-305">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-308">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="1472b-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-311">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="1472b-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-314">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="1472b-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-317">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-320">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-323">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="1472b-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-326">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-329">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-332">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-335">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-338">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="1472b-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-341">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="1472b-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-344">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="1472b-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-347">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="1472b-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-350">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="1472b-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-353">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="1472b-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-356">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-359">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-360">InternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-362">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="1472b-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-365">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="1472b-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-368">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-370">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-371">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="1472b-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-374">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="1472b-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-377">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="1472b-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-380">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="1472b-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-383">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="1472b-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-386">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-389">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-392">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-395">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-398">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-401">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-404">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-407">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-409">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-410">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-413">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-416">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-419">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="1472b-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-422">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-423">IntranetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-425">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-428">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-431">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-434">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-437">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-440">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-443">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-446">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-449">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-451">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-452">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-454">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-455">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-457">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-458">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-460">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-461">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-462">LocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-464">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-466">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-467">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-470">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-472">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-473">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-476">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-478">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-479">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-482">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-484">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-485">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-488">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-490">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-491">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-493">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-494">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-496">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-497">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-498">LockedDownInternetZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-499">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-500">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-502">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-503">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-505">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-506">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-508">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-509">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-512">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-514">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-515">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-517">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-518">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-521">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-524">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-526">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-527">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-529">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-530">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-532">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-533">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-536">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-538">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-539">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-541">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-542">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-544">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-545">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-547">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-548">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-550">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-551">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-553">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-554">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-556">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-557">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-559">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-560">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-562">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-563">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-565">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-566">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-567">LockedDownLocalMachineZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-568">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-569">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-571">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-572">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-574">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-575">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-577">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-578">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-580">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-581">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-583">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-584">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-586">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-587">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-590">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-592">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-593">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-595">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-596">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-598">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-599">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-601">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-602">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-603">LockedDownRestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-604">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-605">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-607">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-608">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-610">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-611">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-613">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-614">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-616">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-617">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-619">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-620">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-622">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-623">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-625">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-626">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-628">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-629">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-631">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-632">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-634">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-635">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-637">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-638">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-639">LockedDownTrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-640">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-641">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-643">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-644">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="1472b-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-646">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-647">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="1472b-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-649">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-650">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="1472b-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-652">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-653">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1472b-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-655">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-656">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1472b-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1472b-657">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1472b-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="1472b-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-659">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-660">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-662">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-663">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="1472b-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-665">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-666">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-668">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-669">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="1472b-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-671">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-672">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-674">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-675">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="1472b-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-677">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-678">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-680">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-681">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-683">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-684">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="1472b-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-686">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-687">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="1472b-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-689">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-690">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="1472b-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-692">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-693">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-695">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-696">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-698">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-699">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-701">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-702">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="1472b-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-704">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-705">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="1472b-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-707">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-708">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-710">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-711">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-713">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-714">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="1472b-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-716">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-717">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="1472b-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-719">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-720">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="1472b-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-722">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-723">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-725">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-726">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-728">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-729">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="1472b-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-731">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-732">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-734">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-735">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-737">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-738">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-740">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-741">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-743">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-744">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="1472b-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-746">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-747">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="1472b-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-749">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-750">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="1472b-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-752">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-753">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="1472b-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-755">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-756">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="1472b-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-758">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-759">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-761">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-762">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-763">RestrictedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-764">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-765">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="1472b-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-767">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-768">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="1472b-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-770">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-771">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-773">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-774">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="1472b-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-776">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-777">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="1472b-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-779">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-780">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="1472b-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-782">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-783">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="1472b-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-785">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-786">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-787">RestrictedSitesZoneScriptingOfJAVAApplets</span><span class="sxs-lookup"><span data-stu-id="1472b-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-788">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-789">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="1472b-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-791">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-792">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="1472b-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-794">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-795">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="1472b-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-797">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-798">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="1472b-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-800">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-801">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="1472b-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-803">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-804">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="1472b-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-806">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-807">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="1472b-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-809">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-810">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="1472b-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-812">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-813">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="1472b-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-815">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-816">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-818">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-819">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-821">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-822">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="1472b-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-824">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-825">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="1472b-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-827">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-828">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="1472b-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-830">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-831">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="1472b-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-833">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-834">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="1472b-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-836">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-837">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="1472b-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-839">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-840">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-842">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-843">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-845">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-846">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="1472b-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-848">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-849">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="1472b-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-851">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-852">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1472b-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="1472b-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-854">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-855">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-856">TrustedSitesZoneJAVAPermissions</span><span class="sxs-lookup"><span data-stu-id="1472b-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-857">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-858">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1472b-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="1472b-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-860">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1472b-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1472b-861">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1472b-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1472b-862">規格需求</span><span class="sxs-lookup"><span data-stu-id="1472b-862">Requirements</span></span>



| <span data-ttu-id="1472b-863">需求</span><span class="sxs-lookup"><span data-stu-id="1472b-863">Requirement</span></span> | <span data-ttu-id="1472b-864">值</span><span class="sxs-lookup"><span data-stu-id="1472b-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1472b-865">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1472b-865">Minimum supported client</span></span><br/> | <span data-ttu-id="1472b-866">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1472b-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1472b-867">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1472b-867">Minimum supported server</span></span><br/> | <span data-ttu-id="1472b-868">都不支援</span><span class="sxs-lookup"><span data-stu-id="1472b-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1472b-869">命名空間</span><span class="sxs-lookup"><span data-stu-id="1472b-869">Namespace</span></span><br/>                | <span data-ttu-id="1472b-870">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1472b-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1472b-871">MOF</span><span class="sxs-lookup"><span data-stu-id="1472b-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1472b-872"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="1472b-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1472b-873">DLL</span><span class="sxs-lookup"><span data-stu-id="1472b-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1472b-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1472b-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

