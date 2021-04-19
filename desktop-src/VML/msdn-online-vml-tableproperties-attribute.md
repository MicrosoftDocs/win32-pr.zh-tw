---
title: VML TableProperties 屬性
description: VML TableProperties 屬性
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967897"
---
# <a name="vml-tableproperties-attribute"></a><span data-ttu-id="30f09-103">VML TableProperties 屬性</span><span class="sxs-lookup"><span data-stu-id="30f09-103">VML TableProperties Attribute</span></span>

<span data-ttu-id="30f09-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="30f09-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="30f09-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="30f09-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="30f09-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="30f09-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="30f09-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="30f09-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="30f09-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="30f09-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="30f09-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="30f09-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="30f09-110">決定資料表屬性。</span><span class="sxs-lookup"><span data-stu-id="30f09-110">Determines table properties.</span></span> <span data-ttu-id="30f09-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="30f09-111">Read/write.</span></span> <span data-ttu-id="30f09-112">**Integer** (整數)。</span><span class="sxs-lookup"><span data-stu-id="30f09-112">**Integer**.</span></span>

<span data-ttu-id="30f09-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="30f09-113">**Applies To**</span></span>

[<span data-ttu-id="30f09-114">形狀</span><span class="sxs-lookup"><span data-stu-id="30f09-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="30f09-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="30f09-115">**Tag Syntax**</span></span>

<span data-ttu-id="30f09-116"><v： *element* o:tableproperties = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="30f09-116"><v: *element* o:tableproperties=" *expression* "></span></span>

<span data-ttu-id="30f09-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="30f09-117">**Remarks**</span></span>

<span data-ttu-id="30f09-118">由 Microsoft PowerPoint 用於原生資料表。</span><span class="sxs-lookup"><span data-stu-id="30f09-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="30f09-119">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="30f09-119">Default value is 0.</span></span> <span data-ttu-id="30f09-120">只會使用這個整數的前三個位。</span><span class="sxs-lookup"><span data-stu-id="30f09-120">Only the first three bits of this integer are used.</span></span>

<span data-ttu-id="30f09-121">雖然此值是儲存在圖形中，但此屬性只有在資料表是由群組的圖形組成時才有用。可以合併位。</span><span class="sxs-lookup"><span data-stu-id="30f09-121">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.Bits may be combined.</span></span>

<span data-ttu-id="30f09-122">包含下列位值。</span><span class="sxs-lookup"><span data-stu-id="30f09-122">The following bit values are included.</span></span>



| <span data-ttu-id="30f09-123">bit</span><span class="sxs-lookup"><span data-stu-id="30f09-123">Bit</span></span> | <span data-ttu-id="30f09-124">描述</span><span class="sxs-lookup"><span data-stu-id="30f09-124">Description</span></span>                              |
|-----|------------------------------------------|
| <span data-ttu-id="30f09-125">1</span><span class="sxs-lookup"><span data-stu-id="30f09-125">1</span></span>   | <span data-ttu-id="30f09-126">設定圖形群組是否為數據表。</span><span class="sxs-lookup"><span data-stu-id="30f09-126">Set if the group of shapes is a table.</span></span>   |
| <span data-ttu-id="30f09-127">2</span><span class="sxs-lookup"><span data-stu-id="30f09-127">2</span></span>   | <span data-ttu-id="30f09-128">設定圖形是否為預留位置。</span><span class="sxs-lookup"><span data-stu-id="30f09-128">Set if the shape is a placeholder.</span></span>       |
| <span data-ttu-id="30f09-129">3</span><span class="sxs-lookup"><span data-stu-id="30f09-129">3</span></span>   | <span data-ttu-id="30f09-130">設定資料表文字是否為雙向。</span><span class="sxs-lookup"><span data-stu-id="30f09-130">Set if the table text is bi-directional.</span></span> |



 

<span data-ttu-id="30f09-131">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="30f09-131">*Microsoft Office Extensions Attribute*</span></span>

 

 