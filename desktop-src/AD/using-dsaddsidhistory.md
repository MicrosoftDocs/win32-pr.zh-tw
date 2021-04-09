---
title: 使用 DsAddSidHistory
description: 本主題說明如何使用 DsAddSidHistory 函數。
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- 使用 DsAddSidHistory Active Directory
- 使用 DsAddSidHistory Active Directory Active Directory
- DsAddSidHistory Active Directory，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d45792dbd8c7a2bfa2dd047111a3ed165a2011e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671207"
---
# <a name="using-dsaddsidhistory"></a><span data-ttu-id="08a42-106">使用 DsAddSidHistory</span><span class="sxs-lookup"><span data-stu-id="08a42-106">Using DsAddSidHistory</span></span>

<span data-ttu-id="08a42-107">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)函式會從一個網域 (來源網域) 取得安全性主體 (SID) 的主要帳戶安全識別碼，然後將它新增至不同樹系中另一個 (目的地) 網域中安全性主體的 **sIDHistory** 屬性。</span><span class="sxs-lookup"><span data-stu-id="08a42-107">The [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) function gets the primary account security identifier (SID) of a security principal from one domain (the source domain) and adds it to the **sIDHistory** attribute of a security principal in another (destination) domain in a different forest.</span></span> <span data-ttu-id="08a42-108">當來源網域處於 Windows 2000 原生模式時，此函式也會抓取來源主體的 **sIDHistory** 值，並將其新增至目的地主體的 **sidhistory**。</span><span class="sxs-lookup"><span data-stu-id="08a42-108">When the source domain is in Windows 2000 native mode, this function also retrieves the **sIDHistory** values of the source principal and adds them to the destination principal's **sIDHistory**.</span></span>

<span data-ttu-id="08a42-109">將 Sid 新增至安全性主體的 **sIDHistory** 是一項安全性敏感的作業，可有效地授與目的地主體存取來源主體可存取的所有資源，但前提是該信任存在於適用的資源網域到目的地網域中。</span><span class="sxs-lookup"><span data-stu-id="08a42-109">Adding SIDs to a security principal's **sIDHistory** is a security-sensitive operation that effectively grants to the destination principal access to all resources accessible to the source principal, provided that trusts exist from applicable resource domains to the destination domain.</span></span>

<span data-ttu-id="08a42-110">在原生模式 Windows 2000 網域中，使用者登入會建立存取權杖，其中包含使用者主要帳戶 SID 和群組 Sid，以及使用者為其成員之群組的使用者 **sidhistory** 和 **sIDHistory** 。</span><span class="sxs-lookup"><span data-stu-id="08a42-110">In a native mode Windows 2000 domain a user logon creates an access token that contains the user primary account SID and group SIDs, as well as the user **sIDHistory** and the **sIDHistory** of the groups of which the user is a member.</span></span> <span data-ttu-id="08a42-111">將這些先前的 Sid (**sIDHistory** 值) 在使用者的權杖中，會授與使用者存取受存取控制清單保護之資源的存取權 (acl) 包含先前的 sid。</span><span class="sxs-lookup"><span data-stu-id="08a42-111">Having these former SIDs (**sIDHistory** values) in the user's token grants the user access to resources protected by access-control lists (ACLs) containing the former SIDs.</span></span>

<span data-ttu-id="08a42-112">這種操作可加速特定的 Windows 2000 部署案例。</span><span class="sxs-lookup"><span data-stu-id="08a42-112">This operation facilitates certain Windows 2000 deployment scenarios.</span></span> <span data-ttu-id="08a42-113">尤其是，它支援一種案例，其中會為已存在於 Windows NT 4.0 生產環境中的使用者和群組建立新 Windows 2000 樹系中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="08a42-113">In particular, it supports a scenario in which accounts in a new Windows 2000 forest are created for users and groups that already exist in an Windows NT 4.0 production environment.</span></span> <span data-ttu-id="08a42-114">藉由將 Windows NT 4.0 帳戶 SID 放在 Windows 2000 帳戶 **sIDHistory** 中，就會保留使用者登入新的 Windows 2000 帳戶的網路資源存取權。</span><span class="sxs-lookup"><span data-stu-id="08a42-114">By placing the Windows NT 4.0 account SID in the Windows 2000 account **sIDHistory**, access to network resources is preserved for the user logging onto his new Windows 2000 account.</span></span>

<span data-ttu-id="08a42-115">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 也支援將 Windows NT 4.0 備份網域控制站 (bdc) 資源伺服器 (或原生模式 windows 2000 網域中的 dc 和成員伺服器，) 到 Windows 2000 網域做為成員伺服器。</span><span class="sxs-lookup"><span data-stu-id="08a42-115">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) also supports migration of Windows NT 4.0 backup domain controllers (BDCs) resource servers (or DCs and member servers in a native mode Windows 2000 domain) to a Windows 2000 domain as member servers.</span></span> <span data-ttu-id="08a42-116">這項遷移需要在目的地 Windows 2000 網域中，建立包含在其 SIDHistory 的網域本機群組的網網域本機群組（在其 **sIDHistory** 中），在 BDC (或在來源網域中的 Windows 2000 伺服器) 上 acl 中所參考的網域本機群組的主要 sid。</span><span class="sxs-lookup"><span data-stu-id="08a42-116">This migration requires the creation, in the destination Windows 2000 domain, of domain local groups that contain, in their **sIDHistory**, the primary SIDs of the local groups defined on the BDC (or domain local groups referenced in ACLs on the Windows 2000 servers) in the source domain.</span></span> <span data-ttu-id="08a42-117">藉由建立包含 **sIDHistory** 的目的地本機群組和來源本機群組的所有成員，將會針對所有成員維護由參考來源本機群組之 acl 所保護的已遷移伺服器資源存取權。</span><span class="sxs-lookup"><span data-stu-id="08a42-117">By creating a destination local group containing the **sIDHistory** and all members of the source local group, access to the migrated server resources, protected by ACLs referencing the source local group, is maintained for all members.</span></span>

> [!Note]  
> <span data-ttu-id="08a42-118">使用 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 需要瞭解在這些案例和其他案例中，其管理和安全性方面的影響。</span><span class="sxs-lookup"><span data-stu-id="08a42-118">Use of [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requires an understanding of its broader administrative and security implications in these and other scenarios.</span></span> <span data-ttu-id="08a42-119">Dommig.doc 如需詳細資訊，請參閱 Windows 2000 支援工具中的「規劃從 Windows NT 到 Microsoft Windows 2000」的白皮書。</span><span class="sxs-lookup"><span data-stu-id="08a42-119">For more information, see the white paper "Planning Migration from Windows NT to Microsoft Windows 2000", delivered as Dommig.doc in the Windows 2000 Support Tools.</span></span> <span data-ttu-id="08a42-120">您也可以在產品 CD 的 [支援工具] 下找到此檔集 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="08a42-120">This documentation may also be found on the product CD under \\support\\tools.</span></span>

 

## <a name="authorization-requirements"></a><span data-ttu-id="08a42-121">授權需求</span><span class="sxs-lookup"><span data-stu-id="08a42-121">Authorization Requirements</span></span>

<span data-ttu-id="08a42-122">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 需要來源和目的地網域中的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="08a42-122">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requires administrator privileges in the source and destination domains.</span></span> <span data-ttu-id="08a42-123">具體而言，此 API 的呼叫端必須是目的地網域中網域系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="08a42-123">Specifically, the caller of this API must be a member of the Domain Administrators group in the destination domain.</span></span> <span data-ttu-id="08a42-124">執行此成員資格的硬式編碼檢查。</span><span class="sxs-lookup"><span data-stu-id="08a42-124">A hard-coded check for this membership is performed.</span></span> <span data-ttu-id="08a42-125">此外， *SrcDomainCreds* 參數中提供的呼叫端或帳戶（如果不是 **Null**）必須是來源網域中的系統管理員或網域系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="08a42-125">Also, the caller or the account provided in the *SrcDomainCreds* parameter, if not **NULL**, must be a member of either the Administrators or Domain Administrators group in the source domain.</span></span>

## <a name="domain-and-trust-requirements"></a><span data-ttu-id="08a42-126">網域和信任需求</span><span class="sxs-lookup"><span data-stu-id="08a42-126">Domain and Trust Requirements</span></span>

<span data-ttu-id="08a42-127">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 要求目的地網域必須處於 Windows 2000 原生模式或更新版本，因為只有此網欄位型別支援 **sIDHistory** 屬性。</span><span class="sxs-lookup"><span data-stu-id="08a42-127">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requires that the destination domain be in Windows 2000 native mode or later, because only this domain type supports the **sIDHistory** attribute.</span></span> <span data-ttu-id="08a42-128">來源網域可以是 Windows NT 4.0 或 Windows 2000、混合模式或原生模式。</span><span class="sxs-lookup"><span data-stu-id="08a42-128">The source domain may be either Windows NT 4.0 or Windows 2000, mixed or native mode.</span></span> <span data-ttu-id="08a42-129">來源和目的地網域不得位於相同的樹系中。</span><span class="sxs-lookup"><span data-stu-id="08a42-129">The source and destination domains must not be in the same forest.</span></span> <span data-ttu-id="08a42-130">Windows NT 4.0 網域的定義不在樹系中。</span><span class="sxs-lookup"><span data-stu-id="08a42-130">Windows NT 4.0 domains are by definition not in a forest.</span></span> <span data-ttu-id="08a42-131">此樹系內的條件約束可確保不會在相同的樹系中建立重複的 Sid （不論是否顯示為主要 Sid 或 **sIDHistory** 值）。</span><span class="sxs-lookup"><span data-stu-id="08a42-131">This inter-forest constraint ensures that duplicate SIDs, whether appearing as primary SIDs or **sIDHistory** values, are not created in the same forest.</span></span>

<span data-ttu-id="08a42-132">在下表所列的情況下， [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)需要來源網域到目的地網域的外部信任。</span><span class="sxs-lookup"><span data-stu-id="08a42-132">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requires an external trust from the source domain to the destination domain in the cases listed in the following table.</span></span>



| <span data-ttu-id="08a42-133">案例</span><span class="sxs-lookup"><span data-stu-id="08a42-133">Case</span></span>                                                                             | <span data-ttu-id="08a42-134">Description</span><span class="sxs-lookup"><span data-stu-id="08a42-134">Description</span></span>                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a42-135">來源網域是 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="08a42-135">The source domain is Windows 2000.</span></span><br/>                                    | <span data-ttu-id="08a42-136">來源 **sIDHistory** 屬性（僅適用于 Windows 2000 來源網域）可能會使用 LDAP 唯讀，這需要此信任以進行完整性保護。</span><span class="sxs-lookup"><span data-stu-id="08a42-136">The source **sIDHistory** attribute, available only in Windows 2000 source domains, may be read only using LDAP, which requires this trust for integrity protection.</span></span><br/>                                                                                             |
| <span data-ttu-id="08a42-137">來源網域是 Windows NT 4.0，而 *SrcDomainCreds* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="08a42-137">The source domain is Windows NT 4.0 and *SrcDomainCreds* is **NULL**.</span></span><br/> | <span data-ttu-id="08a42-138">使用呼叫端認證支援來源網域作業所需的模擬，取決於此信任。</span><span class="sxs-lookup"><span data-stu-id="08a42-138">The impersonation, required to support source domain operations using the caller's credentials, depends on this trust.</span></span> <span data-ttu-id="08a42-139">模擬也需要目的地網域控制站預設在網域控制站上啟用「受信任的委派」。</span><span class="sxs-lookup"><span data-stu-id="08a42-139">Impersonation also requires that the destination domain controller has "Trusted for Delegation" enabled by default on domain controllers.</span></span><br/> |



 

<span data-ttu-id="08a42-140">但是，如果來源網域是 Windows NT 4.0 且 *SrcDomainCreds* 不是 **Null**，則來源和目的地網域之間不需要信任。</span><span class="sxs-lookup"><span data-stu-id="08a42-140">However, there is no trust required between the source and destination domains if the source domain is Windows NT 4.0 and *SrcDomainCreds* is not **NULL**.</span></span>

## <a name="source-domain-controller-requirements"></a><span data-ttu-id="08a42-141">來源網域控制站需求</span><span class="sxs-lookup"><span data-stu-id="08a42-141">Source Domain Controller Requirements</span></span>

<span data-ttu-id="08a42-142">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 需要在來源網域中選取作為作業目標的網域控制站成為 Windows NT 4.0 網域中的 pdc，或 Windows 2000 網域中的 pdc 模擬器。</span><span class="sxs-lookup"><span data-stu-id="08a42-142">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requires that the domain controller, selected as the target for operations in the source domain, be the PDC in Windows NT 4.0 domains or the PDC Emulator in Windows 2000 domains.</span></span> <span data-ttu-id="08a42-143">來源網域審核是透過寫入作業產生的，因此，在 Windows NT 4.0 來源網域中需要 PDC，而且僅限 PDC 的限制可確保在單一電腦上產生 **DsAddSidHistory** 的審核。</span><span class="sxs-lookup"><span data-stu-id="08a42-143">Source domain auditing is generated by way of write operations, therefore, the PDC is required in Windows NT 4.0 source domains, and the PDC-only restriction ensures that **DsAddSidHistory** audits are generated on a single computer.</span></span> <span data-ttu-id="08a42-144">這可減少審核所有 Dc 之審核記錄的需求，以監視此作業的使用情形。</span><span class="sxs-lookup"><span data-stu-id="08a42-144">This reduces the need to review the audit logs of all DCs to monitor use of this operation.</span></span>

> [!Note]  
> <span data-ttu-id="08a42-145">在 Windows NT 4.0 來源網域中，來源網域中的作業 PDC (目標) 必須執行 Service Pack 4 (SP4) 和更新版本，以確保適當的審核支援。</span><span class="sxs-lookup"><span data-stu-id="08a42-145">In Windows NT 4.0 source domains, the PDC (target of operations in the source domain) must be running Service Pack 4 (SP4) and later to ensure proper auditing support.</span></span>

 

<span data-ttu-id="08a42-146">您必須在來源網域控制站上，將下列登錄值建立為 REG \_ DWORD 值，並在 Windows NT 4.0 和 Windows 2000 來源 dc 設定為1。</span><span class="sxs-lookup"><span data-stu-id="08a42-146">The following registry value must be created as a REG\_DWORD value and set to 1 on the source domain controller for both Windows NT 4.0 and Windows 2000 source DCs.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

<span data-ttu-id="08a42-147">設定此值會啟用 TCP 傳輸上的 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="08a42-147">Setting this value enables RPC calls over the TCP transport.</span></span> <span data-ttu-id="08a42-148">這是必要的，因為根據預設，SAMRPC 介面只能在具名管道上進行遠端處理。</span><span class="sxs-lookup"><span data-stu-id="08a42-148">This is required because, by default, SAMRPC interfaces are remotable only on named pipes.</span></span> <span data-ttu-id="08a42-149">使用具名管道會導致認證管理系統適用于進行網路呼叫的互動式登入使用者，但對於使用使用者提供的認證進行網路呼叫的系統程式來說，並不具彈性。</span><span class="sxs-lookup"><span data-stu-id="08a42-149">Using named pipes results in a credential management system suitable for interactively logged-on users making networked calls, but is not flexible for a system process that makes network calls with user-supplied credentials.</span></span> <span data-ttu-id="08a42-150">RPC over TCP 更適合該用途。</span><span class="sxs-lookup"><span data-stu-id="08a42-150">RPC over TCP is more suitable for that purpose.</span></span> <span data-ttu-id="08a42-151">設定這個值並不會降低系統安全性。</span><span class="sxs-lookup"><span data-stu-id="08a42-151">Setting this value does not diminish system security.</span></span> <span data-ttu-id="08a42-152">如果已建立或變更此值，則必須重新開機來源網域控制站，這項設定才會生效。</span><span class="sxs-lookup"><span data-stu-id="08a42-152">If this value is created or changed, the source domain controller must be restarted for this setting to take effect.</span></span>

<span data-ttu-id="08a42-153"><SrcDomainName>為了進行審核，必須在來源網域中建立新的本機群組 "$ $ $"。</span><span class="sxs-lookup"><span data-stu-id="08a42-153">A new local group, "<SrcDomainName>$$$", must be created in the source domain for auditing purposes.</span></span>

## <a name="auditing"></a><span data-ttu-id="08a42-154">稽核</span><span class="sxs-lookup"><span data-stu-id="08a42-154">Auditing</span></span>

<span data-ttu-id="08a42-155">系統會審核 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)作業，以確保來源和目的地網域系統管理員都能夠偵測此函式的執行時間。</span><span class="sxs-lookup"><span data-stu-id="08a42-155">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) operations are audited to ensure that both source and destination domain administrators are able to detect when this function has been run.</span></span> <span data-ttu-id="08a42-156">來源和目的地網域都必須進行審核。</span><span class="sxs-lookup"><span data-stu-id="08a42-156">Auditing is mandatory in both the source and destination domains.</span></span> <span data-ttu-id="08a42-157">**DsAddSidHistory** 會確認每個網域中的 Audit 模式都是 on，且「成功/失敗」事件的帳戶管理審核是開啟的。</span><span class="sxs-lookup"><span data-stu-id="08a42-157">**DsAddSidHistory** verifies that the Audit Mode is on in each domain and that Account Management auditing of Success/Failure events is on.</span></span> <span data-ttu-id="08a42-158">在目的地網域中，會針對每個成功或失敗的 **DsAddSidHistory** 作業產生唯一的「新增 Sid 歷程記錄」 audit 事件。</span><span class="sxs-lookup"><span data-stu-id="08a42-158">In the destination domain, a unique "Add Sid History" audit event is generated for each successful or failed **DsAddSidHistory** operation.</span></span>

<span data-ttu-id="08a42-159">在 Windows NT 4.0 系統上無法使用唯一的「新增 Sid 歷程記錄」審核事件。</span><span class="sxs-lookup"><span data-stu-id="08a42-159">Unique "Add Sid History" audit events are not available on Windows NT 4.0 systems.</span></span> <span data-ttu-id="08a42-160">若要產生明確反映對來源網域使用 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 的 audit 事件，它會針對名稱為 audit 記錄檔中唯一識別碼的特殊群組執行作業。</span><span class="sxs-lookup"><span data-stu-id="08a42-160">To generate audit events that unambiguously reflect use of [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) against the source domain, it performs operations on a special group whose name is the unique identifier in the audit log.</span></span> <span data-ttu-id="08a42-161">本機群組 " <SrcDomainName> $ $ $" 的名稱是由附加三個貨幣符號 ($)  (ASCII 碼 = 0x24 和 Unicode = U + 0024) 的來源網域 NetBIOS 名稱所組成，必須在呼叫 **DsAddSidHistory** 之前于來源網域控制站上建立。</span><span class="sxs-lookup"><span data-stu-id="08a42-161">A local group, "<SrcDomainName>$$$", whose name is composed of the source domain NetBIOS name appended with three dollar signs ($) (ASCII code = 0x24 and Unicode = U+0024), must be created on the source domain controller prior to calling **DsAddSidHistory**.</span></span> <span data-ttu-id="08a42-162">這項作業的目標每個來源使用者和全域群組都會加入至此群組的成員資格，然後從這個群組中移除。</span><span class="sxs-lookup"><span data-stu-id="08a42-162">Each source user and global group that is a target of this operation is added to and then removed from the membership of this group.</span></span> <span data-ttu-id="08a42-163">這會產生來源網域中的「新增成員」和「刪除」成員審核事件，藉由搜尋參考組名的事件來監視。</span><span class="sxs-lookup"><span data-stu-id="08a42-163">This generates Add Member and Delete Member audit events in the source domain, which can be monitored by searching for events that reference the group name.</span></span>

> [!Note]  
> <span data-ttu-id="08a42-164">無法審核 Windows NT 4.0 或 Windows 2000 混合模式來源網域中本機群組的 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)作業，因為無法將本機群組設為另一個本機群組的成員，因此無法新增至特殊的 " <SrcDomainName> $ $ $" 本機群組。</span><span class="sxs-lookup"><span data-stu-id="08a42-164">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) operations on local groups in a Windows NT 4.0, or Windows 2000 mixed-mode source domain cannot be audited because local groups cannot be made members of another local group and therefore cannot be added to the special "<SrcDomainName>$$$" local group.</span></span> <span data-ttu-id="08a42-165">這項缺少的審核並不會對來源網域提出安全性問題，因為此作業不會影響來源網域資源的存取。</span><span class="sxs-lookup"><span data-stu-id="08a42-165">This lack of auditing does not present a security issue to the source domain, because source domain resource access is not affected by this operation.</span></span> <span data-ttu-id="08a42-166">將來源本機群組的 SID 新增至目的地本機群組，並不會將存取權授與任何其他使用者的來源資源（受該本機群組保護）。</span><span class="sxs-lookup"><span data-stu-id="08a42-166">Adding the SID of a source local group to a destination local group does not grant access to source resources, protected by that local group, to any additional users.</span></span> <span data-ttu-id="08a42-167">將成員新增至目的地本機群組不會授與他們存取來源資源的許可權。</span><span class="sxs-lookup"><span data-stu-id="08a42-167">Adding members to the destination local group does not grant them access to source resources.</span></span> <span data-ttu-id="08a42-168">新增的成員只會被授與從來源網域遷移之目的地網域中的伺服器存取權，這可能會有受來源本機群組 SID 保護的資源。</span><span class="sxs-lookup"><span data-stu-id="08a42-168">Added members are granted access only to servers in the destination domain migrated from the source domain, which may have resources protected by the source local group SID.</span></span>

 

## <a name="data-transmission-security"></a><span data-ttu-id="08a42-169">資料傳輸安全性</span><span class="sxs-lookup"><span data-stu-id="08a42-169">Data Transmission Security</span></span>

<span data-ttu-id="08a42-170">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 會強制執行下列安全性措施：</span><span class="sxs-lookup"><span data-stu-id="08a42-170">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) enforces the following security measures:</span></span>

-   <span data-ttu-id="08a42-171">從 Windows 2000 工作站呼叫，呼叫者的認證是用來驗證和隱私權-保護對目的地網域控制站的 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="08a42-171">Called from a Windows 2000 workstation, the caller's credentials are used to authenticate and privacy-protect the RPC call to the destination domain controller.</span></span> <span data-ttu-id="08a42-172">如果 *SrcDomainCreds* 不是 **Null**，則工作站和目的地 DC 都必須支援128位加密，以保護認證的安全。</span><span class="sxs-lookup"><span data-stu-id="08a42-172">If *SrcDomainCreds* is not **NULL**, both the workstation and the destination DC must support 128-bit encryption to privacy-protect the credentials.</span></span> <span data-ttu-id="08a42-173">如果無法使用128位加密且提供 *SrcDomainCreds* ，則必須在目的地 DC 上進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="08a42-173">If 128-bit encryption is not available and *SrcDomainCreds* are provided, then the call must be made on the destination DC.</span></span>
-   <span data-ttu-id="08a42-174">目的地網域控制站會使用 *SrcDomainCreds* 或呼叫端的認證與來源網域控制站進行通訊，以相互驗證和完整性-使用 SAM 查閱) 和 **sIDHistory** (（使用 LDAP 讀取) ）來保護來源帳戶 SID 的讀取 (。</span><span class="sxs-lookup"><span data-stu-id="08a42-174">The destination domain controller communicates with the source domain controller using either *SrcDomainCreds* or the caller's credentials to mutually authenticate and integrity-protect the read of the source account SID (using a SAM lookup) and **sIDHistory** (using an LDAP read).</span></span>

## <a name="threat-models"></a><span data-ttu-id="08a42-175">威脅模型</span><span class="sxs-lookup"><span data-stu-id="08a42-175">Threat Models</span></span>

<span data-ttu-id="08a42-176">下表列出與 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 呼叫相關聯的潛在威脅，並解決與特定威脅相關的安全性措施。</span><span class="sxs-lookup"><span data-stu-id="08a42-176">The following table lists the potential threats associated with the [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) call and addresses the security measures pertinent to the particular threat.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08a42-177">潛在威脅</span><span class="sxs-lookup"><span data-stu-id="08a42-177">Potential threat</span></span></th>
<th><span data-ttu-id="08a42-178">安全性措施</span><span class="sxs-lookup"><span data-stu-id="08a42-178">Security measure</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08a42-179">攔截式攻擊</span><span class="sxs-lookup"><span data-stu-id="08a42-179">Man in the Middle Attack</span></span><br/> <span data-ttu-id="08a42-180">未經授權的使用者會攔截來源物件傳回呼叫的 <em>查閱 SID</em> ，將來源物件 SID 取代為要插入至目標物件 SIDhistory 的任意 SID。</span><span class="sxs-lookup"><span data-stu-id="08a42-180">An unauthorized user intercepts the <em>lookup SID of source object</em> return call, replacing the source object SID with an arbitrary SID for insertion into a target object SIDhistory.</span></span><br/></td>
<td><span data-ttu-id="08a42-181"><em>來源物件的查閱 SID</em>是經過驗證的 RPC，使用呼叫端的系統管理員認證與封包完整性訊息保護。</span><span class="sxs-lookup"><span data-stu-id="08a42-181">The <em>lookup SID of source object</em> is an authenticated RPC, using the caller's administrator credentials, with packet integrity message protection.</span></span> <span data-ttu-id="08a42-182">這可確保無法在沒有偵測的情況下修改傳回呼叫。</span><span class="sxs-lookup"><span data-stu-id="08a42-182">This ensures that the return call cannot be modified without detection.</span></span> <span data-ttu-id="08a42-183">目的地網域控制站會建立唯一的 [ &quot; 新增 sid 歷程記錄] &quot; audit 事件，以反映新增至目的地帳戶 <strong>sIDHistory</strong>的 sid。</span><span class="sxs-lookup"><span data-stu-id="08a42-183">The destination domain controller creates a unique &quot;Add SID History&quot; audit event that reflects the SID added to the destination account <strong>sIDHistory</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08a42-184">特洛伊來源網域</span><span class="sxs-lookup"><span data-stu-id="08a42-184">Trojan Source Domain</span></span><br/> <span data-ttu-id="08a42-185">未經授權的使用者 &quot; &quot; 在私人網路上建立特洛伊木馬來源網域，而該網域的網域 SID 和與合法來源網域的帳戶 sid 相同。</span><span class="sxs-lookup"><span data-stu-id="08a42-185">An unauthorized user creates a &quot;Trojan Horse&quot; source domain on a private network that has the same domain SID and some of the same account SIDs as the legitimate source domain.</span></span> <span data-ttu-id="08a42-186">未經授權的使用者接著會嘗試在目的地網域中執行 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> ，以取得來源帳戶的 SID。</span><span class="sxs-lookup"><span data-stu-id="08a42-186">The unauthorized user then attempts to run <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> in a destination domain to obtain the SID of a source account.</span></span> <span data-ttu-id="08a42-187">這樣做不需要真正的來源網域系統管理員認證，也不需要離開實際來源網域中的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="08a42-187">This is done without the need for the real source Domain Administrator credentials and without leaving an audit trail in the real source domain.</span></span> <span data-ttu-id="08a42-188">未經授權的使用者建立特洛伊程式檔來源網域的方法，可能是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="08a42-188">The unauthorized user's method for creating the Trojan Horse source domain could be one of the following:</span></span>
<ul>
<li><span data-ttu-id="08a42-189">取得來源網域 SAM 的複本 (BDC 備份) 。</span><span class="sxs-lookup"><span data-stu-id="08a42-189">Obtain a copy (BDC backup) of the source domain SAM.</span></span></li>
<li><span data-ttu-id="08a42-190">建立新的網域，改變磁片上的網域 SID 以符合合法的來源網域 SID，然後建立足夠的使用者以具現化具有所需 SID 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="08a42-190">Create a new domain, altering the domain SID on disk to match the legitimate source domain SID, then create enough users to instantiate an account with the desired SID.</span></span></li>
<li><span data-ttu-id="08a42-191">建立 BDC 複本。</span><span class="sxs-lookup"><span data-stu-id="08a42-191">Create a BDC replica.</span></span> <span data-ttu-id="08a42-192">這需要來源網域系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="08a42-192">This requires source domain Administrator credentials.</span></span> <span data-ttu-id="08a42-193">然後，未經授權的使用者會將複本帶到私人網路以執行攻擊。</span><span class="sxs-lookup"><span data-stu-id="08a42-193">Then the unauthorized user takes the replica to a private network to implement the attack.</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="08a42-194">雖然有許多方法可讓未經授權的使用者取得或建立所需的來源物件 SID，但未經授權的使用者無法使用它來更新帳戶的 <strong>sIDHistory</strong> ，而不是目的地網域系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="08a42-194">Although there are many ways for an unauthorized user to retrieve or create a desired source object SID, the unauthorized user cannot use it to update an account's <strong>sIDHistory</strong> without being a member of the destination Domain Administrators group.</span></span> <span data-ttu-id="08a42-195">因為網域系統管理員成員資格的檢查是以硬式編碼的方式在目標 DC 上進行，所以沒有任何方法可進行磁片修改來變更保護此功能的存取控制資料。</span><span class="sxs-lookup"><span data-stu-id="08a42-195">Because the check, on the destination domain controller, for Domain Administrator membership is hard-coded, on the target DC, there is no method for doing a disk modification to change the access control data protecting this function.</span></span> <span data-ttu-id="08a42-196">在目的地網域中，會審核嘗試複製特洛伊程式的來源帳戶。</span><span class="sxs-lookup"><span data-stu-id="08a42-196">An attempt to clone a Trojan Horse source account is audited in the destination domain.</span></span> <span data-ttu-id="08a42-197">只要針對高度信任的個人保留網域系統管理員群組的成員資格，就可以減輕這種攻擊。</span><span class="sxs-lookup"><span data-stu-id="08a42-197">This attack is mitigated by reserving membership in the Domain Administrators group for only highly trusted individuals.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08a42-198">SID 歷程記錄的磁片修改</span><span class="sxs-lookup"><span data-stu-id="08a42-198">On-disk Modification of SID History</span></span><br/> <span data-ttu-id="08a42-199">具有網域系統管理員認證的複雜未授權使用者，以及對目的地網域中之 DC 的實體存取權，可以修改磁片上的帳戶 <strong>sIDHistory</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="08a42-199">A sophisticated unauthorized user, with Domain Administrator credentials and with physical access to a DC in the destination domain, could modify an account <strong>sIDHistory</strong> value on disk.</span></span><br/></td>
<td><span data-ttu-id="08a42-200">使用 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>不會啟用這項嘗試。</span><span class="sxs-lookup"><span data-stu-id="08a42-200">This attempt is not enabled by use of <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>.</span></span> <span data-ttu-id="08a42-201">這項攻擊的解決方式是防止實體存取所有高度信任的系統管理員以外的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="08a42-201">This attack is mitigated by preventing physical access to domain controllers to all except highly trusted administrators.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08a42-202">用來移除保護的惡意程式碼</span><span class="sxs-lookup"><span data-stu-id="08a42-202">Rogue Code Used to Remove Protections</span></span><br/> <span data-ttu-id="08a42-203">未經授權的使用者或 rogue 系統管理員若具有目錄服務程式碼的實體存取權，就可以建立以下的惡意程式碼：</span><span class="sxs-lookup"><span data-stu-id="08a42-203">An unauthorized user or rogue administrator with physical access to the Directory Service code could create rogue code that:</span></span>
<ol>
<li><span data-ttu-id="08a42-204">移除程式碼中 Domain Administrators 群組的成員資格檢查。</span><span class="sxs-lookup"><span data-stu-id="08a42-204">Removes the check for membership in the Domain Administrators group in the code.</span></span></li>
<li><span data-ttu-id="08a42-205">變更來源網域控制站上的呼叫，將 SID 指向未進行審核的 LookupSidFromName。</span><span class="sxs-lookup"><span data-stu-id="08a42-205">Changes the calls on the source domain controller that points the SID to a LookupSidFromName that is not audited.</span></span></li>
<li><span data-ttu-id="08a42-206">移除 audit log 呼叫。</span><span class="sxs-lookup"><span data-stu-id="08a42-206">Removes audit log calls.</span></span></li>
</ol>
<br/></td>
<td><span data-ttu-id="08a42-207">具有 DS 程式碼實體存取權的人員，以及足以建立 rogue 程式碼的知識，都具有任意修改帳戶 <strong>sIDHistory</strong> 屬性的能力。</span><span class="sxs-lookup"><span data-stu-id="08a42-207">Someone with physical access to the DS code and knowledgeable enough to create rogue code has the capability of arbitrarily modifying the <strong>sIDHistory</strong> attribute of an account.</span></span> <span data-ttu-id="08a42-208"><a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> API 不會增加此安全性風險。</span><span class="sxs-lookup"><span data-stu-id="08a42-208">The <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> API does not increase this security risk.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08a42-209">易受遭竊 Sid 的資源</span><span class="sxs-lookup"><span data-stu-id="08a42-209">Resources Vulnerable to Stolen SIDs</span></span><br/> <span data-ttu-id="08a42-210">如果未經授權的使用者使用這裡所述的其中一種方法來修改帳戶 <strong>sIDHistory</strong>，且感興趣的資源網域信任未經授權的使用者帳戶網域，則未經授權的使用者可能會未經授權存取遭竊的 sid 資源，而不會在 SID 遭竊的帳戶網域中留下審核記錄。</span><span class="sxs-lookup"><span data-stu-id="08a42-210">If an unauthorized user has succeeded in using one of the methods described here to modify an account <strong>sIDHistory</strong>, and if the resource domains of interest trust the unauthorized user account domain, then the unauthorized user can get unauthorized access to the stolen SID's resources, potentially without leaving an audit trail in the account domain from which the SID was stolen.</span></span><br/></td>
<td><span data-ttu-id="08a42-211">資源網域系統管理員只會設定從安全性觀點來合理的信任關係，以保護其資源。</span><span class="sxs-lookup"><span data-stu-id="08a42-211">Resource domain administrators protect their resources by setting up only those trust relationships that make sense from a security perspective.</span></span> <span data-ttu-id="08a42-212">在受信任的目標網域中，使用 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> 受限於網域系統管理員群組的成員，這些成員在其職責範圍內已經有廣泛的許可權。</span><span class="sxs-lookup"><span data-stu-id="08a42-212">Use of <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> is restricted, in the trusted target domain, to members of the Domain Administrators group who already have broad permissions within the scope of their responsibilities.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08a42-213">Rogue 目標網域</span><span class="sxs-lookup"><span data-stu-id="08a42-213">Rogue Target Domain</span></span><br/> <span data-ttu-id="08a42-214">未經授權的使用者建立 Windows 2000 網域，其 <strong>sIDHistory</strong> 包含已從來源網域遭竊的 SID。</span><span class="sxs-lookup"><span data-stu-id="08a42-214">An unauthorized user creates a Windows 2000 domain with an account whose <strong>sIDHistory</strong> contains a SID that has been stolen from a source domain.</span></span> <span data-ttu-id="08a42-215">未經授權的使用者會使用此帳戶來取得資源的未經授權存取權。</span><span class="sxs-lookup"><span data-stu-id="08a42-215">The unauthorized user uses this account for unauthorized access to resources.</span></span><br/></td>
<td><span data-ttu-id="08a42-216">未經授權的使用者需要來源網域的系統管理員認證，才能使用 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>，並在來源網域控制站上保留審核記錄。</span><span class="sxs-lookup"><span data-stu-id="08a42-216">The unauthorized user requires Administrator credentials for the source domain in order to use <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>, and leaves an audit trail on the source domain controller.</span></span> <span data-ttu-id="08a42-217">Rogue 目標網域只會在信任 rogue 網域的其他網域中取得未經授權的存取權，這需要這些資源網域中的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="08a42-217">The rogue target domain gains unauthorized access only in other domains that trust the rogue domain, which requires Administrator privileges in those resource domains.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="operational-constraints"></a><span data-ttu-id="08a42-218">操作條件約束</span><span class="sxs-lookup"><span data-stu-id="08a42-218">Operational Constraints</span></span>

<span data-ttu-id="08a42-219">本節描述使用 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 函式的操作條件約束。</span><span class="sxs-lookup"><span data-stu-id="08a42-219">This section describes the operational constraints of using the [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) function.</span></span>

<span data-ttu-id="08a42-220">*SrcPrincipal* 的 SID 不得存在於目的地樹系中，可做為主要帳戶 SID 或帳戶的 **sIDHistory** 。</span><span class="sxs-lookup"><span data-stu-id="08a42-220">The SID of *SrcPrincipal* must not already exist in the destination forest, either as a primary account SID or in the **sIDHistory** of an account.</span></span> <span data-ttu-id="08a42-221">例外狀況是在嘗試將 SID 新增至包含相同 SID 的 **sIDHistory** 時， [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)不會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="08a42-221">The exception is that [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) does not generate an error when attempting to add a SID to a **sIDHistory** that contains an identical SID.</span></span> <span data-ttu-id="08a42-222">此行為可讓 **DsAddSidHistory** 以相同的輸入執行多次，進而產生成功和一致的結束狀態，以供工具開發人員方便使用。</span><span class="sxs-lookup"><span data-stu-id="08a42-222">This behavior enables **DsAddSidHistory** to be run multiple times with identical input, resulting in success and a consistent end state, for tool developer ease-of-use.</span></span>

> [!Note]  
> <span data-ttu-id="08a42-223">通用類別目錄複寫延遲可能會提供一個視窗，在這段期間可能會建立重複的 Sid。</span><span class="sxs-lookup"><span data-stu-id="08a42-223">Global Catalog replication latency may provide a window during which duplicate SIDs may be created.</span></span> <span data-ttu-id="08a42-224">不過，系統管理員可以輕鬆地刪除重複的 Sid。</span><span class="sxs-lookup"><span data-stu-id="08a42-224">However, duplicate SIDs can be easily deleted by an administrator.</span></span>

 

<span data-ttu-id="08a42-225">*SrcPrincipal* 和 *DstPrincipal* 必須是下列其中一種類型：</span><span class="sxs-lookup"><span data-stu-id="08a42-225">*SrcPrincipal* and *DstPrincipal* must be one of the following types:</span></span>

-   <span data-ttu-id="08a42-226">User</span><span class="sxs-lookup"><span data-stu-id="08a42-226">User</span></span>
-   <span data-ttu-id="08a42-227">啟用安全性的群組，包括：</span><span class="sxs-lookup"><span data-stu-id="08a42-227">Security Enabled Group, including:</span></span>

    <dl> <span data-ttu-id="08a42-228">本機群組</span><span class="sxs-lookup"><span data-stu-id="08a42-228">Local group</span></span>  
    <span data-ttu-id="08a42-229">通用群組</span><span class="sxs-lookup"><span data-stu-id="08a42-229">Global group</span></span>  
    <span data-ttu-id="08a42-230">僅)  (Windows 2000 原生模式的網域本機群組</span><span class="sxs-lookup"><span data-stu-id="08a42-230">Domain local group (Windows 2000 native mode only)</span></span>  
    <span data-ttu-id="08a42-231">萬用群組 (Windows 2000 原生模式) </span><span class="sxs-lookup"><span data-stu-id="08a42-231">Universal group (Windows 2000 native mode only)</span></span>  
    </dl>

<span data-ttu-id="08a42-232">*SrcPrincipal* 和 *DstPrincipal* 的物件類型必須相符。</span><span class="sxs-lookup"><span data-stu-id="08a42-232">The object types of *SrcPrincipal* and *DstPrincipal* must match.</span></span>

-   <span data-ttu-id="08a42-233">如果 *SrcPrincipal* 是使用者， *DstPrincipal* 必須是使用者。</span><span class="sxs-lookup"><span data-stu-id="08a42-233">If *SrcPrincipal* is a User, *DstPrincipal* must be a User.</span></span>
-   <span data-ttu-id="08a42-234">如果 *SrcPrincipal* 是本機或網域本機群組， *DstPrincipal* 必須是網域本機群組。</span><span class="sxs-lookup"><span data-stu-id="08a42-234">If *SrcPrincipal* is a Local or Domain Local Group, *DstPrincipal* must be a Domain Local Group.</span></span>
-   <span data-ttu-id="08a42-235">如果 *SrcPrincipal* 是全域群組或萬用群組， *DstPrincipal* 必須是全域群組或萬用群組。</span><span class="sxs-lookup"><span data-stu-id="08a42-235">If *SrcPrincipal* is a Global or Universal Group, *DstPrincipal* must be a Global or Universal Group.</span></span>

<span data-ttu-id="08a42-236">*SrcPrincipal* 和 *DstPrincipal* 不可以是下列其中一種類型： ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 失敗，並在這些情況下發生錯誤) </span><span class="sxs-lookup"><span data-stu-id="08a42-236">*SrcPrincipal* and *DstPrincipal* cannot be one of the following types: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) fails with an error in these cases)</span></span>

-   <span data-ttu-id="08a42-237">電腦 (工作站或網域控制站) </span><span class="sxs-lookup"><span data-stu-id="08a42-237">Computer (workstation or domain controller)</span></span>
-   <span data-ttu-id="08a42-238">網域間信任</span><span class="sxs-lookup"><span data-stu-id="08a42-238">Inter-domain trust</span></span>
-   <span data-ttu-id="08a42-239">暫時重複的帳戶 (幾乎未使用的功能，這是 LANman 的舊版) </span><span class="sxs-lookup"><span data-stu-id="08a42-239">Temporary duplicate account (virtually unused feature, a legacy of LANman)</span></span>
-   <span data-ttu-id="08a42-240">具有知名 Sid 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="08a42-240">Accounts with Well Known SIDs.</span></span> <span data-ttu-id="08a42-241">已知的 Sid 在每個網域中都相同;因此，將它們新增至 **sIDHistory** 會違反 Windows 2000 樹系的 SID 唯一性需求。</span><span class="sxs-lookup"><span data-stu-id="08a42-241">Well Known SIDs are identical in every domain; thus adding them to a **sIDHistory** would violate the SID uniqueness requirement of a Windows 2000 forest.</span></span> <span data-ttu-id="08a42-242">已知 Sid 的帳戶包含下列本機群組：</span><span class="sxs-lookup"><span data-stu-id="08a42-242">Accounts with Well Known SIDs include the following local groups:</span></span>

    <dl> <span data-ttu-id="08a42-243">Account Operators</span><span class="sxs-lookup"><span data-stu-id="08a42-243">Account operators</span></span>  
    <span data-ttu-id="08a42-244">系統管理員</span><span class="sxs-lookup"><span data-stu-id="08a42-244">Administrators</span></span>  
    <span data-ttu-id="08a42-245">Backup Operators</span><span class="sxs-lookup"><span data-stu-id="08a42-245">Backup operators</span></span>  
    <span data-ttu-id="08a42-246">Guests</span><span class="sxs-lookup"><span data-stu-id="08a42-246">Guests</span></span>  
    <span data-ttu-id="08a42-247">列印運算子</span><span class="sxs-lookup"><span data-stu-id="08a42-247">Print operators</span></span>  
    <span data-ttu-id="08a42-248">Replicator</span><span class="sxs-lookup"><span data-stu-id="08a42-248">Replicator</span></span>  
    <span data-ttu-id="08a42-249">Server Operators</span><span class="sxs-lookup"><span data-stu-id="08a42-249">Server operators</span></span>  
    <span data-ttu-id="08a42-250">使用者</span><span class="sxs-lookup"><span data-stu-id="08a42-250">Users</span></span>  
    </dl>

<span data-ttu-id="08a42-251">如果 *SrcPrincipal* 有已知的相對識別碼 (RID) 和網域專屬的前置詞，也就是網域系統管理員、網域使用者及網域電腦，則 *DstPrincipal* 必須擁有相同的已知 RID，才能讓 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 成功。</span><span class="sxs-lookup"><span data-stu-id="08a42-251">If *SrcPrincipal* has a well-known relative identifier (RID) and a domain specific prefix, that is, Domain Administrators, Domain Users, and Domain Computers, then *DstPrincipal* must possess the same well-known RID in order for [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) to succeed.</span></span> <span data-ttu-id="08a42-252">具有已知 Rid 的帳戶包含下列使用者和全域群組：</span><span class="sxs-lookup"><span data-stu-id="08a42-252">Accounts with well-known RIDs include the following users and global groups:</span></span>

-   <span data-ttu-id="08a42-253">系統管理員</span><span class="sxs-lookup"><span data-stu-id="08a42-253">Administrator</span></span>
-   <span data-ttu-id="08a42-254">來賓</span><span class="sxs-lookup"><span data-stu-id="08a42-254">Guest</span></span>
-   <span data-ttu-id="08a42-255">Domain Administrators</span><span class="sxs-lookup"><span data-stu-id="08a42-255">Domain administrators</span></span>
-   <span data-ttu-id="08a42-256">網域來賓</span><span class="sxs-lookup"><span data-stu-id="08a42-256">Domain guests</span></span>
-   <span data-ttu-id="08a42-257">網域使用者</span><span class="sxs-lookup"><span data-stu-id="08a42-257">Domain users</span></span>

## <a name="setting-the-registry-value"></a><span data-ttu-id="08a42-258">設定登錄值</span><span class="sxs-lookup"><span data-stu-id="08a42-258">Setting the Registry Value</span></span>

<span data-ttu-id="08a42-259">下列程式說明如何設定 TcpipClientSupport 登錄值。</span><span class="sxs-lookup"><span data-stu-id="08a42-259">The following procedure shows how to set the TcpipClientSupport registry value.</span></span>

<span data-ttu-id="08a42-260">**若要設定 TcpipClientSupport 登錄值**</span><span class="sxs-lookup"><span data-stu-id="08a42-260">**To Set the TcpipClientSupport Registry Value**</span></span>

1.  <span data-ttu-id="08a42-261">建立下列登錄值作為 \_ 來源網域控制站上的 REG DWORD 值，並將其值設定為1。</span><span class="sxs-lookup"><span data-stu-id="08a42-261">Create the following registry value as a REG\_DWORD value on the source domain controller and set its value to 1.</span></span>

    <span data-ttu-id="08a42-262">**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ TcpipClientSupport**</span><span class="sxs-lookup"><span data-stu-id="08a42-262">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Lsa\\TcpipClientSupport**</span></span>

2.  <span data-ttu-id="08a42-263">然後，重新開機來源網域控制站。</span><span class="sxs-lookup"><span data-stu-id="08a42-263">Then, restart the source domain controller.</span></span> <span data-ttu-id="08a42-264">此登錄值會導致 SAM 在 TCP/IP 上接聽。</span><span class="sxs-lookup"><span data-stu-id="08a42-264">This registry value causes the SAM to listen on TCP/IP.</span></span> <span data-ttu-id="08a42-265">如果未在來源網域控制站上設定此值， [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)將會失敗。</span><span class="sxs-lookup"><span data-stu-id="08a42-265">[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) will fail if this value is not set on the source domain controller.</span></span>

## <a name="enabling-auditing-of-usergroup-management-events"></a><span data-ttu-id="08a42-266">啟用使用者/群組管理事件的審核</span><span class="sxs-lookup"><span data-stu-id="08a42-266">Enabling Auditing of User/Group Management Events</span></span>

<span data-ttu-id="08a42-267">下列程式說明如何在 Windows 2000 或 Windows Server 2003 來源或目的地網域中啟用使用者/群組管理事件的審核。</span><span class="sxs-lookup"><span data-stu-id="08a42-267">The following procedure shows how to enable auditing of User/Group management events in a Windows 2000 or Windows Server 2003 source or destination domain.</span></span>

<span data-ttu-id="08a42-268">**啟用 Windows 2000 或 Windows Server 2003 來源或目的地網域中的使用者/群組管理事件的審核**</span><span class="sxs-lookup"><span data-stu-id="08a42-268">**To enable auditing of User/Group management events in a Windows 2000 or Windows Server 2003 source or destination domain**</span></span>

1.  <span data-ttu-id="08a42-269">在 Active Directory 消費者和電腦 MMC 嵌入式管理單元中，選取 [目的地網域網域控制站] 容器。</span><span class="sxs-lookup"><span data-stu-id="08a42-269">In the Active Directory Users and Computers MMC Snap-in, select the destination domain Domain Controllers container.</span></span>
2.  <span data-ttu-id="08a42-270">以滑鼠右鍵按一下 [ **網域控制站** ]，然後選擇 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="08a42-270">Right-click **Domain Controllers** and choose **Properties**.</span></span>
3.  <span data-ttu-id="08a42-271">按一下 [ **群組原則** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="08a42-271">Click the **Group Policy** tab.</span></span>
4.  <span data-ttu-id="08a42-272">選取 [ **預設網域控制站原則** ]，然後按一下 [ **編輯**]。</span><span class="sxs-lookup"><span data-stu-id="08a42-272">Select the **Default Domain Controllers Policy** and click **Edit**.</span></span>
5.  <span data-ttu-id="08a42-273">在 [ **電腦 \\ 設定 Windows 設定 \\ 安全性設定 \\ 本機原則 \\ 稽核原則**] 下，按兩下 [ **審核帳戶管理**]。</span><span class="sxs-lookup"><span data-stu-id="08a42-273">Under **Computer Configuration\\Windows Settings\\Security Settings\\Local Policies\\Audit Policy**, double-click **Audit Account Management**.</span></span>
6.  <span data-ttu-id="08a42-274">在 [ **審核帳戶管理** ] 視窗中，選取 [ **成功** ] 和 [ **失敗** ] 審核。</span><span class="sxs-lookup"><span data-stu-id="08a42-274">In the **Audit Account Management** window, select both **Success** and **Failure** auditing.</span></span> <span data-ttu-id="08a42-275">原則更新會在重新開機之後或重新整理之後生效。</span><span class="sxs-lookup"><span data-stu-id="08a42-275">Policy updates take effect after a restart or after a refresh occurs.</span></span>
7.  <span data-ttu-id="08a42-276">藉由在群組原則 MMC 嵌入式管理單元中查看有效稽核原則來確認是否已啟用審核。</span><span class="sxs-lookup"><span data-stu-id="08a42-276">Verify that auditing is enabled by viewing the effective audit policy in the Group Policy MMC Snap-in.</span></span>

<span data-ttu-id="08a42-277">下列程式說明如何在 Windows NT 4.0 網域中啟用使用者/群組管理事件的審核。</span><span class="sxs-lookup"><span data-stu-id="08a42-277">The following procedure shows how to enable auditing of User/Group management events in a Windows NT 4.0 domain.</span></span>

<span data-ttu-id="08a42-278">**啟用 Windows NT 4.0 網域中的使用者/群組管理事件的審核**</span><span class="sxs-lookup"><span data-stu-id="08a42-278">**To enable auditing of User/Group management events in a Windows NT 4.0 domain**</span></span>

1.  <span data-ttu-id="08a42-279">在 [ **網域的使用者管理員**] 中，按一下 [ **原則** ] 功能表，然後選取 [ **Audit**]。</span><span class="sxs-lookup"><span data-stu-id="08a42-279">In **User Manager for Domains**, click the **Policies** menu and select **Audit**.</span></span>
2.  <span data-ttu-id="08a42-280">選取 [ **Audit 這些事件**]。</span><span class="sxs-lookup"><span data-stu-id="08a42-280">Select **Audit These Events**.</span></span>
3.  <span data-ttu-id="08a42-281">針對 **使用者和群組管理**，請檢查 **成功和失敗**。</span><span class="sxs-lookup"><span data-stu-id="08a42-281">For **User and Group Management**, check **Success and Failure**.</span></span>

<span data-ttu-id="08a42-282">下列程式說明如何在 Windows NT 4.0、Windows 2000 或 Windows Server 2003 來源網域中啟用使用者/群組管理事件的審核。</span><span class="sxs-lookup"><span data-stu-id="08a42-282">The following procedure shows how to enable auditing of User/Group management events in a Windows NT 4.0, Windows 2000, or Windows Server 2003 source domain.</span></span>

<span data-ttu-id="08a42-283">**啟用 Windows NT 4.0、Windows 2000 或 Windows Server 2003 來源網域中的使用者/群組管理事件的審核**</span><span class="sxs-lookup"><span data-stu-id="08a42-283">**To enable auditing of User/Group management events in a Windows NT 4.0, Windows 2000, or Windows Server 2003 source domain**</span></span>

1.  <span data-ttu-id="08a42-284">在 [ **網域的使用者管理員**] 中，按一下 [ **使用者** ] 功能表，然後選取 [ **新的本機群組**]。</span><span class="sxs-lookup"><span data-stu-id="08a42-284">In **User Manager for Domains**, click the **User** menu and select **New Local Group**.</span></span>
2.  <span data-ttu-id="08a42-285">輸入由來源網域 NetBIOS 名稱所組成的組名，該名稱會附加三個貨幣符號 ($) ，例如 FABRIKAM $ $ $。</span><span class="sxs-lookup"><span data-stu-id="08a42-285">Enter a group name composed of the source domain NetBIOS name appended with three dollar signs ($), for example, FABRIKAM$$$.</span></span> <span data-ttu-id="08a42-286">[描述] 欄位應該會指出此群組是用來審核 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 或複製作業的使用。</span><span class="sxs-lookup"><span data-stu-id="08a42-286">The description field should indicate that this group is used to audit use of [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) or cloning operations.</span></span> <span data-ttu-id="08a42-287">確定群組中沒有成員。</span><span class="sxs-lookup"><span data-stu-id="08a42-287">Ensure there are no members in the group.</span></span> <span data-ttu-id="08a42-288">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="08a42-288">Click **OK**.</span></span>

<span data-ttu-id="08a42-289">如果未如這裡所述啟用來源和目的地的審核， [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 作業就會失敗。</span><span class="sxs-lookup"><span data-stu-id="08a42-289">The [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) operation fails if source and destination auditing are not enabled as described here.</span></span>

## <a name="set-up-trust-if-required"></a><span data-ttu-id="08a42-290">視需要設定信任</span><span class="sxs-lookup"><span data-stu-id="08a42-290">Set up Trust if Required</span></span>

<span data-ttu-id="08a42-291">如果下列其中一項為 true，就必須從來源網域將信任建立到目的地網域 (這必須發生在不同的樹系) 中：</span><span class="sxs-lookup"><span data-stu-id="08a42-291">If one of the following is true, a trust must be established from the source domain to the destination domain (this must occur in a different forest):</span></span>

-   <span data-ttu-id="08a42-292">來源網域是 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="08a42-292">The source domain is Windows Server 2003.</span></span>
-   <span data-ttu-id="08a42-293">來源網域是 Windows NT 4.0，而 *SrcDomainCreds* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="08a42-293">The source domain is Windows NT 4.0 and *SrcDomainCreds* is **NULL**.</span></span>

 

 





