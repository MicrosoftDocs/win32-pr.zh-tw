---
description: 為了增強 Windows Management Instrumentation 的 (WMI) 共用的提供者主機進程 (wmiprvse.exe) 的安全性，已對 Windows 平臺進行變更，以服務安全識別碼 (SID) 保護提供者主機進程。
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: 用來控制提供者安全性的登錄機碼和值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997970"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a><span data-ttu-id="9091c-103">用來控制提供者安全性的登錄機碼和值</span><span class="sxs-lookup"><span data-stu-id="9091c-103">Registry Keys and Values for Controlling Provider Security</span></span>

<span data-ttu-id="9091c-104">為了增強 Windows Management Instrumentation 的 (WMI) 共用的提供者主機進程 (wmiprvse.exe) 的安全性，已對 Windows 平臺進行變更，以 [*服務安全識別碼 (SID)*](gloss-s.md)保護提供者主機進程。</span><span class="sxs-lookup"><span data-stu-id="9091c-104">To enhance the security of the Windows Management Instrumentation (WMI) shared provider host process (wmiprvse.exe), changes were made to Windows platforms that secure the provider host process with a [*service security identifier (SID)*](gloss-s.md).</span></span> <span data-ttu-id="9091c-105">這些變更引進下列 WMI 共用主機的執行模式：安全且相容。</span><span class="sxs-lookup"><span data-stu-id="9091c-105">These changes introduce the following running modes for the WMI shared host: secure and compatible.</span></span>

<span data-ttu-id="9091c-106">本主題包含下列章節：</span><span class="sxs-lookup"><span data-stu-id="9091c-106">The following sections are covered in this topic:</span></span>

-   [<span data-ttu-id="9091c-107">安全且相容的模式</span><span class="sxs-lookup"><span data-stu-id="9091c-107">Secure and Compatible Modes</span></span>](#secure-and-compatible-modes)
-   [<span data-ttu-id="9091c-108">登錄機碼和值</span><span class="sxs-lookup"><span data-stu-id="9091c-108">Registry Keys and Values</span></span>](#registry-keys-and-values)
-   [<span data-ttu-id="9091c-109">將提供者設定為在安全或相容模式中執行</span><span class="sxs-lookup"><span data-stu-id="9091c-109">Configuring a Provider to Run in Secure or Compatible Mode</span></span>](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a><span data-ttu-id="9091c-110">安全且相容的模式</span><span class="sxs-lookup"><span data-stu-id="9091c-110">Secure and Compatible Modes</span></span>

<span data-ttu-id="9091c-111">從 Windows 7 開始，已新增下列兩個 WMI 共用主機進程的執行模式：</span><span class="sxs-lookup"><span data-stu-id="9091c-111">Starting in Windows 7, the following two running modes for the WMI shared host process were added:</span></span>

<dl> <dt>

<span data-ttu-id="9091c-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>安全模式</span><span class="sxs-lookup"><span data-stu-id="9091c-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Secure mode</span></span>
</dt> <dd>

<span data-ttu-id="9091c-113">WMI 提供者主機進程資源是以 [*服務 SID*](gloss-s.md)來保護。</span><span class="sxs-lookup"><span data-stu-id="9091c-113">WMI provider host process resources are secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="9091c-114">只有 *服務 SID* 具有這些資源的許可權。</span><span class="sxs-lookup"><span data-stu-id="9091c-114">Only the *service SID* has permissions for these resources.</span></span>

</dd> <dt>

<span data-ttu-id="9091c-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>相容模式</span><span class="sxs-lookup"><span data-stu-id="9091c-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Compatible mode</span></span>
</dt> <dd>

<span data-ttu-id="9091c-116">WMI 共用提供者主機進程不會受到 [*服務 SID*](gloss-s.md)的保護。</span><span class="sxs-lookup"><span data-stu-id="9091c-116">The WMI shared provider host process is not secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="9091c-117">視裝載模型而定，提供者主機進程允許存取 NetworkService 或 LocalService 帳戶。</span><span class="sxs-lookup"><span data-stu-id="9091c-117">The provider host process allows access to the NetworkService or LocalService accounts depending on the hosting model.</span></span> <span data-ttu-id="9091c-118">如需裝載模型的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9091c-118">For more information about hosting models, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

<span data-ttu-id="9091c-119">**Windows Vista 和 Windows Server 2008：** 若要存取登錄機碼和值，以控制提供者主機進程的安全和相容模式，您必須在 [KB 959454](https://support.microsoft.com/kb/959454)中安裝安全性更新。</span><span class="sxs-lookup"><span data-stu-id="9091c-119">**Windows Vista and Windows Server 2008:** To access the registry keys and values for controlling secure and compatible modes for the provider host process, you must install the security update in [KB 959454](https://support.microsoft.com/kb/959454).</span></span> <span data-ttu-id="9091c-120">如需詳細資訊，請參閱 [Microsoft 資訊安全公告 MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx)。</span><span class="sxs-lookup"><span data-stu-id="9091c-120">For more information, see the [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span></span>

## <a name="registry-keys-and-values"></a><span data-ttu-id="9091c-121">登錄機碼和值</span><span class="sxs-lookup"><span data-stu-id="9091c-121">Registry Keys and Values</span></span>

<span data-ttu-id="9091c-122">安全且相容的模式設定是透過登錄機碼來指定。</span><span class="sxs-lookup"><span data-stu-id="9091c-122">The secure and compatible mode settings are specified through registry keys.</span></span> <span data-ttu-id="9091c-123">WMI 的登錄機碼位於 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ 的登錄中。</span><span class="sxs-lookup"><span data-stu-id="9091c-123">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<span data-ttu-id="9091c-124">下列清單中所述的下列登錄機碼和 **DWORD** 值已加入，可控制 WMI 提供者的行為。</span><span class="sxs-lookup"><span data-stu-id="9091c-124">The following registry keys and **DWORD** value described in the following list were added to control the behavior of WMI providers.</span></span>

<dl> <dt>

<span data-ttu-id="9091c-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="9091c-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="9091c-126">此索引鍵控制個別提供者的行為。</span><span class="sxs-lookup"><span data-stu-id="9091c-126">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="9091c-127">此機碼中列出的所有提供者一律會在安全模式中執行。</span><span class="sxs-lookup"><span data-stu-id="9091c-127">All of the providers that are listed in this key always run in secure mode.</span></span> <span data-ttu-id="9091c-128">Windows 隨附的所有收件匣提供者都會列在此機碼底下，並且預設會在安全模式下執行。</span><span class="sxs-lookup"><span data-stu-id="9091c-128">All inbox providers that are shipped with Windows are listed under this key, and are run in secure mode by default.</span></span>

<span data-ttu-id="9091c-129">此索引鍵優先于 **CompatibleHostProviders** 索引鍵中所列的提供者。</span><span class="sxs-lookup"><span data-stu-id="9091c-129">This key takes precedence over providers listed in the **CompatibleHostProviders** key.</span></span>

</dd> <dt>

<span data-ttu-id="9091c-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="9091c-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="9091c-131">此索引鍵控制個別提供者的行為。</span><span class="sxs-lookup"><span data-stu-id="9091c-131">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="9091c-132">此機碼中列出的所有提供者一律會以相容模式執行。</span><span class="sxs-lookup"><span data-stu-id="9091c-132">All providers that are listed in this key always run in compatible mode.</span></span> <span data-ttu-id="9091c-133">依預設，此索引鍵是空的。</span><span class="sxs-lookup"><span data-stu-id="9091c-133">This key is empty by default.</span></span>

<span data-ttu-id="9091c-134">如果提供者同時列在 **SecuredHostProviders** 索引鍵和 **CompatibleHostProviders** 索引鍵中，則提供者會在安全模式中執行。</span><span class="sxs-lookup"><span data-stu-id="9091c-134">If a provider is listed both in the **SecuredHostProviders** key and in the **CompatibleHostProviders** key, the provider is run in secure mode.</span></span>

> [!Note]  
> <span data-ttu-id="9091c-135">如果 **DefaultSecuredHost** 機碼設定為1，而且已知提供者無法在安全模式下運作， **CompatibleHostProviders** 索引鍵會為協力廠商應用程式提供應用程式相容性。</span><span class="sxs-lookup"><span data-stu-id="9091c-135">The **CompatibleHostProviders** key provides application compatibility for third-party applications if the **DefaultSecuredHost** key is set to 1 and the provider is known to not function in secure mode.</span></span>

 

</dd> <dt>

<span data-ttu-id="9091c-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span><span class="sxs-lookup"><span data-stu-id="9091c-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span></span>
</dt> <dd>

<span data-ttu-id="9091c-137">全域登錄 **DWORD** 值，可判斷 **SecuredHostProviders** 或 **CompatibleHostProviders** 索引鍵中未列出的所有提供者是否在安全或相容模式中執行。</span><span class="sxs-lookup"><span data-stu-id="9091c-137">A global registry **DWORD** value that determines whether all of the providers, which are not listed in the **SecuredHostProviders** or **CompatibleHostProviders** keys, are run in the secure or compatible mode.</span></span> <span data-ttu-id="9091c-138">這個 **DWORD** 值可讓系統管理員決定協力廠商提供者必須執行的模式。</span><span class="sxs-lookup"><span data-stu-id="9091c-138">This **DWORD** value lets the administrator decide under which mode a third-party provider must run.</span></span> <span data-ttu-id="9091c-139">依預設，此值會設定為零，而且所有協力廠商提供者都會在相容模式中執行。</span><span class="sxs-lookup"><span data-stu-id="9091c-139">By default, this value is set to zero and all third-party providers are run in compatible mode.</span></span> <span data-ttu-id="9091c-140">系統管理員可以藉由將 **DefaultSecuredHost** 值設定為1，使其電腦更安全。</span><span class="sxs-lookup"><span data-stu-id="9091c-140">Administrators can make their computer more secure by default by setting the **DefaultSecuredHost** value to 1.</span></span>

> [!Note]  
> <span data-ttu-id="9091c-141">**DefaultSecuredHost** 值不會影響其他的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="9091c-141">The **DefaultSecuredHost** value does not affect the other registry keys.</span></span> <span data-ttu-id="9091c-142">**SecuredHostProviders** 索引鍵中所列的提供者會保留在安全模式中，而且 **CompatibleHostProviders** 機碼中列出的提供者仍會保持相容模式。</span><span class="sxs-lookup"><span data-stu-id="9091c-142">The providers that are listed in the **SecuredHostProviders** key remain in secure mode, and the ones that are listed in the **CompatibleHostProviders** key remain in compatible mode.</span></span>

 

<span data-ttu-id="9091c-143">可能的設定如下：</span><span class="sxs-lookup"><span data-stu-id="9091c-143">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="9091c-144"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="9091c-144"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="9091c-145">指定提供者在相容模式中執行。</span><span class="sxs-lookup"><span data-stu-id="9091c-145">Specifies that providers run in compatible mode.</span></span>

</dd> <dt>

<span data-ttu-id="9091c-146"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="9091c-146"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="9091c-147">指定提供者在安全模式下執行。</span><span class="sxs-lookup"><span data-stu-id="9091c-147">Specifies that providers run in secure mode.</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="9091c-148">下列清單列出提供者的可能登錄設定和相關聯的執行模式。</span><span class="sxs-lookup"><span data-stu-id="9091c-148">The following list lists the possible registry settings and the associated running modes for a provider.</span></span>



| <span data-ttu-id="9091c-149">列在 SecuredHostProviders 底下</span><span class="sxs-lookup"><span data-stu-id="9091c-149">Listed under SecuredHostProviders</span></span> | <span data-ttu-id="9091c-150">列在 CompatibleHostProviders 底下</span><span class="sxs-lookup"><span data-stu-id="9091c-150">Listed under CompatibleHostProviders</span></span> | <span data-ttu-id="9091c-151">DefaultSecuredHost 設定</span><span class="sxs-lookup"><span data-stu-id="9091c-151">DefaultSecuredHost Setting</span></span> | <span data-ttu-id="9091c-152">模式</span><span class="sxs-lookup"><span data-stu-id="9091c-152">Mode</span></span>       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| <span data-ttu-id="9091c-153">否</span><span class="sxs-lookup"><span data-stu-id="9091c-153">No</span></span>                                | <span data-ttu-id="9091c-154">否</span><span class="sxs-lookup"><span data-stu-id="9091c-154">No</span></span>                                   | <span data-ttu-id="9091c-155">0</span><span class="sxs-lookup"><span data-stu-id="9091c-155">0</span></span>                          | <span data-ttu-id="9091c-156">相容</span><span class="sxs-lookup"><span data-stu-id="9091c-156">Compatible</span></span> |
| <span data-ttu-id="9091c-157">否</span><span class="sxs-lookup"><span data-stu-id="9091c-157">No</span></span>                                | <span data-ttu-id="9091c-158">是</span><span class="sxs-lookup"><span data-stu-id="9091c-158">Yes</span></span>                                  | <span data-ttu-id="9091c-159">0</span><span class="sxs-lookup"><span data-stu-id="9091c-159">0</span></span>                          | <span data-ttu-id="9091c-160">相容</span><span class="sxs-lookup"><span data-stu-id="9091c-160">Compatible</span></span> |
| <span data-ttu-id="9091c-161">是</span><span class="sxs-lookup"><span data-stu-id="9091c-161">Yes</span></span>                               | <span data-ttu-id="9091c-162">否</span><span class="sxs-lookup"><span data-stu-id="9091c-162">No</span></span>                                   | <span data-ttu-id="9091c-163">0</span><span class="sxs-lookup"><span data-stu-id="9091c-163">0</span></span>                          | <span data-ttu-id="9091c-164">安全</span><span class="sxs-lookup"><span data-stu-id="9091c-164">Secure</span></span>     |
| <span data-ttu-id="9091c-165">是</span><span class="sxs-lookup"><span data-stu-id="9091c-165">Yes</span></span>                               | <span data-ttu-id="9091c-166">是</span><span class="sxs-lookup"><span data-stu-id="9091c-166">Yes</span></span>                                  | <span data-ttu-id="9091c-167">0</span><span class="sxs-lookup"><span data-stu-id="9091c-167">0</span></span>                          | <span data-ttu-id="9091c-168">安全</span><span class="sxs-lookup"><span data-stu-id="9091c-168">Secure</span></span>     |
| <span data-ttu-id="9091c-169">否</span><span class="sxs-lookup"><span data-stu-id="9091c-169">No</span></span>                                | <span data-ttu-id="9091c-170">否</span><span class="sxs-lookup"><span data-stu-id="9091c-170">No</span></span>                                   | <span data-ttu-id="9091c-171">1</span><span class="sxs-lookup"><span data-stu-id="9091c-171">1</span></span>                          | <span data-ttu-id="9091c-172">安全</span><span class="sxs-lookup"><span data-stu-id="9091c-172">Secure</span></span>     |
| <span data-ttu-id="9091c-173">否</span><span class="sxs-lookup"><span data-stu-id="9091c-173">No</span></span>                                | <span data-ttu-id="9091c-174">是</span><span class="sxs-lookup"><span data-stu-id="9091c-174">Yes</span></span>                                  | <span data-ttu-id="9091c-175">1</span><span class="sxs-lookup"><span data-stu-id="9091c-175">1</span></span>                          | <span data-ttu-id="9091c-176">相容</span><span class="sxs-lookup"><span data-stu-id="9091c-176">Compatible</span></span> |
| <span data-ttu-id="9091c-177">是</span><span class="sxs-lookup"><span data-stu-id="9091c-177">Yes</span></span>                               | <span data-ttu-id="9091c-178">否</span><span class="sxs-lookup"><span data-stu-id="9091c-178">No</span></span>                                   | <span data-ttu-id="9091c-179">1</span><span class="sxs-lookup"><span data-stu-id="9091c-179">1</span></span>                          | <span data-ttu-id="9091c-180">安全</span><span class="sxs-lookup"><span data-stu-id="9091c-180">Secure</span></span>     |
| <span data-ttu-id="9091c-181">是</span><span class="sxs-lookup"><span data-stu-id="9091c-181">Yes</span></span>                               | <span data-ttu-id="9091c-182">是</span><span class="sxs-lookup"><span data-stu-id="9091c-182">Yes</span></span>                                  | <span data-ttu-id="9091c-183">1</span><span class="sxs-lookup"><span data-stu-id="9091c-183">1</span></span>                          | <span data-ttu-id="9091c-184">安全</span><span class="sxs-lookup"><span data-stu-id="9091c-184">Secure</span></span>     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a><span data-ttu-id="9091c-185">將提供者設定為在安全或相容模式中執行</span><span class="sxs-lookup"><span data-stu-id="9091c-185">Configuring a Provider to Run in Secure or Compatible Mode</span></span>

<span data-ttu-id="9091c-186">您可以使用群組原則管理主控台 (GPMC) 來修改登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="9091c-186">The registry keys can be modified using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="9091c-187">如需詳細資訊，請參閱 [群組原則管理主控台](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)。</span><span class="sxs-lookup"><span data-stu-id="9091c-187">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="9091c-188">下列程式說明如何使用群組原則喜好設定來管理安全且相容的模式設定。</span><span class="sxs-lookup"><span data-stu-id="9091c-188">The following procedures illustrate how to manage secure and compatible mode settings by using group policy preferences.</span></span> <span data-ttu-id="9091c-189">如需群組原則喜好設定的詳細資訊，請參閱 [群組原則喜好設定總覽](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="9091c-189">For more information about group policy preferences, see the [Group Policy Preferences Overview](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span></span>

<span data-ttu-id="9091c-190">**使用群組原則將提供者新增至安全或相容模式**</span><span class="sxs-lookup"><span data-stu-id="9091c-190">**To add a provider to either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="9091c-191">開啟 GPMC。</span><span class="sxs-lookup"><span data-stu-id="9091c-191">Open the GPMC.</span></span>
2.  <span data-ttu-id="9091c-192"> (GPO) 建立群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="9091c-192">Create a Group Policy Object (GPO).</span></span>
3.  <span data-ttu-id="9091c-193">編輯 GPO。</span><span class="sxs-lookup"><span data-stu-id="9091c-193">Edit the GPO.</span></span>
4.  <span data-ttu-id="9091c-194">流覽至 [喜好設定]/[Windows 設定]/[登錄]。</span><span class="sxs-lookup"><span data-stu-id="9091c-194">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="9091c-195">以滑鼠右鍵按一下並選取 [新增]。 登錄。</span><span class="sxs-lookup"><span data-stu-id="9091c-195">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="9091c-196">此動作會顯示使用者介面，您可以在其中輸入登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="9091c-196">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="9091c-197">選取 [ **建立** ] 命令。</span><span class="sxs-lookup"><span data-stu-id="9091c-197">Select the **Create** command.</span></span>
7.  <span data-ttu-id="9091c-198">選取下列登錄機碼路徑：</span><span class="sxs-lookup"><span data-stu-id="9091c-198">Select the following registry key path:</span></span>

    <span data-ttu-id="9091c-199">**安全模式： HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="9091c-199">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="9091c-200">**相容模式： HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="9091c-200">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="9091c-201">在 [ **名稱** ] 欄位中，輸入您要新增至此金鑰的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="9091c-201">In the **name** field, enter the name of the provider you want to add to this key.</span></span> <span data-ttu-id="9091c-202">提供者名稱的格式必須如下： <namespace> ： <\_ \_ RELPATH>。</span><span class="sxs-lookup"><span data-stu-id="9091c-202">The provider name must be in the following format: <namespace>:<\_\_RELPATH>.</span></span> <span data-ttu-id="9091c-203">例如，根 \\ cimv2： \_ \_ win32provider. Name = "MyProvider"。</span><span class="sxs-lookup"><span data-stu-id="9091c-203">For example, root\\cimv2:\_\_win32provider.name="MyProvider".</span></span>
9.  <span data-ttu-id="9091c-204">在 [ **資料** ] 欄位中，輸入0。</span><span class="sxs-lookup"><span data-stu-id="9091c-204">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="9091c-205">按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="9091c-205">Click OK.</span></span>

<span data-ttu-id="9091c-206">**若要使用群組原則從安全或相容模式移除提供者**</span><span class="sxs-lookup"><span data-stu-id="9091c-206">**To remove a provider from either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="9091c-207">開啟 GPMC。</span><span class="sxs-lookup"><span data-stu-id="9091c-207">Open the GPMC.</span></span>
2.  <span data-ttu-id="9091c-208">建立 GPO。</span><span class="sxs-lookup"><span data-stu-id="9091c-208">Create a GPO.</span></span>
3.  <span data-ttu-id="9091c-209">編輯 GPO。</span><span class="sxs-lookup"><span data-stu-id="9091c-209">Edit the GPO.</span></span>
4.  <span data-ttu-id="9091c-210">流覽至 [喜好設定]/[Windows 設定]/[登錄]。</span><span class="sxs-lookup"><span data-stu-id="9091c-210">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="9091c-211">以滑鼠右鍵按一下並選取 [新增]。 登錄。</span><span class="sxs-lookup"><span data-stu-id="9091c-211">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="9091c-212">此動作會顯示使用者介面，您可以在其中輸入登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="9091c-212">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="9091c-213">選取 [ **移除** ] 命令。</span><span class="sxs-lookup"><span data-stu-id="9091c-213">Select the **Remove** command.</span></span>
7.  <span data-ttu-id="9091c-214">選取下列登錄機碼路徑：</span><span class="sxs-lookup"><span data-stu-id="9091c-214">Select the following registry key path:</span></span>

    <span data-ttu-id="9091c-215">**安全模式： HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="9091c-215">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="9091c-216">**相容模式： HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="9091c-216">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="9091c-217">在 [ **名稱** ] 欄位中，輸入您要從此索引鍵移除的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="9091c-217">In the **name** field, enter the name of the provider you want to remove from this key.</span></span>
9.  <span data-ttu-id="9091c-218">在 [ **資料** ] 欄位中，輸入0。</span><span class="sxs-lookup"><span data-stu-id="9091c-218">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="9091c-219">按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="9091c-219">Click OK.</span></span>

<span data-ttu-id="9091c-220">下列程式提供有關如何修改未列在 **SecuredHostProviders** 或 **CompatibleHostProviders** 索引鍵中之提供者行為的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9091c-220">The following procedure provides details about how to modify the behavior of providers that are not listed in either the **SecuredHostProviders** or **CompatibleHostProviders** keys.</span></span>

<span data-ttu-id="9091c-221">**使用群組原則來變更 DefaultSecuredHost 索引鍵的預設值**</span><span class="sxs-lookup"><span data-stu-id="9091c-221">**To change the default value of the DefaultSecuredHost key by using Group Policy**</span></span>

1.  <span data-ttu-id="9091c-222">開啟 GPMC。</span><span class="sxs-lookup"><span data-stu-id="9091c-222">Open the GPMC.</span></span>
2.  <span data-ttu-id="9091c-223">建立 GPO。</span><span class="sxs-lookup"><span data-stu-id="9091c-223">Create a GPO.</span></span>
3.  <span data-ttu-id="9091c-224">編輯 GPO。</span><span class="sxs-lookup"><span data-stu-id="9091c-224">Edit the GPO.</span></span>
4.  <span data-ttu-id="9091c-225">流覽至 [喜好設定]/[Windows 設定]/[登錄]。</span><span class="sxs-lookup"><span data-stu-id="9091c-225">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="9091c-226">以滑鼠右鍵按一下並選取 [新增]。 登錄。</span><span class="sxs-lookup"><span data-stu-id="9091c-226">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="9091c-227">此動作會顯示使用者介面，您可以在其中輸入登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="9091c-227">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="9091c-228">選取 [ **更新** ] 命令。</span><span class="sxs-lookup"><span data-stu-id="9091c-228">Select the **Update** command.</span></span>
7.  <span data-ttu-id="9091c-229">選取下列登錄機碼路徑： **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**。</span><span class="sxs-lookup"><span data-stu-id="9091c-229">Select the following registry key path: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**.</span></span>
8.  <span data-ttu-id="9091c-230">在 [ **名稱** ] 欄位中，輸入 **DefaultSecuredHost**。</span><span class="sxs-lookup"><span data-stu-id="9091c-230">In the **name** field, enter **DefaultSecuredHost**.</span></span>
9.  <span data-ttu-id="9091c-231">在 [ **資料** ] 欄位中，輸入0表示相容模式，或輸入1表示安全模式。</span><span class="sxs-lookup"><span data-stu-id="9091c-231">In the **data** field, enter 0 for compatible mode or 1 for secure mode.</span></span>
10. <span data-ttu-id="9091c-232">按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="9091c-232">Click OK.</span></span>

 

 
