---
title: VML IVgAdjustments 資料類型
description: VML IVgAdjustments 資料類型
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29f85f93218db098ca247fa66b1f493e9c622a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463304"
---
# <a name="vml-ivgadjustments-data-type"></a><span data-ttu-id="0f74b-103">VML IVgAdjustments 資料類型</span><span class="sxs-lookup"><span data-stu-id="0f74b-103">VML IVgAdjustments Data Type</span></span>

<span data-ttu-id="0f74b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="0f74b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0f74b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="0f74b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0f74b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="0f74b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0f74b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="0f74b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0f74b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="0f74b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0f74b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="0f74b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0f74b-110">可在公式中使用之圖形的調整集合。</span><span class="sxs-lookup"><span data-stu-id="0f74b-110">Collection of adjustments to a shape that can be used in formulas.</span></span> <span data-ttu-id="0f74b-111">調整可用來作為暫時預留位置，或因任何原因而使用變數。</span><span class="sxs-lookup"><span data-stu-id="0f74b-111">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="0f74b-112">集合中只有8項調整。</span><span class="sxs-lookup"><span data-stu-id="0f74b-112">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="0f74b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0f74b-113">Attributes</span></span> | <span data-ttu-id="0f74b-114">Description</span><span class="sxs-lookup"><span data-stu-id="0f74b-114">Description</span></span>                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f74b-115">長度</span><span class="sxs-lookup"><span data-stu-id="0f74b-115">Length</span></span>     | <span data-ttu-id="0f74b-116">**Integer** (整數)。</span><span class="sxs-lookup"><span data-stu-id="0f74b-116">**Integer**.</span></span> <span data-ttu-id="0f74b-117">調整的數目。</span><span class="sxs-lookup"><span data-stu-id="0f74b-117">Number of adjustments.</span></span> <span data-ttu-id="0f74b-118">不能大於8。</span><span class="sxs-lookup"><span data-stu-id="0f74b-118">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="0f74b-119">項目</span><span class="sxs-lookup"><span data-stu-id="0f74b-119">Item</span></span>       | <span data-ttu-id="0f74b-120">**Long**。</span><span class="sxs-lookup"><span data-stu-id="0f74b-120">**Long**.</span></span> <span data-ttu-id="0f74b-121">從0到7的索引調整陣列。</span><span class="sxs-lookup"><span data-stu-id="0f74b-121">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="0f74b-122">請注意，可能會 sparcely 指定調整;也就是說，中繼陣列值可能不一定會填滿。</span><span class="sxs-lookup"><span data-stu-id="0f74b-122">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="0f74b-123">例如，專案1、3和5的值可能是3，而專案 (0) 、專案 (2) 和專案 (4) 指定。</span><span class="sxs-lookup"><span data-stu-id="0f74b-123">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="0f74b-124">若要查看專案是否存在，請使用 Exists 屬性。</span><span class="sxs-lookup"><span data-stu-id="0f74b-124">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="0f74b-125">Exists</span><span class="sxs-lookup"><span data-stu-id="0f74b-125">Exists</span></span>     | <span data-ttu-id="0f74b-126">**IVgTriState**。</span><span class="sxs-lookup"><span data-stu-id="0f74b-126">**IVgTriState**.</span></span> <span data-ttu-id="0f74b-127">判斷指定的調整是否存在。</span><span class="sxs-lookup"><span data-stu-id="0f74b-127">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="0f74b-128">請注意，必須使用索引;也就是說， (專案) 必須用來取出專案的存在。</span><span class="sxs-lookup"><span data-stu-id="0f74b-128">Note that an index must be used; that is, exists(item) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                           |
| <span data-ttu-id="0f74b-129">值</span><span class="sxs-lookup"><span data-stu-id="0f74b-129">Value</span></span>      | <span data-ttu-id="0f74b-130">**字串**。</span><span class="sxs-lookup"><span data-stu-id="0f74b-130">**String**.</span></span> <span data-ttu-id="0f74b-131">數值的文字標記法，每個數位之間都有逗號。</span><span class="sxs-lookup"><span data-stu-id="0f74b-131">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

 

 