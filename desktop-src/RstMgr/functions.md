---
title: 重新開機管理員函式
description: 重新開機管理員 API 會使用下表中所識別的功能。
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- 重新開機管理員重新開機管理員、參考、函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839851"
---
# <a name="restart-manager-functions"></a>重新開機管理員函式

重新開機管理員 API 會使用下表中所識別的功能。



| 函式                                           | 描述                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | 修改關機或重新開機動作。                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | 啟動新的重新開機管理員會話。                                                                                                                                                        |
| [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | 將應用程式的處理常式加入至現有的重新開機管理員會話。                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | 結束重新開機管理員會話。                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | 將資源（例如檔案名、服務簡短名稱或 [**RM \_ 唯一 \_ 進程**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) 結構）註冊到重新開機管理員會話。                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | 供安裝程式用來取得受註冊資源影響的所有應用程式清單及其目前狀態。                                                                              |
| [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | 查詢關閉的狀態，並重新啟動已套用的修改。                                                                                                     |
| [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | 起始應用程式和服務的關閉。                                                                                                                                        |
| [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | 移除已套用的關機和重新開機修改。                                                                                                                   |
| [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | 重新開機 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) 函式已關閉的應用程式和服務，並使用 **RegisterApplicationRestart** 註冊要重新開機的應用程式和服務。 |
| [**RmCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | 取消目前的 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)、 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)或 [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) 函數。                                                            |



 

 

 




