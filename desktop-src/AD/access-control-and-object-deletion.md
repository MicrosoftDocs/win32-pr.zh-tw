---
title: 存取控制和物件刪除
description: Active Directory 可讓您刪除物件，如果您有權刪除對物件或 ADS 的存取權，您可以刪除 \_ \_ \_ \_ 父容器上物件類型的子系。
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- 存取控制和物件刪除 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681626"
---
# <a name="access-control-and-object-deletion"></a><span data-ttu-id="36939-104">存取控制和物件刪除</span><span class="sxs-lookup"><span data-stu-id="36939-104">Access Control and Object Deletion</span></span>

<span data-ttu-id="36939-105">如果您有下列其中一個存取權限，Active Directory Domain Services 可讓您刪除物件：</span><span class="sxs-lookup"><span data-stu-id="36939-105">Active Directory Domain Services enable you to delete an object if you have one of the following access rights:</span></span>

-   <span data-ttu-id="36939-106">刪除物件本身的存取權</span><span class="sxs-lookup"><span data-stu-id="36939-106">DELETE access to the object itself</span></span>
-   <span data-ttu-id="36939-107">ADS \_ RIGHT \_ DS \_ \_ 會刪除父容器上該物件類型的子存取</span><span class="sxs-lookup"><span data-stu-id="36939-107">ADS\_RIGHT\_DS\_DELETE\_CHILD access for that object type on the parent container</span></span>

<span data-ttu-id="36939-108">請注意，系統會在拒絕刪除之前，先驗證物件及其父系的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="36939-108">Be aware that the system verifies the security descriptor for both the object and its parent before denying the deletion.</span></span> <span data-ttu-id="36939-109">這表示如果使用者已刪除父系的子系存取權，則明確拒絕使用者刪除存取權的 ACE 將沒有任何作用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36939-109">This means that an ACE that explicitly denies DELETE access to a user has no effect if the user has DELETE\_CHILD access on the parent.</span></span> <span data-ttu-id="36939-110">同樣地， \_ 如果物件本身允許刪除存取權，就可以覆寫在父系上拒絕刪除子存取的 ACE。</span><span class="sxs-lookup"><span data-stu-id="36939-110">Similarly, an ACE that denies DELETE\_CHILD access on the parent can be overridden if DELETE access is allowed on the object itself.</span></span>

<span data-ttu-id="36939-111">若要執行樹狀結構刪除作業（例如使用 [**IADsDeleteOps：:D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) 方法），您必須擁有 \_ \_ \_ 該物件的 ADS 正確 DS 刪除 \_ 樹狀結構存取權。</span><span class="sxs-lookup"><span data-stu-id="36939-111">To perform a tree-delete operation, for example using the [**IADsDeleteOps::DeleteObject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) method, you must have ADS\_RIGHT\_DS\_DELETE\_TREE access to the object.</span></span> <span data-ttu-id="36939-112">如果您有這個存取權限，就可以刪除該物件和任何子物件，不論子物件上的保護為何。</span><span class="sxs-lookup"><span data-stu-id="36939-112">If you have this access right, you can delete the object and any child objects regardless of the protections on the child objects.</span></span> <span data-ttu-id="36939-113">如果您沒有 ADS \_ RIGHT DS delete tree 存取權來刪除樹狀結構 \_ \_ \_ ，則必須以遞迴方式跨越樹狀結構，並個別刪除每個物件。</span><span class="sxs-lookup"><span data-stu-id="36939-113">To delete a tree if you do not have ADS\_RIGHT\_DS\_DELETE\_TREE access, you must recursively traverse the tree, deleting each object individually.</span></span> <span data-ttu-id="36939-114">在此情況下，您必須對樹狀結構中的每個物件具有必要的刪除或刪除 \_ 子存取權。</span><span class="sxs-lookup"><span data-stu-id="36939-114">In this case, you must have the necessary DELETE or DELETE\_CHILD access for each object in the tree.</span></span>

> [!WARNING]
> <span data-ttu-id="36939-115">如果使用者的 ADS 具有 \_ 適當的 \_ DS \_ 刪除 \_ 樹狀結構存取權，這讓他們能夠刪除整個子樹，包括所有子物件。</span><span class="sxs-lookup"><span data-stu-id="36939-115">If users have ADS\_RIGHT\_DS\_DELETE\_TREE access for an object, this gives them the ability to delete a whole subtree, including all child objects.</span></span> <span data-ttu-id="36939-116">基於這個理由，您可以考慮撤銷父容器上所有使用者的「刪除子樹」存取權限。</span><span class="sxs-lookup"><span data-stu-id="36939-116">For this reason, you may consider revoking "Delete Subtree" access permission for all users on a parent container.</span></span>

 

 

 