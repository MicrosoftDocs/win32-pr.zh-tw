---
title: Action. Type 屬性
description: 針對腳本，會取得動作的類型。
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Type 屬性工作排程器
- Type 屬性工作排程器，Action 物件
- Action 物件工作排程器、Type 屬性
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466037"
---
# <a name="actiontype-property"></a><span data-ttu-id="d8ab0-106">Action. Type 屬性</span><span class="sxs-lookup"><span data-stu-id="d8ab0-106">Action.Type property</span></span>

<span data-ttu-id="d8ab0-107">針對腳本，會取得動作的類型。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-107">For scripting, gets the type of the action.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ab0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8ab0-108">Syntax</span></span>


```VB
Action.Type As Integer
```



## <a name="property-value"></a><span data-ttu-id="d8ab0-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d8ab0-109">Property value</span></span>

<span data-ttu-id="d8ab0-110">這個屬性會傳回下列其中一個 [**工作 \_ 動作 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) 列舉常數。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-110">This property returns one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="d8ab0-111">值</span><span class="sxs-lookup"><span data-stu-id="d8ab0-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="d8ab0-112">意義</span><span class="sxs-lookup"><span data-stu-id="d8ab0-112">Meaning</span></span>                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="d8ab0-113"><dt>**工作 \_動作 \_ EXEC**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8ab0-113"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="d8ab0-114">此動作會執行命令列操作。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-114">This action performs a command-line operation.</span></span> <span data-ttu-id="d8ab0-115">例如，動作可以執行腳本、啟動可執行檔，或者，如果提供檔的名稱，請尋找其相關聯的應用程式，並使用檔啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-115">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="d8ab0-116"><dt>**工作 \_ACTION \_ COM \_ 處理常式**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d8ab0-116"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="d8ab0-117">此動作會引發處理常式。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-117">This action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="d8ab0-118"><dt>**工作 \_動作 \_ 傳送 \_ 電子郵件**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d8ab0-118"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="d8ab0-119">此動作會傳送電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-119">This action sends an email message.</span></span><br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="d8ab0-120"><dt>**工作 \_動作 \_ 顯示 \_ 訊息**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d8ab0-120"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="d8ab0-121">此動作會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-121">This action shows a message box.</span></span><br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="d8ab0-122">備註</span><span class="sxs-lookup"><span data-stu-id="d8ab0-122">Remarks</span></span>

<span data-ttu-id="d8ab0-123">動作類型是在建立動作時定義的，而且稍後無法變更。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-123">The action type is defined when the action is created and cannot be changed later.</span></span> <span data-ttu-id="d8ab0-124">如需建立動作的詳細資訊，請參閱 [**actioncollection 動作。**](actioncollection-create.md)</span><span class="sxs-lookup"><span data-stu-id="d8ab0-124">For information on creating an action, see [**ActionCollection.Create**](actioncollection-create.md).</span></span>

<span data-ttu-id="d8ab0-125">如需動作和工作如何一起運作的詳細資訊，請參閱工作 [動作](task-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="d8ab0-125">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ab0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8ab0-126">Requirements</span></span>



| <span data-ttu-id="d8ab0-127">需求</span><span class="sxs-lookup"><span data-stu-id="d8ab0-127">Requirement</span></span> | <span data-ttu-id="d8ab0-128">值</span><span class="sxs-lookup"><span data-stu-id="d8ab0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ab0-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8ab0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ab0-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8ab0-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d8ab0-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8ab0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ab0-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8ab0-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8ab0-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d8ab0-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8ab0-134"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d8ab0-134"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d8ab0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d8ab0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8ab0-136"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8ab0-136"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ab0-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8ab0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ab0-138">**工作 \_ 動作 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d8ab0-138">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="d8ab0-139">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d8ab0-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d8ab0-140">**動作**</span><span class="sxs-lookup"><span data-stu-id="d8ab0-140">**Action**</span></span>](action.md)
</dt> </dl>

 

 





