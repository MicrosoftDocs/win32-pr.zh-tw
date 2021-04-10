---
title: VML ForceDash 屬性
description: VML ForceDash 屬性
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023786"
---
# <a name="vml-forcedash-attribute"></a><span data-ttu-id="716f9-103">VML ForceDash 屬性</span><span class="sxs-lookup"><span data-stu-id="716f9-103">VML ForceDash Attribute</span></span>

<span data-ttu-id="716f9-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="716f9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="716f9-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="716f9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="716f9-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="716f9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="716f9-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="716f9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="716f9-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="716f9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="716f9-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="716f9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="716f9-110">決定當圖形沒有線條或填滿時，是否使用虛線輪廓繪製圖形。</span><span class="sxs-lookup"><span data-stu-id="716f9-110">Determines whether a dashed outline is used to draw a shape when a shape has no line or fill.</span></span> <span data-ttu-id="716f9-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="716f9-111">Read/write.</span></span> <span data-ttu-id="716f9-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="716f9-112">**VgTriState**.</span></span>

<span data-ttu-id="716f9-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="716f9-113">**Applies To**</span></span>

[<span data-ttu-id="716f9-114">形狀</span><span class="sxs-lookup"><span data-stu-id="716f9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="716f9-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="716f9-115">**Tag Syntax**</span></span>

<span data-ttu-id="716f9-116"><v： *element* o:forcedash = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="716f9-116"><v: *element* o:forcedash=" *expression* "></span></span>

<span data-ttu-id="716f9-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="716f9-117">**Remarks**</span></span>

<span data-ttu-id="716f9-118">當圖形沒有線條且沒有填滿時，由 Microsoft PowerPoint 預留位置用來繪製虛線外框。</span><span class="sxs-lookup"><span data-stu-id="716f9-118">Used by Microsoft PowerPoint placeholders to draw a dashed outline when there is no line and no fill for a shape.</span></span> <span data-ttu-id="716f9-119">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="716f9-119">Default is **False**.</span></span> <span data-ttu-id="716f9-120">若 **為 True**，則會使用虛線外框來表示預留位置。</span><span class="sxs-lookup"><span data-stu-id="716f9-120">If **True**, a dashed outline will be used to indicate a placeholder.</span></span>

<span data-ttu-id="716f9-121">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="716f9-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="716f9-122">**範例**</span><span class="sxs-lookup"><span data-stu-id="716f9-122">**Example**</span></span>

<span data-ttu-id="716f9-123">如果沒有線條或填滿，則會使用虛線來呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="716f9-123">A dashed line will be used to render the shape if there is no line or fill.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 