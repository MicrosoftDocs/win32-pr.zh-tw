---
description: 包含以脈衝寬度調整 (PWM) 控制器的 pin 或通道目前的工作週期百分比。
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: 'PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110681"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a><span data-ttu-id="bc88e-103">PWM \_ PIN \_ 取得 \_ 主動式的工作 \_ \_ 週期 \_ 百分比 \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="bc88e-103">PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT structure</span></span>

<span data-ttu-id="bc88e-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="bc88e-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc88e-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="bc88e-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc88e-106">包含以脈衝寬度調整 (PWM) 控制器的 pin 或通道目前的工作週期百分比。</span><span class="sxs-lookup"><span data-stu-id="bc88e-106">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc88e-107">語法</span><span class="sxs-lookup"><span data-stu-id="bc88e-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="bc88e-108">成員</span><span class="sxs-lookup"><span data-stu-id="bc88e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc88e-109">**百分比**</span><span class="sxs-lookup"><span data-stu-id="bc88e-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="bc88e-110">目前的 PWM 信號工作週期，以 PWM 百分比表示，也 \_ 就是 ULONGLONG 值。</span><span class="sxs-lookup"><span data-stu-id="bc88e-110">The current PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc88e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc88e-111">Requirements</span></span>



| <span data-ttu-id="bc88e-112">需求</span><span class="sxs-lookup"><span data-stu-id="bc88e-112">Requirement</span></span> | <span data-ttu-id="bc88e-113">值</span><span class="sxs-lookup"><span data-stu-id="bc88e-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc88e-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc88e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bc88e-115">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc88e-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc88e-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc88e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bc88e-117">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc88e-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bc88e-118">最小 KMDF 版本</span><span class="sxs-lookup"><span data-stu-id="bc88e-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="bc88e-119">1.19</span><span class="sxs-lookup"><span data-stu-id="bc88e-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="bc88e-120">最小的 UMDF 版本</span><span class="sxs-lookup"><span data-stu-id="bc88e-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="bc88e-121">2.19</span><span class="sxs-lookup"><span data-stu-id="bc88e-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="bc88e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bc88e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc88e-123"><dt>Pwm (包含 Pwm) </dt></span><span class="sxs-lookup"><span data-stu-id="bc88e-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc88e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc88e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc88e-125">**IOCTL \_ PWM PIN 取得使用中的工作 \_ \_ \_ \_ \_ 週期 \_ 百分比**</span><span class="sxs-lookup"><span data-stu-id="bc88e-125">**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




