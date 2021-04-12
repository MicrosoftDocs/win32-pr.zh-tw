---
title: Actioncollection 動作. Create 方法
description: 針對腳本，會建立新的動作，並將其加入至集合。
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- 建立方法工作排程器
- 建立方法工作排程器，Actioncollection 動作物件
- Actioncollection 動作物件工作排程器，建立方法
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508879"
---
# <a name="actioncollectioncreate-method"></a><span data-ttu-id="d7009-106">Actioncollection 動作. Create 方法</span><span class="sxs-lookup"><span data-stu-id="d7009-106">ActionCollection.Create method</span></span>

<span data-ttu-id="d7009-107">針對腳本，會建立新的動作，並將其加入至集合。</span><span class="sxs-lookup"><span data-stu-id="d7009-107">For scripting, creates and adds a new action to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7009-108">語法</span><span class="sxs-lookup"><span data-stu-id="d7009-108">Syntax</span></span>


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="d7009-109">參數</span><span class="sxs-lookup"><span data-stu-id="d7009-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7009-110">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7009-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7009-111">此參數會設定為下列其中一個工作 [**\_ 動作 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) 列舉常數。</span><span class="sxs-lookup"><span data-stu-id="d7009-111">This parameter is set to one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="d7009-112">值</span><span class="sxs-lookup"><span data-stu-id="d7009-112">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="d7009-113">意義</span><span class="sxs-lookup"><span data-stu-id="d7009-113">Meaning</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="d7009-114"><dt>**工作 \_動作 \_ EXEC**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d7009-114"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="d7009-115">動作會執行命令列操作。</span><span class="sxs-lookup"><span data-stu-id="d7009-115">The action performs a command-line operation.</span></span> <span data-ttu-id="d7009-116">例如，動作可以執行腳本、啟動可執行檔，或者，如果提供檔的名稱，請尋找其相關聯的應用程式，並使用檔啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7009-116">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="d7009-117"><dt>**工作 \_ACTION \_ COM \_ 處理常式**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d7009-117"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="d7009-118">動作會引發處理常式。</span><span class="sxs-lookup"><span data-stu-id="d7009-118">The action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="d7009-119"><dt>**工作 \_動作 \_ 傳送 \_ 電子郵件**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d7009-119"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="d7009-120">此動作會傳送電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="d7009-120">This action sends email message.</span></span><br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="d7009-121"><dt>**工作 \_動作 \_ 顯示 \_ 訊息**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d7009-121"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="d7009-122">此動作會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="d7009-122">This action shows a message box.</span></span><br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7009-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7009-123">Return value</span></span>

<span data-ttu-id="d7009-124">代表新動作的 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d7009-124">An [**Action**](action.md) object that represents the new action.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7009-125">備註</span><span class="sxs-lookup"><span data-stu-id="d7009-125">Remarks</span></span>

<span data-ttu-id="d7009-126">您無法將32個以上的動作加入至集合。</span><span class="sxs-lookup"><span data-stu-id="d7009-126">You cannot add more than 32 actions to the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7009-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7009-127">Requirements</span></span>



| <span data-ttu-id="d7009-128">需求</span><span class="sxs-lookup"><span data-stu-id="d7009-128">Requirement</span></span> | <span data-ttu-id="d7009-129">值</span><span class="sxs-lookup"><span data-stu-id="d7009-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7009-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7009-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d7009-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7009-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d7009-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7009-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d7009-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7009-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7009-134">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d7009-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7009-135"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7009-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7009-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d7009-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7009-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7009-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7009-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7009-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7009-139">**工作 \_ 動作 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d7009-139">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="d7009-140">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d7009-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d7009-141">**Actioncollection 動作**</span><span class="sxs-lookup"><span data-stu-id="d7009-141">**ActionCollection**</span></span>](actioncollection.md)
</dt> <dt>

[<span data-ttu-id="d7009-142">**行動**</span><span class="sxs-lookup"><span data-stu-id="d7009-142">**Action**</span></span>](action.md)
</dt> <dt>

[<span data-ttu-id="d7009-143">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="d7009-143">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="d7009-144">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="d7009-144">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="d7009-145">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="d7009-145">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> <dt>

[<span data-ttu-id="d7009-146">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="d7009-146">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





