---
description: 當用戶端完成與任何伺服器的通訊，或使用傳遞至 AcquireCredentialsHandle 函式的其他認證完成時，用戶端必須呼叫 FreeCredentialsHandle 函數。
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: 結束 SSPI 會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690143"
---
# <a name="ending-an-sspi-session"></a><span data-ttu-id="82b47-103">結束 SSPI 會話</span><span class="sxs-lookup"><span data-stu-id="82b47-103">Ending an SSPI Session</span></span>

<span data-ttu-id="82b47-104">在用戶端和伺服器完成通訊之後，雙方都會以各自的內容控制碼呼叫 [**DeleteSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) 函式。</span><span class="sxs-lookup"><span data-stu-id="82b47-104">After the client and server have finished communicating, both sides call the [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) function with their respective context handles.</span></span> <span data-ttu-id="82b47-105">當用戶端完成與任何伺服器的通訊，或使用傳遞至 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 函式的其他認證完成時，用戶端必須呼叫 [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) 函數。</span><span class="sxs-lookup"><span data-stu-id="82b47-105">When the client has finished communicating with any server or has finished using the additional credentials passed to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, the client must call the [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) function.</span></span> <span data-ttu-id="82b47-106">當伺服器準備好要關閉並卸載 DLL 之前，伺服器必須呼叫 **DeleteSecurityCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="82b47-106">When the server is ready to shut down and before unloading the DLL, the server must call **DeleteSecurityContext**.</span></span>

 

 
