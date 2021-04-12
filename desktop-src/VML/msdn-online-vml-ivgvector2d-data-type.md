---
title: VML IVgVector2D 資料類型
description: VML IVgVector2D 資料類型
ms.assetid: e4455d07-53f6-4d35-a70f-dbf969b32c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdbf24f93fe821de71bf13638ae30f1acc7e72b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315610"
---
# <a name="vml-ivgvector2d-data-type"></a><span data-ttu-id="7ce10-103">VML IVgVector2D 資料類型</span><span class="sxs-lookup"><span data-stu-id="7ce10-103">VML IVgVector2D Data Type</span></span>

<span data-ttu-id="7ce10-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7ce10-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7ce10-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7ce10-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7ce10-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7ce10-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7ce10-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7ce10-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7ce10-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7ce10-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7ce10-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7ce10-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7ce10-110">指定由兩個 **雙精度浮** 點陣列成的二維向量。</span><span class="sxs-lookup"><span data-stu-id="7ce10-110">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ce10-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7ce10-111">Attributes</span></span></th>
<th><span data-ttu-id="7ce10-112">描述</span><span class="sxs-lookup"><span data-stu-id="7ce10-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ce10-113">值</span><span class="sxs-lookup"><span data-stu-id="7ce10-113">Value</span></span></td>
<td><span data-ttu-id="7ce10-114">字串。</span><span class="sxs-lookup"><span data-stu-id="7ce10-114">String.</span></span> <span data-ttu-id="7ce10-115">以空格分隔的兩個向量數位的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="7ce10-115">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ce10-116">X</span><span class="sxs-lookup"><span data-stu-id="7ce10-116">X</span></span></td>
<td><span data-ttu-id="7ce10-117">雙。</span><span class="sxs-lookup"><span data-stu-id="7ce10-117">Double.</span></span> <span data-ttu-id="7ce10-118">這個向量的 X 元件。</span><span class="sxs-lookup"><span data-stu-id="7ce10-118">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ce10-119">Y</span><span class="sxs-lookup"><span data-stu-id="7ce10-119">Y</span></span></td>
<td><span data-ttu-id="7ce10-120">雙。</span><span class="sxs-lookup"><span data-stu-id="7ce10-120">Double.</span></span> <span data-ttu-id="7ce10-121">這個向量的 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="7ce10-121">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ce10-122">類型</span><span class="sxs-lookup"><span data-stu-id="7ce10-122">Type</span></span></td>
<td><span data-ttu-id="7ce10-123">VgVectorType.</span><span class="sxs-lookup"><span data-stu-id="7ce10-123">VgVectorType.</span></span> <span data-ttu-id="7ce10-124">此向量的預期單位。</span><span class="sxs-lookup"><span data-stu-id="7ce10-124">Expected units for this vector.</span></span> <span data-ttu-id="7ce10-125">值為：</span><span class="sxs-lookup"><span data-stu-id="7ce10-125">Values are:</span></span>
<ul>
<li><span data-ttu-id="7ce10-126">Measure</span><span class="sxs-lookup"><span data-stu-id="7ce10-126">Measure</span></span></li>
<li><span data-ttu-id="7ce10-127">長度</span><span class="sxs-lookup"><span data-stu-id="7ce10-127">Length</span></span></li>
<li><span data-ttu-id="7ce10-128">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="7ce10-128">AngleInDegrees</span></span></li>
<li><span data-ttu-id="7ce10-129">Fraction</span><span class="sxs-lookup"><span data-stu-id="7ce10-129">Fraction</span></span></li>
<li><span data-ttu-id="7ce10-130">數字</span><span class="sxs-lookup"><span data-stu-id="7ce10-130">Number</span></span></li>
<li><span data-ttu-id="7ce10-131">百分比</span><span class="sxs-lookup"><span data-stu-id="7ce10-131">Percentage</span></span></li>
<li><span data-ttu-id="7ce10-132">整數</span><span class="sxs-lookup"><span data-stu-id="7ce10-132">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 