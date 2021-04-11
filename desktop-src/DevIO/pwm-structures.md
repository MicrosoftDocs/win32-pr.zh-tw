---
description: 深入瞭解： PWM 結構
ms.assetid: 992E3913-C1C4-48C1-A550-475CF44AB065
title: PWM 結構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99511820f8500cd8df827a80664f6c274d732665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936240"
---
# <a name="pwm-structures"></a><span data-ttu-id="0c651-103">PWM 結構</span><span class="sxs-lookup"><span data-stu-id="0c651-103">PWM Structures</span></span>

<span data-ttu-id="0c651-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="0c651-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0c651-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="0c651-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0c651-106">下列結構適用于脈衝寬度的調製：</span><span class="sxs-lookup"><span data-stu-id="0c651-106">The following structures are used with Pulse Width Modulation:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0c651-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="0c651-107">In this section</span></span>



| <span data-ttu-id="0c651-108">主題</span><span class="sxs-lookup"><span data-stu-id="0c651-108">Topic</span></span>                                                                                                                        | <span data-ttu-id="0c651-109">描述</span><span class="sxs-lookup"><span data-stu-id="0c651-109">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c651-110">**PWM \_ 控制器 \_ 取得 \_ 實際 \_ 期間 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="0c651-110">**PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT**</span></span>](pwm-controller-get-actual-period-output.md)<br/>                   | <span data-ttu-id="0c651-111">包含脈衝寬度調製 (PWM) 控制器的有效輸出信號期間。</span><span class="sxs-lookup"><span data-stu-id="0c651-111">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span><br/>                    |
| [<span data-ttu-id="0c651-112">**PWM \_ 控制器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="0c651-112">**PWM\_CONTROLLER\_INFO**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_info)<br/>                                                              | <span data-ttu-id="0c651-113">代表 (PWM) 控制器的脈衝寬度調製特性的靜態資訊。</span><span class="sxs-lookup"><span data-stu-id="0c651-113">Represents the static information that characterizes a Pulse Width Modulation (PWM) controller.</span></span> <br/>              |
| [<span data-ttu-id="0c651-114">**PWM \_ 控制器 \_ 設定 \_ 所需的 \_ 期間 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="0c651-114">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_input)<br/>                   | <span data-ttu-id="0c651-115">包含適用于脈衝寬度調製 (PWM) 控制器之建議信號的輸入值。</span><span class="sxs-lookup"><span data-stu-id="0c651-115">Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller.</span></span> <br/>       |
| [<span data-ttu-id="0c651-116">**PWM \_ 控制器 \_ 設定的 \_ 預期 \_ 期間 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="0c651-116">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_OUTPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_output)<br/>                 | <span data-ttu-id="0c651-117">包含脈衝寬度調製 (PWM) 控制器的有效輸出信號期間。</span><span class="sxs-lookup"><span data-stu-id="0c651-117">Contains the effective output signal period of the Pulse Width Modulation (PWM) controller.</span></span><br/>                   |
| [<span data-ttu-id="0c651-118">**PWM \_ PIN \_ 取得 \_ 主動式的工作 \_ \_ 週期 \_ 百分比 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="0c651-118">**PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT**</span></span>](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/> | <span data-ttu-id="0c651-119">包含以脈衝寬度調整 (PWM) 控制器的 pin 或通道目前的工作週期百分比。</span><span class="sxs-lookup"><span data-stu-id="0c651-119">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/> |
| [<span data-ttu-id="0c651-120">**PWM 釘選設定使用中的工作 \_ \_ \_ \_ \_ 週期 \_ 百分比 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="0c651-120">**PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT**</span></span>](pwm-pin-set-active-duty-cycle-percentage-input.md)<br/>   | <span data-ttu-id="0c651-121">包含在脈衝寬度調製 (PWM) 控制器的 pin 或通道所需的工作週期百分比。</span><span class="sxs-lookup"><span data-stu-id="0c651-121">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/>   |
| [<span data-ttu-id="0c651-122">**PWM \_ 針腳 \_ 取得 \_ 極性 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="0c651-122">**PWM\_PIN\_GET\_POLARITY\_OUTPUT**</span></span>](pwm-pin-get-polarity-output.md)<br/>                                            | <span data-ttu-id="0c651-123">包含要傳回的極性值。</span><span class="sxs-lookup"><span data-stu-id="0c651-123">Contains a polarity value to return.</span></span><br/>                                                                          |
| [<span data-ttu-id="0c651-124">**PWM \_ 針腳 \_ 設定 \_ 極性 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="0c651-124">**PWM\_PIN\_SET\_POLARITY\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input)<br/>                                              | <span data-ttu-id="0c651-125">包含 pin 或通道極性的所需值。</span><span class="sxs-lookup"><span data-stu-id="0c651-125">Contains a desired value for polarity of a pin or channel.</span></span><br/>                                                    |
| [<span data-ttu-id="0c651-126">**PWM \_ PIN \_ 已 \_ 開始 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="0c651-126">**PWM\_PIN\_IS\_STARTED\_OUTPUT**</span></span>](pwm-pin-is-started-output.md)<br/>                                                | <span data-ttu-id="0c651-127">包含 pin 的目前信號產生狀態。</span><span class="sxs-lookup"><span data-stu-id="0c651-127">Contains the current signal generation state of a pin.</span></span><br/>                                                        |



 

 

 




