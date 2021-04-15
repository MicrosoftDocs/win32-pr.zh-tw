---
title: TaskSettings. RestartCount 屬性
description: 針對腳本，取得或設定工作排程器將嘗試重新開機工作的次數。
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- RestartCount 屬性工作排程器
- RestartCount 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、RestartCount 屬性
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384345"
---
# <a name="tasksettingsrestartcount-property"></a><span data-ttu-id="6cb0d-106">TaskSettings. RestartCount 屬性</span><span class="sxs-lookup"><span data-stu-id="6cb0d-106">TaskSettings.RestartCount property</span></span>

<span data-ttu-id="6cb0d-107">針對腳本，取得或設定工作排程器將嘗試重新開機工作的次數。</span><span class="sxs-lookup"><span data-stu-id="6cb0d-107">For scripting, gets or sets the number of times that the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="6cb0d-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6cb0d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb0d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cb0d-109">Syntax</span></span>


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a><span data-ttu-id="6cb0d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6cb0d-110">Property value</span></span>

<span data-ttu-id="6cb0d-111">工作排程器將嘗試重新開機工作的次數。</span><span class="sxs-lookup"><span data-stu-id="6cb0d-111">The number of times that the Task Scheduler will attempt to restart the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb0d-112">備註</span><span class="sxs-lookup"><span data-stu-id="6cb0d-112">Remarks</span></span>

<span data-ttu-id="6cb0d-113">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Count**](taskschedulerschema-count-restarttype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="6cb0d-113">When reading or writing XML for a task, this setting is specified in the [**Count**](taskschedulerschema-count-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb0d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cb0d-114">Requirements</span></span>



| <span data-ttu-id="6cb0d-115">需求</span><span class="sxs-lookup"><span data-stu-id="6cb0d-115">Requirement</span></span> | <span data-ttu-id="6cb0d-116">值</span><span class="sxs-lookup"><span data-stu-id="6cb0d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb0d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cb0d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb0d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cb0d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6cb0d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cb0d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb0d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cb0d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6cb0d-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6cb0d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="6cb0d-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6cb0d-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6cb0d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6cb0d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cb0d-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cb0d-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb0d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cb0d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb0d-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="6cb0d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





