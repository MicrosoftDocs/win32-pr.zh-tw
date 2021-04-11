---
description: ICE14 會驗證 Windows Installer 資料庫的功能資料表。
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319507"
---
# <a name="ice14"></a><span data-ttu-id="757d4-103">ICE14</span><span class="sxs-lookup"><span data-stu-id="757d4-103">ICE14</span></span>

<span data-ttu-id="757d4-104">ICE14 會驗證功能的下列各項：</span><span class="sxs-lookup"><span data-stu-id="757d4-104">ICE14 validates the following for features:</span></span>

-   <span data-ttu-id="757d4-105">在 [功能資料表](feature-table.md)的 [屬性] 資料行中，該根父功能沒有設定 msidbFeatureAttributesFollowParent 位。</span><span class="sxs-lookup"><span data-stu-id="757d4-105">That root parent features do not have the msidbFeatureAttributesFollowParent bit set in the Attributes column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="757d4-106">根功能沒有父系。</span><span class="sxs-lookup"><span data-stu-id="757d4-106">A root feature does not have a parent.</span></span>
-   <span data-ttu-id="757d4-107">在功能資料表的功能和功能父資料行中，沒有任何功能具有相同的專案 \_ 。 [](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="757d4-107">That no feature has the same entry in the Feature and Feature\_Parent columns of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="757d4-108">沒有任何功能可以是本身的父系。</span><span class="sxs-lookup"><span data-stu-id="757d4-108">No feature can be its own parent.</span></span>

## <a name="result"></a><span data-ttu-id="757d4-109">結果</span><span class="sxs-lookup"><span data-stu-id="757d4-109">Result</span></span>

<span data-ttu-id="757d4-110">ICE14 會在功能資料表的功能和功能的父資料行中找到具有 msidbFeatureAttributesFollowParent 位集或功能相同專案的根功能時張貼錯誤訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="757d4-110">ICE14 posts an error message if it finds a root feature with the msidbFeatureAttributesFollowParent bit set or a feature with identical entries in the Feature and Feature\_Parent columns of the Feature table.</span></span>

## <a name="example"></a><span data-ttu-id="757d4-111">範例</span><span class="sxs-lookup"><span data-stu-id="757d4-111">Example</span></span>

<span data-ttu-id="757d4-112">在下列範例中，ICE14 會傳回下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="757d4-112">ICE14 would return the following errors for the following example:</span></span>

-   <span data-ttu-id="757d4-113">功能運動在檔案資料表的功能和功能父資料行中具有相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="757d4-113">The feature Sport has the same value in the Feature and Feature\_Parent columns of the File table.</span></span>
-   <span data-ttu-id="757d4-114">根功能運動已設定 msidbFeatureAttributesFollowParent 位。</span><span class="sxs-lookup"><span data-stu-id="757d4-114">The root feature Sport has the msidbFeatureAttributesFollowParent bit set.</span></span>

<span data-ttu-id="757d4-115">在此範例的功能樹狀結構中，運動是根功能以及游泳和足球功能的父系。</span><span class="sxs-lookup"><span data-stu-id="757d4-115">In the feature tree of this example, Sport is the root feature and a parent of the Swimming and Football features.</span></span> <span data-ttu-id="757d4-116">自由樣式是游泳的子功能。</span><span class="sxs-lookup"><span data-stu-id="757d4-116">Freestyle is a child feature of Swimming.</span></span> <span data-ttu-id="757d4-117">TouchFootball 是足球的子功能。</span><span class="sxs-lookup"><span data-stu-id="757d4-117">TouchFootball is a child feature of Football.</span></span>

<span data-ttu-id="757d4-118">[功能表](feature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="757d4-118">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="757d4-119">功能</span><span class="sxs-lookup"><span data-stu-id="757d4-119">Feature</span></span>       | <span data-ttu-id="757d4-120">屬性</span><span class="sxs-lookup"><span data-stu-id="757d4-120">Attributes</span></span> | <span data-ttu-id="757d4-121">功能 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="757d4-121">Feature\_Parent</span></span> |
|---------------|------------|-----------------|
| <span data-ttu-id="757d4-122">運動項目</span><span class="sxs-lookup"><span data-stu-id="757d4-122">Sport</span></span>         | <span data-ttu-id="757d4-123">4</span><span class="sxs-lookup"><span data-stu-id="757d4-123">4</span></span>          | <span data-ttu-id="757d4-124">運動項目</span><span class="sxs-lookup"><span data-stu-id="757d4-124">Sport</span></span>           |
| <span data-ttu-id="757d4-125">游泳</span><span class="sxs-lookup"><span data-stu-id="757d4-125">Swimming</span></span>      | <span data-ttu-id="757d4-126">1</span><span class="sxs-lookup"><span data-stu-id="757d4-126">1</span></span>          | <span data-ttu-id="757d4-127">運動項目</span><span class="sxs-lookup"><span data-stu-id="757d4-127">Sport</span></span>           |
| <span data-ttu-id="757d4-128">足球</span><span class="sxs-lookup"><span data-stu-id="757d4-128">Football</span></span>      | <span data-ttu-id="757d4-129">4</span><span class="sxs-lookup"><span data-stu-id="757d4-129">4</span></span>          | <span data-ttu-id="757d4-130">運動項目</span><span class="sxs-lookup"><span data-stu-id="757d4-130">Sport</span></span>           |
| <span data-ttu-id="757d4-131">自由泳</span><span class="sxs-lookup"><span data-stu-id="757d4-131">Freestyle</span></span>     | <span data-ttu-id="757d4-132">1</span><span class="sxs-lookup"><span data-stu-id="757d4-132">1</span></span>          | <span data-ttu-id="757d4-133">游泳</span><span class="sxs-lookup"><span data-stu-id="757d4-133">Swimming</span></span>        |
| <span data-ttu-id="757d4-134">TouchFootball</span><span class="sxs-lookup"><span data-stu-id="757d4-134">TouchFootball</span></span> | <span data-ttu-id="757d4-135">4</span><span class="sxs-lookup"><span data-stu-id="757d4-135">4</span></span>          | <span data-ttu-id="757d4-136">足球</span><span class="sxs-lookup"><span data-stu-id="757d4-136">Football</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="757d4-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="757d4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="757d4-138">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="757d4-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



