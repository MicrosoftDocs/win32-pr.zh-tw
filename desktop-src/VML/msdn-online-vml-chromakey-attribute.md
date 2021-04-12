---
title: VML Chromakey 屬性
description: VML Chromakey 屬性
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315634"
---
# <a name="vml-chromakey-attribute"></a><span data-ttu-id="eecd1-103">VML Chromakey 屬性</span><span class="sxs-lookup"><span data-stu-id="eecd1-103">VML Chromakey Attribute</span></span>

<span data-ttu-id="eecd1-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="eecd1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eecd1-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="eecd1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eecd1-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="eecd1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eecd1-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="eecd1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eecd1-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="eecd1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eecd1-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="eecd1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eecd1-110">定義將被視為透明影像的色彩值。</span><span class="sxs-lookup"><span data-stu-id="eecd1-110">Defines the color value of the image that will be treated as transparent.</span></span> <span data-ttu-id="eecd1-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eecd1-111">Read/write.</span></span> <span data-ttu-id="eecd1-112">**VgColor**。</span><span class="sxs-lookup"><span data-stu-id="eecd1-112">**VgColor**.</span></span>

<span data-ttu-id="eecd1-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="eecd1-113">**Applies To**</span></span>

[<span data-ttu-id="eecd1-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="eecd1-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="eecd1-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="eecd1-115">**Tag Syntax**</span></span>

<span data-ttu-id="eecd1-116"><v： *element* chromakey = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="eecd1-116"><v: *element* chromakey=" *expression* "></span></span>

<span data-ttu-id="eecd1-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="eecd1-117">**Script Syntax**</span></span>

<span data-ttu-id="eecd1-118"> chromakey = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="eecd1-118">*element* .chromakey="*expression*"</span></span>

<span data-ttu-id="eecd1-119">*運算式* =\*\* chromakey</span><span class="sxs-lookup"><span data-stu-id="eecd1-119">*expression*=*element*.chromakey</span></span>

<span data-ttu-id="eecd1-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="eecd1-120">**Remarks**</span></span>

<span data-ttu-id="eecd1-121">您可以使用此屬性，藉由將透明度加密為特定色彩，讓影像的部分變成透明。</span><span class="sxs-lookup"><span data-stu-id="eecd1-121">Use this attribute to make parts of an image transparent by keying the transparency to a specific color.</span></span> <span data-ttu-id="eecd1-122">例如，如果您將 **Chromakey** 值設為 **黑色**，則影像中任何黑色的部分將會是透明的，填滿色彩將會「顯示」影像的該部分。</span><span class="sxs-lookup"><span data-stu-id="eecd1-122">For example, if you make the **Chromakey** value **black**, then any portion of the image that is black will be transparent, and the fill color will "show through" that portion of the image.</span></span>

<span data-ttu-id="eecd1-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="eecd1-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="eecd1-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="eecd1-124">**Example**</span></span>

<span data-ttu-id="eecd1-125">實心黑色影像的區域會變成透明的，允許綠色填滿色彩改為顯示在這些區域中。</span><span class="sxs-lookup"><span data-stu-id="eecd1-125">The areas of the image that are solid black will become transparent, allowing the green fill color to show through those areas instead.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 