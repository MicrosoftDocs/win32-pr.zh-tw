---
description: 當用戶端和伺服器完成安全性內容的設定時，就可以使用訊息支援函式。
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: 簽署訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f8151a66120575bfcaeda62955a7f6aa47e8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988936"
---
# <a name="signing-a-message"></a><span data-ttu-id="fa97f-103">簽署訊息</span><span class="sxs-lookup"><span data-stu-id="fa97f-103">Signing a Message</span></span>

<span data-ttu-id="fa97f-104">當用戶端和伺服器完成 [*安全性內容*](../secgloss/s-gly.md)的設定時，就可以使用訊息支援函式。</span><span class="sxs-lookup"><span data-stu-id="fa97f-104">When a client and server finish setting up the [*security context*](../secgloss/s-gly.md), message support functions can be used.</span></span> <span data-ttu-id="fa97f-105">用戶端和伺服器使用建立會話時所建立的安全性內容權杖，以呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函數。</span><span class="sxs-lookup"><span data-stu-id="fa97f-105">The client and server use the security context token created when the session was established to call [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions.</span></span> <span data-ttu-id="fa97f-106">內容權杖可以搭配 [**EncryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) 和 [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) 以進行通訊 [*隱私權*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="fa97f-106">The context token can be used with [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) for communications [*privacy*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="fa97f-107">下列範例顯示用戶端產生簽署的訊息，以傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="fa97f-107">The following example shows the client side generating a signed message to send to the server.</span></span> <span data-ttu-id="fa97f-108">在呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)之前，用戶端會使用 [**SecPkgCoNtext \_ 大小**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes)結構來呼叫 [**QueryCoNtextAttributes (一般)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) ，以決定保存訊息簽章所需的緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="fa97f-108">Before calling [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), the client calls [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) with a [**SecPkgContext\_Sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) structure to determine the length of the buffer needed to hold the message signature.</span></span> <span data-ttu-id="fa97f-109">如果 **cbMaxSignature** 成員為零，則 [*安全性封裝*](../secgloss/s-gly.md) 不支援簽章訊息。</span><span class="sxs-lookup"><span data-stu-id="fa97f-109">If the **cbMaxSignature** member is zero, the [*security package*](../secgloss/s-gly.md) does not support signing messages.</span></span> <span data-ttu-id="fa97f-110">否則，此成員會指出要配置以接收簽章的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="fa97f-110">Otherwise, this member indicates the size of the buffer to allocate to receive the signature.</span></span>

<span data-ttu-id="fa97f-111">此範例假設名為 *phCoNtext* 的 **SecHandle** 變數和名為 *s* 的 **通訊端** 結構已初始化。</span><span class="sxs-lookup"><span data-stu-id="fa97f-111">The example assumes that a **SecHandle** variable named *phContext* and a **SOCKET** structure named *s* are initialized.</span></span> <span data-ttu-id="fa97f-112">如需這些變數的宣告和連線，請參閱搭配 [使用 sspi 與 Windows 通訊端用戶端](using-sspi-with-a-windows-sockets-client.md) ，以及搭配 [Windows 通訊端伺服器使用 sspi](using-sspi-with-a-windows-sockets-server.md)。</span><span class="sxs-lookup"><span data-stu-id="fa97f-112">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="fa97f-113">此範例包含 Secur32 中的函式呼叫，這些函數必須包含在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="fa97f-113">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_Sizes ContextSizes;
char *MessageBuffer = "This is a sample buffer to be signed.";
DWORD MessageBufferSize = strlen(MessageBuffer);
SecBufferDesc InputBufferDescriptor;
SecBuffer InputSecurityToken[2];

ss = QueryContextAttributes(
    &phContext,
    SECPKG_ATTR_SIZES,
    &ContextSizes
    );
if(ContextSizes.cbMaxSignature == 0)
{
     MyHandleError("This session does not support message signing.");
}
//--------------------------------------------------------------------
// The message as a byte string is in the variable 
// MessageBuffer, and its length is in MessageBufferSize. 

//--------------------------------------------------------------------
// Build the buffer descriptor and the buffers 
// to pass to the MakeSignature call.

InputBufferDescriptor.cBuffers = 2;
InputBufferDescriptor.pBuffers = InputSecurityToken;
InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

//--------------------------------------------------------------------
// Build a security buffer for the message itself. If 
// the SECBUFFER_READONLY attribute is set, the buffer will not be
// signed.

InputSecurityToken[0].BufferType = SECBUFFER_DATA;
InputSecurityToken[0].cbBuffer = MessageBufferSize;
InputSecurityToken[0].pvBuffer = MessageBuffer;

//--------------------------------------------------------------------
// Allocate and build a security buffer for the message
// signature.

InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
InputSecurityToken[1].cbBuffer = ContextSizes.cbMaxSignature;
InputSecurityToken[1].pvBuffer = 
        (void *)malloc(ContextSizes.cbMaxSignature);

//--------------------------------------------------------------------
// Call MakeSignature 
// For the NTLM package, the sequence number need not be specified 
// because the package provides sequencing.
// The quality of service parameter is ignored.

Ss = MakeSignature(
    &phContext,
    0,                       // no quality of service
    &InputBufferDescriptor,  // input message descriptor
    0                        // no sequence number
    );
if (SEC_SUCCESS(ss))
{
     printf("Have made a signature.\n");
}
else
{ 
    MyHandleError("MakeSignature Failed."); 
}

//--------------------------------------------------------------------
//  Send the message.

if(!SendMsg(
    s,
    (BYTE *)InputSecurityToken[0].pvBuffer,
    InputSecurityToken[0].cbBuffer))
{
     MyHandleError("The message was not sent.");
}

//--------------------------------------------------------------------
//   Send the signature.

if(!SendMsg(
     s,
    (BYTE *)InputSecurityToken[1].pvBuffer,
    InputSecurityToken[1].cbBuffer ))
{
     MyHandleError("The signature was not sent.");
}
```



<span data-ttu-id="fa97f-114">如果內容已設定為允許簽署訊息，且輸入緩衝區描述項的格式正確， [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="fa97f-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) returns **TRUE** if the context is set up to allow signing messages and if the input buffer descriptor is correctly formatted.</span></span> <span data-ttu-id="fa97f-115">簽署訊息之後，訊息及其長度的簽章會傳送至遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="fa97f-115">After the message is signed, the message and the signature with their lengths are sent to the remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="fa97f-116">[**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構的資料內容會被傳送，而不是 **之 secbuffer** 結構本身或 [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc)結構。</span><span class="sxs-lookup"><span data-stu-id="fa97f-116">The data contents of the [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures are sent, not the **SecBuffer** structures themselves nor the [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="fa97f-117">接收應用程式會建立新的 **之 secbuffer** 結構和新的 **SecBufferDesc** 結構，以驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="fa97f-117">New **SecBuffer** structures and a new **SecBufferDesc** structure are created by the receiving application to verify the signature.</span></span>

 

 

 
