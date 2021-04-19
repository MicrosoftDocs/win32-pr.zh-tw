---
title: BUTTONGROUP 電臺
description: 單選屬性會指定或抓取值，指出 BUTTONGROUP 是否包含在選項按鈕中。
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP 電臺 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990294"
---
# <a name="buttongroupradio"></a><span data-ttu-id="bd878-104">BUTTONGROUP 電臺</span><span class="sxs-lookup"><span data-stu-id="bd878-104">BUTTONGROUP.radio</span></span>

<span data-ttu-id="bd878-105">**單選** 屬性會指定或抓取值，指出 **BUTTONGROUP** 是否包含在選項按鈕中。</span><span class="sxs-lookup"><span data-stu-id="bd878-105">The **radio** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>

``` syntax
        elementID.radio
```

## <a name="possible-values"></a><span data-ttu-id="bd878-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="bd878-106">Possible Values</span></span>

<span data-ttu-id="bd878-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="bd878-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="bd878-108">值</span><span class="sxs-lookup"><span data-stu-id="bd878-108">Value</span></span> | <span data-ttu-id="bd878-109">描述</span><span class="sxs-lookup"><span data-stu-id="bd878-109">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="bd878-110">true</span><span class="sxs-lookup"><span data-stu-id="bd878-110">true</span></span>  | <span data-ttu-id="bd878-111">**BUTTONGROUP** 為單選樣式。</span><span class="sxs-lookup"><span data-stu-id="bd878-111">The **BUTTONGROUP** is radio style.</span></span>              |
| <span data-ttu-id="bd878-112">false</span><span class="sxs-lookup"><span data-stu-id="bd878-112">false</span></span> | <span data-ttu-id="bd878-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="bd878-113">Default.</span></span> <span data-ttu-id="bd878-114">**BUTTONGROUP** 不是無線電樣式。</span><span class="sxs-lookup"><span data-stu-id="bd878-114">The **BUTTONGROUP** is not radio style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bd878-115">備註</span><span class="sxs-lookup"><span data-stu-id="bd878-115">Remarks</span></span>

<span data-ttu-id="bd878-116">如果 [**無線電**] 設定為 [true]， **BUTTONGROUP** 中的所有 **BUTTONELEMENT** 元素都會是粘滯，但是一次只有一個按鈕會處於關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="bd878-116">If **radio** is set to true, all the **BUTTONELEMENT** elements in the **BUTTONGROUP** will be sticky, but only one button at a time will be in the down state.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd878-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd878-117">Requirements</span></span>



| <span data-ttu-id="bd878-118">需求</span><span class="sxs-lookup"><span data-stu-id="bd878-118">Requirement</span></span> | <span data-ttu-id="bd878-119">值</span><span class="sxs-lookup"><span data-stu-id="bd878-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bd878-120">版本</span><span class="sxs-lookup"><span data-stu-id="bd878-120">Version</span></span><br/> | <span data-ttu-id="bd878-121">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="bd878-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd878-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd878-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd878-123">**BUTTONELEMENT。**</span><span class="sxs-lookup"><span data-stu-id="bd878-123">**BUTTONELEMENT.sticky**</span></span>](buttonelement-sticky.md)
</dt> <dt>

[<span data-ttu-id="bd878-124">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="bd878-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





