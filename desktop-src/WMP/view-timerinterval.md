---
title: TimerInterval
description: TimerInterval 屬性會指定或抓取計時器引發事件至 ontimer 事件處理常式的間隔（以毫秒為單位）。
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- TimerInterval Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992146"
---
# <a name="viewtimerinterval"></a><span data-ttu-id="f1045-104">TimerInterval</span><span class="sxs-lookup"><span data-stu-id="f1045-104">VIEW.timerInterval</span></span>

<span data-ttu-id="f1045-105">**TimerInterval** 屬性會指定或抓取計時器引發事件至 **ontimer** 事件處理常式的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1045-105">The **timerInterval** attribute specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span>

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a><span data-ttu-id="f1045-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="f1045-106">Possible Values</span></span>

<span data-ttu-id="f1045-107">此屬性是讀取/寫入 **號碼** (**長**) ，預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="f1045-107">This attribute is a read/write **Number** (**long**) with a default value of 1000.</span></span>



| <span data-ttu-id="f1045-108">值</span><span class="sxs-lookup"><span data-stu-id="f1045-108">Value</span></span>        | <span data-ttu-id="f1045-109">描述</span><span class="sxs-lookup"><span data-stu-id="f1045-109">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="f1045-110">0</span><span class="sxs-lookup"><span data-stu-id="f1045-110">0</span></span>            | <span data-ttu-id="f1045-111">計時器事件不會引發。</span><span class="sxs-lookup"><span data-stu-id="f1045-111">The timer event does not fire.</span></span> |
| <span data-ttu-id="f1045-112">50 及以上</span><span class="sxs-lookup"><span data-stu-id="f1045-112">50 and above</span></span> | <span data-ttu-id="f1045-113">以毫秒為單位的間隔。</span><span class="sxs-lookup"><span data-stu-id="f1045-113">The interval in milliseconds.</span></span>  |



 

<span data-ttu-id="f1045-114">低於 50 (的任何值都包含負數，但不包括零) 會產生錯誤，並維持先前的值。</span><span class="sxs-lookup"><span data-stu-id="f1045-114">Any value below 50 (including negative numbers, but not including zero) generates an error and the previous value is maintained.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1045-115">備註</span><span class="sxs-lookup"><span data-stu-id="f1045-115">Remarks</span></span>

<span data-ttu-id="f1045-116">如果未執行任何 **ontimer** 事件處理常式，則不會自動引發。</span><span class="sxs-lookup"><span data-stu-id="f1045-116">This will not fire automatically if no **ontimer** event handler is implemented.</span></span> <span data-ttu-id="f1045-117">因此，即使預設值為非零，也不會降低效能。</span><span class="sxs-lookup"><span data-stu-id="f1045-117">Thus there is no performance degradation even though the default value is nonzero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1045-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1045-118">Requirements</span></span>



| <span data-ttu-id="f1045-119">需求</span><span class="sxs-lookup"><span data-stu-id="f1045-119">Requirement</span></span> | <span data-ttu-id="f1045-120">值</span><span class="sxs-lookup"><span data-stu-id="f1045-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f1045-121">版本</span><span class="sxs-lookup"><span data-stu-id="f1045-121">Version</span></span><br/> | <span data-ttu-id="f1045-122">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="f1045-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1045-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1045-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1045-124">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="f1045-124">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="f1045-125">**VIEW. ontimer**</span><span class="sxs-lookup"><span data-stu-id="f1045-125">**VIEW.ontimer**</span></span>](view-ontimer.md)
</dt> </dl>

 

 





