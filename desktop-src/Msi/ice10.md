---
description: ICE10 會驗證子功能的通告狀態是否符合其父項功能的狀態。
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979902"
---
# <a name="ice10"></a><span data-ttu-id="2a51b-103">ICE10</span><span class="sxs-lookup"><span data-stu-id="2a51b-103">ICE10</span></span>

<span data-ttu-id="2a51b-104">ICE10 會驗證子功能的通告狀態是否符合其父項功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a51b-104">ICE10 validates that the advertise state of child features matches that of its parent feature.</span></span>

<span data-ttu-id="2a51b-105">子功能可能不允許廣告，但其父功能允許廣告。</span><span class="sxs-lookup"><span data-stu-id="2a51b-105">A child feature may not disallow advertisement while its parent feature allows advertisement.</span></span> <span data-ttu-id="2a51b-106">因此，父系和子屬性的下列組合是不正確。</span><span class="sxs-lookup"><span data-stu-id="2a51b-106">The following combination of parent and child attributes is therefore invalid.</span></span>

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

<span data-ttu-id="2a51b-107">這種組合無效，因為它會在每次應通告父系時關閉父系。</span><span class="sxs-lookup"><span data-stu-id="2a51b-107">This combination is invalid because it would turn off the parent whenever the parent was supposed to be advertised.</span></span> <span data-ttu-id="2a51b-108">不過，允許反向。</span><span class="sxs-lookup"><span data-stu-id="2a51b-108">However, the reverse is allowed.</span></span> <span data-ttu-id="2a51b-109">當父系標示為不允許公告時，可以將子系標示為優先使用公告。</span><span class="sxs-lookup"><span data-stu-id="2a51b-109">A child can be marked to favor advertisement while the parent is marked to disallow advertisement.</span></span>

<span data-ttu-id="2a51b-110">ICE10 自訂動作會從 [功能](feature-table.md) 資料表的 [屬性] 資料行中，決定父項和子功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a51b-110">The ICE10 custom action determines the state of parent and child features from the Attributes column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="2a51b-111">請注意，將功能的狀態設定為0，並將其父系或子系設定為偏好或不允許公告是有效的。</span><span class="sxs-lookup"><span data-stu-id="2a51b-111">Note that it is valid to set the state of a feature to 0 and have its parent or child set to favor or disallow advertisement.</span></span>

## <a name="result"></a><span data-ttu-id="2a51b-112">結果</span><span class="sxs-lookup"><span data-stu-id="2a51b-112">Result</span></span>

<span data-ttu-id="2a51b-113">如果 [功能](feature-table.md) 資料表的 [屬性] 資料行包含 [公告] 狀態的不符，ICE10 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="2a51b-113">ICE10 posts an error if the Attributes column of the [Feature](feature-table.md) table contains a mismatch in the advertise state.</span></span>

## <a name="example"></a><span data-ttu-id="2a51b-114">範例</span><span class="sxs-lookup"><span data-stu-id="2a51b-114">Example</span></span>

<span data-ttu-id="2a51b-115">ICE10 會針對所顯示的範例張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2a51b-115">ICE10 posts the following error message for the example shown.</span></span>

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

<span data-ttu-id="2a51b-116">請注意，在此範例中，Microsoft Excel 和 Microsoft Word 是 Microsoft Office 的子功能。</span><span class="sxs-lookup"><span data-stu-id="2a51b-116">Note for this example that Microsoft Excel and Microsoft Word are child features of Microsoft Office.</span></span>

<span data-ttu-id="2a51b-117">[功能](feature-table.md) 表 (部分) </span><span class="sxs-lookup"><span data-stu-id="2a51b-117">[Feature](feature-table.md) table (partial)</span></span>



| <span data-ttu-id="2a51b-118">功能</span><span class="sxs-lookup"><span data-stu-id="2a51b-118">Feature</span></span> | <span data-ttu-id="2a51b-119">功能 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="2a51b-119">Feature\_Parent</span></span> | <span data-ttu-id="2a51b-120">屬性</span><span class="sxs-lookup"><span data-stu-id="2a51b-120">Attributes</span></span> |
|---------|-----------------|------------|
| <span data-ttu-id="2a51b-121">Office</span><span class="sxs-lookup"><span data-stu-id="2a51b-121">Office</span></span>  | <span data-ttu-id="2a51b-122">Null</span><span class="sxs-lookup"><span data-stu-id="2a51b-122">Null</span></span>            | <span data-ttu-id="2a51b-123">4</span><span class="sxs-lookup"><span data-stu-id="2a51b-123">4</span></span>          |
| <span data-ttu-id="2a51b-124">Excel</span><span class="sxs-lookup"><span data-stu-id="2a51b-124">Excel</span></span>   | <span data-ttu-id="2a51b-125">Office</span><span class="sxs-lookup"><span data-stu-id="2a51b-125">Office</span></span>          | <span data-ttu-id="2a51b-126">4</span><span class="sxs-lookup"><span data-stu-id="2a51b-126">4</span></span>          |
| <span data-ttu-id="2a51b-127">Word</span><span class="sxs-lookup"><span data-stu-id="2a51b-127">Word</span></span>    | <span data-ttu-id="2a51b-128">Office</span><span class="sxs-lookup"><span data-stu-id="2a51b-128">Office</span></span>          | <span data-ttu-id="2a51b-129">8</span><span class="sxs-lookup"><span data-stu-id="2a51b-129">8</span></span>          |



 

<span data-ttu-id="2a51b-130">在此範例中，Word 設定為 [不允許公告]，其與父系、Office 的 [允許公告] 狀態衝突。</span><span class="sxs-lookup"><span data-stu-id="2a51b-130">In the example, Word is set to disallow advertisement, which conflicts with the allow advertisement state of its parent, Office.</span></span>

<span data-ttu-id="2a51b-131">在某些情況下，ICE10 會張貼下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="2a51b-131">In some cases ICE10 posts the following error:</span></span>

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

<span data-ttu-id="2a51b-132">這是指不正確外鍵參考。</span><span class="sxs-lookup"><span data-stu-id="2a51b-132">This refers to an invalid foreign key reference.</span></span> <span data-ttu-id="2a51b-133">修正方法是讓「子系」指向其正確的父功能，或將父項功能 ' Parent ' 的專案加入至 [功能](feature-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="2a51b-133">The fix is to have 'Child' point to its correct parent feature, or add an entry for the parent feature 'Parent' to the [Feature](feature-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a51b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a51b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a51b-135">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="2a51b-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



