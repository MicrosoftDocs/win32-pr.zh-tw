---
title: CURSOR 資源
description: 定義在顯示畫面或動畫游標上定義游標形狀的點陣圖。
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- 資料指標資源功能表與其他資源
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966033"
---
# <a name="cursor-resource"></a><span data-ttu-id="5c7d1-104">CURSOR 資源</span><span class="sxs-lookup"><span data-stu-id="5c7d1-104">CURSOR resource</span></span>

<span data-ttu-id="5c7d1-105">定義在顯示畫面或動畫游標上定義游標形狀的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="5c7d1-105">Defines a bitmap that defines the shape of the cursor on the display screen or an animated cursor.</span></span>

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a><span data-ttu-id="5c7d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c7d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c7d1-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="5c7d1-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="5c7d1-108">識別資源的唯一名稱或16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="5c7d1-108">Unique name or a 16-bit unsigned integer identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5c7d1-109"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="5c7d1-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="5c7d1-110">包含資源的檔案名。</span><span class="sxs-lookup"><span data-stu-id="5c7d1-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="5c7d1-111">名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5c7d1-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="5c7d1-112">路徑應該是加上引號的字串。</span><span class="sxs-lookup"><span data-stu-id="5c7d1-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="5c7d1-113">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="5c7d1-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="5c7d1-114">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="5c7d1-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c7d1-115">備註</span><span class="sxs-lookup"><span data-stu-id="5c7d1-115">Remarks</span></span>

<span data-ttu-id="5c7d1-116">圖示和游標資源可以包含一個以上的影像。</span><span class="sxs-lookup"><span data-stu-id="5c7d1-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="5c7d1-117">範例</span><span class="sxs-lookup"><span data-stu-id="5c7d1-117">Examples</span></span>

<span data-ttu-id="5c7d1-118">下列範例會定義兩個數據指標資源：依名稱 (cursor1) ，另一個則依據 number (2) ：</span><span class="sxs-lookup"><span data-stu-id="5c7d1-118">The following example defines two cursor resources; one by name (cursor1) and the other by number (2):</span></span>

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a><span data-ttu-id="5c7d1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c7d1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7d1-120">使用資料指標</span><span class="sxs-lookup"><span data-stu-id="5c7d1-120">Using Cursors</span></span>](./using-cursors.md)
</dt> </dl>

 

 