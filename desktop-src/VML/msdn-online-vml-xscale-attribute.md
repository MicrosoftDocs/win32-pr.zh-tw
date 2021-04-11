---
title: VML XScale 屬性
description: VML XScale 屬性
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315304"
---
# <a name="vml-xscale-attribute"></a><span data-ttu-id="41766-103">VML XScale 屬性</span><span class="sxs-lookup"><span data-stu-id="41766-103">VML XScale Attribute</span></span>

<span data-ttu-id="41766-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="41766-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="41766-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="41766-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="41766-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="41766-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="41766-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="41766-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="41766-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="41766-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="41766-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="41766-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="41766-110">決定是否要使用直接 textpath，而不是圖形路徑。</span><span class="sxs-lookup"><span data-stu-id="41766-110">Determines whether a straight textpath will be used instead of the shape path.</span></span> <span data-ttu-id="41766-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41766-111">Read/write.</span></span> <span data-ttu-id="41766-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="41766-112">**VgTriState**.</span></span>

<span data-ttu-id="41766-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="41766-113">**Applies To**</span></span>

[<span data-ttu-id="41766-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="41766-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="41766-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="41766-115">**Tag Syntax**</span></span>

<span data-ttu-id="41766-116"><v： *element* style = "xscale： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="41766-116"><v: *element* style="xscale: *expression* "></span></span>

<span data-ttu-id="41766-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="41766-117">**Script Syntax**</span></span>

<span data-ttu-id="41766-118"> xscale = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="41766-118">*element* .style.xscale="*expression*"</span></span>

<span data-ttu-id="41766-119">*運算式* =\*\* xscale</span><span class="sxs-lookup"><span data-stu-id="41766-119">*expression*=*element*.style.xscale</span></span>

<span data-ttu-id="41766-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="41766-120">**Remarks**</span></span>

<span data-ttu-id="41766-121">若 **為 True**，則會沿著圖形下限的 x 值，從左至右沿著 apath 執行文字。</span><span class="sxs-lookup"><span data-stu-id="41766-121">If **True**, the text runs along apath from left to right along the x value of the lower boundary of the shape.</span></span> <span data-ttu-id="41766-122">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="41766-122">The default value is **False**.</span></span>

<span data-ttu-id="41766-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="41766-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="41766-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="41766-124">**Example**</span></span>

<span data-ttu-id="41766-125">文字會像是在水平線上繪製一樣，即使圖形路徑是對角線也是一樣。</span><span class="sxs-lookup"><span data-stu-id="41766-125">The text will appear as if it were drawn on a horizontal line, even though the shape path is a diagonal.</span></span>


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 