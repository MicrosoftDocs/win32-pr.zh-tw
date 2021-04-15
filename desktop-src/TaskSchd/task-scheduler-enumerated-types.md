---
title: 工作排程器列舉類型
description: 列出工作排程器 Api 使用的列舉。
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- 工作排程器工作排程器、參考、列舉類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508208"
---
# <a name="task-scheduler-enumerated-types"></a><span data-ttu-id="5321c-104">工作排程器列舉類型</span><span class="sxs-lookup"><span data-stu-id="5321c-104">Task Scheduler Enumerated Types</span></span>

<span data-ttu-id="5321c-105">描述定義工作排程器 Api 所使用之常數的列舉類型。</span><span class="sxs-lookup"><span data-stu-id="5321c-105">Describes the enumerated types that define the constants that are used by the Task Scheduler APIs.</span></span>


<span data-ttu-id="5321c-106">下列列舉類型是在工作排程器2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="5321c-106">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="5321c-107">列舉型別</span><span class="sxs-lookup"><span data-stu-id="5321c-107">Enumeration</span></span>                                                                  | <span data-ttu-id="5321c-108">描述</span><span class="sxs-lookup"><span data-stu-id="5321c-108">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5321c-109">**工作 \_ 動作 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="5321c-109">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="5321c-110">定義工作可執行檔動作類型。</span><span class="sxs-lookup"><span data-stu-id="5321c-110">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="5321c-111">**工作 \_ 相容性**</span><span class="sxs-lookup"><span data-stu-id="5321c-111">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="5321c-112">定義工作相容的工作排程器版本或 AT 命令。</span><span class="sxs-lookup"><span data-stu-id="5321c-112">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="5321c-113">**工作 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="5321c-113">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="5321c-114">定義工作排程器服務如何建立、更新或停用工作。</span><span class="sxs-lookup"><span data-stu-id="5321c-114">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="5321c-115">**工作 \_ 列舉 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="5321c-115">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="5321c-116">定義工作排程器如何透過已註冊的工作來列舉。</span><span class="sxs-lookup"><span data-stu-id="5321c-116">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="5321c-117">**工作 \_ 實例 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="5321c-117">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="5321c-118">定義當工作排程器啟動工作的新實例時，如何處理工作的現有實例。</span><span class="sxs-lookup"><span data-stu-id="5321c-118">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="5321c-119">**工作 \_ 登入類型**</span><span class="sxs-lookup"><span data-stu-id="5321c-119">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="5321c-120">定義執行工作所需的登入技巧。</span><span class="sxs-lookup"><span data-stu-id="5321c-120">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="5321c-121">**TASK \_ PROCESSTOKENSID 類型**</span><span class="sxs-lookup"><span data-stu-id="5321c-121">**TASK\_PROCESSTOKENSID TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | <span data-ttu-id="5321c-122">定義工作可使用的進程 SID 類型。</span><span class="sxs-lookup"><span data-stu-id="5321c-122">Defines the types of process SID that can used by tasks.</span></span>                                                         |
| [<span data-ttu-id="5321c-123">**工作 \_ 執行 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="5321c-123">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="5321c-124">定義工作的執行方式。</span><span class="sxs-lookup"><span data-stu-id="5321c-124">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="5321c-125">**TASK \_ RUNLEVEL \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="5321c-125">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="5321c-126">定義 LUA 提高許可權旗標，指定將執行工作的許可權層級。</span><span class="sxs-lookup"><span data-stu-id="5321c-126">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="5321c-127">**工作 \_ 會話 \_ 狀態 \_ 變更 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="5321c-127">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="5321c-128">定義您可用來觸發工作啟動的終端機伺服器會話狀態變更類型。</span><span class="sxs-lookup"><span data-stu-id="5321c-128">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="5321c-129">**工作 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="5321c-129">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="5321c-130">定義已註冊工作可以處於的不同狀態。</span><span class="sxs-lookup"><span data-stu-id="5321c-130">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="5321c-131">**工作 \_ 觸發程式 \_ TYPE2**</span><span class="sxs-lookup"><span data-stu-id="5321c-131">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="5321c-132">定義工作可使用的觸發程式類型。</span><span class="sxs-lookup"><span data-stu-id="5321c-132">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 


> [!WARNING]
> <span data-ttu-id="5321c-133">工作排程器1.0 列舉僅適用于 Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="5321c-133">The Task Scheduler 1.0 enumerations are available only in Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5321c-134">它們已在 Windows Vista 中淘汰，未來可能會完全移除。</span><span class="sxs-lookup"><span data-stu-id="5321c-134">They are deprecated as of Windows Vista and may be removed completely in the future.</span></span> <span data-ttu-id="5321c-135">請改用上述的工作排程器2.0 列舉。</span><span class="sxs-lookup"><span data-stu-id="5321c-135">Please use the Task Scheduler 2.0 enumerations listed above instead.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5321c-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="5321c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5321c-137">工作排程器</span><span class="sxs-lookup"><span data-stu-id="5321c-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5321c-138">工作排程器參考</span><span class="sxs-lookup"><span data-stu-id="5321c-138">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




