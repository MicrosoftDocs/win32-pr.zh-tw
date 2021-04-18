---
title: Trigger.Id 屬性
description: 針對腳本，取得或設定觸發程式的識別碼。
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Id 屬性工作排程器
- Id 屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，識別碼屬性
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508428"
---
# <a name="triggerid-property"></a><span data-ttu-id="8244b-106">Trigger.Id 屬性</span><span class="sxs-lookup"><span data-stu-id="8244b-106">Trigger.Id property</span></span>

<span data-ttu-id="8244b-107">針對腳本，取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8244b-107">For scripting, gets or sets the identifier for the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="8244b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8244b-108">Syntax</span></span>


```VB
Trigger.Id As String
```



## <a name="property-value"></a><span data-ttu-id="8244b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8244b-109">Property value</span></span>

<span data-ttu-id="8244b-110">觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8244b-110">The identifier for the trigger.</span></span> <span data-ttu-id="8244b-111">工作排程器使用此識別碼來進行記錄。</span><span class="sxs-lookup"><span data-stu-id="8244b-111">This identifier is used by the Task Scheduler for logging purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="8244b-112">備註</span><span class="sxs-lookup"><span data-stu-id="8244b-112">Remarks</span></span>

<span data-ttu-id="8244b-113">讀取或寫入工作的 XML 時，會在個別觸發程式專案的 Id 屬性中指定觸發程式識別碼 (例如，工作排程器架構之 [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) 元素) 的 id 屬性。</span><span class="sxs-lookup"><span data-stu-id="8244b-113">When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element) of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8244b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8244b-114">Requirements</span></span>



| <span data-ttu-id="8244b-115">需求</span><span class="sxs-lookup"><span data-stu-id="8244b-115">Requirement</span></span> | <span data-ttu-id="8244b-116">值</span><span class="sxs-lookup"><span data-stu-id="8244b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8244b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8244b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8244b-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8244b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8244b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8244b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8244b-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8244b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8244b-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8244b-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8244b-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8244b-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8244b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8244b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8244b-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8244b-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8244b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8244b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8244b-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8244b-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





