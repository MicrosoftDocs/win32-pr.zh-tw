---
title: 取消目前的重新開機管理員操作
description: 當使用者動作指示安裝程式執行不同的動作時，您可以使用下列方法來取消目前的重新開機管理員操作。
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675972"
---
# <a name="canceling-the-current-restart-manager-operation"></a><span data-ttu-id="2be5c-103">取消目前的重新開機管理員操作</span><span class="sxs-lookup"><span data-stu-id="2be5c-103">Canceling the Current Restart Manager Operation</span></span>

<span data-ttu-id="2be5c-104">當使用者動作指示安裝程式執行不同的動作時，您可以使用下列方法來取消目前的重新開機管理員操作。</span><span class="sxs-lookup"><span data-stu-id="2be5c-104">When a user action directs the installer to perform a different action, the following method can be used to cancel the current Restart Manager operation.</span></span>

<span data-ttu-id="2be5c-105">**取消目前的重新開機管理員操作**</span><span class="sxs-lookup"><span data-stu-id="2be5c-105">**To cancel the current Restart Manager operation**</span></span>

-   <span data-ttu-id="2be5c-106">安裝程式可以從另一個執行緒呼叫 [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) 函數，以取消目前的 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) 或 [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) 作業。</span><span class="sxs-lookup"><span data-stu-id="2be5c-106">The installer can call the [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) function from another thread to cancel the current [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) operation.</span></span> <span data-ttu-id="2be5c-107">重新開機管理員可能會根據呼叫 **RMCancelCurrentTask** 函式時，作業已完成的程度，來取消作業。</span><span class="sxs-lookup"><span data-stu-id="2be5c-107">The Restart Manager may cancel the operation depending on the extent to which the operation has completed when the **RMCancelCurrentTask** function is called.</span></span>

 

 




