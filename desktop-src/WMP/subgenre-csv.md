---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player 線上商店，subgenre.csv
- 線上商店、subgenre.csv
- 輸入1個線上商店，subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969479"
---
# <a name="subgenrecsv"></a><span data-ttu-id="96bbd-107">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="96bbd-107">subgenre.csv</span></span>

<span data-ttu-id="96bbd-108">此檔案包含目錄中所代表之每個 subgenre 的專案。</span><span class="sxs-lookup"><span data-stu-id="96bbd-108">This file contains an entry for each subgenre represented in the catalog.</span></span> <span data-ttu-id="96bbd-109">每個專案都是由下表所述定位字元分隔欄位所組成的資料列。</span><span class="sxs-lookup"><span data-stu-id="96bbd-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="96bbd-110">欄位必須依列出的順序出現。</span><span class="sxs-lookup"><span data-stu-id="96bbd-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="96bbd-111">下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="96bbd-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="96bbd-112">它不會參考內容的資料類型。</span><span class="sxs-lookup"><span data-stu-id="96bbd-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="96bbd-113">例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。</span><span class="sxs-lookup"><span data-stu-id="96bbd-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="96bbd-114">欄位</span><span class="sxs-lookup"><span data-stu-id="96bbd-114">Field</span></span>             | <span data-ttu-id="96bbd-115">必要</span><span class="sxs-lookup"><span data-stu-id="96bbd-115">Required</span></span> | <span data-ttu-id="96bbd-116">格式</span><span class="sxs-lookup"><span data-stu-id="96bbd-116">Format</span></span>                                                                                            | <span data-ttu-id="96bbd-117">描述</span><span class="sxs-lookup"><span data-stu-id="96bbd-117">Description</span></span>                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96bbd-118">SubGenreID</span><span class="sxs-lookup"><span data-stu-id="96bbd-118">SubGenreID</span></span>        | <span data-ttu-id="96bbd-119">Yes</span><span class="sxs-lookup"><span data-stu-id="96bbd-119">Yes</span></span>      | <span data-ttu-id="96bbd-120">非負整數。</span><span class="sxs-lookup"><span data-stu-id="96bbd-120">Non-negative integer.</span></span>                                                                             | <span data-ttu-id="96bbd-121">Subgenre 識別碼 (識別碼) ，在 subgenre.csv 中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="96bbd-121">Subgenre identifier (ID), unique within subgenre.csv.</span></span> <span data-ttu-id="96bbd-122">最多允許 1024 subgenres。</span><span class="sxs-lookup"><span data-stu-id="96bbd-122">Up to 1024 subgenres are allowed.</span></span>                                                                   |
| <span data-ttu-id="96bbd-123">SubGenreTitle</span><span class="sxs-lookup"><span data-stu-id="96bbd-123">SubGenreTitle</span></span>     | <span data-ttu-id="96bbd-124">Yes</span><span class="sxs-lookup"><span data-stu-id="96bbd-124">Yes</span></span>      | <span data-ttu-id="96bbd-125">Unicode 字串。範例：智慧型 Dance 音樂 (IDM) </span><span class="sxs-lookup"><span data-stu-id="96bbd-125">Unicode string.Example: Intelligent Dance Music (IDM)</span></span><br/>                                  | <span data-ttu-id="96bbd-126">Subgenre 顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="96bbd-126">Subgenre display name.</span></span>                                                                                                                                    |
| <span data-ttu-id="96bbd-127">SubGenreSubtitle</span><span class="sxs-lookup"><span data-stu-id="96bbd-127">SubGenreSubtitle</span></span>  | <span data-ttu-id="96bbd-128">No</span><span class="sxs-lookup"><span data-stu-id="96bbd-128">No</span></span>       | <span data-ttu-id="96bbd-129">Unicode 字串。範例： New、percussive 電子音樂，不是單純的技術。</span><span class="sxs-lookup"><span data-stu-id="96bbd-129">Unicode string.Example: New, percussive electronic music that's not quite pure techno.</span></span><br/> | <span data-ttu-id="96bbd-130">描述 subgenre 顯示名稱的意義。</span><span class="sxs-lookup"><span data-stu-id="96bbd-130">Describe the meaning of the subgenre display name.</span></span> <span data-ttu-id="96bbd-131">應小於64個字元。</span><span class="sxs-lookup"><span data-stu-id="96bbd-131">Should be less than 64 characters.</span></span>                                                                     |
| <span data-ttu-id="96bbd-132">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="96bbd-132">FeedsAreAvailable</span></span> | <span data-ttu-id="96bbd-133">Yes</span><span class="sxs-lookup"><span data-stu-id="96bbd-133">Yes</span></span>      | <span data-ttu-id="96bbd-134">布林值。格式： \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="96bbd-134">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="96bbd-135">範例：0</span><span class="sxs-lookup"><span data-stu-id="96bbd-135">Example: 0</span></span><br/>                                         | <span data-ttu-id="96bbd-136">藉由跳至摘要來指出是否可以使用「無線電播放」。</span><span class="sxs-lookup"><span data-stu-id="96bbd-136">Indicates whether "radio play" is possible by jumping to a feed.</span></span>                                                                                          |
| <span data-ttu-id="96bbd-137">連結的 \_ GenreID</span><span class="sxs-lookup"><span data-stu-id="96bbd-137">Linked\_GenreID</span></span>   | <span data-ttu-id="96bbd-138">Yes</span><span class="sxs-lookup"><span data-stu-id="96bbd-138">Yes</span></span>      | <span data-ttu-id="96bbd-139">非負整數 (GenreID) 。範例：12</span><span class="sxs-lookup"><span data-stu-id="96bbd-139">Non-negative integer (GenreID).Example: 12</span></span><br/>                                             | <span data-ttu-id="96bbd-140">父類型的 GenreID。</span><span class="sxs-lookup"><span data-stu-id="96bbd-140">The GenreID of the parent genre.</span></span> <span data-ttu-id="96bbd-141">只允許一個父系。</span><span class="sxs-lookup"><span data-stu-id="96bbd-141">Only one parent is allowed.</span></span>                                                                                              |
| <span data-ttu-id="96bbd-142">SortOrderRank</span><span class="sxs-lookup"><span data-stu-id="96bbd-142">SortOrderRank</span></span>     | <span data-ttu-id="96bbd-143">Yes</span><span class="sxs-lookup"><span data-stu-id="96bbd-143">Yes</span></span>      | <span data-ttu-id="96bbd-144">非負整數。範例：23</span><span class="sxs-lookup"><span data-stu-id="96bbd-144">Non-negative integer.Example: 23</span></span><br/>                                                       | <span data-ttu-id="96bbd-145">在使用者介面中用來排序 subgenres 的排名，最好是唯一的。</span><span class="sxs-lookup"><span data-stu-id="96bbd-145">A ranking, ideally unique, used for sorting subgenres in the user interface.</span></span> <span data-ttu-id="96bbd-146">如果父類型有10個 subgenres，則這可能是從1到10的整數。</span><span class="sxs-lookup"><span data-stu-id="96bbd-146">If the parent genre has 10 subgenres, this might be an integer from 1 to 10.</span></span> |



 

 

 





