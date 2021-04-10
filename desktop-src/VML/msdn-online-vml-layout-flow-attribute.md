---
title: VML Layout-Flow 屬性
description: VML Layout-Flow 屬性
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933401"
---
# <a name="vml-layout-flow-attribute"></a><span data-ttu-id="14257-103">VML Layout-Flow 屬性</span><span class="sxs-lookup"><span data-stu-id="14257-103">VML Layout-Flow Attribute</span></span>

<span data-ttu-id="14257-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="14257-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="14257-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="14257-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="14257-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="14257-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="14257-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="14257-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="14257-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="14257-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="14257-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="14257-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="14257-110">決定文字方塊中文字版面配置的流程。</span><span class="sxs-lookup"><span data-stu-id="14257-110">Determines the flow of the text layout in a textbox.</span></span> <span data-ttu-id="14257-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="14257-111">Read/write.</span></span> <span data-ttu-id="14257-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="14257-112">**String**.</span></span>

<span data-ttu-id="14257-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="14257-113">**Applies To**</span></span>

[<span data-ttu-id="14257-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="14257-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="14257-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="14257-115">**Tag Syntax**</span></span>

<span data-ttu-id="14257-116"><v： *element* style = "layout-flow： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="14257-116"><v: *element* style="layout-flow: *expression* "></span></span>

<span data-ttu-id="14257-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="14257-117">**Remarks**</span></span>

<span data-ttu-id="14257-118">數值包括：</span><span class="sxs-lookup"><span data-stu-id="14257-118">Values include:</span></span>



| <span data-ttu-id="14257-119">值</span><span class="sxs-lookup"><span data-stu-id="14257-119">Value</span></span>                  | <span data-ttu-id="14257-120">描述</span><span class="sxs-lookup"><span data-stu-id="14257-120">Description</span></span>                                 |
|------------------------|---------------------------------------------|
| <span data-ttu-id="14257-121">水平</span><span class="sxs-lookup"><span data-stu-id="14257-121">horizontal</span></span>             | <span data-ttu-id="14257-122">文字會以水準方式顯示。</span><span class="sxs-lookup"><span data-stu-id="14257-122">Text is displayed horizontally.</span></span> <span data-ttu-id="14257-123">預設值。</span><span class="sxs-lookup"><span data-stu-id="14257-123">Default.</span></span>    |
| <span data-ttu-id="14257-124">垂直</span><span class="sxs-lookup"><span data-stu-id="14257-124">vertical</span></span>               | <span data-ttu-id="14257-125">文字會垂直顯示。</span><span class="sxs-lookup"><span data-stu-id="14257-125">Text is displayed vertically.</span></span>               |
| <span data-ttu-id="14257-126">垂直-表意文字</span><span class="sxs-lookup"><span data-stu-id="14257-126">vertical-ideographic</span></span>   | <span data-ttu-id="14257-127">會垂直顯示表意字。</span><span class="sxs-lookup"><span data-stu-id="14257-127">Ideographic text is displayed vertically.</span></span>   |
| <span data-ttu-id="14257-128">水準-表意文字</span><span class="sxs-lookup"><span data-stu-id="14257-128">horizontal-ideographic</span></span> | <span data-ttu-id="14257-129">以水準方式顯示表意字。</span><span class="sxs-lookup"><span data-stu-id="14257-129">Ideographic text is displayed horizontally.</span></span> |



 

<span data-ttu-id="14257-130">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="14257-130">*VML Standard Attribute*</span></span>

<span data-ttu-id="14257-131">**範例**</span><span class="sxs-lookup"><span data-stu-id="14257-131">**Example**</span></span>

<span data-ttu-id="14257-132">文字方塊中的文字流程將會垂直流動。</span><span class="sxs-lookup"><span data-stu-id="14257-132">The text flow in the textbox will flow vertically.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 