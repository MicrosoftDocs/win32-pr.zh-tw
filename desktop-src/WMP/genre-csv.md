---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player 線上商店，genre.csv
- 線上商店、genre.csv
- 輸入1個線上商店，genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932424"
---
# <a name="genrecsv"></a><span data-ttu-id="c0845-107">genre.csv</span><span class="sxs-lookup"><span data-stu-id="c0845-107">genre.csv</span></span>

<span data-ttu-id="c0845-108">此檔案包含目錄中所代表之每個類型的專案。</span><span class="sxs-lookup"><span data-stu-id="c0845-108">This file contains an entry for each genre represented in the catalog.</span></span> <span data-ttu-id="c0845-109">每個專案都是由下表所述定位字元分隔欄位所組成的資料列。</span><span class="sxs-lookup"><span data-stu-id="c0845-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="c0845-110">欄位必須依列出的順序出現。</span><span class="sxs-lookup"><span data-stu-id="c0845-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="c0845-111">genre.csv 中的所有欄位都是必要的。</span><span class="sxs-lookup"><span data-stu-id="c0845-111">All fields in genre.csv are required.</span></span>

<span data-ttu-id="c0845-112">下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="c0845-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="c0845-113">它不會參考內容的資料類型。</span><span class="sxs-lookup"><span data-stu-id="c0845-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="c0845-114">例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。</span><span class="sxs-lookup"><span data-stu-id="c0845-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="c0845-115">欄位</span><span class="sxs-lookup"><span data-stu-id="c0845-115">Field</span></span>             | <span data-ttu-id="c0845-116">格式</span><span class="sxs-lookup"><span data-stu-id="c0845-116">Format</span></span>                                                    | <span data-ttu-id="c0845-117">描述</span><span class="sxs-lookup"><span data-stu-id="c0845-117">Description</span></span>                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0845-118">內容類型 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c0845-118">Genre\_ID</span></span>         | <span data-ttu-id="c0845-119">非負整數。範例：22</span><span class="sxs-lookup"><span data-stu-id="c0845-119">Non-negative integer.Example: 22</span></span><br/>               | <span data-ttu-id="c0845-120">內容類型識別碼，在 genre.csv 中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c0845-120">Genre identifier, unique within genre.csv.</span></span> <span data-ttu-id="c0845-121">必須小於 2 ^ 32。</span><span class="sxs-lookup"><span data-stu-id="c0845-121">Must be less than 2^32.</span></span> <span data-ttu-id="c0845-122">最多可以有64的內容。</span><span class="sxs-lookup"><span data-stu-id="c0845-122">A maximum of 64 genres is possible.</span></span>                                             |
| <span data-ttu-id="c0845-123">GenreTitle</span><span class="sxs-lookup"><span data-stu-id="c0845-123">GenreTitle</span></span>        | <span data-ttu-id="c0845-124">Unicode 字串。範例：搖滾</span><span class="sxs-lookup"><span data-stu-id="c0845-124">Unicode string.Example: Rock</span></span><br/>                   | <span data-ttu-id="c0845-125">內容類型顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c0845-125">Genre display name.</span></span>                                                                                                                                |
| <span data-ttu-id="c0845-126">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="c0845-126">FeedsAreAvailable</span></span> | <span data-ttu-id="c0845-127">布林值。格式： \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="c0845-127">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="c0845-128">範例：0</span><span class="sxs-lookup"><span data-stu-id="c0845-128">Example: 0</span></span><br/> | <span data-ttu-id="c0845-129">藉由跳至摘要來指出是否可以使用「無線電播放」行為。</span><span class="sxs-lookup"><span data-stu-id="c0845-129">Indicates whether "radio play" behavior is possible by jumping to a feed.</span></span>                                                                          |
| <span data-ttu-id="c0845-130">HasComposer</span><span class="sxs-lookup"><span data-stu-id="c0845-130">HasComposer</span></span>       | <span data-ttu-id="c0845-131">布林值。格式： \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="c0845-131">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="c0845-132">範例：1</span><span class="sxs-lookup"><span data-stu-id="c0845-132">Example: 1</span></span><br/> | <span data-ttu-id="c0845-133">如果此類型應該將編輯器資訊儲存在目錄中，則為 True。</span><span class="sxs-lookup"><span data-stu-id="c0845-133">True if this genre should save composer information in the catalog.</span></span> <span data-ttu-id="c0845-134">如果未設定，則會忽略編輯器資訊，而不會將它編譯成類別目錄。</span><span class="sxs-lookup"><span data-stu-id="c0845-134">If not set, composer information is ignored and not compiled into the catalog.</span></span> |



 

 

 





