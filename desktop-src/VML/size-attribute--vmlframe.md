---
title: 'Size 屬性 (VMLFrame) '
description: 'Size 屬性 (VMLFrame) '
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023540"
---
# <a name="size-attribute-vmlframe"></a><span data-ttu-id="ef4c7-103">Size 屬性 (VMLFrame) </span><span class="sxs-lookup"><span data-stu-id="ef4c7-103">Size Attribute (VMLFrame)</span></span>

<span data-ttu-id="ef4c7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ef4c7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ef4c7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ef4c7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ef4c7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ef4c7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ef4c7-110">定義框架裁剪區域的大小。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-110">Defines the size of the clipping region of the frame.</span></span> <span data-ttu-id="ef4c7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ef4c7-111">Read/write.</span></span> <span data-ttu-id="ef4c7-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-112">**VgVector2D**.</span></span>

<span data-ttu-id="ef4c7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-113">**Applies To**</span></span>

[<span data-ttu-id="ef4c7-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="ef4c7-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="ef4c7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-115">**Tag Syntax**</span></span>

<span data-ttu-id="ef4c7-116"><v： *element* size = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ef4c7-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="ef4c7-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-117">**Script Syntax**</span></span>

<span data-ttu-id="ef4c7-118">*元素* 。 size = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ef4c7-118">*element* .size="*expression*"</span></span>

<span data-ttu-id="ef4c7-119">*運算式* =*元素*。大小</span><span class="sxs-lookup"><span data-stu-id="ef4c7-119">*expression*=*element*.size</span></span>

<span data-ttu-id="ef4c7-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-120">**Remarks**</span></span>

<span data-ttu-id="ef4c7-121">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-121">The default value is 0,0.</span></span> <span data-ttu-id="ef4c7-122">請注意，只有當 [剪輯](msdn-online-vml-clip-attribute.md)為 **True** 時，**大小** 才會運作。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-122">Note that **Size** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="ef4c7-123">在這個屬性中，大小會定義為框架的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-123">In this attribute, the size is defined as the width and height of the frame.</span></span>

<span data-ttu-id="ef4c7-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="ef4c7-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ef4c7-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-125">**Example**</span></span>

<span data-ttu-id="ef4c7-126">裁剪區域的大小將會是50pt，50pt。</span><span class="sxs-lookup"><span data-stu-id="ef4c7-126">The size of the clipping region will be 50pt, 50pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 