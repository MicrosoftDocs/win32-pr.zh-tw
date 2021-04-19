---
description: 存取控制專案 (ACE) 是存取控制清單中 (ACL) 的元素。
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: 存取控制專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986882"
---
# <a name="access-control-entries"></a><span data-ttu-id="609ae-103">存取控制專案</span><span class="sxs-lookup"><span data-stu-id="609ae-103">Access Control Entries</span></span>

<span data-ttu-id="609ae-104">[*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ACE) 是 [*存取控制清單*](/windows/desktop/SecGloss/a-gly)中 (ACL) 的元素。</span><span class="sxs-lookup"><span data-stu-id="609ae-104">An [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) is an element in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span> <span data-ttu-id="609ae-105">ACL 可以有零或多個 Ace。</span><span class="sxs-lookup"><span data-stu-id="609ae-105">An ACL can have zero or more ACEs.</span></span> <span data-ttu-id="609ae-106">每個 ACE 都會控制或監視指定之受信任者對物件的存取。</span><span class="sxs-lookup"><span data-stu-id="609ae-106">Each ACE controls or monitors access to an object by a specified trustee.</span></span> <span data-ttu-id="609ae-107">如需有關在物件 Acl 中新增、移除或變更 Ace 的詳細資訊，請參閱 [使用 c + + 修改物件的 acl](modifying-the-acls-of-an-object-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="609ae-107">For information about adding, removing, or changing the ACEs in an object's ACLs, see [Modifying the ACLs of an Object in C++](modifying-the-acls-of-an-object-in-c--.md).</span></span>

<span data-ttu-id="609ae-108">Ace 有六種類型，所有安全物件都支援這三種類型。</span><span class="sxs-lookup"><span data-stu-id="609ae-108">There are six types of ACEs, three of which are supported by all securable objects.</span></span> <span data-ttu-id="609ae-109">其他三種類型是目錄服務物件所支援的 [特定物件 ace](object-specific-aces.md) 。</span><span class="sxs-lookup"><span data-stu-id="609ae-109">The other three types are [Object-specific ACEs](object-specific-aces.md) supported by directory service objects.</span></span>

<span data-ttu-id="609ae-110">所有類型的 Ace 都包含下列存取控制資訊：</span><span class="sxs-lookup"><span data-stu-id="609ae-110">All types of ACEs contain the following access control information:</span></span>

-   <span data-ttu-id="609ae-111"> (SID) 的 [安全識別碼](security-identifiers.md) ，可識別套用 ACE 的 [信任者](trustees.md) 。</span><span class="sxs-lookup"><span data-stu-id="609ae-111">A [security identifier](security-identifiers.md) (SID) that identifies the [trustee](trustees.md) to which the ACE applies.</span></span>
-   <span data-ttu-id="609ae-112">[*存取遮罩*](/windows/desktop/SecGloss/a-gly)，指定由 ACE 控制的 [存取權限](access-rights-and-access-masks.md)。</span><span class="sxs-lookup"><span data-stu-id="609ae-112">An [*access mask*](/windows/desktop/SecGloss/a-gly) that specifies the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span>
-   <span data-ttu-id="609ae-113">指出 ACE 類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="609ae-113">A flag that indicates the type of ACE.</span></span>
-   <span data-ttu-id="609ae-114">一組位旗標，可決定子容器或物件是否可以從附加 ACL 的主要物件繼承 ACE。</span><span class="sxs-lookup"><span data-stu-id="609ae-114">A set of bit flags that determine whether child containers or objects can inherit the ACE from the primary object to which the ACL is attached.</span></span>

<span data-ttu-id="609ae-115">下表列出所有安全物件所支援的三種 ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="609ae-115">The following table lists the three ACE types supported by all securable objects.</span></span>



| <span data-ttu-id="609ae-116">類型</span><span class="sxs-lookup"><span data-stu-id="609ae-116">Type</span></span>               | <span data-ttu-id="609ae-117">Description</span><span class="sxs-lookup"><span data-stu-id="609ae-117">Description</span></span>                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="609ae-118">拒絕存取的 ACE</span><span class="sxs-lookup"><span data-stu-id="609ae-118">Access-denied ACE</span></span>  | <span data-ttu-id="609ae-119">用於 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，以拒絕信任者的存取權限。</span><span class="sxs-lookup"><span data-stu-id="609ae-119">Used in a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) to deny access rights to a trustee.</span></span>                                       |
| <span data-ttu-id="609ae-120">存取-允許的 ACE</span><span class="sxs-lookup"><span data-stu-id="609ae-120">Access-allowed ACE</span></span> | <span data-ttu-id="609ae-121">在 DACL 中用來允許信任者的存取權限。</span><span class="sxs-lookup"><span data-stu-id="609ae-121">Used in a DACL to allow access rights to a trustee.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="609ae-122">系統-audit ACE</span><span class="sxs-lookup"><span data-stu-id="609ae-122">System-audit ACE</span></span>   | <span data-ttu-id="609ae-123">用於 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) 在信任者嘗試執行指定的存取權限時，產生審核記錄。</span><span class="sxs-lookup"><span data-stu-id="609ae-123">Used in a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) to generate an audit record when the trustee attempts to exercise the specified access rights.</span></span> |



 

<span data-ttu-id="609ae-124">如需物件特定 Ace 的表格，請參閱 [物件特定的 ace](object-specific-aces.md)。</span><span class="sxs-lookup"><span data-stu-id="609ae-124">For a table of object-specific ACEs, see [Object-specific ACEs](object-specific-aces.md).</span></span>

> [!Note]  
> <span data-ttu-id="609ae-125">目前不支援系統警示物件 Ace。</span><span class="sxs-lookup"><span data-stu-id="609ae-125">System-alarm object ACEs are not currently supported.</span></span>

 

 

 
