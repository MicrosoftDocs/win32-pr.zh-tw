---
description: Microsoft 辨識器會使用下列 Guid。
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: 屬性 Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115912"
---
# <a name="property-guids"></a><span data-ttu-id="76a63-103">屬性 Guid</span><span class="sxs-lookup"><span data-stu-id="76a63-103">Property GUIDs</span></span>

<span data-ttu-id="76a63-104">Microsoft 辨識器會使用下列 Guid。</span><span class="sxs-lookup"><span data-stu-id="76a63-104">The Microsoft recognizers use the following GUIDs.</span></span> <span data-ttu-id="76a63-105">如果可能的話，應用程式應該使用這些 Guid。</span><span class="sxs-lookup"><span data-stu-id="76a63-105">Whenever possible, applications should use these GUIDs.</span></span> <span data-ttu-id="76a63-106">不過，在預期的情況下，其他辨識器會針對不受 Microsoft 辨識器支援的屬性使用額外的 Guid。</span><span class="sxs-lookup"><span data-stu-id="76a63-106">However, it is expected and encouraged that other recognizers will use additional GUIDs for properties that are not supported by the Microsoft recognizers.</span></span>

<span data-ttu-id="76a63-107">已開發所有屬性函式，並瞭解 Guid 清單可能會由其他辨識器延伸。</span><span class="sxs-lookup"><span data-stu-id="76a63-107">All property functions have been developed with the understanding that the list of GUIDs may be extended by other recognizers.</span></span> <span data-ttu-id="76a63-108">這些屬性函數包括：</span><span class="sxs-lookup"><span data-stu-id="76a63-108">These property functions include:</span></span>

-   [<span data-ttu-id="76a63-109">**GetCoNtextPropertyList 函式**</span><span class="sxs-lookup"><span data-stu-id="76a63-109">**GetContextPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [<span data-ttu-id="76a63-110">**GetCoNtextPropertyValue 函式**</span><span class="sxs-lookup"><span data-stu-id="76a63-110">**GetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [<span data-ttu-id="76a63-111">**GetResultPropertyList 函式**</span><span class="sxs-lookup"><span data-stu-id="76a63-111">**GetResultPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [<span data-ttu-id="76a63-112">**SetCoNtextPropertyValue 函式**</span><span class="sxs-lookup"><span data-stu-id="76a63-112">**SetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

<span data-ttu-id="76a63-113">下表列出在 msinkaut 中所定義的 Tablet PC 屬性 Guid (安裝于 c： \\ Program Files \\ MICROSOFT Tablet PC Platform SDK \\ 預設) 。</span><span class="sxs-lookup"><span data-stu-id="76a63-113">The following table lists Tablet PC property GUIDs defined in msinkaut.h (installed in c:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include by default).</span></span>



| <span data-ttu-id="76a63-114">GUID</span><span class="sxs-lookup"><span data-stu-id="76a63-114">GUID</span></span>                                                  | <span data-ttu-id="76a63-115">定義</span><span class="sxs-lookup"><span data-stu-id="76a63-115">Definition</span></span>                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76a63-116">INKRECOGNITIONPROPERTY \_ BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="76a63-116">INKRECOGNITIONPROPERTY\_BOXNUMBER</span></span><br/>          | <span data-ttu-id="76a63-117">Box 模式中的辨識器替代方塊索引</span><span class="sxs-lookup"><span data-stu-id="76a63-117">The recognizer alternate box index in box mode</span></span><br/>                                    |
| <span data-ttu-id="76a63-118">INKRECOGNITIONPROPERTY \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="76a63-118">INKRECOGNITIONPROPERTY\_LINENUMBER</span></span><br/>         | <span data-ttu-id="76a63-119">行號</span><span class="sxs-lookup"><span data-stu-id="76a63-119">The line number</span></span><br/>                                                                   |
| <span data-ttu-id="76a63-120">INKRECOGNITIONPROPERTY \_ 分割</span><span class="sxs-lookup"><span data-stu-id="76a63-120">INKRECOGNITIONPROPERTY\_SEGMENTATION</span></span><br/>       | <span data-ttu-id="76a63-121">辨識器如何分割單字和字元</span><span class="sxs-lookup"><span data-stu-id="76a63-121">How the recognizer segments words and characters</span></span><br/>                                  |
| <span data-ttu-id="76a63-122">INKRECOGNITIONPROPERTY \_ HOTPOINT</span><span class="sxs-lookup"><span data-stu-id="76a63-122">INKRECOGNITIONPROPERTY\_HOTPOINT</span></span><br/>           | <span data-ttu-id="76a63-123">手勢作用點</span><span class="sxs-lookup"><span data-stu-id="76a63-123">The gesture hot point</span></span><br/>                                                             |
| <span data-ttu-id="76a63-124">INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="76a63-124">INKRECOGNITIONPROPERTY\_MAXIMUMSTROKECOUNT</span></span><br/> | <span data-ttu-id="76a63-125">區段的最大筆觸數目</span><span class="sxs-lookup"><span data-stu-id="76a63-125">Maximum number of strokes for a segment</span></span><br/>                                           |
| <span data-ttu-id="76a63-126">INKRECOGNITIONPROPERTY \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="76a63-126">INKRECOGNITIONPROPERTY\_POINTSPERINCH</span></span><br/>      | <span data-ttu-id="76a63-127">每英寸點數計量</span><span class="sxs-lookup"><span data-stu-id="76a63-127">The points-per-inch metric</span></span><br/>                                                        |
| <span data-ttu-id="76a63-128">INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="76a63-128">INKRECOGNITIONPROPERTY\_CONFIDENCELEVEL</span></span><br/>    | <span data-ttu-id="76a63-129">[**信賴度 \_層級**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) 列舉</span><span class="sxs-lookup"><span data-stu-id="76a63-129">[**CONFIDENCE\_LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) enumeration</span></span><br/>                         |
| <span data-ttu-id="76a63-130">INKRECOGNITIONPROPERTY \_ LINEMETRICS</span><span class="sxs-lookup"><span data-stu-id="76a63-130">INKRECOGNITIONPROPERTY\_LINEMETRICS</span></span><br/>        | <span data-ttu-id="76a63-131">>lattice 中使用的計算基準、中線或兩者的相關資訊</span><span class="sxs-lookup"><span data-stu-id="76a63-131">Information for computing baseline, midline, or both, that is used in the lattice</span></span><br/> |



 

 

 




