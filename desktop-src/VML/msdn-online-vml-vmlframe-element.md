---
title: VML VMLFrame 元素
description: VML VMLFrame 元素
ms.assetid: a1582223-d6e2-42d1-95bb-97f6f1d453d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f53371afb0c2790ff6dd666f0121b30b586c51b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092785"
---
# <a name="vml-vmlframe-element"></a><span data-ttu-id="79fb1-103">VML VMLFrame 元素</span><span class="sxs-lookup"><span data-stu-id="79fb1-103">VML VMLFrame Element</span></span>

<span data-ttu-id="79fb1-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="79fb1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="79fb1-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="79fb1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="79fb1-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="79fb1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="79fb1-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="79fb1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="79fb1-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="79fb1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="79fb1-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="79fb1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="79fb1-110">定義外部形狀的框架。</span><span class="sxs-lookup"><span data-stu-id="79fb1-110">Defines a frame for an external shape.</span></span>

<span data-ttu-id="79fb1-111">下列屬性會修改框架。</span><span class="sxs-lookup"><span data-stu-id="79fb1-111">The following attributes modify a frame.</span></span>



| <span data-ttu-id="79fb1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="79fb1-112">Attribute</span></span>                                     | <span data-ttu-id="79fb1-113">描述</span><span class="sxs-lookup"><span data-stu-id="79fb1-113">Description</span></span>                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="79fb1-114">剪輯</span><span class="sxs-lookup"><span data-stu-id="79fb1-114">Clip</span></span>](msdn-online-vml-clip-attribute.md)    | <span data-ttu-id="79fb1-115">判斷是否會裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="79fb1-115">Determines whether the image will be clipped.</span></span>                         |
| [<span data-ttu-id="79fb1-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="79fb1-116">ID</span></span>](id-attribute--vmlframe--vml.md)         | <span data-ttu-id="79fb1-117">定義框架的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="79fb1-117">Defines a unique identifier for the frame.</span></span>                            |
| [<span data-ttu-id="79fb1-118">起源</span><span class="sxs-lookup"><span data-stu-id="79fb1-118">Origin</span></span>](origin-attribute--vmlframe--vml.md) | <span data-ttu-id="79fb1-119">指定框架的原點。</span><span class="sxs-lookup"><span data-stu-id="79fb1-119">Specifies the origin of the frame.</span></span>                                    |
| [<span data-ttu-id="79fb1-120">大小</span><span class="sxs-lookup"><span data-stu-id="79fb1-120">Size</span></span>](size-attribute--vmlframe.md)          | <span data-ttu-id="79fb1-121">指定框架的大小。</span><span class="sxs-lookup"><span data-stu-id="79fb1-121">Specifies the size of the frame.</span></span>                                      |
| [<span data-ttu-id="79fb1-122">Src</span><span class="sxs-lookup"><span data-stu-id="79fb1-122">Src</span></span>](src-attribute--vmlframe--vml.md)       | <span data-ttu-id="79fb1-123">指定要顯示在框架中的資料來源。</span><span class="sxs-lookup"><span data-stu-id="79fb1-123">Specifies the source of the data that will be displayed in the frame.</span></span> |
| [<span data-ttu-id="79fb1-124">Style</span><span class="sxs-lookup"><span data-stu-id="79fb1-124">Style</span></span>](msdn-online-vml-style-attribute.md)  | <span data-ttu-id="79fb1-125">定義可以用來放置框架的一般 CSS 樣式。</span><span class="sxs-lookup"><span data-stu-id="79fb1-125">Defines the normal CSS styles that can be used to position the frame.</span></span> |



 

<span data-ttu-id="79fb1-126">**備註**</span><span class="sxs-lookup"><span data-stu-id="79fb1-126">**Remarks**</span></span>

<span data-ttu-id="79fb1-127">要顯示在框架中的來源資料可以包含在相同的網頁中，也可以是另一個頁面的一部分。</span><span class="sxs-lookup"><span data-stu-id="79fb1-127">The source data to be displayed in the frame can be contained in the same Web page or be part of another page.</span></span> <span data-ttu-id="79fb1-128">透過腳本，可以動態變更來源，並可修改顯示特性。</span><span class="sxs-lookup"><span data-stu-id="79fb1-128">Through scripting, the source can be changed dynamically and the display characteristics can be modified.</span></span>

<span data-ttu-id="79fb1-129">**VMLFrame** 內的物件為「縮放比例」。</span><span class="sxs-lookup"><span data-stu-id="79fb1-129">Objects inside the **VMLFrame** are "zoom scaled."</span></span> <span data-ttu-id="79fb1-130">亦即，它們會像中繼檔一樣調整，其中線條粗細、陰影位移和文字區域都會按星號調整。</span><span class="sxs-lookup"><span data-stu-id="79fb1-130">That is, they scale like metafiles, where line weights, shadow offsets, and text area are all scaled proportionally.</span></span> <span data-ttu-id="79fb1-131">這與群組不同，其中的物件大小和位置會依比例調整，但是線條、陰影等則不會。</span><span class="sxs-lookup"><span data-stu-id="79fb1-131">This is different from a group, where object size and position are scaled proportionally, but line, shadow, etc. are not.</span></span>

<span data-ttu-id="79fb1-132">以下是將影像載入框架所需的最少程式碼。</span><span class="sxs-lookup"><span data-stu-id="79fb1-132">The following is the minimum code needed to load an image into a frame.</span></span>


```HTML
   <v:vmlframe
     style="top:1;left:1;width:50;height:50">
     src="external.vml#rect01"/>
   </v:vmlframe>
```



<span data-ttu-id="79fb1-133">如果檔案是外部檔案，它必須是 XML 檔。</span><span class="sxs-lookup"><span data-stu-id="79fb1-133">If the file is external, it must be an XML file.</span></span> <span data-ttu-id="79fb1-134">下列程式碼是指定必須包含可識別之圖形的外部原始程式檔時所需的最少程式碼。</span><span class="sxs-lookup"><span data-stu-id="79fb1-134">The following code is the minimum code needed to specify an external source file that must contain an identifiable shape.</span></span> <span data-ttu-id="79fb1-135">此範例包含顯示點陣圖的影像圖形。</span><span class="sxs-lookup"><span data-stu-id="79fb1-135">This sample contains an image shape that displays a bitmap.</span></span>


```HTML
   <xml xmlns:v = "urn:schemas-microsoft-com:vml">
   <v:image id="rect01"
     style="height:100;width:100;top:50;left:50">
     src="kids.jpg">
   </v:rect>
   </xml>
```



> [!Note]  
> <span data-ttu-id="79fb1-136">在 VML 的發行前版本中，這個元素稱為 **VMLCanvas** 。</span><span class="sxs-lookup"><span data-stu-id="79fb1-136">In pre-release versions of VML, this element was called **VMLCanvas** .</span></span>

 

<span data-ttu-id="79fb1-137">**範例**</span><span class="sxs-lookup"><span data-stu-id="79fb1-137">**Examples**</span></span>

-   <span data-ttu-id="79fb1-138">[簡單 VMLFrame 範例](/previous-versions/bb263920(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79fb1-138">[Simple VMLFrame Example](/previous-versions/bb263920(v=vs.85))</span></span>
-   <span data-ttu-id="79fb1-139">[動態 VMLFrame 範例](/previous-versions/bb263902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79fb1-139">[Dynamic VMLFrame Example](/previous-versions/bb263902(v=vs.85))</span></span>

 

 