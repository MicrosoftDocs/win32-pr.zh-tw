---
description: 關閉 Schannel 連接
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: 關閉 Schannel 連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689479"
---
# <a name="shutting-down-an-schannel-connection"></a><span data-ttu-id="87447-103">關閉 Schannel 連接</span><span class="sxs-lookup"><span data-stu-id="87447-103">Shutting Down an Schannel Connection</span></span>

<span data-ttu-id="87447-104">當用戶端或伺服器完成連線時，必須將其關閉。</span><span class="sxs-lookup"><span data-stu-id="87447-104">When a client or server is finished with a connection, it must shut it down.</span></span> <span data-ttu-id="87447-105">另一方則必須辨識關機並刪除連接。</span><span class="sxs-lookup"><span data-stu-id="87447-105">The other party, in turn, must recognize the shutdown and delete the connection.</span></span>

<span data-ttu-id="87447-106">**關閉 Schannel 連接**</span><span class="sxs-lookup"><span data-stu-id="87447-106">**To shut down an Schannel connection**</span></span>

1.  <span data-ttu-id="87447-107">呼叫 [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) 函式，並指定 SCHANNEL \_ SHUTDOWN 控制項標記。</span><span class="sxs-lookup"><span data-stu-id="87447-107">Call the [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) function, specifying the SCHANNEL\_SHUTDOWN control token.</span></span>
2.  <span data-ttu-id="87447-108">從 ApplyControlToken 收到 SEC \_ E \_ OK 傳回值之後 [](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken)，請)  (用戶端上呼叫 [**InitializeSecurityCoNtext (schannel**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) ，) 或 [**AcceptSecurityCoNtext (schannel**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext))  (伺服器) 函式，傳入空的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="87447-108">After receiving an SEC\_E\_OK return value from [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), call the [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) or [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servers) function, passing in empty buffers.</span></span>
3.  <span data-ttu-id="87447-109">繼續進行，直到函式傳回每秒的 \_ \_ 內容 \_ 過期，或秒 \_ E \_ 確定連接已關閉。</span><span class="sxs-lookup"><span data-stu-id="87447-109">Proceed as though your application were creating a new connection until the function returns SEC\_I\_CONTEXT\_EXPIRED or SEC\_E\_OK to indicate that the connection is shut down.</span></span>
4.  <span data-ttu-id="87447-110">將最終輸出資訊（如果有的話）傳送給遠端方。</span><span class="sxs-lookup"><span data-stu-id="87447-110">Send the final output information, if any, to the remote party.</span></span>
5.  <span data-ttu-id="87447-111">呼叫 [**DeleteSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) 以釋放連接所保留的資源。</span><span class="sxs-lookup"><span data-stu-id="87447-111">Call [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) to free resources held by the connection.</span></span>

## <a name="recognizing-a-shutdown"></a><span data-ttu-id="87447-112">辨識關機</span><span class="sxs-lookup"><span data-stu-id="87447-112">Recognizing a Shutdown</span></span>

<span data-ttu-id="87447-113">[**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)函式會傳回 \_ \_ \_ 當訊息寄件者關閉連線時，我內容已過期的秒數。</span><span class="sxs-lookup"><span data-stu-id="87447-113">The [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) function returns SEC\_I\_CONTEXT\_EXPIRED when the message sender has shut down the connection.</span></span> <span data-ttu-id="87447-114">收到此傳回值之後，請依照本主題稍早所述的程式來關閉 Schannel 連接。</span><span class="sxs-lookup"><span data-stu-id="87447-114">After receiving this return value, follow the procedure To shut down an Schannel connection, earlier in this topic.</span></span>

 

 
