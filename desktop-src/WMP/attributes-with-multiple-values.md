---
title: '具有多個值的屬性 (Windows Media Player SDK) '
description: 具有多個值的屬性
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player，媒體專案的屬性
- Windows Media Player 物件模型，媒體專案的屬性
- 物件模型、媒體專案的屬性
- Windows Media Player 行動裝置，媒體專案的屬性
- Windows Media Player ActiveX 控制項、媒體專案的屬性
- Windows Media Player 的行動 ActiveX 控制項、媒體專案的屬性
- ActiveX 控制項、媒體專案的屬性
- Windows Media Player 文件庫、媒體專案的屬性
- 文件庫、媒體專案的屬性
- 屬性，多個值
- 多個屬性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383718"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="bb069-114">具有多個值的屬性 (Windows Media Player SDK) </span><span class="sxs-lookup"><span data-stu-id="bb069-114">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="bb069-115">某些媒體專案屬性可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="bb069-115">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="bb069-116">例如， **Author**、 **WM/書寫器** 和 **WM/** 內容屬性都可以有一個以上的值。</span><span class="sxs-lookup"><span data-stu-id="bb069-116">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="bb069-117">這類屬性的資料類型是 **多重值字串**。</span><span class="sxs-lookup"><span data-stu-id="bb069-117">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="bb069-118">在 Windows Media Player 中，程式庫會在單一欄位中顯示多個值，並以分號分隔這些值。</span><span class="sxs-lookup"><span data-stu-id="bb069-118">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="bb069-119">不過，每個值實際上都是 Windows Media 專案中的個別屬性。</span><span class="sxs-lookup"><span data-stu-id="bb069-119">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="bb069-120">您可以撰寫程式碼來判斷指定的屬性是否有多個值，然後取得這些值。</span><span class="sxs-lookup"><span data-stu-id="bb069-120">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="bb069-121">您必須使用 *媒體*。**getItemInfoByType**。</span><span class="sxs-lookup"><span data-stu-id="bb069-121">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="bb069-122">如果您使用 *媒體*。**getItemInfo** 方法若要取得多重值屬性，您只會取出第一個值。</span><span class="sxs-lookup"><span data-stu-id="bb069-122">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="bb069-123">[閱讀屬性值](reading-attribute-values.md)主題中的最後一個範例示範如何使用 *媒體*。**getAttributeCountByType** 和 *媒體*。**getItemInfoByType** 方法，以取得指定屬性的多個值。</span><span class="sxs-lookup"><span data-stu-id="bb069-123">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb069-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb069-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb069-125">**媒體專案屬性**</span><span class="sxs-lookup"><span data-stu-id="bb069-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb069-126">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="bb069-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="bb069-127">**從 CD 或 DVD 讀取屬性值**</span><span class="sxs-lookup"><span data-stu-id="bb069-127">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




