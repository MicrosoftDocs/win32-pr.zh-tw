---
title: 取消目前的重新開機管理員操作
description: 當使用者動作指示安裝程式執行不同的動作時，您可以使用下列方法來取消目前的重新開機管理員操作。
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c745a76ab8c72acaff0b9f1ae85ded380e1113c3687822e916b422cad9ef51f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010246"
---
# <a name="canceling-the-current-restart-manager-operation"></a>取消目前的重新開機管理員操作

當使用者動作指示安裝程式執行不同的動作時，您可以使用下列方法來取消目前的重新開機管理員操作。

**取消目前的重新開機管理員操作**

-   安裝程式可以從另一個執行緒呼叫 [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) 函數，以取消目前的 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) 或 [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) 作業。 重新開機管理員可能會根據呼叫 **RMCancelCurrentTask** 函式時，作業已完成的程度，來取消作業。

 

 




