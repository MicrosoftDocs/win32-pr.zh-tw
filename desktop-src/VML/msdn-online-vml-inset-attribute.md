---
title: VML 內凹屬性
description: VML 內凹屬性
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092809"
---
# <a name="vml-inset-attribute"></a><span data-ttu-id="47627-103">VML 內凹屬性</span><span class="sxs-lookup"><span data-stu-id="47627-103">VML Inset Attribute</span></span>

<span data-ttu-id="47627-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="47627-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="47627-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="47627-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="47627-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="47627-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="47627-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="47627-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="47627-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="47627-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="47627-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="47627-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="47627-110">指定 textbox 文字的內部邊界值。</span><span class="sxs-lookup"><span data-stu-id="47627-110">Specifies inner margin values for textbox text.</span></span> <span data-ttu-id="47627-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47627-111">Read/write.</span></span> <span data-ttu-id="47627-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="47627-112">**String**.</span></span>

<span data-ttu-id="47627-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="47627-113">**Applies To**</span></span>

[<span data-ttu-id="47627-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="47627-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="47627-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="47627-115">**Tag Syntax**</span></span>

<span data-ttu-id="47627-116"><v： *element* 內凹 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="47627-116"><v: *element* inset=" *expression* "></span></span>

<span data-ttu-id="47627-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="47627-117">**Script Syntax**</span></span>

<span data-ttu-id="47627-118">*元素* . 內陷 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="47627-118">*element* .inset="*expression*"</span></span>

<span data-ttu-id="47627-119">*運算式* =*元素*。內凹</span><span class="sxs-lookup"><span data-stu-id="47627-119">*expression*=*element*.inset</span></span>

<span data-ttu-id="47627-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="47627-120">**Remarks**</span></span>

<span data-ttu-id="47627-121">內部文字邊界值會指定為包含四個值的字串，每個值都以逗號或空格分隔。</span><span class="sxs-lookup"><span data-stu-id="47627-121">The internal text margin value is specified as a string containing four values, each separated by commas or spaces.</span></span> <span data-ttu-id="47627-122">值會從 **Path** 的 [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)屬性所指定方塊的左邊、上、右和下邊緣測量內凹。</span><span class="sxs-lookup"><span data-stu-id="47627-122">The values measure inset from the left, top, right, and bottom edges of the box specified by the [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) attribute of **Path**.</span></span> <span data-ttu-id="47627-123">遺漏值會設定為預設值，也就是「0.1 in、0.05 in、0.1 in、0.05 in」。</span><span class="sxs-lookup"><span data-stu-id="47627-123">Missing values are set to the default, which is "0.1in, 0.05in, 0.1in, 0.05in".</span></span>

<span data-ttu-id="47627-124">如果是瀏覽器中不支援旋轉的旋轉圖形，周框方塊會貼齊最接近90度的倍數。</span><span class="sxs-lookup"><span data-stu-id="47627-124">For rotated shapes in browsers that do not support rotation, the bounding box will snap to the closest multiple of 90 degrees.</span></span>

<span data-ttu-id="47627-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="47627-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="47627-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="47627-126">**Example**</span></span>

<span data-ttu-id="47627-127">Textbox 會有10圖元的內凹邊界。</span><span class="sxs-lookup"><span data-stu-id="47627-127">The textbox will have an inset margin of 10 pixels.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 