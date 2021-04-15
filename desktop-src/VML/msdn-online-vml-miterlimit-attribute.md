---
title: VML MiterLimit 屬性
description: VML MiterLimit 屬性
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463301"
---
# <a name="vml-miterlimit-attribute"></a><span data-ttu-id="244d4-103">VML MiterLimit 屬性</span><span class="sxs-lookup"><span data-stu-id="244d4-103">VML MiterLimit Attribute</span></span>

<span data-ttu-id="244d4-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="244d4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="244d4-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="244d4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="244d4-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="244d4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="244d4-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="244d4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="244d4-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="244d4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="244d4-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="244d4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="244d4-110">定義斜接接點的平滑。</span><span class="sxs-lookup"><span data-stu-id="244d4-110">Defines the smoothness of the miter joint.</span></span> <span data-ttu-id="244d4-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="244d4-111">Read/write.</span></span> <span data-ttu-id="244d4-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="244d4-112">**VgNumber**.</span></span>

<span data-ttu-id="244d4-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="244d4-113">**Applies To**</span></span>

[<span data-ttu-id="244d4-114">中風</span><span class="sxs-lookup"><span data-stu-id="244d4-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="244d4-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="244d4-115">**Tag Syntax**</span></span>

<span data-ttu-id="244d4-116"><v： *element* miterlimit = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="244d4-116"><v: *element* miterlimit=" *expression* "></span></span>

<span data-ttu-id="244d4-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="244d4-117">**Script Syntax**</span></span>

<span data-ttu-id="244d4-118"> miterlimit = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="244d4-118">*element* .miterlimit="*expression*"</span></span>

<span data-ttu-id="244d4-119">*運算式* =\*\* miterlimit</span><span class="sxs-lookup"><span data-stu-id="244d4-119">*expression*=*element*.miterlimit</span></span>

<span data-ttu-id="244d4-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="244d4-120">**Remarks**</span></span>

<span data-ttu-id="244d4-121">聯合的內部點和外部點之間的最大距離。</span><span class="sxs-lookup"><span data-stu-id="244d4-121">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="244d4-122">此數位是線條粗細的倍數。</span><span class="sxs-lookup"><span data-stu-id="244d4-122">This number is a multiple of the thickness of the line.</span></span>

<span data-ttu-id="244d4-123">預設值為 8。</span><span class="sxs-lookup"><span data-stu-id="244d4-123">The default value is 8.</span></span>

<span data-ttu-id="244d4-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="244d4-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="244d4-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="244d4-125">**Example**</span></span>

<span data-ttu-id="244d4-126">聚合線條上的接點是一個限制為10的接點，也就是5倍的2點。</span><span class="sxs-lookup"><span data-stu-id="244d4-126">The joints on the polyline are mitered with a limit of 10, that is, 5 times 2 points.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 