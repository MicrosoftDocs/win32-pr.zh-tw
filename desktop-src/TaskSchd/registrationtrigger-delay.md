---
title: RegistrationTrigger Delay 屬性
description: 針對腳本，取得或設定在註冊工作與啟動工作之間的時間長度。
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，RegistrationTrigger 物件
- RegistrationTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509124"
---
# <a name="registrationtriggerdelay-property"></a><span data-ttu-id="c7162-106">RegistrationTrigger Delay 屬性</span><span class="sxs-lookup"><span data-stu-id="c7162-106">RegistrationTrigger.Delay property</span></span>

<span data-ttu-id="c7162-107">針對腳本，取得或設定在註冊工作與啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="c7162-107">For scripting, gets or sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="c7162-108">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="c7162-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7162-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7162-109">Syntax</span></span>


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="c7162-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="c7162-110">Property value</span></span>

<span data-ttu-id="c7162-111">註冊系統與啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="c7162-111">The amount of time between when the system is registered and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7162-112">備註</span><span class="sxs-lookup"><span data-stu-id="c7162-112">Remarks</span></span>

<span data-ttu-id="c7162-113">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**delay**](taskschedulerschema-delay-registrationtriggertype-element.md) 元素指定開機延遲。</span><span class="sxs-lookup"><span data-stu-id="c7162-113">When reading or writing XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c7162-114">如果註冊了具有延遲註冊觸發程式的工作，且在延遲期間關閉或重新開機工作的電腦，在執行工作之前，工作將不會執行，而且會遺失延遲。</span><span class="sxs-lookup"><span data-stu-id="c7162-114">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7162-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7162-115">Requirements</span></span>



| <span data-ttu-id="c7162-116">需求</span><span class="sxs-lookup"><span data-stu-id="c7162-116">Requirement</span></span> | <span data-ttu-id="c7162-117">值</span><span class="sxs-lookup"><span data-stu-id="c7162-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7162-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7162-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7162-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7162-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c7162-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7162-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7162-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7162-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7162-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c7162-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7162-123"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7162-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7162-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c7162-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7162-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7162-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7162-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7162-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7162-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c7162-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





