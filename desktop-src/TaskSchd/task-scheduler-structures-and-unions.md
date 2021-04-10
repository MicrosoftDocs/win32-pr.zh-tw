---
title: 工作排程器結構和等位
description: 列出工作排程器 1.0 Api 所使用的結構和等位。
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- 工作排程器工作排程器、參考、結構和等位
- 觸發程式工作排程器，結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183118"
---
# <a name="task-scheduler-structures-and-unions"></a>工作排程器結構和等位

本節說明工作排程器 Api 所使用的結構和等位。

下列所有結構和等位都是由工作排程器1.0 所使用。



| Name                                               | 描述                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**日常**](/windows/desktop/api/Mstask/ns-mstask-daily)                             | 定義工作執行的間隔（以天為單位）。                                                                          |
| [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | 定義工作將執行的當月日期。                                                                                 |
| [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | 定義工作依月、周和星期幾執行的 () 日期。                                                     |
| [**工作 \_ 觸發程式**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | 定義執行排程 [*工作專案*](w.md)的時間。                                                  |
| [**觸發程式 \_ 類型聯 \_ 集**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | 在工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)程式結構的 **型** 別成員內定義觸發程式的調用排程。 |
| [**每週**](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | 定義工作調用之間的間隔（以周為單位）。                                                                  |



 

 

 




