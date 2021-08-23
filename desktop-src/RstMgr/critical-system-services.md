---
title: 重要的系統服務
description: 重新開機管理員無法停止和重新開機重要的系統服務，不需要重新開機系統。 更新這些服務中的任何一個使用的檔案或資源時，都需要重新開機系統。
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8a50eca43a62d24e0ab6363844bef7457aaf05b34251f5d804dacabaead5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010226"
---
# <a name="critical-system-services"></a>重要的系統服務

重新開機管理員無法停止和重新開機重要的系統服務，不需要重新開機系統。 更新這些服務中的任何一個使用的檔案或資源時，都需要重新開機系統。

**判斷進程是否為重要的系統服務。**

1.  使用 [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) 函式註冊處理常式。
2.  呼叫 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) 函數，以取得 [**RM \_ 進程 \_ 資訊**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) 結構。
3.  傳回的 [**rm \_ 進程 \_ 資訊**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info)結構的 **ApplicationType** 成員包含 [**rm \_ 應用程式 \_ 類型**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type)的列舉值。 此值會設定為重要系統進程的 **RmCriticial** 。

重要的系統服務包含 smss.exe、csrss.exe、wininit.exe、logonui.exe、lsass.exe、services.exe、winlogon.exe、系統、使用 RPCSS 的 svchost.exe，以及 Dcom/PnP 的 svchost.exe。

 

 




