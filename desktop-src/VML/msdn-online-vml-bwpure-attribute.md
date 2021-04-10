---
title: VML BWPure 屬性
description: VML BWPure 屬性
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842444"
---
# <a name="vml-bwpure-attribute"></a><span data-ttu-id="376cd-103">VML BWPure 屬性</span><span class="sxs-lookup"><span data-stu-id="376cd-103">VML BWPure Attribute</span></span>

<span data-ttu-id="376cd-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="376cd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="376cd-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="376cd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="376cd-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="376cd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="376cd-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="376cd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="376cd-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="376cd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="376cd-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="376cd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="376cd-110">定義純黑色和白色輸出裝置的黑色和白色模式。</span><span class="sxs-lookup"><span data-stu-id="376cd-110">Defines the black-and-white mode for pure black-and-white output devices.</span></span> <span data-ttu-id="376cd-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="376cd-111">Read/write.</span></span> <span data-ttu-id="376cd-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="376cd-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="376cd-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="376cd-113">**Applies To**</span></span>

[<span data-ttu-id="376cd-114">形狀</span><span class="sxs-lookup"><span data-stu-id="376cd-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="376cd-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="376cd-115">**Tag Syntax**</span></span>

<span data-ttu-id="376cd-116"><v： *element* o:bwpure = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="376cd-116"><v: *element* o:bwpure=" *expression* "></span></span>

<span data-ttu-id="376cd-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="376cd-117">**Remarks**</span></span>

<span data-ttu-id="376cd-118">當 [BWMode](msdn-online-vml-bwmode-attribute.md) 設定為 **auto** 時，這個屬性會用來判斷如何以純黑色和白色呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="376cd-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in pure black and white.</span></span>

<span data-ttu-id="376cd-119">如需此屬性值的詳細資訊，請參閱 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="376cd-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="376cd-120">預設值是 **auto**。</span><span class="sxs-lookup"><span data-stu-id="376cd-120">The default is **auto**.</span></span>

<span data-ttu-id="376cd-121">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="376cd-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="376cd-122">**範例**</span><span class="sxs-lookup"><span data-stu-id="376cd-122">**Example**</span></span>

<span data-ttu-id="376cd-123">圖形會作為純黑色和白色輸出的高對比影像來處理。</span><span class="sxs-lookup"><span data-stu-id="376cd-123">The shape is processed as a high contrast image for pure black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 