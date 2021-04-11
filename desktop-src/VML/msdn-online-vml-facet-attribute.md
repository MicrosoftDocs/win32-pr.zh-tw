---
title: VML Facet 屬性
description: VML Facet 屬性
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d4fec254ff3e6af35d82cd45146c201701555b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092833"
---
# <a name="vml-facet-attribute"></a><span data-ttu-id="bf74b-103">VML Facet 屬性</span><span class="sxs-lookup"><span data-stu-id="bf74b-103">VML Facet Attribute</span></span>

<span data-ttu-id="bf74b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="bf74b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bf74b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="bf74b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bf74b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="bf74b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bf74b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="bf74b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bf74b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="bf74b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bf74b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="bf74b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bf74b-110">定義用來描述拉伸曲線表面的 facet 數目。</span><span class="sxs-lookup"><span data-stu-id="bf74b-110">Defines the number of facets used to describe curved surfaces of an extrusion.</span></span> <span data-ttu-id="bf74b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf74b-111">Read/write.</span></span> <span data-ttu-id="bf74b-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="bf74b-112">**VgNumber**.</span></span>

<span data-ttu-id="bf74b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="bf74b-113">**Applies To**</span></span>

[<span data-ttu-id="bf74b-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="bf74b-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="bf74b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="bf74b-115">**Tag Syntax**</span></span>

<span data-ttu-id="bf74b-116"><o： *element* facet = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="bf74b-116"><o: *element* facet=" *expression* "></span></span>

<span data-ttu-id="bf74b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="bf74b-117">**Script Syntax**</span></span>

<span data-ttu-id="bf74b-118">*元素* 。 facet = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="bf74b-118">*element* .facet="*expression*"</span></span>

<span data-ttu-id="bf74b-119">*運算式* =*元素*。 facet</span><span class="sxs-lookup"><span data-stu-id="bf74b-119">*expression*=*element*.facet</span></span>

<span data-ttu-id="bf74b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="bf74b-120">**Remarks**</span></span>

<span data-ttu-id="bf74b-121">定義轉譯引擎將接近延伸的方式。</span><span class="sxs-lookup"><span data-stu-id="bf74b-121">Defines the way that a rendering engine will approximate the extrusion.</span></span> <span data-ttu-id="bf74b-122">較低的數位會表示轉譯引擎的轉譯容錯較低，而且會產生更多 facet。</span><span class="sxs-lookup"><span data-stu-id="bf74b-122">A lower number will indicate a lower rendering tolerance to the rendering engine and will yield more facets.</span></span> <span data-ttu-id="bf74b-123">較高的數位會讓您的延伸顯示更多面向。</span><span class="sxs-lookup"><span data-stu-id="bf74b-123">Higher numbers will make the extrusion appear more faceted.</span></span> <span data-ttu-id="bf74b-124">預設值為30000。</span><span class="sxs-lookup"><span data-stu-id="bf74b-124">The default value is 30,000.</span></span>

<span data-ttu-id="bf74b-125">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="bf74b-125">*Microsoft Office Extensions Attribute*</span></span>

 

 