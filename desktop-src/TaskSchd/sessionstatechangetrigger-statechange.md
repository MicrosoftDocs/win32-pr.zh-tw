---
title: SessionStateChangeTrigger. StateChange 屬性
description: 針對腳本，取得或設定會觸發工作啟動的終端機伺服器會話變更類型。
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- StateChange 屬性工作排程器
- StateChange 屬性工作排程器，SessionStateChangeTrigger 物件
- SessionStateChangeTrigger 物件工作排程器、StateChange 屬性
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685686"
---
# <a name="sessionstatechangetriggerstatechange-property"></a><span data-ttu-id="df83c-106">SessionStateChangeTrigger. StateChange 屬性</span><span class="sxs-lookup"><span data-stu-id="df83c-106">SessionStateChangeTrigger.StateChange property</span></span>

<span data-ttu-id="df83c-107">針對腳本，取得或設定會觸發工作啟動的終端機伺服器會話變更類型。</span><span class="sxs-lookup"><span data-stu-id="df83c-107">For scripting, gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span>

## <a name="syntax"></a><span data-ttu-id="df83c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="df83c-108">Syntax</span></span>


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a><span data-ttu-id="df83c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="df83c-109">Property value</span></span>

<span data-ttu-id="df83c-110">觸發工作以啟動的終端機伺服器會話變更類型。</span><span class="sxs-lookup"><span data-stu-id="df83c-110">The kind of Terminal Server session change that triggers a task to launch.</span></span>

<span data-ttu-id="df83c-111">可能的值來自工作 [**\_ 會話 \_ 狀態 \_ 變更 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) 列舉。</span><span class="sxs-lookup"><span data-stu-id="df83c-111">The possible values are from the [**TASK\_SESSION\_STATE\_CHANGE\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) enumeration.</span></span>



| <span data-ttu-id="df83c-112">值</span><span class="sxs-lookup"><span data-stu-id="df83c-112">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="df83c-113">意義</span><span class="sxs-lookup"><span data-stu-id="df83c-113">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <span data-ttu-id="df83c-114"><dt>**工作 \_主控台 \_ 連接**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="df83c-114"><dt>**TASK\_CONSOLE\_CONNECT**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="df83c-115">終端機伺服器主控台連接狀態變更。</span><span class="sxs-lookup"><span data-stu-id="df83c-115">Terminal Server console connection state change.</span></span> <span data-ttu-id="df83c-116">例如，當您藉由切換電腦上的使用者，連接到本機電腦上的使用者會話時。</span><span class="sxs-lookup"><span data-stu-id="df83c-116">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <span data-ttu-id="df83c-117"><dt>**工作 \_主控台 \_ 中斷**</dt>連線 <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="df83c-117"><dt>**TASK\_CONSOLE\_DISCONNECT**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="df83c-118">終端機伺服器主控台中斷連接狀態變更。</span><span class="sxs-lookup"><span data-stu-id="df83c-118">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="df83c-119">例如，當您藉由切換電腦上的使用者，在本機電腦上中斷使用者會話的連線時。</span><span class="sxs-lookup"><span data-stu-id="df83c-119">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span><br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <span data-ttu-id="df83c-120"><dt>**工作 \_遠端 \_ 連接**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="df83c-120"><dt>**TASK\_REMOTE\_CONNECT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="df83c-121">終端機伺服器遠端線上狀態變更。</span><span class="sxs-lookup"><span data-stu-id="df83c-121">Terminal Server remote connection state change.</span></span> <span data-ttu-id="df83c-122">例如，當使用者從遠端電腦使用遠端桌面連線程式連接到使用者會話時。</span><span class="sxs-lookup"><span data-stu-id="df83c-122">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span><br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <span data-ttu-id="df83c-123"><dt>**工作 \_遠端 \_ 中斷**</dt>連線 <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="df83c-123"><dt>**TASK\_REMOTE\_DISCONNECT**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="df83c-124">終端機伺服器遠端中斷連接狀態變更。</span><span class="sxs-lookup"><span data-stu-id="df83c-124">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="df83c-125">例如，當使用者從遠端電腦使用遠端桌面連線程式時，從使用者會話中斷連線。</span><span class="sxs-lookup"><span data-stu-id="df83c-125">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span><br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <span data-ttu-id="df83c-126"><dt>**工作 \_會話 \_ 鎖定**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="df83c-126"><dt>**TASK\_SESSION\_LOCK**</dt> <dt>7</dt></span></span> </dl>                   | <span data-ttu-id="df83c-127">終端機伺服器會話鎖定狀態變更。</span><span class="sxs-lookup"><span data-stu-id="df83c-127">Terminal Server session locked state change.</span></span> <span data-ttu-id="df83c-128">例如，此狀態變更會在電腦鎖定時執行工作。</span><span class="sxs-lookup"><span data-stu-id="df83c-128">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <span data-ttu-id="df83c-129"><dt>**工作 \_會話 \_ 解除鎖定**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="df83c-129"><dt>**TASK\_SESSION\_UNLOCK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="df83c-130">終端機伺服器會話已解除鎖定狀態變更。</span><span class="sxs-lookup"><span data-stu-id="df83c-130">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="df83c-131">例如，此狀態變更會在電腦解除鎖定時，讓工作執行。</span><span class="sxs-lookup"><span data-stu-id="df83c-131">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="df83c-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="df83c-132">Requirements</span></span>



| <span data-ttu-id="df83c-133">需求</span><span class="sxs-lookup"><span data-stu-id="df83c-133">Requirement</span></span> | <span data-ttu-id="df83c-134">值</span><span class="sxs-lookup"><span data-stu-id="df83c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df83c-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df83c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="df83c-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df83c-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="df83c-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df83c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="df83c-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df83c-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df83c-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="df83c-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="df83c-140"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="df83c-140"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="df83c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="df83c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df83c-142"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df83c-142"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





