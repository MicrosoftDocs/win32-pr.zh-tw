---
title: BootTrigger Delay 屬性
description: 針對腳本，取得或設定值，這個值表示系統開機和啟動工作之間的時間長度。
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，BootTrigger 物件
- BootTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104669"
---
# <a name="boottriggerdelay-property"></a><span data-ttu-id="30c9d-106">BootTrigger Delay 屬性</span><span class="sxs-lookup"><span data-stu-id="30c9d-106">BootTrigger.Delay property</span></span>

<span data-ttu-id="30c9d-107">針對腳本，取得或設定值，這個值表示系統開機和啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="30c9d-107">For scripting, gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c9d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30c9d-108">Syntax</span></span>


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="30c9d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="30c9d-109">Property value</span></span>

<span data-ttu-id="30c9d-110">值，指出系統開機和啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="30c9d-110">A value that indicates the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="30c9d-111">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="30c9d-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="30c9d-112">備註</span><span class="sxs-lookup"><span data-stu-id="30c9d-112">Remarks</span></span>

<span data-ttu-id="30c9d-113">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**delay**](taskschedulerschema-delay-boottriggertype-element.md) 元素指定開機延遲。</span><span class="sxs-lookup"><span data-stu-id="30c9d-113">When reading or writing your own XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="30c9d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="30c9d-114">Requirements</span></span>



| <span data-ttu-id="30c9d-115">需求</span><span class="sxs-lookup"><span data-stu-id="30c9d-115">Requirement</span></span> | <span data-ttu-id="30c9d-116">值</span><span class="sxs-lookup"><span data-stu-id="30c9d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30c9d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30c9d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30c9d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30c9d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="30c9d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30c9d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30c9d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30c9d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30c9d-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="30c9d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="30c9d-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30c9d-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30c9d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="30c9d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30c9d-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c9d-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30c9d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30c9d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c9d-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="30c9d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="30c9d-127">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="30c9d-127">**BootTrigger**</span></span>](boottrigger.md)
</dt> </dl>

 

 





