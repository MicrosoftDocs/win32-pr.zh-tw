---
title: VML InvX 屬性
description: VML InvX 屬性
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682551"
---
# <a name="vml-invx-attribute"></a><span data-ttu-id="fd9a4-103">VML InvX 屬性</span><span class="sxs-lookup"><span data-stu-id="fd9a4-103">VML InvX Attribute</span></span>

<span data-ttu-id="fd9a4-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fd9a4-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fd9a4-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fd9a4-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fd9a4-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fd9a4-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fd9a4-110">判斷控制碼的 x 位置是否反轉。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-110">Determines whether the x position of the handle is inverted.</span></span> <span data-ttu-id="fd9a4-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd9a4-111">Read/write.</span></span> <span data-ttu-id="fd9a4-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-112">**VgTriState**.</span></span>

<span data-ttu-id="fd9a4-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="fd9a4-113">**Applies To**</span></span>

<span data-ttu-id="fd9a4-114">[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) </span><span class="sxs-lookup"><span data-stu-id="fd9a4-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="fd9a4-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="fd9a4-115">**Tag Syntax**</span></span>

<span data-ttu-id="fd9a4-116"><v： *element* invx = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="fd9a4-116"><v: *element* invx=" *expression* "></span></span>

<span data-ttu-id="fd9a4-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="fd9a4-117">**Remarks**</span></span>

<span data-ttu-id="fd9a4-118">若 **為 True**，則會將 **CoordOrigin** x 值的 x 值減去 **CoordSize** 的 x 值，以反轉控制碼的 x 位置。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-118">If **True**, the x position of the handle is inverted by subtracting the x value from the x value of **CoordOrigin** added to the x value of **CoordSize**.</span></span> <span data-ttu-id="fd9a4-119">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="fd9a4-119">The default value is **False**.</span></span>

<span data-ttu-id="fd9a4-120">這個屬性等同于</span><span class="sxs-lookup"><span data-stu-id="fd9a4-120">This attribute is the equivalent of</span></span>

<span data-ttu-id="fd9a4-121">coordorigin. x + coordsize. x-h. x</span><span class="sxs-lookup"><span data-stu-id="fd9a4-121">coordorigin.x + coordsize.x - h.position.x</span></span>

<span data-ttu-id="fd9a4-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="fd9a4-122">*VML Standard Attribute*</span></span>

 

 