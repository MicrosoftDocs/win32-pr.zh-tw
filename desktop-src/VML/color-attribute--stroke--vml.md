---
title: 'Color 屬性 (筆觸)  (VML) '
description: 'Color 屬性 (筆觸)  (VML) '
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967491"
---
# <a name="color-attribute-strokevml"></a><span data-ttu-id="5cd67-103">Color 屬性 (筆觸)  (VML) </span><span class="sxs-lookup"><span data-stu-id="5cd67-103">Color Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="5cd67-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="5cd67-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5cd67-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="5cd67-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5cd67-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="5cd67-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5cd67-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="5cd67-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5cd67-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="5cd67-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5cd67-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="5cd67-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5cd67-110">定義筆劃的色彩。</span><span class="sxs-lookup"><span data-stu-id="5cd67-110">Defines the color of a stroke.</span></span> <span data-ttu-id="5cd67-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5cd67-111">Read/write.</span></span> <span data-ttu-id="5cd67-112">**VgColor**。</span><span class="sxs-lookup"><span data-stu-id="5cd67-112">**VgColor**.</span></span>

<span data-ttu-id="5cd67-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="5cd67-113">**Applies To**</span></span>

[<span data-ttu-id="5cd67-114">中風</span><span class="sxs-lookup"><span data-stu-id="5cd67-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="5cd67-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="5cd67-115">**Tag Syntax**</span></span>

<span data-ttu-id="5cd67-116"><v： *element* color = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5cd67-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="5cd67-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="5cd67-117">**Script Syntax**</span></span>

<span data-ttu-id="5cd67-118">*element* 。 color = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5cd67-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="5cd67-119">*運算式* =*元素*。色彩</span><span class="sxs-lookup"><span data-stu-id="5cd67-119">*expression*=*element*.color</span></span>

<span data-ttu-id="5cd67-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="5cd67-120">**Remarks**</span></span>

<span data-ttu-id="5cd67-121">覆寫圖形的 **StrokeColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5cd67-121">Overrides the **StrokeColor** attribute of a shape.</span></span> <span data-ttu-id="5cd67-122">預設值為 **黑色**。</span><span class="sxs-lookup"><span data-stu-id="5cd67-122">The default value is **black**.</span></span>

<span data-ttu-id="5cd67-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="5cd67-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="5cd67-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="5cd67-124">**Example**</span></span>

<span data-ttu-id="5cd67-125">圖形具有 **綠色** 的筆觸色彩，而不是 **紅色**。</span><span class="sxs-lookup"><span data-stu-id="5cd67-125">The shape has a stroke color of **green**, not **red**.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 