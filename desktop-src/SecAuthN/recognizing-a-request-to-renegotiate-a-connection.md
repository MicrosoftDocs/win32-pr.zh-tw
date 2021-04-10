---
description: DecryptMessage (一般) 函式會針對來自訊息寄件者的重新送出要求進行陷阱。 它會藉由解密訊息資料並傳回 SEC 的重新協商值，來通知您的應用程式 \_ \_ 。
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: 辨識重新協商連接的要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026710"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a><span data-ttu-id="11c95-104">辨識重新協商連接的要求</span><span class="sxs-lookup"><span data-stu-id="11c95-104">Recognizing a Request to Renegotiate a Connection</span></span>

<span data-ttu-id="11c95-105">[**DecryptMessage (一般)**](decryptmessage--general.md)函式會針對來自訊息寄件者的重新送出要求進行陷阱。</span><span class="sxs-lookup"><span data-stu-id="11c95-105">The [**DecryptMessage (General)**](decryptmessage--general.md) function traps requests for renegotiation coming from the message sender.</span></span> <span data-ttu-id="11c95-106">它會藉由解密訊息資料並傳回 SEC 的重新協商值，來通知您的應用程式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="11c95-106">It notifies your application by decrypting the message data and returning the SEC\_I\_RENEGOTIATE value.</span></span>

<span data-ttu-id="11c95-107">您的應用程式必須藉由呼叫 [**AcceptSecurityCoNtext (一般)**](acceptsecuritycontext--general.md) (伺服器來處理這類要求) 或 [**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md) (用戶端) 和傳遞 SECBUFFER_EXTRA 中的 DecryptMessage 所傳回的 SECBUFFER_TOKEN 內容。</span><span class="sxs-lookup"><span data-stu-id="11c95-107">Your application must handle such requests by calling [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (servers) or [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) and passing the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="11c95-108">在這個初始呼叫傳回值之後，請繼續進行，如同您的應用程式正在建立新的連接。</span><span class="sxs-lookup"><span data-stu-id="11c95-108">After this initial call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 



