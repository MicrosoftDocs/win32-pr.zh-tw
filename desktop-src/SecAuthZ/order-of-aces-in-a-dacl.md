---
description: 當進程嘗試存取安全物件時，系統會逐步完成存取控制專案 (Ace) 在物件任意存取控制清單 (DACL) 直到找到允許或拒絕所要求存取權的 Ace 為止。
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: DACL 中的 Ace 順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988293"
---
# <a name="order-of-aces-in-a-dacl"></a><span data-ttu-id="9129f-103">DACL 中的 Ace 順序</span><span class="sxs-lookup"><span data-stu-id="9129f-103">Order of ACEs in a DACL</span></span>

<span data-ttu-id="9129f-104">當 [*進程*](/windows/desktop/SecGloss/p-gly) 嘗試存取安全物件時，系統會逐步執行 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 在物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 中， (DACL) 直到找到允許或拒絕所要求存取權的 ace 為止。</span><span class="sxs-lookup"><span data-stu-id="9129f-104">When a [*process*](/windows/desktop/SecGloss/p-gly) tries to access a securable object, the system steps through the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) until it finds ACEs that allow or deny the requested access.</span></span> <span data-ttu-id="9129f-105">DACL 允許使用者的存取權限會視 DACL 中的 Ace 順序而有所不同。</span><span class="sxs-lookup"><span data-stu-id="9129f-105">The access rights that a DACL allows a user could vary depending on the order of ACEs in the DACL.</span></span> <span data-ttu-id="9129f-106">因此，Windows XP 作業系統會在安全物件的 DACL 中定義 Ace 的慣用順序。</span><span class="sxs-lookup"><span data-stu-id="9129f-106">Consequently, the Windows XP operating system defines a preferred order for ACEs in the DACL of a securable object.</span></span> <span data-ttu-id="9129f-107">慣用的順序提供簡單的架構，可確保拒絕存取的 ACE 實際上會拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="9129f-107">The preferred order provides a simple framework that ensures that an access-denied ACE actually denies access.</span></span> <span data-ttu-id="9129f-108">如需有關檢查存取權之系統演算法的詳細資訊，請參閱 [Dacl 如何控制物件的存取權](how-dacls-control-access-to-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="9129f-108">For more information about the system's algorithm for checking access, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="9129f-109">在 Windows Server 2003 和 Windows XP 中，Ace 的正確順序很複雜，因為引進了物件特有的 Ace 和自動繼承。</span><span class="sxs-lookup"><span data-stu-id="9129f-109">For Windows Server 2003 and Windows XP, the proper order of ACEs is complicated by the introduction of object-specific ACEs and automatic inheritance.</span></span>

<span data-ttu-id="9129f-110">下列步驟說明慣用的順序：</span><span class="sxs-lookup"><span data-stu-id="9129f-110">The following steps describe the preferred order:</span></span>

1.  <span data-ttu-id="9129f-111">所有明確的 Ace 都會放在群組中任何繼承的 Ace 之前。</span><span class="sxs-lookup"><span data-stu-id="9129f-111">All explicit ACEs are placed in a group before any inherited ACEs.</span></span>
2.  <span data-ttu-id="9129f-112">在明確的 Ace 群組內，會在允許存取的 Ace 之前放置拒絕存取的 Ace。</span><span class="sxs-lookup"><span data-stu-id="9129f-112">Within the group of explicit ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>
3.  <span data-ttu-id="9129f-113">繼承的 Ace 會以繼承的 Ace 順序放置。</span><span class="sxs-lookup"><span data-stu-id="9129f-113">Inherited ACEs are placed in the order in which they are inherited.</span></span> <span data-ttu-id="9129f-114">從子物件的父系繼承的 Ace 會優先，然後是繼承自祖系的 Ace，依此類推物件的樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="9129f-114">ACEs inherited from the child object's parent come first, then ACEs inherited from the grandparent, and so on up the tree of objects.</span></span>
4.  <span data-ttu-id="9129f-115">針對每個繼承的 Ace 層級，會在允許存取的 Ace 之前放置拒絕存取的 Ace。</span><span class="sxs-lookup"><span data-stu-id="9129f-115">For each level of inherited ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>

<span data-ttu-id="9129f-116">當然，ACL 中並非所有 ACE 類型都是必要的。</span><span class="sxs-lookup"><span data-stu-id="9129f-116">Of course, not all ACE types are required in an ACL.</span></span>

<span data-ttu-id="9129f-117">[**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex)和 [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace)之類的函式會將 ACE 新增至 ACL 的結尾。</span><span class="sxs-lookup"><span data-stu-id="9129f-117">Functions such as [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) and [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) add an ACE to the end of an ACL.</span></span> <span data-ttu-id="9129f-118">呼叫端必須負責確保以正確的順序加入 Ace。</span><span class="sxs-lookup"><span data-stu-id="9129f-118">It is the caller's responsibility to ensure that the ACEs are added in the proper order.</span></span>

 

 
