---
title: StartBoundary 屬性
description: 針對腳本，取得或設定啟動觸發程式的日期和時間。
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- StartBoundary 屬性工作排程器
- StartBoundary 屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，StartBoundary 屬性
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685731"
---
# <a name="triggerstartboundary-property"></a><span data-ttu-id="d8a31-106">StartBoundary 屬性</span><span class="sxs-lookup"><span data-stu-id="d8a31-106">Trigger.StartBoundary property</span></span>

<span data-ttu-id="d8a31-107">針對腳本，取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d8a31-107">For scripting, gets or sets the date and time when the trigger is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a31-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8a31-108">Syntax</span></span>


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="d8a31-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d8a31-109">Property value</span></span>

<span data-ttu-id="d8a31-110">啟用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d8a31-110">The date and time when the trigger is activated.</span></span> <span data-ttu-id="d8a31-111">日期和時間必須採用下列格式： YYYY-MM-DD DDTHH： MM： SS (+-) HH： MM。</span><span class="sxs-lookup"><span data-stu-id="d8a31-111">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="d8a31-112">例如，太平洋時區2005年10月11日的日期將會寫入1:21:17 至 2005-10-11T13：21： 17-08：00。</span><span class="sxs-lookup"><span data-stu-id="d8a31-112">For example the date October 11th, 2005 at 1:21:17 in the Pacific Time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="d8a31-113">格式的 (+-) HH： MM 區段會將時區描述為提前或後方的特定時數，國際標準時間 (格林尼治平均時間) 。</span><span class="sxs-lookup"><span data-stu-id="d8a31-113">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a31-114">備註</span><span class="sxs-lookup"><span data-stu-id="d8a31-114">Remarks</span></span>

<span data-ttu-id="d8a31-115">讀取或寫入工作的 XML 時，觸發程式起始界限是在工作排程器架構的 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="d8a31-115">When reading or writing XML for a task, the trigger start boundary is specified in the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8a31-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8a31-116">Requirements</span></span>



| <span data-ttu-id="d8a31-117">需求</span><span class="sxs-lookup"><span data-stu-id="d8a31-117">Requirement</span></span> | <span data-ttu-id="d8a31-118">值</span><span class="sxs-lookup"><span data-stu-id="d8a31-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a31-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8a31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d8a31-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8a31-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d8a31-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8a31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d8a31-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8a31-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8a31-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d8a31-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8a31-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d8a31-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d8a31-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d8a31-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8a31-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8a31-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8a31-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8a31-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a31-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d8a31-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





