---
title: VML 灰階屬性
description: VML 灰階屬性
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375740"
---
# <a name="vml-grayscale-attribute"></a><span data-ttu-id="fecbb-103">VML 灰階屬性</span><span class="sxs-lookup"><span data-stu-id="fecbb-103">VML GrayScale Attribute</span></span>

<span data-ttu-id="fecbb-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="fecbb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fecbb-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="fecbb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fecbb-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="fecbb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fecbb-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="fecbb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fecbb-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="fecbb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fecbb-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="fecbb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fecbb-110">判斷圖片是否會以灰階模式顯示。</span><span class="sxs-lookup"><span data-stu-id="fecbb-110">Determines whether a picture will be displayed in grayscale mode.</span></span> <span data-ttu-id="fecbb-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fecbb-111">Read/write.</span></span> <span data-ttu-id="fecbb-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="fecbb-112">**VgTriState**.</span></span>

<span data-ttu-id="fecbb-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="fecbb-113">**Applies To**</span></span>

[<span data-ttu-id="fecbb-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="fecbb-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="fecbb-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="fecbb-115">**Tag Syntax**</span></span>

<span data-ttu-id="fecbb-116"><v： *element* 灰階 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="fecbb-116"><v: *element* grayscale=" *expression* "></span></span>

<span data-ttu-id="fecbb-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="fecbb-117">**Script Syntax**</span></span>

<span data-ttu-id="fecbb-118">*元素* 。灰階 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="fecbb-118">*element* .grayscale="*expression*"</span></span>

<span data-ttu-id="fecbb-119">*運算式* =*元素*. 灰階</span><span class="sxs-lookup"><span data-stu-id="fecbb-119">*expression*=*element*.grayscale</span></span>

<span data-ttu-id="fecbb-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="fecbb-120">**Remarks**</span></span>

<span data-ttu-id="fecbb-121">若 **為 True**，則圖片會以灰階顯示，而不是以色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="fecbb-121">If **True**, the picture will be displayed in grayscale instead of color.</span></span> <span data-ttu-id="fecbb-122">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="fecbb-122">The default is **False**.</span></span>

<span data-ttu-id="fecbb-123">此值是根據 CCIR 建議709，其偏好較高的綠色權數，並為自然色彩產生更滿意的結果。</span><span class="sxs-lookup"><span data-stu-id="fecbb-123">The value is based according to CCIR recommendation 709, which favors more green weight and produces more pleasing results for natural color.</span></span>

<span data-ttu-id="fecbb-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="fecbb-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="fecbb-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="fecbb-125">**Example**</span></span>

<span data-ttu-id="fecbb-126">影像會以灰階顯示，而不是以色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="fecbb-126">The image will be displayed in grayscale instead of color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 