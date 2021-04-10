---
title: VML ConnectType 屬性
description: VML ConnectType 屬性
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092743"
---
# <a name="vml-connecttype-attribute"></a><span data-ttu-id="102df-103">VML ConnectType 屬性</span><span class="sxs-lookup"><span data-stu-id="102df-103">VML ConnectType Attribute</span></span>

<span data-ttu-id="102df-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="102df-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="102df-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="102df-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="102df-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="102df-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="102df-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="102df-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="102df-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="102df-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="102df-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="102df-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="102df-110">定義用來將圖形附加至其他圖形的連接點類型。</span><span class="sxs-lookup"><span data-stu-id="102df-110">Defines the type of connection points used for attaching shapes to other shapes.</span></span> <span data-ttu-id="102df-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="102df-111">Read/write.</span></span> <span data-ttu-id="102df-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="102df-112">**String**.</span></span>

<span data-ttu-id="102df-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="102df-113">**Applies To**</span></span>

[<span data-ttu-id="102df-114">路徑</span><span class="sxs-lookup"><span data-stu-id="102df-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="102df-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="102df-115">**Tag Syntax**</span></span>

<span data-ttu-id="102df-116"><v： *element* o:connecttype = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="102df-116"><v: *element* o:connecttype=" *expression* "></span></span>

<span data-ttu-id="102df-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="102df-117">**Remarks**</span></span>

<span data-ttu-id="102df-118">數值包括：</span><span class="sxs-lookup"><span data-stu-id="102df-118">Values include:</span></span>



| <span data-ttu-id="102df-119">值</span><span class="sxs-lookup"><span data-stu-id="102df-119">Value</span></span>    | <span data-ttu-id="102df-120">描述</span><span class="sxs-lookup"><span data-stu-id="102df-120">Description</span></span>                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102df-121">無</span><span class="sxs-lookup"><span data-stu-id="102df-121">none</span></span>     | <span data-ttu-id="102df-122">沒有連接網站。</span><span class="sxs-lookup"><span data-stu-id="102df-122">No connection sites.</span></span> <span data-ttu-id="102df-123">預設值。</span><span class="sxs-lookup"><span data-stu-id="102df-123">Default.</span></span>                                                                                                         |
| <span data-ttu-id="102df-124">rect</span><span class="sxs-lookup"><span data-stu-id="102df-124">rect</span></span>     | <span data-ttu-id="102df-125">標準四個連接點位於頂端、底部、左方和右邊的點。</span><span class="sxs-lookup"><span data-stu-id="102df-125">Standard four connection points at midpoints of top, bottom, left, and right sides.</span></span>                                                   |
| <span data-ttu-id="102df-126">區段</span><span class="sxs-lookup"><span data-stu-id="102df-126">segments</span></span> | <span data-ttu-id="102df-127">使用圖形的編輯點。</span><span class="sxs-lookup"><span data-stu-id="102df-127">The edit points of the shape are used.</span></span> <span data-ttu-id="102df-128">編輯點是圖形化編輯器中用來選取圖形元件的黑色點。</span><span class="sxs-lookup"><span data-stu-id="102df-128">Edit points are the black dots in a graphical editor that are used to select parts of a shape.</span></span> |
| <span data-ttu-id="102df-129">自訂</span><span class="sxs-lookup"><span data-stu-id="102df-129">custom</span></span>   | <span data-ttu-id="102df-130">連接位置的自訂陣列。</span><span class="sxs-lookup"><span data-stu-id="102df-130">A custom array of connection locations.</span></span>                                                                                               |



 

<span data-ttu-id="102df-131">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="102df-131">*Microsoft Office Extensions Attribute*</span></span>

 

 