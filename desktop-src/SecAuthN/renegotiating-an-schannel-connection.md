---
description: 若要變更連接的屬性（例如，加密套件或用戶端驗證），您可以要求 &\# 0034; 重做&\# 0034; 或重新協商連接。
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: 重新交涉 Schannel 連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978951"
---
# <a name="renegotiating-an-schannel-connection"></a><span data-ttu-id="ca538-103">重新交涉 Schannel 連線</span><span class="sxs-lookup"><span data-stu-id="ca538-103">Renegotiating an Schannel Connection</span></span>

<span data-ttu-id="ca538-104">若要變更連接的屬性（例如，加密套件或用戶端驗證），您可以要求「重做」或重新協商連接。</span><span class="sxs-lookup"><span data-stu-id="ca538-104">To change a connection's attributes, such as the cipher suite or client authentication, you can request a "redo" or renegotiation of the connection.</span></span>

<span data-ttu-id="ca538-105">如果您想要變更的屬性是以認證來控制，您必須先取得新的認證，然後再重新協商連接。</span><span class="sxs-lookup"><span data-stu-id="ca538-105">If the attributes you want to change are controlled by credentials, you must obtain new credentials before you renegotiate the connection.</span></span> <span data-ttu-id="ca538-106">如需詳細資訊，請參閱 [取得 Schannel 認證](obtaining-schannel-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="ca538-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

<span data-ttu-id="ca538-107">若要從用戶端應用程式要求重做，請呼叫 [**InitializeSecurityCoNtext (Schannel)**](./initializesecuritycontext--schannel.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="ca538-107">To request a redo from a client application, call the [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="ca538-108">伺服器應用程式會呼叫 [**AcceptSecurityCoNtext (Schannel)**](acceptsecuritycontext--schannel.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="ca538-108">Server applications call the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="ca538-109">設定參數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ca538-109">Set the parameters as follows:</span></span>

-   <span data-ttu-id="ca538-110">在 *phCoNtext* 參數中指定現有的 [*安全性內容*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY)。</span><span class="sxs-lookup"><span data-stu-id="ca538-110">Specify the existing [*security context*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) in the *phContext* parameter.</span></span>
-   <span data-ttu-id="ca538-111">只有在建立內容時， (用戶端) 在 *pszTargetName* 參數) 指定相同的伺服器名稱 (。</span><span class="sxs-lookup"><span data-stu-id="ca538-111">(Clients only) Specify the same server name (in the *pszTargetName* parameter) as specified when establishing the context.</span></span>
-   <span data-ttu-id="ca538-112">使用 *phCredential* 參數（如果適用）來指定新的認證。</span><span class="sxs-lookup"><span data-stu-id="ca538-112">Specify new credentials, using the *phCredential* parameter, if applicable.</span></span>
-   <span data-ttu-id="ca538-113">如果您想要變更與認證無關的內容屬性，請使用 *fCoNtextReq* 參數來指定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ca538-113">If you want to change context attributes unrelated to the credentials, specify these attributes using the *fContextReq* parameter.</span></span>

<span data-ttu-id="ca538-114">呼叫適當的函式之後，您的應用程式應該將結果傳送至用戶端，並使用 [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) 函式繼續處理傳入訊息。</span><span class="sxs-lookup"><span data-stu-id="ca538-114">After calling the appropriate function, your application should send the results to the client and continue processing incoming messages using the [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function.</span></span>

<span data-ttu-id="ca538-115">[**DecryptMessage (schannel)**](decryptmessage--schannel.md)函式在 \_ \_ 您的應用程式準備好進行應用程式時，將會傳回秒的重新協商。</span><span class="sxs-lookup"><span data-stu-id="ca538-115">The [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function will return SEC\_I\_RENEGOTIATE when Schannel is ready for your application to proceed.</span></span> <span data-ttu-id="ca538-116">當您收到 SEC 次 \_ 重新 \_ 協商傳回碼時，您的應用程式必須將 [**AcceptSecurityCoNtext (schannel)**](acceptsecuritycontext--schannel.md) (伺服器) 或 [**InitializeSecurityCoNtext (schannel)**](./initializesecuritycontext--schannel.md) (用戶端) ，並傳遞 SECBUFFER_EXTRA 中從 DecryptMessage 傳回的 SECBUFFER_TOKEN 內容。</span><span class="sxs-lookup"><span data-stu-id="ca538-116">When you receive the SEC\_I\_RENEGOTIATE return code, your application must call [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (servers) or [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clients), and pass the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="ca538-117">在這個呼叫傳回值之後，請繼續進行，如同您的應用程式正在建立新的連接。</span><span class="sxs-lookup"><span data-stu-id="ca538-117">After this call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 
