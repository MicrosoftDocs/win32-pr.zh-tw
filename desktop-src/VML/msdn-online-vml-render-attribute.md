---
title: VML 轉譯屬性
description: VML 轉譯屬性
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106991295"
---
# <a name="vml-render-attribute"></a><span data-ttu-id="e7897-103">VML 轉譯屬性</span><span class="sxs-lookup"><span data-stu-id="e7897-103">VML Render Attribute</span></span>

<span data-ttu-id="e7897-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="e7897-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e7897-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="e7897-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e7897-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="e7897-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e7897-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="e7897-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e7897-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="e7897-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e7897-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="e7897-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e7897-110">定義延伸的呈現模式。</span><span class="sxs-lookup"><span data-stu-id="e7897-110">Defines the rendering mode of the extrusion.</span></span> <span data-ttu-id="e7897-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e7897-111">Read/write.</span></span> <span data-ttu-id="e7897-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="e7897-112">**String**.</span></span>

<span data-ttu-id="e7897-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="e7897-113">**Applies To**</span></span>

[<span data-ttu-id="e7897-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="e7897-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="e7897-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="e7897-115">**Tag Syntax**</span></span>

<span data-ttu-id="e7897-116"><o： *element* render = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e7897-116"><o: *element* render=" *expression* "></span></span>

<span data-ttu-id="e7897-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="e7897-117">**Script Syntax**</span></span>

<span data-ttu-id="e7897-118">*element* = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e7897-118">*element* .render="*expression*"</span></span>

<span data-ttu-id="e7897-119">*運算式* =*element*。 render</span><span class="sxs-lookup"><span data-stu-id="e7897-119">*expression*=*element*.render</span></span>

<span data-ttu-id="e7897-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="e7897-120">**Remarks**</span></span>

<span data-ttu-id="e7897-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="e7897-121">Values include:</span></span>



| <span data-ttu-id="e7897-122">值</span><span class="sxs-lookup"><span data-stu-id="e7897-122">Value</span></span>        | <span data-ttu-id="e7897-123">描述</span><span class="sxs-lookup"><span data-stu-id="e7897-123">Description</span></span>                                                   |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="e7897-124">固體</span><span class="sxs-lookup"><span data-stu-id="e7897-124">solid</span></span>        | <span data-ttu-id="e7897-125">轉譯會顯示穩固的形狀。</span><span class="sxs-lookup"><span data-stu-id="e7897-125">Rendering displays a solid shape.</span></span> <span data-ttu-id="e7897-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="e7897-126">Default.</span></span>                    |
| <span data-ttu-id="e7897-127">著色</span><span class="sxs-lookup"><span data-stu-id="e7897-127">wireframe</span></span>    | <span data-ttu-id="e7897-128">轉譯會顯示線框圖形。</span><span class="sxs-lookup"><span data-stu-id="e7897-128">Rendering displays a wireframe shape.</span></span>                         |
| <span data-ttu-id="e7897-129">boundingcube</span><span class="sxs-lookup"><span data-stu-id="e7897-129">boundingcube</span></span> | <span data-ttu-id="e7897-130">轉譯會顯示包含圖形的周框 cube。</span><span class="sxs-lookup"><span data-stu-id="e7897-130">Rendering displays the bounding cube that contains the shape.</span></span> |



 

<span data-ttu-id="e7897-131">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="e7897-131">*Microsoft Office Extensions Attribute*</span></span>

 

 