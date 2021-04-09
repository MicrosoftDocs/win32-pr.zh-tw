---
description: 包含脈衝寬度調製 (PWM) 控制器的有效輸出信號期間。
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: 'PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688848"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a><span data-ttu-id="12d2a-103">PWM \_ 控制器 \_ 取得 \_ 實際 \_ 期間 \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="12d2a-103">PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT structure</span></span>

<span data-ttu-id="12d2a-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="12d2a-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="12d2a-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="12d2a-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="12d2a-106">包含脈衝寬度調製 (PWM) 控制器的有效輸出信號期間。</span><span class="sxs-lookup"><span data-stu-id="12d2a-106">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d2a-107">語法</span><span class="sxs-lookup"><span data-stu-id="12d2a-107">Syntax</span></span>


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="12d2a-108">成員</span><span class="sxs-lookup"><span data-stu-id="12d2a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="12d2a-109">**ActualPeriod**</span><span class="sxs-lookup"><span data-stu-id="12d2a-109">**ActualPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="12d2a-110">在控制器輸出通道上測量的有效輸出信號週期。</span><span class="sxs-lookup"><span data-stu-id="12d2a-110">The effective output signal period as it would be measured on the output channels of the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12d2a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="12d2a-111">Requirements</span></span>



| <span data-ttu-id="12d2a-112">需求</span><span class="sxs-lookup"><span data-stu-id="12d2a-112">Requirement</span></span> | <span data-ttu-id="12d2a-113">值</span><span class="sxs-lookup"><span data-stu-id="12d2a-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d2a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12d2a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="12d2a-115">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12d2a-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="12d2a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12d2a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="12d2a-117">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12d2a-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="12d2a-118">最小 KMDF 版本</span><span class="sxs-lookup"><span data-stu-id="12d2a-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="12d2a-119">1.19</span><span class="sxs-lookup"><span data-stu-id="12d2a-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="12d2a-120">最小的 UMDF 版本</span><span class="sxs-lookup"><span data-stu-id="12d2a-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="12d2a-121">2.19</span><span class="sxs-lookup"><span data-stu-id="12d2a-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="12d2a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="12d2a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d2a-123"><dt>Pwm (包含 Pwm) </dt></span><span class="sxs-lookup"><span data-stu-id="12d2a-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d2a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12d2a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d2a-125">**IOCTL \_ PWM \_ 控制器 \_ 取得 \_ 實際 \_ 期間**</span><span class="sxs-lookup"><span data-stu-id="12d2a-125">**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




