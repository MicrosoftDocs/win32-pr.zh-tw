---
description: 包含 pin 的目前信號產生狀態。
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: 'PWM_PIN_IS_STARTED_OUTPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972540"
---
# <a name="pwm_pin_is_started_output-structure"></a><span data-ttu-id="761fe-103">PWM \_ PIN \_ 已 \_ 啟動 \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="761fe-103">PWM\_PIN\_IS\_STARTED\_OUTPUT structure</span></span>

<span data-ttu-id="761fe-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="761fe-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="761fe-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="761fe-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="761fe-106">包含 pin 的目前信號產生狀態。</span><span class="sxs-lookup"><span data-stu-id="761fe-106">Contains the current signal generation state of a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="761fe-107">語法</span><span class="sxs-lookup"><span data-stu-id="761fe-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="761fe-108">成員</span><span class="sxs-lookup"><span data-stu-id="761fe-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="761fe-109">**IsStarted**</span><span class="sxs-lookup"><span data-stu-id="761fe-109">**IsStarted**</span></span>
</dt> <dd>

<span data-ttu-id="761fe-110">釘選目前信號產生狀態。</span><span class="sxs-lookup"><span data-stu-id="761fe-110">The pin current signal generation state.</span></span> <span data-ttu-id="761fe-111">True 值表示已啟動 pin。</span><span class="sxs-lookup"><span data-stu-id="761fe-111">A value of true means that the pin is started.</span></span> <span data-ttu-id="761fe-112">False 值表示已停止 pin。</span><span class="sxs-lookup"><span data-stu-id="761fe-112">A value of false means that the pin is stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="761fe-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="761fe-113">Requirements</span></span>



| <span data-ttu-id="761fe-114">需求</span><span class="sxs-lookup"><span data-stu-id="761fe-114">Requirement</span></span> | <span data-ttu-id="761fe-115">值</span><span class="sxs-lookup"><span data-stu-id="761fe-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="761fe-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="761fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="761fe-117">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="761fe-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="761fe-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="761fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="761fe-119">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="761fe-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="761fe-120">最小 KMDF 版本</span><span class="sxs-lookup"><span data-stu-id="761fe-120">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="761fe-121">1.19</span><span class="sxs-lookup"><span data-stu-id="761fe-121">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="761fe-122">最小的 UMDF 版本</span><span class="sxs-lookup"><span data-stu-id="761fe-122">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="761fe-123">2.19</span><span class="sxs-lookup"><span data-stu-id="761fe-123">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="761fe-124">標頭</span><span class="sxs-lookup"><span data-stu-id="761fe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="761fe-125"><dt>Pwm (包含 Pwm) </dt></span><span class="sxs-lookup"><span data-stu-id="761fe-125"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="761fe-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="761fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761fe-127">**已 \_ 啟動 IOCTL PWM \_ 釘選 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="761fe-127">**IOCTL\_PWM\_PIN\_IS\_STARTED**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




