---
title: IdleSettings. WaitTimeout 屬性
description: 針對腳本，取得或設定值，這個值會指出工作排程器等候閒置條件發生的時間量。
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- WaitTimeout 屬性工作排程器
- WaitTimeout 屬性工作排程器，IdleSettings 物件
- IdleSettings 物件工作排程器、WaitTimeout 屬性
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025198"
---
# <a name="idlesettingswaittimeout-property"></a><span data-ttu-id="19005-106">IdleSettings. WaitTimeout 屬性</span><span class="sxs-lookup"><span data-stu-id="19005-106">IdleSettings.WaitTimeout property</span></span>

<span data-ttu-id="19005-107">針對腳本，取得或設定值，這個值會指出工作排程器等候閒置條件發生的時間量。</span><span class="sxs-lookup"><span data-stu-id="19005-107">For scripting, gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="19005-108">如果未指定此屬性的值，工作排程器服務將會無限期地等候閒置的條件發生。</span><span class="sxs-lookup"><span data-stu-id="19005-108">If no value is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span>

## <a name="syntax"></a><span data-ttu-id="19005-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="19005-109">Syntax</span></span>


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a><span data-ttu-id="19005-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="19005-110">Property value</span></span>

<span data-ttu-id="19005-111">值，指出工作排程器將等候閒置條件發生的時間量。</span><span class="sxs-lookup"><span data-stu-id="19005-111">A value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="19005-112">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="19005-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="19005-113">允許的最小時間是1分鐘。</span><span class="sxs-lookup"><span data-stu-id="19005-113">The minimum time allowed is 1 minute.</span></span> <span data-ttu-id="19005-114">如果這個值為 **Null**，則會將延遲設定為預設值1小時。</span><span class="sxs-lookup"><span data-stu-id="19005-114">If this value is **NULL**, then the delay will be set to the default of 1 hour.</span></span>

## <a name="remarks"></a><span data-ttu-id="19005-115">備註</span><span class="sxs-lookup"><span data-stu-id="19005-115">Remarks</span></span>

<span data-ttu-id="19005-116">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="19005-116">When reading or writing XML for a task, this setting is specified in the [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="19005-117">如果工作是由閒置觸發程式觸發，則會忽略 **IdleSettings. WaitTimeout** 屬性。</span><span class="sxs-lookup"><span data-stu-id="19005-117">If a task is triggered by an idle trigger, then the **IdleSettings.WaitTimeout** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="19005-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="19005-118">Requirements</span></span>



| <span data-ttu-id="19005-119">需求</span><span class="sxs-lookup"><span data-stu-id="19005-119">Requirement</span></span> | <span data-ttu-id="19005-120">值</span><span class="sxs-lookup"><span data-stu-id="19005-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19005-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19005-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19005-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19005-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="19005-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19005-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19005-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19005-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19005-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="19005-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="19005-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="19005-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="19005-127">DLL</span><span class="sxs-lookup"><span data-stu-id="19005-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19005-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19005-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19005-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19005-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19005-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="19005-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="19005-131">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="19005-131">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





