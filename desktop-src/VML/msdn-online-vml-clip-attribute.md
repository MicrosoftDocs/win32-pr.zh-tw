---
title: VML 剪輯屬性
description: VML 剪輯屬性
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967677"
---
# <a name="vml-clip-attribute"></a><span data-ttu-id="51e95-103">VML 剪輯屬性</span><span class="sxs-lookup"><span data-stu-id="51e95-103">VML Clip Attribute</span></span>

<span data-ttu-id="51e95-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="51e95-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="51e95-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="51e95-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="51e95-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="51e95-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="51e95-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="51e95-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="51e95-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="51e95-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="51e95-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="51e95-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="51e95-110">判斷裁剪是否開啟。</span><span class="sxs-lookup"><span data-stu-id="51e95-110">Determines whether the clipping is on.</span></span> <span data-ttu-id="51e95-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51e95-111">Read/write.</span></span> <span data-ttu-id="51e95-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="51e95-112">**VgTriState**.</span></span>

<span data-ttu-id="51e95-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="51e95-113">**Applies To**</span></span>

[<span data-ttu-id="51e95-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="51e95-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="51e95-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="51e95-115">**Tag Syntax**</span></span>

<span data-ttu-id="51e95-116"><v： *element* clip = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="51e95-116"><v: *element* clip=" *expression* "></span></span>

<span data-ttu-id="51e95-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="51e95-117">**Script Syntax**</span></span>

<span data-ttu-id="51e95-118">*元素* 。剪輯 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="51e95-118">*element* .clip="*expression*"</span></span>

<span data-ttu-id="51e95-119">*運算式* =*元素*. 剪輯</span><span class="sxs-lookup"><span data-stu-id="51e95-119">*expression*=*element*.clip</span></span>

<span data-ttu-id="51e95-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="51e95-120">**Remarks**</span></span>

<span data-ttu-id="51e95-121">如果 **剪輯** 為 **False**，圖形將會縮放以符合框架。</span><span class="sxs-lookup"><span data-stu-id="51e95-121">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="51e95-122">若 **為 True**，將不會顯示框架外之圖形的任何部分。</span><span class="sxs-lookup"><span data-stu-id="51e95-122">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="51e95-123">請注意，除非 **剪輯** 為 **True**，否則不會使用 [原始](origin-attribute--vmlframe--vml.md)和 [大小](size-attribute--vmlframe.md)。</span><span class="sxs-lookup"><span data-stu-id="51e95-123">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="51e95-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="51e95-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="51e95-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="51e95-125">**Example**</span></span>

<span data-ttu-id="51e95-126">外部檔案中定義的映射將會被裁剪。</span><span class="sxs-lookup"><span data-stu-id="51e95-126">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 