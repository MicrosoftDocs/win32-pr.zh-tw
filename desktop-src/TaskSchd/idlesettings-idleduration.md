---
title: IdleSettings. IdleDuration 屬性
description: 針對腳本，取得或設定值，這個值表示電腦在工作執行前必須處於閒置狀態的時間量。
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- IdleDuration 屬性工作排程器
- IdleDuration 屬性工作排程器，IdleSettings 物件
- IdleSettings 物件工作排程器、IdleDuration 屬性
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686146"
---
# <a name="idlesettingsidleduration-property"></a><span data-ttu-id="738b8-106">IdleSettings. IdleDuration 屬性</span><span class="sxs-lookup"><span data-stu-id="738b8-106">IdleSettings.IdleDuration property</span></span>

<span data-ttu-id="738b8-107">針對腳本，取得或設定值，這個值表示電腦在工作執行前必須處於閒置狀態的時間量。</span><span class="sxs-lookup"><span data-stu-id="738b8-107">For scripting, gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span>

## <a name="syntax"></a><span data-ttu-id="738b8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="738b8-108">Syntax</span></span>


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a><span data-ttu-id="738b8-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="738b8-109">Property value</span></span>

<span data-ttu-id="738b8-110">值，這個值表示) 執行工作之前，電腦必須處於閒置狀態的時間量。</span><span class="sxs-lookup"><span data-stu-id="738b8-110">A value that indicates the amount of time that the computer must be in an idle state before the task is run).</span></span> <span data-ttu-id="738b8-111">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="738b8-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="738b8-112">最小值是一分鐘。</span><span class="sxs-lookup"><span data-stu-id="738b8-112">The minimum value is one minute.</span></span> <span data-ttu-id="738b8-113">如果這個值為 **Null**，則會將延遲設定為預設值10分鐘。</span><span class="sxs-lookup"><span data-stu-id="738b8-113">If this value is **NULL**, then the delay will be set to the default of 10 minutes.</span></span>

## <a name="remarks"></a><span data-ttu-id="738b8-114">備註</span><span class="sxs-lookup"><span data-stu-id="738b8-114">Remarks</span></span>

<span data-ttu-id="738b8-115">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="738b8-115">When reading or writing XML for a task, this setting is specified in the [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="738b8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="738b8-116">Requirements</span></span>



| <span data-ttu-id="738b8-117">需求</span><span class="sxs-lookup"><span data-stu-id="738b8-117">Requirement</span></span> | <span data-ttu-id="738b8-118">值</span><span class="sxs-lookup"><span data-stu-id="738b8-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="738b8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="738b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="738b8-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="738b8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="738b8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="738b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="738b8-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="738b8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="738b8-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="738b8-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="738b8-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="738b8-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="738b8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="738b8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="738b8-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="738b8-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="738b8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="738b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738b8-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="738b8-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="738b8-129">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="738b8-129">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





