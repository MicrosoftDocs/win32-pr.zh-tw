---
title: VIEW. size
description: 大小方法會在指定的邊緣上調整視圖的大小。
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- VIEW. size Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989523"
---
# <a name="viewsize"></a><span data-ttu-id="ecaef-104">VIEW. size</span><span class="sxs-lookup"><span data-stu-id="ecaef-104">VIEW.size</span></span>

<span data-ttu-id="ecaef-105">大小方法會在指定的邊緣上調整 **視圖** 的 **大小**。</span><span class="sxs-lookup"><span data-stu-id="ecaef-105">The **size** method resizes the **VIEW** on a specified edge.</span></span>

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a><span data-ttu-id="ecaef-106">參數</span><span class="sxs-lookup"><span data-stu-id="ecaef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecaef-107"><span id="handle"></span><span id="HANDLE"></span>*處理*</span><span class="sxs-lookup"><span data-stu-id="ecaef-107"><span id="handle"></span><span id="HANDLE"></span>*handle*</span></span>
</dt> <dd>

<span data-ttu-id="ecaef-108">字串，指定調整大小時要移動的邊緣或角落。</span><span class="sxs-lookup"><span data-stu-id="ecaef-108">String specifying the edge or corner to move when sizing.</span></span> <span data-ttu-id="ecaef-109">此字串必須有下列八個值的其中一個。</span><span class="sxs-lookup"><span data-stu-id="ecaef-109">This string must have one of the following eight values.</span></span>



| <span data-ttu-id="ecaef-110">Edge</span><span class="sxs-lookup"><span data-stu-id="ecaef-110">Edge</span></span>   | <span data-ttu-id="ecaef-111">邊角</span><span class="sxs-lookup"><span data-stu-id="ecaef-111">Corner</span></span>      |
|--------|-------------|
| <span data-ttu-id="ecaef-112">top</span><span class="sxs-lookup"><span data-stu-id="ecaef-112">top</span></span>    | <span data-ttu-id="ecaef-113">右上</span><span class="sxs-lookup"><span data-stu-id="ecaef-113">topright</span></span>    |
| <span data-ttu-id="ecaef-114">向右</span><span class="sxs-lookup"><span data-stu-id="ecaef-114">right</span></span>  | <span data-ttu-id="ecaef-115">bottomright</span><span class="sxs-lookup"><span data-stu-id="ecaef-115">bottomright</span></span> |
| <span data-ttu-id="ecaef-116">下</span><span class="sxs-lookup"><span data-stu-id="ecaef-116">bottom</span></span> | <span data-ttu-id="ecaef-117">bottomleft</span><span class="sxs-lookup"><span data-stu-id="ecaef-117">bottomleft</span></span>  |
| <span data-ttu-id="ecaef-118">left</span><span class="sxs-lookup"><span data-stu-id="ecaef-118">left</span></span>   | <span data-ttu-id="ecaef-119">下拉式功能表</span><span class="sxs-lookup"><span data-stu-id="ecaef-119">topleft</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecaef-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecaef-120">Return Value</span></span>

<span data-ttu-id="ecaef-121">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ecaef-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecaef-122">備註</span><span class="sxs-lookup"><span data-stu-id="ecaef-122">Remarks</span></span>

<span data-ttu-id="ecaef-123">通常會從 **onmousedown** 處理常式內呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ecaef-123">This method is typically called from within an **onmousedown** handler.</span></span> <span data-ttu-id="ecaef-124">當滑鼠拖曳時，它會負責調整大小，並在放開滑鼠按鍵時停止調整大小。</span><span class="sxs-lookup"><span data-stu-id="ecaef-124">It takes care of resizing while the mouse is dragged and stops resizing when the mouse button is released.</span></span> <span data-ttu-id="ecaef-125">如果 **視圖** 的大小受到限制，您就無法拖曳滑鼠來將 **視圖** 的大小調整到超出限制的範圍。</span><span class="sxs-lookup"><span data-stu-id="ecaef-125">If the size of the **VIEW** is restricted, you cannot drag the mouse to resize the **View** beyond the restricted bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="ecaef-126">範例</span><span class="sxs-lookup"><span data-stu-id="ecaef-126">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="ecaef-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecaef-127">Requirements</span></span>



| <span data-ttu-id="ecaef-128">需求</span><span class="sxs-lookup"><span data-stu-id="ecaef-128">Requirement</span></span> | <span data-ttu-id="ecaef-129">值</span><span class="sxs-lookup"><span data-stu-id="ecaef-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ecaef-130">版本</span><span class="sxs-lookup"><span data-stu-id="ecaef-130">Version</span></span><br/> | <span data-ttu-id="ecaef-131">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="ecaef-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ecaef-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecaef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecaef-133">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="ecaef-133">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





