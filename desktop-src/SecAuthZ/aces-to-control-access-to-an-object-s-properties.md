---
description: 用來控制物件屬性存取權的 Ace
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: 用來控制物件屬性存取權的 Ace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192436"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a><span data-ttu-id="c7a50-103">用來控制物件屬性存取權的 Ace</span><span class="sxs-lookup"><span data-stu-id="c7a50-103">ACEs to Control Access to an Object's Properties</span></span>

<span data-ttu-id="c7a50-104">目錄服務的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL)  (DS) 物件可以包含 (ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 階層，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c7a50-104">The [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of a directory service (DS) object can contain a hierarchy of [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), as follows:</span></span>

1.  <span data-ttu-id="c7a50-105">保護物件本身的 Ace</span><span class="sxs-lookup"><span data-stu-id="c7a50-105">ACEs that protect the object itself</span></span>
2.  <span data-ttu-id="c7a50-106">保護物件上指定之屬性集的[特定物件 ace](object-specific-aces.md)</span><span class="sxs-lookup"><span data-stu-id="c7a50-106">[Object-specific ACEs](object-specific-aces.md) that protect a specified property set on the object</span></span>
3.  <span data-ttu-id="c7a50-107">保護物件上指定之屬性的物件特定 Ace</span><span class="sxs-lookup"><span data-stu-id="c7a50-107">Object-specific ACEs that protect a specified property on the object</span></span>

<span data-ttu-id="c7a50-108">在此階層中，在較高層級授與或拒絕的許可權也適用于較低層級。</span><span class="sxs-lookup"><span data-stu-id="c7a50-108">Within this hierarchy, the rights granted or denied at a higher level apply also to the lower levels.</span></span> <span data-ttu-id="c7a50-109">例如，如果屬性集上的特定物件 ACE 允許信任者的 ADS \_ right \_ DS \_ 讀取配置 \_ ，則信任者對該屬性集的所有屬性具有隱含的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="c7a50-109">For example, if an object-specific ACE on a property set allows a trustee the ADS\_RIGHT\_DS\_READ\_PROP right, the trustee has implicit read access to all of the properties of that property set.</span></span> <span data-ttu-id="c7a50-110">同樣地，物件本身上的 ACE （可讓 ADS 使用 \_ 正確的 \_ DS \_ 讀取 \_ 屬性存取）可讓受信任者讀取所有物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a50-110">Similarly, an ACE on the object itself that allows ADS\_RIGHT\_DS\_READ\_PROP access gives the trustee read access to all of the object's properties.</span></span>

<span data-ttu-id="c7a50-111">下圖顯示假設 DS 物件及其屬性集和屬性的樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="c7a50-111">The following illustration shows the tree of a hypothetical DS object and its property sets and properties.</span></span>

![目錄服務物件階層](images/accctrl2.png)

<span data-ttu-id="c7a50-113">假設您想要允許下列存取此 DS 物件的屬性：</span><span class="sxs-lookup"><span data-stu-id="c7a50-113">Suppose you want to allow the following access to the properties of this DS object:</span></span>

-   <span data-ttu-id="c7a50-114">允許群組所有物件屬性的讀取/寫入權限</span><span class="sxs-lookup"><span data-stu-id="c7a50-114">Allow Group A read/write permission to all of the object's properties</span></span>
-   <span data-ttu-id="c7a50-115">允許其他人讀取/寫入所有屬性（屬性 D 除外）的許可權</span><span class="sxs-lookup"><span data-stu-id="c7a50-115">Allow everyone else read/write permission to all properties except Property D</span></span>

<span data-ttu-id="c7a50-116">若要這樣做，請在物件的 DACL 中設定 Ace，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="c7a50-116">To do this, set the ACEs in the object's DACL as shown in the following table.</span></span>



| <span data-ttu-id="c7a50-117">受託 人</span><span class="sxs-lookup"><span data-stu-id="c7a50-117">Trustee</span></span>  | <span data-ttu-id="c7a50-118">物件 GUID</span><span class="sxs-lookup"><span data-stu-id="c7a50-118">Object GUID</span></span>    | <span data-ttu-id="c7a50-119">ACE 類型</span><span class="sxs-lookup"><span data-stu-id="c7a50-119">ACE type</span></span>                  | <span data-ttu-id="c7a50-120">存取權限</span><span class="sxs-lookup"><span data-stu-id="c7a50-120">Access rights</span></span>                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c7a50-121">群組 A</span><span class="sxs-lookup"><span data-stu-id="c7a50-121">Group A</span></span>  | <span data-ttu-id="c7a50-122">無</span><span class="sxs-lookup"><span data-stu-id="c7a50-122">None</span></span>           | <span data-ttu-id="c7a50-123">存取-允許的 ACE</span><span class="sxs-lookup"><span data-stu-id="c7a50-123">Access-allowed ACE</span></span>        | <span data-ttu-id="c7a50-124">ADS \_ 正確 \_ 的 \_ DS \_ 讀取 \| \_ 目錄廣告正確的 \_ DS \_ 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="c7a50-124">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="c7a50-125">所有人</span><span class="sxs-lookup"><span data-stu-id="c7a50-125">Everyone</span></span> | <span data-ttu-id="c7a50-126">屬性集1</span><span class="sxs-lookup"><span data-stu-id="c7a50-126">Property Set 1</span></span> | <span data-ttu-id="c7a50-127">存取-允許的物件 ACE</span><span class="sxs-lookup"><span data-stu-id="c7a50-127">Access-allowed object ACE</span></span> | <span data-ttu-id="c7a50-128">ADS \_ 正確 \_ 的 \_ DS \_ 讀取 \| \_ 目錄廣告正確的 \_ DS \_ 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="c7a50-128">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="c7a50-129">所有人</span><span class="sxs-lookup"><span data-stu-id="c7a50-129">Everyone</span></span> | <span data-ttu-id="c7a50-130">屬性 C</span><span class="sxs-lookup"><span data-stu-id="c7a50-130">Property C</span></span>     | <span data-ttu-id="c7a50-131">存取-允許的物件 ACE</span><span class="sxs-lookup"><span data-stu-id="c7a50-131">Access-allowed object ACE</span></span> | <span data-ttu-id="c7a50-132">ADS \_ 正確 \_ 的 \_ DS \_ 讀取 \| \_ 目錄廣告正確的 \_ DS \_ 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="c7a50-132">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |



 

<span data-ttu-id="c7a50-133">群組 A 的 ACE 沒有物件 GUID，這表示它允許存取所有物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a50-133">The ACE for Group A does not have an object GUID, which means that it allows access to all the object's properties.</span></span> <span data-ttu-id="c7a50-134">屬性集1的物件特定 ACE 可讓每個人都能存取屬性 A 和 B。其他特定物件 ACE 可讓每個人都能存取屬性 C。請注意，雖然這個 DACL 沒有任何拒絕存取的 Ace，但是它會隱含地拒絕屬性 D 存取群組 A 以外的所有人。</span><span class="sxs-lookup"><span data-stu-id="c7a50-134">The object-specific ACE for Property Set 1 allows everyone access to Properties A and B. The other object-specific ACE allows everyone access to Property C. Note that although this DACL does not have any access-denied ACEs, it implicitly denies Property D access to everyone except Group A.</span></span>

<span data-ttu-id="c7a50-135">當使用者嘗試存取物件的屬性時，系統會依序檢查 Ace，直到明確授與、拒絕要求的存取權，或沒有其他 Ace 為止（在這種情況下，會隱含拒絕存取）。</span><span class="sxs-lookup"><span data-stu-id="c7a50-135">When a user tries to access an object's property, the system checks the ACEs, in order, until the requested access is explicitly granted, denied, or there are no more ACEs, in which case, access is implicitly denied.</span></span>

<span data-ttu-id="c7a50-136">系統會評估：</span><span class="sxs-lookup"><span data-stu-id="c7a50-136">The system evaluates:</span></span>

-   <span data-ttu-id="c7a50-137">套用至物件本身的 Ace</span><span class="sxs-lookup"><span data-stu-id="c7a50-137">ACEs that apply to the object itself</span></span>
-   <span data-ttu-id="c7a50-138">套用至屬性集的物件特定 Ace，其中包含正在存取的屬性</span><span class="sxs-lookup"><span data-stu-id="c7a50-138">Object-specific ACEs that apply to the property set that contains the property being accessed</span></span>
-   <span data-ttu-id="c7a50-139">套用至所存取屬性的特定物件 Ace</span><span class="sxs-lookup"><span data-stu-id="c7a50-139">Object-specific ACEs that apply to the property being accessed</span></span>

<span data-ttu-id="c7a50-140">系統會忽略適用于其他屬性集或屬性的物件特定 Ace。</span><span class="sxs-lookup"><span data-stu-id="c7a50-140">The system ignores object-specific ACEs that apply to other property sets or properties.</span></span>

 

 
