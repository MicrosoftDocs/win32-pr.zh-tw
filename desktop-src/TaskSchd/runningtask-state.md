---
title: RunningTask。 State 屬性
description: 針對腳本，會取得正在執行之工作的狀態識別碼。
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- State 屬性工作排程器
- State 屬性工作排程器，RunningTask 物件
- RunningTask 物件工作排程器，State 屬性
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685746"
---
# <a name="runningtaskstate-property"></a><span data-ttu-id="7a17a-106">RunningTask。 State 屬性</span><span class="sxs-lookup"><span data-stu-id="7a17a-106">RunningTask.State property</span></span>

<span data-ttu-id="7a17a-107">針對腳本，會取得正在執行之工作的狀態識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a17a-107">For scripting, gets an identifier for the state of the running task.</span></span>

<span data-ttu-id="7a17a-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7a17a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a17a-109">語法</span><span class="sxs-lookup"><span data-stu-id="7a17a-109">Syntax</span></span>


```VB
RunningTask.State As String
```



## <a name="property-value"></a><span data-ttu-id="7a17a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="7a17a-110">Property value</span></span>

<span data-ttu-id="7a17a-111">正在執行之工作的狀態識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a17a-111">An identifier for the state of the running task.</span></span>



| <span data-ttu-id="7a17a-112">值</span><span class="sxs-lookup"><span data-stu-id="7a17a-112">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="7a17a-113">意義</span><span class="sxs-lookup"><span data-stu-id="7a17a-113">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="7a17a-114"><dt>**工作 \_狀態 \_ 不明**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7a17a-114"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="7a17a-115">工作的狀態未知。</span><span class="sxs-lookup"><span data-stu-id="7a17a-115">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="7a17a-116"><dt>**工作 \_\_停用狀態**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7a17a-116"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="7a17a-117">工作已註冊但已停用，而且沒有工作的實例已排入佇列或正在執行中。</span><span class="sxs-lookup"><span data-stu-id="7a17a-117">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="7a17a-118">工作必須等到啟用之後才能執行。</span><span class="sxs-lookup"><span data-stu-id="7a17a-118">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="7a17a-119"><dt>**工作 \_狀態已 \_ 排入佇列**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7a17a-119"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="7a17a-120">工作的實例已排入佇列。</span><span class="sxs-lookup"><span data-stu-id="7a17a-120">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="7a17a-121"><dt>**工作 \_狀態 \_ 就緒**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7a17a-121"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="7a17a-122">工作已準備好執行，但沒有任何實例已排入佇列或正在執行中。</span><span class="sxs-lookup"><span data-stu-id="7a17a-122">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="7a17a-123"><dt>**工作 \_執行 \_**</dt> <dt>4</dt>的狀態</span><span class="sxs-lookup"><span data-stu-id="7a17a-123"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="7a17a-124">工作的一或多個實例正在執行。</span><span class="sxs-lookup"><span data-stu-id="7a17a-124">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="7a17a-125">備註</span><span class="sxs-lookup"><span data-stu-id="7a17a-125">Remarks</span></span>

<span data-ttu-id="7a17a-126">[**RunningTask**](runningtask-refresh.md)方法會在傳回屬性值之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="7a17a-126">The [**RunningTask.Refresh**](runningtask-refresh.md) method is called before the property value is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a17a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a17a-127">Requirements</span></span>



| <span data-ttu-id="7a17a-128">需求</span><span class="sxs-lookup"><span data-stu-id="7a17a-128">Requirement</span></span> | <span data-ttu-id="7a17a-129">值</span><span class="sxs-lookup"><span data-stu-id="7a17a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a17a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a17a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a17a-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a17a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7a17a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a17a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a17a-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a17a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a17a-134">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7a17a-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a17a-135"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a17a-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a17a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7a17a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a17a-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a17a-137"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





