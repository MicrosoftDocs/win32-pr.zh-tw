---
title: VML InvY 屬性
description: VML InvY 屬性
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315535"
---
# <a name="vml-invy-attribute"></a><span data-ttu-id="b25a8-103">VML InvY 屬性</span><span class="sxs-lookup"><span data-stu-id="b25a8-103">VML InvY Attribute</span></span>

<span data-ttu-id="b25a8-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b25a8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b25a8-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b25a8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b25a8-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b25a8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b25a8-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b25a8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b25a8-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b25a8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b25a8-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b25a8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b25a8-110">判斷控制碼的 y 位置是否反轉。</span><span class="sxs-lookup"><span data-stu-id="b25a8-110">Determines whether the y position of the handle is inverted.</span></span> <span data-ttu-id="b25a8-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b25a8-111">Read/write.</span></span> <span data-ttu-id="b25a8-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="b25a8-112">**VgTriState**.</span></span>

<span data-ttu-id="b25a8-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b25a8-113">**Applies To**</span></span>

<span data-ttu-id="b25a8-114">[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) </span><span class="sxs-lookup"><span data-stu-id="b25a8-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="b25a8-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b25a8-115">**Tag Syntax**</span></span>

<span data-ttu-id="b25a8-116"><v： *element* invy = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b25a8-116"><v: *element* invy=" *expression* "></span></span>

<span data-ttu-id="b25a8-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="b25a8-117">**Remarks**</span></span>

<span data-ttu-id="b25a8-118">若 **為 True**，則會將控制碼的 y 位置從 **CoordOrigin** 的 y 值減去 **CoordSize** 的 y 值，以反轉方向。</span><span class="sxs-lookup"><span data-stu-id="b25a8-118">If **True**, the y position of the handle is inverted by subtracting the y value from the y value of **CoordOrigin** added to the y value of **CoordSize**.</span></span> <span data-ttu-id="b25a8-119">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="b25a8-119">The default value is **False**.</span></span>

<span data-ttu-id="b25a8-120">這個屬性等同于</span><span class="sxs-lookup"><span data-stu-id="b25a8-120">This attribute is the equivalent of</span></span>


```HTML
coordorigin.y + coordsize.y - h.position.y
```



<span data-ttu-id="b25a8-121">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b25a8-121">*VML Standard Attribute*</span></span>

 

 