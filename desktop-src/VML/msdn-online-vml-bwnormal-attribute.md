---
title: VML BWNormal 屬性
description: VML BWNormal 屬性
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023684"
---
# <a name="vml-bwnormal-attribute"></a><span data-ttu-id="0e3fc-103">VML BWNormal 屬性</span><span class="sxs-lookup"><span data-stu-id="0e3fc-103">VML BWNormal Attribute</span></span>

<span data-ttu-id="0e3fc-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0e3fc-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0e3fc-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0e3fc-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0e3fc-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0e3fc-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0e3fc-110">定義一般黑色和白色輸出裝置的黑色和白色模式。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-110">Defines the black-and-white mode for normal black-and-white output devices.</span></span> <span data-ttu-id="0e3fc-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e3fc-111">Read/write.</span></span> <span data-ttu-id="0e3fc-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="0e3fc-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="0e3fc-113">**Applies To**</span></span>

[<span data-ttu-id="0e3fc-114">形狀</span><span class="sxs-lookup"><span data-stu-id="0e3fc-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0e3fc-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="0e3fc-115">**Tag Syntax**</span></span>

<span data-ttu-id="0e3fc-116"><v： *element* o:bwnormal = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="0e3fc-116"><v: *element* o:bwnormal=" *expression* "></span></span>

<span data-ttu-id="0e3fc-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="0e3fc-117">**Remarks**</span></span>

<span data-ttu-id="0e3fc-118">當 [BWMode](msdn-online-vml-bwmode-attribute.md) 設定為 **auto** 時，這個屬性會用來決定如何以一般黑色和白色呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in normal black and white.</span></span>

<span data-ttu-id="0e3fc-119">如需此屬性值的詳細資訊，請參閱 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="0e3fc-120">預設值是 **auto**。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-120">The default value is **auto**.</span></span>

<span data-ttu-id="0e3fc-121">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="0e3fc-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="0e3fc-122">**範例**</span><span class="sxs-lookup"><span data-stu-id="0e3fc-122">**Example**</span></span>

<span data-ttu-id="0e3fc-123">圖形會處理為一般黑色和白色輸出的灰階影像。</span><span class="sxs-lookup"><span data-stu-id="0e3fc-123">The shape is processed as a grayscale image for normal black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 