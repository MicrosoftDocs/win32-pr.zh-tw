---
title: 處理 RAS 錯誤
description: 當發生錯誤時，遠端存取連線管理員會叫用用戶端的通知處理常式。
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- 遠端存取服務 RAS，錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674779"
---
# <a name="handling-ras-errors"></a><span data-ttu-id="9e85c-104">處理 RAS 錯誤</span><span class="sxs-lookup"><span data-stu-id="9e85c-104">Handling RAS Errors</span></span>

<span data-ttu-id="9e85c-105">當發生錯誤時，遠端存取連線管理員會叫用用戶端的通知處理常式。</span><span class="sxs-lookup"><span data-stu-id="9e85c-105">When an error occurs, the Remote Access Connection Manager invokes the client's notification handler.</span></span> <span data-ttu-id="9e85c-106">通知會指出發生錯誤時的連接狀態，以及識別錯誤的程式碼。</span><span class="sxs-lookup"><span data-stu-id="9e85c-106">The notification indicates the connection state when the error occurred, and a code that identifies the error.</span></span> <span data-ttu-id="9e85c-107">在這些情況下，通知處理常式應該呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 來結束 RAS 連接。</span><span class="sxs-lookup"><span data-stu-id="9e85c-107">In these cases, the notification handler should call [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) to end the RAS connection.</span></span>

<span data-ttu-id="9e85c-108">識別 RAS 錯誤的錯誤碼定義于 raserror 檔案中。</span><span class="sxs-lookup"><span data-stu-id="9e85c-108">The error codes that identify RAS errors are defined in the file raserror.h.</span></span> <span data-ttu-id="9e85c-109">RAS 用戶端可以使用 [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) 函數取得描述錯誤的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="9e85c-109">The RAS client can use the [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) function to get a display string describing the error.</span></span> <span data-ttu-id="9e85c-110">如需這些錯誤的說明，請參閱 [路由和遠端存取錯誤碼](routing-and-remote-access-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="9e85c-110">See [Routing and Remote Access Error Codes](routing-and-remote-access-error-codes.md) for a description of these errors.</span></span>

 

 




