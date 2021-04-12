---
description: 包含在脈衝寬度調製 (PWM) 控制器的 pin 或通道所需的工作週期百分比。
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: 'PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385862"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a><span data-ttu-id="c9a27-103">PWM 釘選設定使用中的工作 \_ \_ \_ \_ \_ 週期 \_ 百分比 \_ 輸入結構</span><span class="sxs-lookup"><span data-stu-id="c9a27-103">PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT structure</span></span>

<span data-ttu-id="c9a27-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="c9a27-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c9a27-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="c9a27-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c9a27-106">包含在脈衝寬度調製 (PWM) 控制器的 pin 或通道所需的工作週期百分比。</span><span class="sxs-lookup"><span data-stu-id="c9a27-106">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a27-107">語法</span><span class="sxs-lookup"><span data-stu-id="c9a27-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a><span data-ttu-id="c9a27-108">成員</span><span class="sxs-lookup"><span data-stu-id="c9a27-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9a27-109">**百分比**</span><span class="sxs-lookup"><span data-stu-id="c9a27-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="c9a27-110">所需的 PWM 信號工作週期，以 PWM 百分比表示，也 \_ 就是 ULONGLONG 值。</span><span class="sxs-lookup"><span data-stu-id="c9a27-110">The desired PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9a27-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9a27-111">Requirements</span></span>



| <span data-ttu-id="c9a27-112">需求</span><span class="sxs-lookup"><span data-stu-id="c9a27-112">Requirement</span></span> | <span data-ttu-id="c9a27-113">值</span><span class="sxs-lookup"><span data-stu-id="c9a27-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a27-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9a27-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a27-115">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9a27-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c9a27-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9a27-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a27-117">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9a27-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c9a27-118">最小 KMDF 版本</span><span class="sxs-lookup"><span data-stu-id="c9a27-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="c9a27-119">1.19</span><span class="sxs-lookup"><span data-stu-id="c9a27-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="c9a27-120">最小的 UMDF 版本</span><span class="sxs-lookup"><span data-stu-id="c9a27-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="c9a27-121">2.19</span><span class="sxs-lookup"><span data-stu-id="c9a27-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="c9a27-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c9a27-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9a27-123"><dt>Pwm (包含 Pwm) </dt></span><span class="sxs-lookup"><span data-stu-id="c9a27-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a27-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9a27-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a27-125">**IOCTL \_ PWM \_ 釘選有效的工作 \_ \_ \_ \_ 週期 \_ 百分比**</span><span class="sxs-lookup"><span data-stu-id="c9a27-125">**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




