---
title: VML 方法屬性
description: VML 方法屬性
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965029"
---
# <a name="vml-method-attribute"></a><span data-ttu-id="effa8-103">VML 方法屬性</span><span class="sxs-lookup"><span data-stu-id="effa8-103">VML Method Attribute</span></span>

<span data-ttu-id="effa8-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="effa8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="effa8-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="effa8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="effa8-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="effa8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="effa8-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="effa8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="effa8-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="effa8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="effa8-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="effa8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="effa8-110">定義用來產生漸層填滿的方法。</span><span class="sxs-lookup"><span data-stu-id="effa8-110">Defines the method used to generate a gradient fill.</span></span> <span data-ttu-id="effa8-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="effa8-111">Read/write.</span></span> <span data-ttu-id="effa8-112">**VgSigmaType**。</span><span class="sxs-lookup"><span data-stu-id="effa8-112">**VgSigmaType**.</span></span>

<span data-ttu-id="effa8-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="effa8-113">**Applies To**</span></span>

[<span data-ttu-id="effa8-114">填滿</span><span class="sxs-lookup"><span data-stu-id="effa8-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="effa8-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="effa8-115">**Tag Syntax**</span></span>

<span data-ttu-id="effa8-116"><v： *element* method = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="effa8-116"><v: *element* method=" *expression* "></span></span>

<span data-ttu-id="effa8-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="effa8-117">**Script Syntax**</span></span>

<span data-ttu-id="effa8-118">*元素* . method = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="effa8-118">*element* .method="*expression*"</span></span>

<span data-ttu-id="effa8-119">*運算式* =*element*。方法</span><span class="sxs-lookup"><span data-stu-id="effa8-119">*expression*=*element*.method</span></span>

<span data-ttu-id="effa8-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="effa8-120">**Remarks**</span></span>

<span data-ttu-id="effa8-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="effa8-121">Values include:</span></span>



| <span data-ttu-id="effa8-122">值</span><span class="sxs-lookup"><span data-stu-id="effa8-122">Value</span></span>  | <span data-ttu-id="effa8-123">描述</span><span class="sxs-lookup"><span data-stu-id="effa8-123">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="effa8-124">無</span><span class="sxs-lookup"><span data-stu-id="effa8-124">None</span></span>   | <span data-ttu-id="effa8-125">沒有 sigma 填滿。</span><span class="sxs-lookup"><span data-stu-id="effa8-125">No sigma fill.</span></span>       |
| <span data-ttu-id="effa8-126">線性</span><span class="sxs-lookup"><span data-stu-id="effa8-126">Linear</span></span> | <span data-ttu-id="effa8-127">線性 sigma 填滿。</span><span class="sxs-lookup"><span data-stu-id="effa8-127">Linear sigma fill.</span></span>   |
| <span data-ttu-id="effa8-128">Sigma</span><span class="sxs-lookup"><span data-stu-id="effa8-128">Sigma</span></span>  | <span data-ttu-id="effa8-129">Sigma 填滿。</span><span class="sxs-lookup"><span data-stu-id="effa8-129">Sigma fill.</span></span> <span data-ttu-id="effa8-130">預設值。</span><span class="sxs-lookup"><span data-stu-id="effa8-130">Default.</span></span> |
| <span data-ttu-id="effa8-131">任意</span><span class="sxs-lookup"><span data-stu-id="effa8-131">Any</span></span>    | <span data-ttu-id="effa8-132">任何 sigma 填滿。</span><span class="sxs-lookup"><span data-stu-id="effa8-132">Any sigma fill.</span></span>      |



 

<span data-ttu-id="effa8-133">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="effa8-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="effa8-134">**範例**</span><span class="sxs-lookup"><span data-stu-id="effa8-134">**Example**</span></span>

<span data-ttu-id="effa8-135">圖形會有紅色的線性漸層填滿。</span><span class="sxs-lookup"><span data-stu-id="effa8-135">The shape will have a red linear gradient fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 