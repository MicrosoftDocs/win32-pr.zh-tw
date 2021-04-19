---
title: 'Position 屬性 (H)  (VML) '
description: 'Position 屬性 (H)  (VML) '
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967495"
---
# <a name="position-attribute-hvml"></a><span data-ttu-id="cef80-103">Position 屬性 (H)  (VML) </span><span class="sxs-lookup"><span data-stu-id="cef80-103">Position Attribute (H)(VML)</span></span>

<span data-ttu-id="cef80-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="cef80-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cef80-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="cef80-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cef80-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="cef80-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cef80-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="cef80-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cef80-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="cef80-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cef80-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="cef80-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cef80-110">指定控制碼的 thex 和 y 值。</span><span class="sxs-lookup"><span data-stu-id="cef80-110">Specifies thex and y values of the handle.</span></span> <span data-ttu-id="cef80-111">讀取/寫入 **VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="cef80-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="cef80-112">**適用於**</span><span class="sxs-lookup"><span data-stu-id="cef80-112">**Applies To**</span></span>

<span data-ttu-id="cef80-113">[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) </span><span class="sxs-lookup"><span data-stu-id="cef80-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="cef80-114">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="cef80-114">**Tag Syntax**</span></span>

<span data-ttu-id="cef80-115"><v： *element* position = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cef80-115"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="cef80-116">**備註**</span><span class="sxs-lookup"><span data-stu-id="cef80-116">**Remarks**</span></span>

<span data-ttu-id="cef80-117">x 和 y 值可以是下列其中一種類型：</span><span class="sxs-lookup"><span data-stu-id="cef80-117">x and y values can be one of the following types:</span></span>

-   <span data-ttu-id="cef80-118">常數</span><span class="sxs-lookup"><span data-stu-id="cef80-118">constant</span></span>
-   <span data-ttu-id="cef80-119">公式 (例如， @2) </span><span class="sxs-lookup"><span data-stu-id="cef80-119">formula (for example, @2)</span></span>
-   <span data-ttu-id="cef80-120">調整 (例如， \# 3) </span><span class="sxs-lookup"><span data-stu-id="cef80-120">adjust (for example, \#3)</span></span>
-   <span data-ttu-id="cef80-121">中心</span><span class="sxs-lookup"><span data-stu-id="cef80-121">center</span></span>
-   <span data-ttu-id="cef80-122">下拉式功能表</span><span class="sxs-lookup"><span data-stu-id="cef80-122">topleft</span></span>
-   <span data-ttu-id="cef80-123">bottomright</span><span class="sxs-lookup"><span data-stu-id="cef80-123">bottomright</span></span>

<span data-ttu-id="cef80-124">如果指定了以上的任何類型（除了 *調整* ），則該維度中的控制碼位置是固定的。</span><span class="sxs-lookup"><span data-stu-id="cef80-124">If any of the above types except *adjust* are specified, the handle position is fixed in that dimension.</span></span> <span data-ttu-id="cef80-125">如果指定了調整控點，控制碼就可以在該維度中自由移動，而調整值是由控制碼的位置決定。</span><span class="sxs-lookup"><span data-stu-id="cef80-125">If an adjust handle is specified, the handle is free to move in that dimension and the adjust value is determined by the position of the handle.</span></span>

<span data-ttu-id="cef80-126">如果指定了 [極座標](msdn-online-vml-polar-attribute.md) 屬性， **Position** 屬性代表控制碼的半徑和角度值，而不是 x 和 y。</span><span class="sxs-lookup"><span data-stu-id="cef80-126">If a [Polar](msdn-online-vml-polar-attribute.md) attribute is specified, the **Position** attribute represents the radius and angle values of the handle instead of x and y.</span></span>

<span data-ttu-id="cef80-127">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="cef80-127">The default value is 0,0.</span></span>

<span data-ttu-id="cef80-128">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="cef80-128">*VML Standard Attribute*</span></span>

 

 