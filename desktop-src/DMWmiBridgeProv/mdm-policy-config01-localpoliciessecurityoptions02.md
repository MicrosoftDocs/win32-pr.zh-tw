---
title: MDM_Policy_Config01_LocalPoliciesSecurityOptions02 類別
description: '[MDM \_ 原則 \_ Config01 LocalPoliciesSecurityOptions02] 會設定 \_ 本機原則安全性選項。'
ms.assetid: 07688109-f14a-4a04-91b2-ee928d8911b4
keywords:
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02 類別
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf39e1db2f5d6f823667865054a8c72b18dc916f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025074"
---
# <a name="mdm_policy_config01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="b34af-105">MDM \_ 原則 \_ Config01 \_ LocalPoliciesSecurityOptions02 類別</span><span class="sxs-lookup"><span data-stu-id="b34af-105">MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="b34af-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b34af-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b34af-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b34af-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b34af-108">[MDM \_ 原則 \_ Config01 LocalPoliciesSecurityOptions02] 會設定 \_ 本機原則安全性選項。</span><span class="sxs-lookup"><span data-stu-id="b34af-108">The MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02 configures the local policies security options.</span></span>

<span data-ttu-id="b34af-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b34af-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34af-110">語法</span><span class="sxs-lookup"><span data-stu-id="b34af-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LocalPoliciesSecurityOptions02
{
  string InstanceID;
  string ParentID;
  sint32 Accounts_BlockMicrosoftAccounts;
  sint32 Accounts_EnableGuestAccountStatus;
  sint32 Accounts_EnableAdministratorAccountStatus;
  sint32 Accounts_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly;
  string Accounts_RenameAdministratorAccount;
  string Accounts_RenameGuestAccount;
  string Devices_RestrictCDROMAccessToLocallyLoggedOnUserOnly;
  sint32 Devices_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters;
  sint32 Devices_AllowUndockWithoutHavingToLogon;
  string Devices_AllowedToFormatAndEjectRemovableMedia;
  sint32 InteractiveLogon_DisplayUserInformationWhenTheSessionIsLocked;
  sint32 Interactivelogon_DoNotDisplayLastSignedIn;
  sint32 Interactivelogon_DoNotDisplayUsernameAtSignIn;
  sint32 Interactivelogon_DoNotRequireCTRLALTDEL;
  sint32 InteractiveLogon_MachineInactivityLimit;
  string InteractiveLogon_MessageTextForUsersAttemptingToLogOn;
  string InteractiveLogon_MessageTitleForUsersAttemptingToLogOn;
  sint32 NetworkAccess_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares;
  sint32 NetworkAccess_RestrictAnonymousAccessToNamedPipesAndShares;
  string NetworkAccess_RestrictClientsAllowedToMakeRemoteCallsToSAM;
  sint32 NetworkSecurity_AllowPKU2UAuthenticationRequests;
  sint32 RecoveryConsole_AllowAutomaticAdministrativeLogon;
  sint32 Shutdown_AllowSystemToBeShutDownWithoutHavingToLogOn;
  sint32 Shutdown_ClearVirtualMemoryPageFile;
  sint32 UserAccountControl_AllowUIAccessApplicationsToPromptForElevation;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForAdministrators;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForStandardUsers;
  sint32 UserAccountControl_DetectApplicationInstallationsAndPromptForElevation;
  sint32 UserAccountControl_OnlyElevateExecutableFilesThatAreSignedAndValidated;
  sint32 UserAccountControl_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations;
  sint32 UserAccountControl_RunAllAdministratorsInAdminApprovalMode;
  sint32 UserAccountControl_SwitchToTheSecureDesktopWhenPromptingForElevation;
  sint32 UserAccountControl_UseAdminApprovalMode;
  sint32 UserAccountControl_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations;
};
```

## <a name="members"></a><span data-ttu-id="b34af-111">成員</span><span class="sxs-lookup"><span data-stu-id="b34af-111">Members</span></span>

<span data-ttu-id="b34af-112">**MDM \_ Policy \_ Config01 \_ LocalPoliciesSecurityOptions02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b34af-112">The **MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="b34af-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b34af-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b34af-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b34af-114">Properties</span></span>

<span data-ttu-id="b34af-115">**MDM \_ Policy \_ Config01 \_ LocalPoliciesSecurityOptions02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b34af-115">The **MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b34af-116">帳戶 \_ BlockMicrosoftAccounts</span><span class="sxs-lookup"><span data-stu-id="b34af-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b34af-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="b34af-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b34af-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="b34af-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-125">帳戶 \_ LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span><span class="sxs-lookup"><span data-stu-id="b34af-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-128">帳戶 \_ RenameAdministratorAccount</span><span class="sxs-lookup"><span data-stu-id="b34af-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-131">帳戶 \_ RenameGuestAccount</span><span class="sxs-lookup"><span data-stu-id="b34af-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-134">裝置 \_ AllowedToFormatAndEjectRemovableMedia</span><span class="sxs-lookup"><span data-stu-id="b34af-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-137">裝置 \_ AllowUndockWithoutHavingToLogon</span><span class="sxs-lookup"><span data-stu-id="b34af-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-140">裝置 \_ PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span><span class="sxs-lookup"><span data-stu-id="b34af-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-143">裝置 \_ RestrictCDROMAccessToLocallyLoggedOnUserOnly</span><span class="sxs-lookup"><span data-stu-id="b34af-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b34af-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b34af-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b34af-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34af-149">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b34af-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-150">InteractiveLogon \_ >displayuserinformationwhenthesessionislocked</span><span class="sxs-lookup"><span data-stu-id="b34af-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-151">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-153">Interactivelogon \_ DoNotDisplayLastSignedIn</span><span class="sxs-lookup"><span data-stu-id="b34af-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-154">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-156">Interactivelogon \_ DoNotDisplayUsernameAtSignIn</span><span class="sxs-lookup"><span data-stu-id="b34af-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-157">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-159">Interactivelogon \_ DoNotRequireCTRLALTDEL</span><span class="sxs-lookup"><span data-stu-id="b34af-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-160">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-161">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-162">InteractiveLogon \_ >machineinactivitylimit</span><span class="sxs-lookup"><span data-stu-id="b34af-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-163">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-164">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-165">InteractiveLogon \_ MessageTextForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="b34af-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-167">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-168">InteractiveLogon \_ MessageTitleForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="b34af-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-171">NetworkAccess \_ DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span><span class="sxs-lookup"><span data-stu-id="b34af-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-172">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-174">NetworkAccess \_ RestrictAnonymousAccessToNamedPipesAndShares</span><span class="sxs-lookup"><span data-stu-id="b34af-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-175">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-176">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-177">NetworkAccess \_ >restrictclientsallowedtomakeremotecallstosam</span><span class="sxs-lookup"><span data-stu-id="b34af-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-179">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-180">NetworkSecurity \_ AllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="b34af-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-181">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-182">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b34af-183">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b34af-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b34af-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b34af-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34af-186">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b34af-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-187">RecoveryConsole \_ AllowAutomaticAdministrativeLogon</span><span class="sxs-lookup"><span data-stu-id="b34af-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-188">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-189">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-190">關機 \_ AllowSystemToBeShutDownWithoutHavingToLogOn</span><span class="sxs-lookup"><span data-stu-id="b34af-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-191">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-193">關機 \_ ClearVirtualMemoryPageFile</span><span class="sxs-lookup"><span data-stu-id="b34af-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-194">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-195">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-196">UserAccountControl \_ AllowUIAccessApplicationsToPromptForElevation</span><span class="sxs-lookup"><span data-stu-id="b34af-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-197">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-198">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-199">UserAccountControl \_ BehaviorOfTheElevationPromptForAdministrators</span><span class="sxs-lookup"><span data-stu-id="b34af-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-200">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-201">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-202">UserAccountControl \_ BehaviorOfTheElevationPromptForStandardUsers</span><span class="sxs-lookup"><span data-stu-id="b34af-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-203">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-204">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-205">UserAccountControl \_ DetectApplicationInstallationsAndPromptForElevation</span><span class="sxs-lookup"><span data-stu-id="b34af-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-206">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-207">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-208">UserAccountControl \_ OnlyElevateExecutableFilesThatAreSignedAndValidated</span><span class="sxs-lookup"><span data-stu-id="b34af-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-209">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-210">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-211">UserAccountControl \_ OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span><span class="sxs-lookup"><span data-stu-id="b34af-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-212">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-213">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-214">UserAccountControl \_ RunAllAdministratorsInAdminApprovalMode</span><span class="sxs-lookup"><span data-stu-id="b34af-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-215">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-216">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-217">UserAccountControl \_ SwitchToTheSecureDesktopWhenPromptingForElevation</span><span class="sxs-lookup"><span data-stu-id="b34af-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-218">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-219">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-220">UserAccountControl \_ UseAdminApprovalMode</span><span class="sxs-lookup"><span data-stu-id="b34af-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-221">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-222">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b34af-223">UserAccountControl \_ VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span><span class="sxs-lookup"><span data-stu-id="b34af-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34af-224">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b34af-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b34af-225">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b34af-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b34af-226">規格需求</span><span class="sxs-lookup"><span data-stu-id="b34af-226">Requirements</span></span>



| <span data-ttu-id="b34af-227">需求</span><span class="sxs-lookup"><span data-stu-id="b34af-227">Requirement</span></span> | <span data-ttu-id="b34af-228">值</span><span class="sxs-lookup"><span data-stu-id="b34af-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34af-229">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b34af-229">Minimum supported client</span></span><br/> | <span data-ttu-id="b34af-230">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b34af-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b34af-231">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b34af-231">Minimum supported server</span></span><br/> | <span data-ttu-id="b34af-232">都不支援</span><span class="sxs-lookup"><span data-stu-id="b34af-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b34af-233">命名空間</span><span class="sxs-lookup"><span data-stu-id="b34af-233">Namespace</span></span><br/>                | <span data-ttu-id="b34af-234">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b34af-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b34af-235">MOF</span><span class="sxs-lookup"><span data-stu-id="b34af-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b34af-236"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b34af-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b34af-237">DLL</span><span class="sxs-lookup"><span data-stu-id="b34af-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b34af-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b34af-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

