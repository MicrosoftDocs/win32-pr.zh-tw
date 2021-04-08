---
title: RepetitionPattern. StopAtDurationEnd 屬性
description: 針對腳本，取得或設定布林值，這個值會指出是否在重複模式期間結束時停止正在執行的工作實例。
ms.assetid: 421f2d6f-7c35-44b4-97f2-45f46ca5e40e
keywords:
- StopAtDurationEnd 屬性工作排程器
- StopAtDurationEnd 屬性工作排程器，RepetitionPattern 物件
- RepetitionPattern 物件工作排程器、StopAtDurationEnd 屬性
topic_type:
- apiref
api_name:
- RepetitionPattern.StopAtDurationEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b95d7e8941a4249991692dffbd3cac9ad1ca7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686142"
---
# <a name="repetitionpatternstopatdurationend-property"></a><span data-ttu-id="8c01e-106">RepetitionPattern. StopAtDurationEnd 屬性</span><span class="sxs-lookup"><span data-stu-id="8c01e-106">RepetitionPattern.StopAtDurationEnd property</span></span>

<span data-ttu-id="8c01e-107">針對腳本，取得或設定布林值，這個值會指出是否在重複模式期間結束時停止正在執行的工作實例。</span><span class="sxs-lookup"><span data-stu-id="8c01e-107">For scripting, gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c01e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c01e-108">Syntax</span></span>


```VB
RepetitionPattern.StopAtDurationEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8c01e-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8c01e-109">Property value</span></span>

<span data-ttu-id="8c01e-110">布林值，指出是否在重複模式期間結束時停止正在執行的工作實例。</span><span class="sxs-lookup"><span data-stu-id="8c01e-110">A Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c01e-111">備註</span><span class="sxs-lookup"><span data-stu-id="8c01e-111">Remarks</span></span>

<span data-ttu-id="8c01e-112">讀取或寫入工作的 XML 時，這項資訊是在工作排程器架構的 [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="8c01e-112">When reading or writing XML for a task, this information is specified in the [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c01e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c01e-113">Requirements</span></span>



| <span data-ttu-id="8c01e-114">需求</span><span class="sxs-lookup"><span data-stu-id="8c01e-114">Requirement</span></span> | <span data-ttu-id="8c01e-115">值</span><span class="sxs-lookup"><span data-stu-id="8c01e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c01e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c01e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c01e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c01e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8c01e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c01e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c01e-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c01e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c01e-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8c01e-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c01e-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8c01e-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8c01e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8c01e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c01e-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c01e-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c01e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c01e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c01e-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8c01e-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





