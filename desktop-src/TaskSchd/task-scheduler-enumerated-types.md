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
# <a name="task-scheduler-enumerated-types"></a>工作排程器列舉類型

描述定義工作排程器 Api 所使用之常數的列舉類型。


下列列舉類型是在工作排程器2.0 中引進。



| 列舉型別                                                                  | 描述                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**工作 \_ 動作 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | 定義工作可執行檔動作類型。                                                             |
| [**工作 \_ 相容性**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | 定義工作相容的工作排程器版本或 AT 命令。                      |
| [**工作 \_ 建立**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | 定義工作排程器服務如何建立、更新或停用工作。                                   |
| [**工作 \_ 列舉 \_ 旗標**](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | 定義工作排程器如何透過已註冊的工作來列舉。                                              |
| [**工作 \_ 實例 \_ 原則**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | 定義當工作排程器啟動工作的新實例時，如何處理工作的現有實例。 |
| [**工作 \_ 登入類型**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | 定義執行工作所需的登入技巧。                                                          |
| [**TASK \_ PROCESSTOKENSID 類型**](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | 定義工作可使用的進程 SID 類型。                                                         |
| [**工作 \_ 執行 \_ 旗標**](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | 定義工作的執行方式。                                                                                       |
| [**TASK \_ RUNLEVEL \_ 類型**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | 定義 LUA 提高許可權旗標，指定將執行工作的許可權層級。                         |
| [**工作 \_ 會話 \_ 狀態 \_ 變更 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | 定義您可用來觸發工作啟動的終端機伺服器會話狀態變更類型。               |
| [**工作 \_ 狀態**](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | 定義已註冊工作可以處於的不同狀態。                                                   |
| [**工作 \_ 觸發程式 \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | 定義工作可使用的觸發程式類型。                                                          |



 


> [!WARNING]
> 工作排程器1.0 列舉僅適用于 Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它們已在 Windows Vista 中淘汰，未來可能會完全移除。 請改用上述的工作排程器2.0 列舉。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[工作排程器參考](task-scheduler-reference.md)
</dt> </dl>

 

 




