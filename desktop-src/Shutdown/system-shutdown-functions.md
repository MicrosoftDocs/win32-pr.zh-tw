---
description: 下列函式可用於系統關機。
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: 系統關機功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b1304a2333d817be7cbb51ee599f37cda8b3e185f56cfc5959f1646e9ab639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664338"
---
# <a name="system-shutdown-functions"></a>系統關機功能

下列函式可用於系統關機。



| 函式                                                         | 描述                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | 停止已起始的系統關機。                                                                                    |
| [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | 登出互動式使用者。                                                                                                      |
| [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | 登出互動式使用者、關閉系統，或關閉並重新啟動系統。                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | 起始指定電腦的關機和重新開機，並重新啟動任何已註冊要重新開機的應用程式。    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | 起始指定電腦的關機和選擇性重新開機。                                                                |
| [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | 起始指定電腦的關機和選擇性重新開機，並選擇性地記錄關機的原因。            |
| [**>lockworkstation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | 鎖定工作站的顯示。                                                                                                    |
| [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | 指出系統無法關機，並設定當系統關機啟動時要顯示給使用者的原因字串。 |
| [**ShutdownBlockReasonDestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | 表示系統可以關閉並釋出原因字串。                                                             |
| [**ShutdownBlockReasonQuery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | 抓取 [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) 函數所設定的原因字串。                     |



 

 

 



