---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player 線上商店，artist.csv
- 線上商店、artist.csv
- 輸入1個線上商店，artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311349"
---
# <a name="artistcsv"></a><span data-ttu-id="30a64-107">artist.csv</span><span class="sxs-lookup"><span data-stu-id="30a64-107">artist.csv</span></span>

<span data-ttu-id="30a64-108">此檔案包含目錄中每個演出者的專案。</span><span class="sxs-lookup"><span data-stu-id="30a64-108">This file contains an entry for each artist in the catalog.</span></span> <span data-ttu-id="30a64-109">每個專案都是由下表所述定位字元分隔欄位所組成的資料列。</span><span class="sxs-lookup"><span data-stu-id="30a64-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="30a64-110">欄位必須依列出的順序出現。</span><span class="sxs-lookup"><span data-stu-id="30a64-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="30a64-111">artist.csv 中的所有欄位都是必要的。</span><span class="sxs-lookup"><span data-stu-id="30a64-111">All fields in artist.csv are required.</span></span>

<span data-ttu-id="30a64-112">下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="30a64-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="30a64-113">它不會參考內容的資料類型。</span><span class="sxs-lookup"><span data-stu-id="30a64-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="30a64-114">例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。</span><span class="sxs-lookup"><span data-stu-id="30a64-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="30a64-115">欄位</span><span class="sxs-lookup"><span data-stu-id="30a64-115">Field</span></span>                  | <span data-ttu-id="30a64-116">格式</span><span class="sxs-lookup"><span data-stu-id="30a64-116">Format</span></span>                                            | <span data-ttu-id="30a64-117">描述</span><span class="sxs-lookup"><span data-stu-id="30a64-117">Description</span></span>                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a64-118">ArtistID</span><span class="sxs-lookup"><span data-stu-id="30a64-118">ArtistID</span></span>               | <span data-ttu-id="30a64-119">非負整數。</span><span class="sxs-lookup"><span data-stu-id="30a64-119">Non-negative integer.</span></span> <span data-ttu-id="30a64-120">範例：65832</span><span class="sxs-lookup"><span data-stu-id="30a64-120">Example: 65832</span></span>              | <span data-ttu-id="30a64-121">演出者的唯一識別碼，artist.csv 中唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="30a64-121">Unique identifier for the artist, unique within artist.csv.</span></span> <span data-ttu-id="30a64-122">必須小於 2 ^ 32。</span><span class="sxs-lookup"><span data-stu-id="30a64-122">Must be less than 2^32.</span></span>                        |
| <span data-ttu-id="30a64-123">ArtistName</span><span class="sxs-lookup"><span data-stu-id="30a64-123">ArtistName</span></span>             | <span data-ttu-id="30a64-124">Unicode 字串。範例： Don Funk</span><span class="sxs-lookup"><span data-stu-id="30a64-124">Unicode string.Example: Don Funk</span></span><br/>       | <span data-ttu-id="30a64-125">演出者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="30a64-125">Display name for the artist.</span></span>                                                                               |
| <span data-ttu-id="30a64-126">LinkedGenreID</span><span class="sxs-lookup"><span data-stu-id="30a64-126">LinkedGenreID</span></span>          | <span data-ttu-id="30a64-127">非負整數。範例：313</span><span class="sxs-lookup"><span data-stu-id="30a64-127">Non-negative integer.Example: 313</span></span><br/>      | <span data-ttu-id="30a64-128">演出者主要內容類型的 GenreID。</span><span class="sxs-lookup"><span data-stu-id="30a64-128">GenreID of the artist's primary genre.</span></span> <span data-ttu-id="30a64-129">必須是主要的類型，而不是 subgenre。</span><span class="sxs-lookup"><span data-stu-id="30a64-129">Must be a main genre and not a subgenre.</span></span> <span data-ttu-id="30a64-130">只允許一個值。</span><span class="sxs-lookup"><span data-stu-id="30a64-130">Only one value is allowed.</span></span> |
| <span data-ttu-id="30a64-131">LinkedSimilarArtistIDs</span><span class="sxs-lookup"><span data-stu-id="30a64-131">LinkedSimilarArtistIDs</span></span> | <span data-ttu-id="30a64-132">N/A</span><span class="sxs-lookup"><span data-stu-id="30a64-132">N/A</span></span>                                               | <span data-ttu-id="30a64-133">未在此版本中使用。</span><span class="sxs-lookup"><span data-stu-id="30a64-133">Not used in this release.</span></span> <span data-ttu-id="30a64-134">應為空白。</span><span class="sxs-lookup"><span data-stu-id="30a64-134">Should be empty.</span></span>                                                                 |
| <span data-ttu-id="30a64-135">熱門程度</span><span class="sxs-lookup"><span data-stu-id="30a64-135">Popularity</span></span>             | <span data-ttu-id="30a64-136">可以是整數或十進位值。</span><span class="sxs-lookup"><span data-stu-id="30a64-136">Can be integer or decimal value.</span></span> <span data-ttu-id="30a64-137">範例：1252.25</span><span class="sxs-lookup"><span data-stu-id="30a64-137">Example: 1252.25</span></span> | <span data-ttu-id="30a64-138">熱門等級。</span><span class="sxs-lookup"><span data-stu-id="30a64-138">Popularity ranking.</span></span> <span data-ttu-id="30a64-139">依熱門程度排序時，可以是清單中的位置。</span><span class="sxs-lookup"><span data-stu-id="30a64-139">Can be the position in the list when sorted by popularity.</span></span>                             |
| <span data-ttu-id="30a64-140">FeedsAvailable</span><span class="sxs-lookup"><span data-stu-id="30a64-140">FeedsAvailable</span></span>         | <span data-ttu-id="30a64-141">布林值。</span><span class="sxs-lookup"><span data-stu-id="30a64-141">Boolean.</span></span> <span data-ttu-id="30a64-142">格式： \[ 0 \| 1 \] 範例：0</span><span class="sxs-lookup"><span data-stu-id="30a64-142">Format: \[0\|1\]Example: 0</span></span><br/>    | <span data-ttu-id="30a64-143">未在此版本中使用。</span><span class="sxs-lookup"><span data-stu-id="30a64-143">Not used in this release.</span></span> <span data-ttu-id="30a64-144">應為空白。</span><span class="sxs-lookup"><span data-stu-id="30a64-144">Should be empty.</span></span>                                                                 |



 

 

 





