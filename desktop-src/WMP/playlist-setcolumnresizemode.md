---
title: 播放清單。 setColumnResizeMode
description: SetColumnResizeMode 方法會指定索引資料行本身的大小。
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- 播放清單. setColumnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978528"
---
# <a name="playlistsetcolumnresizemode"></a><span data-ttu-id="66589-104">播放清單。 setColumnResizeMode</span><span class="sxs-lookup"><span data-stu-id="66589-104">PLAYLIST.setColumnResizeMode</span></span>

<span data-ttu-id="66589-105">**SetColumnResizeMode** 方法會指定索引資料行本身的大小。</span><span class="sxs-lookup"><span data-stu-id="66589-105">The **setColumnResizeMode** method specifies how the indexed column sizes itself.</span></span>

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a><span data-ttu-id="66589-106">參數</span><span class="sxs-lookup"><span data-stu-id="66589-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66589-107"><span id="column"></span><span id="COLUMN"></span>*列*</span><span class="sxs-lookup"><span data-stu-id="66589-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="66589-108">**Number** (**long**) 指出要變更之資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="66589-108">**Number** (**long**) indicating the index of the column to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="66589-109"><span id="mode"></span><span id="MODE"></span>*模式*</span><span class="sxs-lookup"><span data-stu-id="66589-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="66589-110">表示調整大小模式的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="66589-110">**String** indicating the sizing mode.</span></span> <span data-ttu-id="66589-111">包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="66589-111">Contains one of the following values.</span></span>



| <span data-ttu-id="66589-112">值</span><span class="sxs-lookup"><span data-stu-id="66589-112">Value</span></span>          | <span data-ttu-id="66589-113">描述</span><span class="sxs-lookup"><span data-stu-id="66589-113">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66589-114">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="66589-114">AutosizeHeader</span></span> | <span data-ttu-id="66589-115">資料行調整大小以容納資料行和標頭中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="66589-115">The column resizes to accommodate all data in both the column and the header.</span></span>                                  |
| <span data-ttu-id="66589-116">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="66589-116">AutosizeData</span></span>   | <span data-ttu-id="66589-117">資料行調整大小以容納資料行中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="66589-117">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="66589-118">固定式</span><span class="sxs-lookup"><span data-stu-id="66589-118">Fixed</span></span>          | <span data-ttu-id="66589-119">此資料行是固定的大小。</span><span class="sxs-lookup"><span data-stu-id="66589-119">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="66589-120">延伸</span><span class="sxs-lookup"><span data-stu-id="66589-120">Stretches</span></span>      | <span data-ttu-id="66589-121">當所有其他資料行調整大小之後，資料行調整大小以使用 **播放清單** 元素中的剩餘空間。</span><span class="sxs-lookup"><span data-stu-id="66589-121">The column resizes to use the remaining space in the **PLAYLIST** element after all other columns are resized.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66589-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="66589-122">Return Value</span></span>

<span data-ttu-id="66589-123">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="66589-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="66589-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="66589-124">Requirements</span></span>



| <span data-ttu-id="66589-125">需求</span><span class="sxs-lookup"><span data-stu-id="66589-125">Requirement</span></span> | <span data-ttu-id="66589-126">值</span><span class="sxs-lookup"><span data-stu-id="66589-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="66589-127">版本</span><span class="sxs-lookup"><span data-stu-id="66589-127">Version</span></span><br/> | <span data-ttu-id="66589-128">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="66589-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66589-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66589-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66589-130">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="66589-130">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





