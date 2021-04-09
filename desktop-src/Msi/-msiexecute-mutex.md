---
description: '\_只有在處理 InstallExecuteSequence 資料表、AdminExecuteSequence 資料表或 AdvtExecuteSequence 資料表時，才會設定 MSIExecute Mutex。'
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849009"
---
# <a name="_msiexecute-mutex"></a>\_MSIExecute Mutex

\_只有在處理[InstallExecuteSequence 資料表](installexecutesequence-table.md)、 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)或[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)時，才會設定 MSIExecute Mutex。

因為兩個安裝無法在相同的進程中執行，所以嘗試呼叫安裝程式的應用程式開發介面 (API) 會 \_ \_ \_ 在兩種情況下，傳回已執行 (1618) 的錯誤安裝：

-   \_MSIExecute Mutex 設定時。
-   目前的進程正在處理 [InstallUISequence 資料表](installuisequence-table.md) 或 [AdminUISequence 資料表](adminuisequence-table.md)。

如需所安裝之應用程式的相關資訊，請參閱 [事件記錄](event-logging.md) 訊息。

如果傳回錯誤 \_ 安裝已在執行 \_ 中的 \_ 錯誤，您可以先取出 Windows Installer 服務的目前狀態，然後再嘗試使用 [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) 函式來開始安裝。 如果所傳回 [**服務 \_ 狀態 \_ 進程**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process)結構的 **DwControlsAccepted** 成員值為「**服務 \_ 接受 \_ 關機**」，則 Windows Installer 服務目前正在執行。

**Windows Installer 2.0：** 不支援。 使用 [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) 函式來取出 Windows Installer 服務的目前狀態需要 Windows Installer 3.0 版或更高版本。

 

 
