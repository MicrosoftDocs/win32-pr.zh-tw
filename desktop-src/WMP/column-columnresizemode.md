---
title: ColumnResizeMode
description: ColumnResizeMode 屬性會指定或抓取此資料行的調整大小模式。
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- ColumnResizeMode Windows Media Player 的資料行
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d17b1a2edd878fb15e69c595e3c061c1963a5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978701"
---
# <a name="columncolumnresizemode"></a><span data-ttu-id="1faee-104">ColumnResizeMode</span><span class="sxs-lookup"><span data-stu-id="1faee-104">COLUMN.columnResizeMode</span></span>

<span data-ttu-id="1faee-105">**ColumnResizeMode** 屬性會指定或抓取此資料行的調整大小模式。</span><span class="sxs-lookup"><span data-stu-id="1faee-105">The **columnResizeMode** attribute specifies or retrieves the resize mode for this column.</span></span>

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a><span data-ttu-id="1faee-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="1faee-106">Possible Values</span></span>

<span data-ttu-id="1faee-107">這個屬性是包含下列其中一個值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="1faee-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="1faee-108">值</span><span class="sxs-lookup"><span data-stu-id="1faee-108">Value</span></span>          | <span data-ttu-id="1faee-109">描述</span><span class="sxs-lookup"><span data-stu-id="1faee-109">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1faee-110">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="1faee-110">AutosizeHeader</span></span> | <span data-ttu-id="1faee-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="1faee-111">Default.</span></span> <span data-ttu-id="1faee-112">資料行調整大小以容納資料行和標頭中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="1faee-112">The column resizes to accommodate all data in both the column and the header.</span></span>                         |
| <span data-ttu-id="1faee-113">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="1faee-113">AutosizeData</span></span>   | <span data-ttu-id="1faee-114">資料行調整大小以容納資料行中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="1faee-114">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="1faee-115">固定式</span><span class="sxs-lookup"><span data-stu-id="1faee-115">Fixed</span></span>          | <span data-ttu-id="1faee-116">此資料行是固定的大小。</span><span class="sxs-lookup"><span data-stu-id="1faee-116">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="1faee-117">延伸</span><span class="sxs-lookup"><span data-stu-id="1faee-117">Stretches</span></span>      | <span data-ttu-id="1faee-118">當所有其他資料行調整大小之後，資料行調整大小以使用 **播放清單** 控制項中的剩餘空間。</span><span class="sxs-lookup"><span data-stu-id="1faee-118">The column resizes to use the remaining space in the **PLAYLIST** control after all other columns are resized.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1faee-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1faee-119">Requirements</span></span>



| <span data-ttu-id="1faee-120">需求</span><span class="sxs-lookup"><span data-stu-id="1faee-120">Requirement</span></span> | <span data-ttu-id="1faee-121">值</span><span class="sxs-lookup"><span data-stu-id="1faee-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1faee-122">版本</span><span class="sxs-lookup"><span data-stu-id="1faee-122">Version</span></span><br/> | <span data-ttu-id="1faee-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="1faee-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1faee-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1faee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1faee-125">**COLUMN 元素**</span><span class="sxs-lookup"><span data-stu-id="1faee-125">**COLUMN Element**</span></span>](column-element.md)
</dt> </dl>

 

 





