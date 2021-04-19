---
title: VIEW. 可調整大小
description: 可調整大小的屬性會抓取值，指出是否可以調整視圖的大小。
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- VIEW. 可調整大小的 Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986148"
---
# <a name="viewresizable"></a><span data-ttu-id="55bdf-104">VIEW. 可調整大小</span><span class="sxs-lookup"><span data-stu-id="55bdf-104">VIEW.resizable</span></span>

<span data-ttu-id="55bdf-105">可重設 **大小** 的屬性會抓取值，指出是否可以調整 **視圖** 的大小。</span><span class="sxs-lookup"><span data-stu-id="55bdf-105">The **resizable** attribute retrieves a value indicating whether the **VIEW** can be resized.</span></span>

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a><span data-ttu-id="55bdf-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="55bdf-106">Possible Values</span></span>

<span data-ttu-id="55bdf-107">這個屬性是唯讀的 **布林** 值，預設值等於 **標題列** 屬性。</span><span class="sxs-lookup"><span data-stu-id="55bdf-107">This attribute is a read-only **Boolean** with a default value equal to the **titlebar** attribute.</span></span>



| <span data-ttu-id="55bdf-108">值</span><span class="sxs-lookup"><span data-stu-id="55bdf-108">Values</span></span> | <span data-ttu-id="55bdf-109">描述</span><span class="sxs-lookup"><span data-stu-id="55bdf-109">Description</span></span>             |
|--------|-------------------------|
| <span data-ttu-id="55bdf-110">true</span><span class="sxs-lookup"><span data-stu-id="55bdf-110">true</span></span>   | <span data-ttu-id="55bdf-111">您可以調整 View 的大小。</span><span class="sxs-lookup"><span data-stu-id="55bdf-111">View can be resized.</span></span>    |
| <span data-ttu-id="55bdf-112">false</span><span class="sxs-lookup"><span data-stu-id="55bdf-112">false</span></span>  | <span data-ttu-id="55bdf-113">無法調整 View 的大小。</span><span class="sxs-lookup"><span data-stu-id="55bdf-113">View cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="55bdf-114">備註</span><span class="sxs-lookup"><span data-stu-id="55bdf-114">Remarks</span></span>

<span data-ttu-id="55bdf-115">如果沒有 **標題列**，因此沒有視窗或框線，您必須使用 **size** 方法來調整 **VIEW** 元素的大小。</span><span class="sxs-lookup"><span data-stu-id="55bdf-115">If there is no **titlebar**, and therefore no window or border, you must use the **size** method to resize the **VIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bdf-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="55bdf-116">Requirements</span></span>



| <span data-ttu-id="55bdf-117">需求</span><span class="sxs-lookup"><span data-stu-id="55bdf-117">Requirement</span></span> | <span data-ttu-id="55bdf-118">值</span><span class="sxs-lookup"><span data-stu-id="55bdf-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="55bdf-119">版本</span><span class="sxs-lookup"><span data-stu-id="55bdf-119">Version</span></span><br/> | <span data-ttu-id="55bdf-120">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="55bdf-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55bdf-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55bdf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55bdf-122">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="55bdf-122">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





