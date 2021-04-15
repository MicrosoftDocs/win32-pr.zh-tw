---
description: WMI 依賴標準的 Windows 安全描述項來控制及保護對安全物件的存取，例如 WMI 命名空間、印表機、服務和 DCOM 應用程式。
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: 存取 WMI 安全物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194716"
---
# <a name="access-to-wmi-securable-objects"></a><span data-ttu-id="a7d64-103">存取 WMI 安全物件</span><span class="sxs-lookup"><span data-stu-id="a7d64-103">Access to WMI Securable Objects</span></span>

<span data-ttu-id="a7d64-104">WMI 依賴標準的 Windows [*安全描述項*](/windows/desktop/SecGloss/s-gly) 來控制及保護對安全物件的存取，例如 WMI 命名空間、印表機、服務和 DCOM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a7d64-104">WMI relies on standard Windows [*security descriptors*](/windows/desktop/SecGloss/s-gly) to control and protect access to securable objects like WMI namespaces, printers, services, and DCOM applications.</span></span> <span data-ttu-id="a7d64-105">如需詳細資訊，請參閱 [WMI 命名空間的存取](access-to-wmi-namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="a7d64-105">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="a7d64-106">本節將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="a7d64-106">The following topics are discussed in this section:</span></span>

-   [<span data-ttu-id="a7d64-107">安全描述項和 Sid</span><span class="sxs-lookup"><span data-stu-id="a7d64-107">Security Descriptors and SIDs</span></span>](#security-descriptors-and-sids)
-   [<span data-ttu-id="a7d64-108">存取控制</span><span class="sxs-lookup"><span data-stu-id="a7d64-108">Access Control</span></span>](#access-control)
-   [<span data-ttu-id="a7d64-109">變更存取安全性</span><span class="sxs-lookup"><span data-stu-id="a7d64-109">Changing Access Security</span></span>](#changing-access-security)
-   [<span data-ttu-id="a7d64-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7d64-110">Related topics</span></span>](#related-topics)

## <a name="security-descriptors-and-sids"></a><span data-ttu-id="a7d64-111">安全描述項和 Sid</span><span class="sxs-lookup"><span data-stu-id="a7d64-111">Security Descriptors and SIDs</span></span>

<span data-ttu-id="a7d64-112">WMI 會使用物件的安全描述項來比較嘗試存取安全物件的使用者 [*存取權杖*](/windows/desktop/SecGloss/a-gly) ，以維護存取安全性。</span><span class="sxs-lookup"><span data-stu-id="a7d64-112">WMI maintains access security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user that attempts to access a securable object with the security descriptor of the object.</span></span>

<span data-ttu-id="a7d64-113">在系統上建立使用者或群組時，系統會將 [*(sid 的安全識別碼*](/windows/desktop/SecGloss/s-gly) 提供給帳戶，) sid 可確保使用與先前刪除之帳戶同名的帳戶，不會繼承先前的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="a7d64-113">When a user or group is created on a system, the account is given a [*security identifier (SID)*](/windows/desktop/SecGloss/s-gly) The SID ensures that an account created with the same name as a previously deleted account does not inherit the previous security settings.</span></span> <span data-ttu-id="a7d64-114">存取權杖的建立方式是結合 SID、使用者所屬群組的清單，以及啟用或停用的許可權清單。</span><span class="sxs-lookup"><span data-stu-id="a7d64-114">An access token is created by combining the SID, the list of groups of which the user is a member, and the list of enabled or disabled privileges.</span></span> <span data-ttu-id="a7d64-115">這些權杖會指派給使用者所擁有的所有進程和執行緒。</span><span class="sxs-lookup"><span data-stu-id="a7d64-115">These tokens are assigned to all processes and threads owned by the user.</span></span>

## <a name="access-control"></a><span data-ttu-id="a7d64-116">存取控制</span><span class="sxs-lookup"><span data-stu-id="a7d64-116">Access Control</span></span>

<span data-ttu-id="a7d64-117">當使用者想要使用受保護的物件時，存取權杖會與物件之安全描述項中 [*(DACL) 的任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 進行比較。</span><span class="sxs-lookup"><span data-stu-id="a7d64-117">When the user wants to use a secured object, the access token is compared with the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) in the security descriptor on the object.</span></span> <span data-ttu-id="a7d64-118">DACL 包含稱為 [*存取控制專案 (ACE)*](/windows/desktop/SecGloss/a-gly)的許可權。</span><span class="sxs-lookup"><span data-stu-id="a7d64-118">The DACL contains permissions called [*access control entries (ACE)*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="a7d64-119">[*系統存取控制清單 (SACL)*](/windows/desktop/SecGloss/s-gly) 進行與 dacl 相同的動作，但可以產生安全性審核事件。</span><span class="sxs-lookup"><span data-stu-id="a7d64-119">[*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) do the same thing as DACLs, but can generate security audit events.</span></span> <span data-ttu-id="a7d64-120">從 Windows Vista 開始，WMI 可以在 Windows 安全性記錄檔中建立審核專案。</span><span class="sxs-lookup"><span data-stu-id="a7d64-120">Starting with Windows Vista, WMI can make auditing entries in the Windows Security Log.</span></span> <span data-ttu-id="a7d64-121">如需有關在 WMI 中進行審核的詳細資訊，請參閱 [Wmi 命名空間的存取](access-to-wmi-namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="a7d64-121">For more information about auditing in WMI, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="a7d64-122">DACL 和 SACL 都包含一份 Ace 清單，說明哪些使用者具有特定存取權限，包括寫入 WMI 存放庫、遠端存取和執行，以及登入許可權。</span><span class="sxs-lookup"><span data-stu-id="a7d64-122">Both the DACL and the SACL consist of a list of ACEs that describe which users have specific access rights, including writing to the WMI repository, remote access and execution, and logon permissions.</span></span> <span data-ttu-id="a7d64-123">WMI 會將這些 Acl 儲存在 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="a7d64-123">WMI stores these ACLs in the WMI repository.</span></span>

<span data-ttu-id="a7d64-124">Ace 具有三種類型的存取層級或授與/拒絕許可權：允許、拒絕 DACL，以及) Sacl 的系統審核 (。</span><span class="sxs-lookup"><span data-stu-id="a7d64-124">ACEs hold three types of access levels or grant/deny rights: allow, deny for DACL, and system audit (for SACLs).</span></span> <span data-ttu-id="a7d64-125">拒絕 Ace 在 DACL 或 SACL 中允許 Ace 之前。</span><span class="sxs-lookup"><span data-stu-id="a7d64-125">Deny ACEs precede allow ACEs in the DACL or SACL.</span></span> <span data-ttu-id="a7d64-126">檢查使用者存取權限時，WMI 會透過存取控制清單連續執行，直到找到適用于要求存取權杖的允許 ACE 為止。</span><span class="sxs-lookup"><span data-stu-id="a7d64-126">When checking the user access rights, WMI runs consecutively through the access control list until it finds an allow ACE that applies to the requesting access token.</span></span> <span data-ttu-id="a7d64-127">在此時間點之後不會檢查剩餘的 Ace。</span><span class="sxs-lookup"><span data-stu-id="a7d64-127">The remaining ACEs are not checked after this point.</span></span> <span data-ttu-id="a7d64-128">如果找不到適當的 allow ACE，則會拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a7d64-128">If no appropriate allow ACE is found, then access is denied.</span></span> <span data-ttu-id="a7d64-129">如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) 和 [建立 DACL](/windows/desktop/SecBP/creating-a-dacl)。</span><span class="sxs-lookup"><span data-stu-id="a7d64-129">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) and [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

## <a name="changing-access-security"></a><span data-ttu-id="a7d64-130">變更存取安全性</span><span class="sxs-lookup"><span data-stu-id="a7d64-130">Changing Access Security</span></span>

<span data-ttu-id="a7d64-131">使用適當的許可權，您可以使用腳本或應用程式來變更安全物件的安全性。</span><span class="sxs-lookup"><span data-stu-id="a7d64-131">With appropriate permissions, you can change the security on a securable object with a script or application.</span></span> <span data-ttu-id="a7d64-132">您也可以使用 [*Wmi 控制項*](gloss-w.md)來變更 wmi 命名空間上的安全性設定，或在定義命名空間類別的 [*受控物件格式 (MOF)*](gloss-m.md)檔中加入 [安全描述項定義語言 (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)字串。</span><span class="sxs-lookup"><span data-stu-id="a7d64-132">You can also change the security settings on WMI namespaces using the [*WMI Control*](gloss-w.md) or by adding a [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) string in the [*Managed Object Format (MOF)*](gloss-m.md) file that defines classes for the namespace.</span></span> <span data-ttu-id="a7d64-133">如需詳細資訊，請參閱 [存取 Wmi 命名空間](access-to-wmi-namespaces.md)、 [保護 wmi 命名空間](securing-wmi-namespaces.md)，以及 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="a7d64-133">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md), [Securing WMI Namespaces](securing-wmi-namespaces.md), and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7d64-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7d64-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7d64-135">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="a7d64-135">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="a7d64-136">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="a7d64-136">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="a7d64-137">使用者帳戶控制和 WMI</span><span class="sxs-lookup"><span data-stu-id="a7d64-137">User Account Control and WMI</span></span>](user-account-control-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="a7d64-138">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="a7d64-138">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="a7d64-139">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="a7d64-139">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
