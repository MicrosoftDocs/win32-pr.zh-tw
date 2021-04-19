---
title: VML FitShape 屬性
description: VML FitShape 屬性
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966267"
---
# <a name="vml-fitshape-attribute"></a><span data-ttu-id="7979b-103">VML FitShape 屬性</span><span class="sxs-lookup"><span data-stu-id="7979b-103">VML FitShape Attribute</span></span>

<span data-ttu-id="7979b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7979b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7979b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7979b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7979b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7979b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7979b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7979b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7979b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7979b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7979b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7979b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7979b-110">定義文字是否適合圖形的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="7979b-110">Defines whether the text fits bounding box of a shape.</span></span> <span data-ttu-id="7979b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7979b-111">Read/write.</span></span> <span data-ttu-id="7979b-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="7979b-112">**VgTriState**.</span></span>

<span data-ttu-id="7979b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="7979b-113">**Applies To**</span></span>

[<span data-ttu-id="7979b-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="7979b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="7979b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="7979b-115">**Tag Syntax**</span></span>

<span data-ttu-id="7979b-116"><v： *element* fitshape = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7979b-116"><v: *element* fitshape=" *expression* "></span></span>

<span data-ttu-id="7979b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="7979b-117">**Script Syntax**</span></span>

<span data-ttu-id="7979b-118"> fitshape = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="7979b-118">*element* .fitshape="*expression*"</span></span>

<span data-ttu-id="7979b-119">*運算式* =\*\* fitshape</span><span class="sxs-lookup"><span data-stu-id="7979b-119">*expression*=*element*.fitshape</span></span>

<span data-ttu-id="7979b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="7979b-120">**Remarks**</span></span>

<span data-ttu-id="7979b-121">若 **為 True**，則會將文字向外延伸至定義整個圖形的方塊邊緣。</span><span class="sxs-lookup"><span data-stu-id="7979b-121">If **True**, stretches the text out to the edges of the box that defines the entire shape.</span></span> <span data-ttu-id="7979b-122">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="7979b-122">The default is **False**.</span></span>

<span data-ttu-id="7979b-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="7979b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7979b-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="7979b-124">**Example**</span></span>

<span data-ttu-id="7979b-125">文字會伸展以符合圖形。</span><span class="sxs-lookup"><span data-stu-id="7979b-125">The text will stretch to fit the shape.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 