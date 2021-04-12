---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Windows Media Player 線上商店，listitem.csv
- 線上商店、listitem.csv
- 輸入1個線上商店，listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372055"
---
# <a name="listitemcsv"></a><span data-ttu-id="fa77f-107">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="fa77f-107">listitem.csv</span></span>

<span data-ttu-id="fa77f-108">此檔案包含清單中所包含之每個專案的專案。</span><span class="sxs-lookup"><span data-stu-id="fa77f-108">This file contains entries for each item that is included in a list.</span></span> <span data-ttu-id="fa77f-109">每個專案都是由下表所述定位字元分隔欄位所組成的資料列。</span><span class="sxs-lookup"><span data-stu-id="fa77f-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="fa77f-110">欄位必須依列出的順序出現。</span><span class="sxs-lookup"><span data-stu-id="fa77f-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="fa77f-111">所有欄位皆為必填項目。</span><span class="sxs-lookup"><span data-stu-id="fa77f-111">All fields are required.</span></span>

<span data-ttu-id="fa77f-112">下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="fa77f-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="fa77f-113">它不會參考內容的資料類型。</span><span class="sxs-lookup"><span data-stu-id="fa77f-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="fa77f-114">例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。</span><span class="sxs-lookup"><span data-stu-id="fa77f-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="fa77f-115">欄位</span><span class="sxs-lookup"><span data-stu-id="fa77f-115">Field</span></span>              | <span data-ttu-id="fa77f-116">格式</span><span class="sxs-lookup"><span data-stu-id="fa77f-116">Format</span></span>                                          | <span data-ttu-id="fa77f-117">描述</span><span class="sxs-lookup"><span data-stu-id="fa77f-117">Description</span></span>                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa77f-118">連結的 \_ ListID</span><span class="sxs-lookup"><span data-stu-id="fa77f-118">Linked\_ListID</span></span>     | <span data-ttu-id="fa77f-119">非負整數。範例：465</span><span class="sxs-lookup"><span data-stu-id="fa77f-119">Non-negative integer.Example: 465</span></span><br/>    | <span data-ttu-id="fa77f-120">此專案所屬清單的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa77f-120">The ID of the list this item is part of.</span></span>                                                                               |
| <span data-ttu-id="fa77f-121">連結 \_ 的</span><span class="sxs-lookup"><span data-stu-id="fa77f-121">Linked\_ListItem</span></span>   | <span data-ttu-id="fa77f-122">非負整數。範例：684793</span><span class="sxs-lookup"><span data-stu-id="fa77f-122">Non-negative integer.Example: 684793</span></span><br/> | <span data-ttu-id="fa77f-123">項目的 ID。</span><span class="sxs-lookup"><span data-stu-id="fa77f-123">The ID of the item.</span></span> <span data-ttu-id="fa77f-124">可以是曲目的識別碼、專輯、演出者、內容類型、subgenre、廣播或其他清單。</span><span class="sxs-lookup"><span data-stu-id="fa77f-124">Can be the ID of a track, an album, an artist, a genre, a subgenre, a radio feed, or another list.</span></span> |
| <span data-ttu-id="fa77f-125">ItemPositionInList</span><span class="sxs-lookup"><span data-stu-id="fa77f-125">ItemPositionInList</span></span> | <span data-ttu-id="fa77f-126">非負整數。範例：5</span><span class="sxs-lookup"><span data-stu-id="fa77f-126">Non-negative integer.Example: 5</span></span><br/>      | <span data-ttu-id="fa77f-127">專案在其清單中的位置。</span><span class="sxs-lookup"><span data-stu-id="fa77f-127">The position of the item within its list.</span></span> <span data-ttu-id="fa77f-128">清單中的第一個專案位於位置0。</span><span class="sxs-lookup"><span data-stu-id="fa77f-128">The first item in a list is at position 0.</span></span>                                   |



 

 

 





