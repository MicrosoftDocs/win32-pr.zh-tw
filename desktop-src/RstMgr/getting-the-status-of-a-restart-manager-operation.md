---
title: 取得重新開機管理員操作的狀態
description: 當許多應用程式和服務必須關閉或重新開機時，重新開機管理員作業可能需要一段很長的時間。 您可以使用下列方法來取得目前作業的狀態。
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093135"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a><span data-ttu-id="572bd-104">取得重新開機管理員操作的狀態</span><span class="sxs-lookup"><span data-stu-id="572bd-104">Getting the Status of a Restart Manager Operation</span></span>

<span data-ttu-id="572bd-105">當許多應用程式和服務必須關閉或重新開機時，重新開機管理員作業可能需要一段很長的時間。</span><span class="sxs-lookup"><span data-stu-id="572bd-105">When many applications and services must be shut down or restarted, the Restart Manager operation can take an extended period of time.</span></span> <span data-ttu-id="572bd-106">您可以使用下列方法來取得目前作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="572bd-106">The following method can be used to obtain the status of the current operation.</span></span>

<span data-ttu-id="572bd-107">**取得目前重新開機管理員操作的狀態**</span><span class="sxs-lookup"><span data-stu-id="572bd-107">**To get the status of the current Restart Manager operation**</span></span>

1.  <span data-ttu-id="572bd-108">安裝程式應該會執行 [**RM \_ 寫入 \_ 狀態 \_ 回檔**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) 函式，以判斷已關閉或重新開機之應用程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="572bd-108">The installer should implement a [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function that determines the status of the applications that have been shut down or restarted.</span></span> <span data-ttu-id="572bd-109">函數可以提供資訊給使用者介面或記錄檔。</span><span class="sxs-lookup"><span data-stu-id="572bd-109">The function can provide the information to the user interface or log.</span></span>
2.  <span data-ttu-id="572bd-110">當呼叫 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)或 [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)函式時，安裝程式會將指標傳遞至 [**RM \_ 寫入 \_ 狀態 \_ 回撥**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback)函式。</span><span class="sxs-lookup"><span data-stu-id="572bd-110">The installer passes the pointer to the [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function when calling the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>

 

 