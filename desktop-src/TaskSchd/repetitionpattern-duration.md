---
title: RepetitionPattern Duration 屬性
description: 針對腳本，取得或設定重複模式的時間長度。
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Duration 屬性工作排程器
- Duration 屬性工作排程器，RepetitionPattern 物件
- RepetitionPattern 物件工作排程器，Duration 屬性
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980289"
---
# <a name="repetitionpatternduration-property"></a><span data-ttu-id="6abf5-106">RepetitionPattern Duration 屬性</span><span class="sxs-lookup"><span data-stu-id="6abf5-106">RepetitionPattern.Duration property</span></span>

<span data-ttu-id="6abf5-107">針對腳本，取得或設定重複模式的時間長度。</span><span class="sxs-lookup"><span data-stu-id="6abf5-107">For scripting, gets or sets how long the pattern is repeated.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abf5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6abf5-108">Syntax</span></span>


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a><span data-ttu-id="6abf5-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="6abf5-109">Property value</span></span>

<span data-ttu-id="6abf5-110">模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="6abf5-110">How long the pattern is repeated.</span></span> <span data-ttu-id="6abf5-111">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="6abf5-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="6abf5-112">允許的最小時間是一分鐘。</span><span class="sxs-lookup"><span data-stu-id="6abf5-112">The minimum time allowed is one minute.</span></span>

<span data-ttu-id="6abf5-113">如果未在持續時間內指定任何值，則會無限期地重複模式。</span><span class="sxs-lookup"><span data-stu-id="6abf5-113">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span>

## <a name="remarks"></a><span data-ttu-id="6abf5-114">備註</span><span class="sxs-lookup"><span data-stu-id="6abf5-114">Remarks</span></span>

<span data-ttu-id="6abf5-115">如果您指定工作的重複持續時間，您也必須指定重複間隔。</span><span class="sxs-lookup"><span data-stu-id="6abf5-115">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="6abf5-116">讀取或寫入工作的 XML 時，重複期間會指定在工作排程器架構的 [**duration**](taskschedulerschema-duration-repetitiontype-element.md) 元素中。</span><span class="sxs-lookup"><span data-stu-id="6abf5-116">When reading or writing XML for a task, the repetition duration is specified in the [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6abf5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6abf5-117">Requirements</span></span>



| <span data-ttu-id="6abf5-118">需求</span><span class="sxs-lookup"><span data-stu-id="6abf5-118">Requirement</span></span> | <span data-ttu-id="6abf5-119">值</span><span class="sxs-lookup"><span data-stu-id="6abf5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6abf5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6abf5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6abf5-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6abf5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6abf5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6abf5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6abf5-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6abf5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6abf5-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6abf5-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6abf5-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6abf5-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6abf5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6abf5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6abf5-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6abf5-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6abf5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6abf5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abf5-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="6abf5-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





