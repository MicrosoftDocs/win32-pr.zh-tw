---
title: VML BWMode 屬性
description: VML BWMode 屬性
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682606"
---
# <a name="vml-bwmode-attribute"></a><span data-ttu-id="08074-103">VML BWMode 屬性</span><span class="sxs-lookup"><span data-stu-id="08074-103">VML BWMode Attribute</span></span>

<span data-ttu-id="08074-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="08074-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="08074-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="08074-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="08074-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="08074-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="08074-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="08074-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="08074-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="08074-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="08074-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="08074-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="08074-110">決定如何針對黑白輸出裝置呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="08074-110">Determines how a shape will render for black-and-white output devices.</span></span> <span data-ttu-id="08074-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08074-111">Read/write.</span></span> <span data-ttu-id="08074-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="08074-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="08074-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="08074-113">**Applies To**</span></span>

[<span data-ttu-id="08074-114">形狀</span><span class="sxs-lookup"><span data-stu-id="08074-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="08074-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="08074-115">**Tag Syntax**</span></span>

<span data-ttu-id="08074-116"><v： *element* o:bwmode = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="08074-116"><v: *element* o:bwmode=" *expression* "></span></span>

<span data-ttu-id="08074-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="08074-117">**Remarks**</span></span>

<span data-ttu-id="08074-118">當圖形列印在黑色和白色印表機上，或是在應用程式中以黑白視圖顯示時，可能會有數個選項。</span><span class="sxs-lookup"><span data-stu-id="08074-118">When a shape is printed on a black-and-white printer or displayed in a black-and-white view in an application, several options are possible.</span></span> <span data-ttu-id="08074-119">如需此屬性值的詳細資訊，請參閱 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="08074-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="08074-120">預設值是 **auto**。</span><span class="sxs-lookup"><span data-stu-id="08074-120">The default value is **auto**.</span></span>

<span data-ttu-id="08074-121">如果指定 **auto** ，則會使用 [BWNormal](msdn-online-vml-bwnormal-attribute.md) 來判斷一般黑白輸出的行為，並使用 [BWPure](msdn-online-vml-bwpure-attribute.md) 來判斷純黑色和白色輸出的行為。</span><span class="sxs-lookup"><span data-stu-id="08074-121">If **auto** is specified, [BWNormal](msdn-online-vml-bwnormal-attribute.md) is used to determine the behavior for normal black-and-white output, and [BWPure](msdn-online-vml-bwpure-attribute.md) is used to determine the behavior for pure black-and-white output.</span></span>

<span data-ttu-id="08074-122">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="08074-122">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="08074-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="08074-123">**Example**</span></span>

<span data-ttu-id="08074-124">圖形的黑色和白色模式是 [ **自動**]。</span><span class="sxs-lookup"><span data-stu-id="08074-124">The black-and-white mode of the shape is **auto**.</span></span>


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 