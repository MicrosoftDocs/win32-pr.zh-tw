---
title: 工作排程器2.0 列舉類型
description: 描述列舉型別，這些列舉型別會定義工作排程器 2.0 Api 所使用的常數。
ms.assetid: d59f017e-df32-4826-954d-9ba338282d0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db410564ab97f0477ecac8aeda2b54b8fd655d62
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316852"
---
# <a name="task-scheduler-20-enumerated-types"></a><span data-ttu-id="72650-103">工作排程器2.0 列舉類型</span><span class="sxs-lookup"><span data-stu-id="72650-103">Task Scheduler 2.0 Enumerated Types</span></span>

<span data-ttu-id="72650-104">描述列舉型別，這些列舉型別會定義工作排程器 2.0 Api 所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="72650-104">Describes the enumerated types that define the constants that are used by the Task Scheduler 2.0 APIs.</span></span>


<span data-ttu-id="72650-105">下列列舉類型是在工作排程器2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="72650-105">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="72650-106">列舉型別</span><span class="sxs-lookup"><span data-stu-id="72650-106">Enumeration</span></span>                                                                  | <span data-ttu-id="72650-107">描述</span><span class="sxs-lookup"><span data-stu-id="72650-107">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72650-108">**工作 \_ 動作 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="72650-108">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="72650-109">定義工作可執行檔動作類型。</span><span class="sxs-lookup"><span data-stu-id="72650-109">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="72650-110">**工作 \_ 相容性**</span><span class="sxs-lookup"><span data-stu-id="72650-110">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="72650-111">定義工作相容的工作排程器版本或 AT 命令。</span><span class="sxs-lookup"><span data-stu-id="72650-111">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="72650-112">**工作 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="72650-112">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="72650-113">定義工作排程器服務如何建立、更新或停用工作。</span><span class="sxs-lookup"><span data-stu-id="72650-113">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="72650-114">**工作 \_ 列舉 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="72650-114">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="72650-115">定義工作排程器如何透過已註冊的工作來列舉。</span><span class="sxs-lookup"><span data-stu-id="72650-115">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="72650-116">**工作 \_ 實例 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="72650-116">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="72650-117">定義當工作排程器啟動工作的新實例時，如何處理工作的現有實例。</span><span class="sxs-lookup"><span data-stu-id="72650-117">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="72650-118">**工作 \_ 登入類型**</span><span class="sxs-lookup"><span data-stu-id="72650-118">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="72650-119">定義執行工作所需的登入技巧。</span><span class="sxs-lookup"><span data-stu-id="72650-119">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="72650-120">**TASK \_ PROCESSTOKENSID \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="72650-120">**TASK\_PROCESSTOKENSID\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)             | <span data-ttu-id="72650-121">定義工作可使用的進程 SID 類型。</span><span class="sxs-lookup"><span data-stu-id="72650-121">Defines the types of process SID that can be used by tasks.</span></span>                                                      |
| [<span data-ttu-id="72650-122">**工作 \_ 執行 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="72650-122">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="72650-123">定義工作的執行方式。</span><span class="sxs-lookup"><span data-stu-id="72650-123">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="72650-124">**TASK \_ RUNLEVEL \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="72650-124">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="72650-125">定義 LUA 提高許可權旗標，指定將執行工作的許可權層級。</span><span class="sxs-lookup"><span data-stu-id="72650-125">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="72650-126">**工作 \_ 會話 \_ 狀態 \_ 變更 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="72650-126">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="72650-127">定義您可用來觸發工作啟動的終端機伺服器會話狀態變更類型。</span><span class="sxs-lookup"><span data-stu-id="72650-127">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="72650-128">**工作 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="72650-128">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="72650-129">定義已註冊工作可以處於的不同狀態。</span><span class="sxs-lookup"><span data-stu-id="72650-129">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="72650-130">**工作 \_ 觸發程式 \_ TYPE2**</span><span class="sxs-lookup"><span data-stu-id="72650-130">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="72650-131">定義工作可使用的觸發程式類型。</span><span class="sxs-lookup"><span data-stu-id="72650-131">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="72650-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="72650-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72650-133">工作排程器</span><span class="sxs-lookup"><span data-stu-id="72650-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="72650-134">工作排程器參考</span><span class="sxs-lookup"><span data-stu-id="72650-134">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




