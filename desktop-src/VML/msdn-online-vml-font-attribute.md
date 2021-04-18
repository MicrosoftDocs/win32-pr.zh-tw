---
title: VML 字型屬性
description: VML 字型屬性
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965861"
---
# <a name="vml-font-attribute"></a><span data-ttu-id="a9a7e-103">VML 字型屬性</span><span class="sxs-lookup"><span data-stu-id="a9a7e-103">VML Font Attribute</span></span>

<span data-ttu-id="a9a7e-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a9a7e-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a9a7e-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a9a7e-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a9a7e-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a9a7e-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a9a7e-110">指定字型屬性的複合值。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-110">Specifies a compound value of font attributes.</span></span> <span data-ttu-id="a9a7e-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9a7e-111">Read/write.</span></span> <span data-ttu-id="a9a7e-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-112">**String**.</span></span>

<span data-ttu-id="a9a7e-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a9a7e-113">**Applies To**</span></span>

[<span data-ttu-id="a9a7e-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a9a7e-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a9a7e-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="a9a7e-115">**Tag Syntax**</span></span>

<span data-ttu-id="a9a7e-116"><v： *element* style = "font-size： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a9a7e-116"><v: *element* style="font: *expression* "></span></span>

<span data-ttu-id="a9a7e-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="a9a7e-117">**Script Syntax**</span></span>

<span data-ttu-id="a9a7e-118">style *. font-family* = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a9a7e-118">*element* .style.font="*expression*"</span></span>

<span data-ttu-id="a9a7e-119">*運算式* =*element*。字型</span><span class="sxs-lookup"><span data-stu-id="a9a7e-119">*expression*=*element*.style.font</span></span>

<span data-ttu-id="a9a7e-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="a9a7e-120">**Remarks**</span></span>

<span data-ttu-id="a9a7e-121">定義字型的屬性，包括系列、樣式、粗細、大小和變異數。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-121">Defines the attributes of a font, including family, style, weight, size, and variant.</span></span> <span data-ttu-id="a9a7e-122">字串中的定義順序為： **字型樣式**、 **字型變異**、 **字型粗細**、 **字型大小**、 **線條高度** 和 **字型系列**。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-122">The order of definitions in the string is: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height**, and **font-family**.</span></span> <span data-ttu-id="a9a7e-123">這些值與標準 HTML 樣式屬性相同。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="a9a7e-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="a9a7e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a9a7e-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="a9a7e-125">**Example**</span></span>

<span data-ttu-id="a9a7e-126">Textpath 文字的字型為斜體、小型大寫字母、粗體、36點 Arial。</span><span class="sxs-lookup"><span data-stu-id="a9a7e-126">The font of the textpath text is italic, small-caps, bold, 36 point Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 