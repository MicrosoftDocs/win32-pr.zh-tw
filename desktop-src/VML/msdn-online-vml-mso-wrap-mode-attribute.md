---
title: VML MSO-Wrap 模式屬性
description: VML MSO-Wrap 模式屬性
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315598"
---
# <a name="vml-mso-wrap-mode-attribute"></a><span data-ttu-id="d0c8e-103">VML MSO-Wrap 模式屬性</span><span class="sxs-lookup"><span data-stu-id="d0c8e-103">VML MSO-Wrap-Mode Attribute</span></span>

<span data-ttu-id="d0c8e-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d0c8e-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d0c8e-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d0c8e-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d0c8e-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d0c8e-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d0c8e-110">定義文字的換行模式。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-110">Defines the wrapping mode for text.</span></span> <span data-ttu-id="d0c8e-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d0c8e-111">Read/write.</span></span> <span data-ttu-id="d0c8e-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-112">**String**.</span></span>

<span data-ttu-id="d0c8e-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="d0c8e-113">**Applies To**</span></span>

[<span data-ttu-id="d0c8e-114">形狀</span><span class="sxs-lookup"><span data-stu-id="d0c8e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d0c8e-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="d0c8e-115">**Tag Syntax**</span></span>

<span data-ttu-id="d0c8e-116"><v： *element* style = "mso-wrap 模式： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d0c8e-116"><v: *element* style="mso-wrap-mode: *expression* "></span></span>

<span data-ttu-id="d0c8e-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="d0c8e-117">**Remarks**</span></span>

<span data-ttu-id="d0c8e-118">數值包括：</span><span class="sxs-lookup"><span data-stu-id="d0c8e-118">Values include:</span></span>



| <span data-ttu-id="d0c8e-119">值</span><span class="sxs-lookup"><span data-stu-id="d0c8e-119">Value</span></span>          | <span data-ttu-id="d0c8e-120">描述</span><span class="sxs-lookup"><span data-stu-id="d0c8e-120">Description</span></span>                          |
|----------------|--------------------------------------|
| <span data-ttu-id="d0c8e-121">square</span><span class="sxs-lookup"><span data-stu-id="d0c8e-121">square</span></span>         | <span data-ttu-id="d0c8e-122">在正方形的形狀周圍環繞文字。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-122">Wraps text around shape in a square.</span></span> |
| <span data-ttu-id="d0c8e-123">緊</span><span class="sxs-lookup"><span data-stu-id="d0c8e-123">tight</span></span>          | <span data-ttu-id="d0c8e-124">文字會包裝在圖形附近。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-124">Text is wrapped close to the shape.</span></span>  |
| <span data-ttu-id="d0c8e-125">頂端和底部</span><span class="sxs-lookup"><span data-stu-id="d0c8e-125">top-and-bottom</span></span> | <span data-ttu-id="d0c8e-126">從上到下的文字跳躍。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-126">Text jumps from top to bottom.</span></span>       |
| <span data-ttu-id="d0c8e-127">至</span><span class="sxs-lookup"><span data-stu-id="d0c8e-127">through</span></span>        | <span data-ttu-id="d0c8e-128">文字會透過圖形顯示。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-128">Text displays through the shape.</span></span>     |
| <span data-ttu-id="d0c8e-129">無</span><span class="sxs-lookup"><span data-stu-id="d0c8e-129">none</span></span>           | <span data-ttu-id="d0c8e-130">文字不會換行。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-130">Text doesn't wrap.</span></span>                   |



 

<span data-ttu-id="d0c8e-131">由 Microsoft PowerPoint 用於儲存至 HTML，以指出在自選圖形內自動換行的 (**正方形**) 或 off (**無**) 。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-131">Used by Microsoft PowerPoint for saving to HTML to indicate whether word wrap inside an AutoShape is on (**square**) or off (**none**).</span></span>

<span data-ttu-id="d0c8e-132">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="d0c8e-132">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="d0c8e-133">**範例**</span><span class="sxs-lookup"><span data-stu-id="d0c8e-133">**Example**</span></span>

<span data-ttu-id="d0c8e-134">下列程式碼表示在 PowerPoint 中開啟自選圖形內的 wordwrap。</span><span class="sxs-lookup"><span data-stu-id="d0c8e-134">The following code indicates that wordwrap inside an AutoShape is turned on in PowerPoint.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 