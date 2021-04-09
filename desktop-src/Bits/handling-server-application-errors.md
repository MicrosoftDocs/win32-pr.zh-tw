---
title: 處理伺服器應用程式錯誤
description: 如果伺服器應用程式成功處理上傳的檔案，應用程式應該會傳回200。
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671436"
---
# <a name="handling-server-application-errors"></a><span data-ttu-id="6da88-103">處理伺服器應用程式錯誤</span><span class="sxs-lookup"><span data-stu-id="6da88-103">Handling Server Application Errors</span></span>

<span data-ttu-id="6da88-104">如果伺服器應用程式成功處理上傳的檔案，應用程式應該會傳回200。</span><span class="sxs-lookup"><span data-stu-id="6da88-104">If the server application successfully processes the uploaded file, the application should return 200.</span></span> <span data-ttu-id="6da88-105">如果應用程式未傳回200，BITS 用戶端會使用錯誤碼來判斷錯誤是暫時性錯誤或嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="6da88-105">If the application does not return 200, the BITS client uses the error code to determine if the error is a transient error or fatal error.</span></span>

<span data-ttu-id="6da88-106">所有3xx 錯誤碼都是暫時性錯誤，除了 300-305 和307之外，這些都是嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="6da88-106">All 3xx error codes are transient errors except 300 - 305 and 307, which are fatal errors.</span></span> <span data-ttu-id="6da88-107">除了408和409之外，所有4xx 錯誤碼都是嚴重錯誤，這是暫時性錯誤。</span><span class="sxs-lookup"><span data-stu-id="6da88-107">All 4xx error codes are fatal errors except for 408 and 409, which are transient errors.</span></span> <span data-ttu-id="6da88-108">所有5xx 錯誤碼都是暫時性錯誤，除了501和505之外，這些都是嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="6da88-108">All 5xx error codes are transient errors except 501 and 505, which are fatal errors.</span></span> <span data-ttu-id="6da88-109">所有其他 HTTP 代碼都會被視為暫時性錯誤。</span><span class="sxs-lookup"><span data-stu-id="6da88-109">All other HTTP codes are considered transient errors.</span></span> <span data-ttu-id="6da88-110">請注意，403錯誤碼是唯一的錯誤碼，可防止 BITS 再次將上傳檔案張貼至伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="6da88-110">Note that a 403 error code is the only error code that prevents BITS from posting the upload file to the server application again.</span></span>

<span data-ttu-id="6da88-111">若要取出錯誤，請呼叫 [**IBackgroundCopyError：： GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) 方法。</span><span class="sxs-lookup"><span data-stu-id="6da88-111">To retrieve the error, call the [**IBackgroundCopyError::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) method.</span></span> <span data-ttu-id="6da88-112">錯誤內容將會是 BG \_ 錯誤 \_ 內容 \_ 遠端 \_ 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6da88-112">The error context will be BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION.</span></span>

 

 




