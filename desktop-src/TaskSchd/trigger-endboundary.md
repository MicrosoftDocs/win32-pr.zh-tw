---
title: EndBoundary 屬性
description: 針對腳本，取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- EndBoundary 屬性工作排程器
- EndBoundary 屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，EndBoundary 屬性
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024878"
---
# <a name="triggerendboundary-property"></a><span data-ttu-id="4302b-107">EndBoundary 屬性</span><span class="sxs-lookup"><span data-stu-id="4302b-107">Trigger.EndBoundary property</span></span>

<span data-ttu-id="4302b-108">針對腳本，取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4302b-108">For scripting, gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="4302b-109">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4302b-109">The trigger cannot start the task after it is deactivated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4302b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4302b-110">Syntax</span></span>


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="4302b-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="4302b-111">Property value</span></span>

<span data-ttu-id="4302b-112">停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4302b-112">The date and time when the trigger is deactivated.</span></span> <span data-ttu-id="4302b-113">日期和時間必須採用下列格式： YYYY-MM-DD DDTHH： MM： SS (+-) HH： MM。</span><span class="sxs-lookup"><span data-stu-id="4302b-113">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="4302b-114">例如，太平洋時區2005年10月11日的日期將會寫入1:21:17 至 2005-10-11T13：21： 17-08：00。</span><span class="sxs-lookup"><span data-stu-id="4302b-114">For example the date October 11th, 2005 at 1:21:17 in the Pacific time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="4302b-115">格式的 (+-) HH： MM 區段會將時區描述為提前或後方的特定時數，國際標準時間 (格林尼治平均時間) 。</span><span class="sxs-lookup"><span data-stu-id="4302b-115">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="4302b-116">備註</span><span class="sxs-lookup"><span data-stu-id="4302b-116">Remarks</span></span>

<span data-ttu-id="4302b-117">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) 元素來指定 enabled 屬性。</span><span class="sxs-lookup"><span data-stu-id="4302b-117">When reading or writing XML for a task, the enabled property is specified using the [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4302b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4302b-118">Requirements</span></span>



| <span data-ttu-id="4302b-119">需求</span><span class="sxs-lookup"><span data-stu-id="4302b-119">Requirement</span></span> | <span data-ttu-id="4302b-120">值</span><span class="sxs-lookup"><span data-stu-id="4302b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4302b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4302b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4302b-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4302b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4302b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4302b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4302b-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4302b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4302b-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4302b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="4302b-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4302b-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4302b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4302b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4302b-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4302b-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4302b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4302b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4302b-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="4302b-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





