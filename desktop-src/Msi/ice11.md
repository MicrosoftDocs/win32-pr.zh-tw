---
description: ICE11 可搭配並行安裝使用。 不建議將並行安裝用於安裝應用程式，以供公開發行。 如需並行安裝的詳細資訊，請參閱並行安裝。
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944537"
---
# <a name="ice11"></a><span data-ttu-id="a05e3-105">ICE11</span><span class="sxs-lookup"><span data-stu-id="a05e3-105">ICE11</span></span>

<span data-ttu-id="a05e3-106">ICE11 可搭配並行安裝使用。</span><span class="sxs-lookup"><span data-stu-id="a05e3-106">The ICE11 is used with concurrent installations.</span></span> <span data-ttu-id="a05e3-107">不建議將並行安裝用於安裝應用程式，以供公開發行。</span><span class="sxs-lookup"><span data-stu-id="a05e3-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="a05e3-108">如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="a05e3-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

## <a name="result"></a><span data-ttu-id="a05e3-109">結果</span><span class="sxs-lookup"><span data-stu-id="a05e3-109">Result</span></span>

<span data-ttu-id="a05e3-110">ICE11 會驗證並行安裝自訂動作之 [CustomAction 資料表](customaction-table.md) 的來源資料行。</span><span class="sxs-lookup"><span data-stu-id="a05e3-110">ICE11 validates the Source column of the [CustomAction table](customaction-table.md) of concurrent installation custom actions.</span></span> <span data-ttu-id="a05e3-111">來源資料行必須包含 (MSI 產品代碼) 的有效 [GUID](guid.md) 。</span><span class="sxs-lookup"><span data-stu-id="a05e3-111">The Source column must contain a valid [GUID](guid.md) (MSI product code).</span></span>

<span data-ttu-id="a05e3-112">如果 CustomAction 資料表的來源資料行針對並行安裝自訂動作所撰寫的錯誤，ICE11 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="a05e3-112">ICE11 posts an error if the Source column of the CustomAction table is authored incorrectly for concurrent installation custom actions.</span></span>

## <a name="example"></a><span data-ttu-id="a05e3-113">範例</span><span class="sxs-lookup"><span data-stu-id="a05e3-113">Example</span></span>

<span data-ttu-id="a05e3-114">ICE 會針對所顯示的範例張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a05e3-114">ICE posts the following error messages for the example shown.</span></span>

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

<span data-ttu-id="a05e3-115">[屬性工作表](property-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="a05e3-115">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="a05e3-116">屬性</span><span class="sxs-lookup"><span data-stu-id="a05e3-116">Property</span></span>        | <span data-ttu-id="a05e3-117">值</span><span class="sxs-lookup"><span data-stu-id="a05e3-117">Value</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="a05e3-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="a05e3-118">**ProductCode**</span></span> | <span data-ttu-id="a05e3-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="a05e3-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |



 

<span data-ttu-id="a05e3-120">[CustomAction 資料表](customaction-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="a05e3-120">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="a05e3-121">CustomAction</span><span class="sxs-lookup"><span data-stu-id="a05e3-121">CustomAction</span></span> | <span data-ttu-id="a05e3-122">類型</span><span class="sxs-lookup"><span data-stu-id="a05e3-122">Type</span></span> | <span data-ttu-id="a05e3-123">來源</span><span class="sxs-lookup"><span data-stu-id="a05e3-123">Source</span></span>                                 |
|--------------|------|----------------------------------------|
| <span data-ttu-id="a05e3-124">CA1</span><span class="sxs-lookup"><span data-stu-id="a05e3-124">CA1</span></span>          | <span data-ttu-id="a05e3-125">39</span><span class="sxs-lookup"><span data-stu-id="a05e3-125">39</span></span>   | <span data-ttu-id="a05e3-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="a05e3-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |
| <span data-ttu-id="a05e3-127">CA2</span><span class="sxs-lookup"><span data-stu-id="a05e3-127">CA2</span></span>          | <span data-ttu-id="a05e3-128">39</span><span class="sxs-lookup"><span data-stu-id="a05e3-128">39</span></span>   | <span data-ttu-id="a05e3-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="a05e3-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span></span> |
| <span data-ttu-id="a05e3-130">CA3</span><span class="sxs-lookup"><span data-stu-id="a05e3-130">CA3</span></span>          | <span data-ttu-id="a05e3-131">39</span><span class="sxs-lookup"><span data-stu-id="a05e3-131">39</span></span>   | <span data-ttu-id="a05e3-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="a05e3-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span></span> |
| <span data-ttu-id="a05e3-133">CA4</span><span class="sxs-lookup"><span data-stu-id="a05e3-133">CA4</span></span>          | <span data-ttu-id="a05e3-134">39</span><span class="sxs-lookup"><span data-stu-id="a05e3-134">39</span></span>   | <span data-ttu-id="a05e3-135">ProductCode</span><span class="sxs-lookup"><span data-stu-id="a05e3-135">ProductCode</span></span>                            |



 

<span data-ttu-id="a05e3-136">若要修正錯誤，在 CA1 中，您無法同時安裝「基底套件」。</span><span class="sxs-lookup"><span data-stu-id="a05e3-136">To fix the errors, for CA1, you cannot do a concurrent installation of the "base package".</span></span> <span data-ttu-id="a05e3-137">這會導致遞迴安裝。</span><span class="sxs-lookup"><span data-stu-id="a05e3-137">This would result in a recursive installation.</span></span> <span data-ttu-id="a05e3-138">您應該移除此專案，或是將來源資料行變更為與基底套件的 GUID 不同的已公告 MSI 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a05e3-138">This entry should be removed or the Source column should be changed to a GUID for an advertised MSI that differs from the base package's GUID.</span></span> <span data-ttu-id="a05e3-139">若為 CA2，請將 GUID 的所有字元設為大寫。</span><span class="sxs-lookup"><span data-stu-id="a05e3-139">For CA2, make all characters of the GUID uppercase.</span></span> <span data-ttu-id="a05e3-140">最後，將 CA4's 來源資料行變更為參考公告 MSI 的有效 GUID。</span><span class="sxs-lookup"><span data-stu-id="a05e3-140">Lastly, change CA4's Source column to reference a valid GUID of an advertised MSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a05e3-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="a05e3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a05e3-142">並行安裝</span><span class="sxs-lookup"><span data-stu-id="a05e3-142">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="a05e3-143">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="a05e3-143">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



