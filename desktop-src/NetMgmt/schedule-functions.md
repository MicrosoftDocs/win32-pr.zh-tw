---
title: 排程函數
description: 網路管理排程服務函式會提交及管理特定時間在指定電腦上執行的工作， (或在未來) 的時間。
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421ae46de8e8152356f64d3855b4fe95c228878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967493"
---
# <a name="schedule-functions"></a>排程函數

網路管理排程服務函式會提交及管理特定時間在指定電腦上執行的工作， (或在未來) 的時間。 作業可以包含命令和程式。 如果電腦上的排程服務正在執行，這些函式會管理遠端和本機電腦上的工作。

排程服務函數如下所示。



| 函式                                                                     | 描述                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | 提交工作，以在指定的未來日期和時間執行。        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | 取消佇列中要在電腦上執行的工作範圍。             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | 列出在指定電腦上佇列的作業。                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | 傳回在電腦上佇列的特定作業的相關資訊。 |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | 捕獲 AT 服務帳戶名稱。                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | 設定 AT 服務帳戶名稱和密碼。                   |



 

若要讓網路管理排程功能成功，呼叫者必須在排程服務執行所在的電腦上具有系統管理員的許可權。 排程服務函式也稱為「作業」和「AT 命令」函數。 如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。

[**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)函式會使用 [**AT \_ INFO**](/windows/desktop/api/Lmat/ns-lmat-at_info)結構來指定提交作業時的資訊，以及由 [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)函數來取得已提交之作業的相關資訊。 [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)使用 [**AT \_ 列舉**](/windows/desktop/api/Lmat/ns-lmat-at_enum)結構來列舉和傳回已提交工作之整個佇列的相關資訊。

 

 