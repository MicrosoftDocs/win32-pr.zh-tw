---
title: VML Specularity 屬性
description: VML Specularity 屬性
ms.assetid: df04c15c-cfad-4172-81fa-a28e13f205fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b4e8814a9bd0cd897ae018cf8b37aa67d732aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842463"
---
# <a name="vml-specularity-attribute"></a><span data-ttu-id="2e92e-103">VML Specularity 屬性</span><span class="sxs-lookup"><span data-stu-id="2e92e-103">VML Specularity Attribute</span></span>

<span data-ttu-id="2e92e-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="2e92e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2e92e-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="2e92e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2e92e-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="2e92e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2e92e-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="2e92e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2e92e-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="2e92e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2e92e-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="2e92e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2e92e-110">定義拉伸圖形的 specularity。</span><span class="sxs-lookup"><span data-stu-id="2e92e-110">Defines the specularity of an extruded shape.</span></span> <span data-ttu-id="2e92e-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e92e-111">Read/write.</span></span> <span data-ttu-id="2e92e-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="2e92e-112">**VgNumber**.</span></span>

<span data-ttu-id="2e92e-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="2e92e-113">**Applies To**</span></span>

[<span data-ttu-id="2e92e-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="2e92e-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="2e92e-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="2e92e-115">**Tag Syntax**</span></span>

<span data-ttu-id="2e92e-116"><o： *element* specularity = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2e92e-116"><o: *element* specularity=" *expression* "></span></span>

<span data-ttu-id="2e92e-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="2e92e-117">**Script Syntax**</span></span>

<span data-ttu-id="2e92e-118"> specularity = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2e92e-118">*element* .specularity="*expression*"</span></span>

<span data-ttu-id="2e92e-119">*運算式* =\*\* specularity</span><span class="sxs-lookup"><span data-stu-id="2e92e-119">*expression*=*element*.specularity</span></span>

<span data-ttu-id="2e92e-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="2e92e-120">**Remarks**</span></span>

<span data-ttu-id="2e92e-121">此值會定義事件光線對反射反映光線的比率。</span><span class="sxs-lookup"><span data-stu-id="2e92e-121">This value defines the ratio of incident light to specularly reflected light.</span></span> <span data-ttu-id="2e92e-122">標準值的範圍是從0到1。</span><span class="sxs-lookup"><span data-stu-id="2e92e-122">Normal values range from 0 to 1.</span></span> <span data-ttu-id="2e92e-123">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="2e92e-123">The default value is 0.</span></span>

<span data-ttu-id="2e92e-124">如果指定大於1的值，則可能會產生不尋常的效果。</span><span class="sxs-lookup"><span data-stu-id="2e92e-124">If values greater than 1 are specified, unusual effects can result.</span></span>

<span data-ttu-id="2e92e-125">Microsoft Office Extensions 屬性</span><span class="sxs-lookup"><span data-stu-id="2e92e-125">Microsoft Office Extensions Attribute</span></span>

 

 