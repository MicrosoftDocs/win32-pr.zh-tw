---
description: 下列範例顯示在透過安全連線將訊息傳送到遠端電腦之前，要加密的訊息。
ms.assetid: 1788b496-ad19-427e-be07-4aa68543fced
title: 加密訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fcc987e17c37f9b2eb80289f257101b51f5f3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847723"
---
# <a name="encrypting-a-message"></a><span data-ttu-id="97354-103">加密訊息</span><span class="sxs-lookup"><span data-stu-id="97354-103">Encrypting a Message</span></span>

<span data-ttu-id="97354-104">下列範例顯示在透過安全連線將訊息傳送到遠端電腦之前，要加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="97354-104">The following example shows a message being encrypted before it is sent to a remote computer over the secure connection.</span></span>

<span data-ttu-id="97354-105">此範例假設名為的 **SecHandle** 變數 `phContext` 和名為的 **通訊端** `s` 已初始化。</span><span class="sxs-lookup"><span data-stu-id="97354-105">The example assumes that a **SecHandle** variable named `phContext` and a **SOCKET** named `s` are initialized.</span></span> <span data-ttu-id="97354-106">如需這些變數的宣告和連線，請參閱搭配 [使用 sspi 與 Windows 通訊端用戶端](using-sspi-with-a-windows-sockets-client.md) ，以及搭配 [Windows 通訊端伺服器使用 sspi](using-sspi-with-a-windows-sockets-server.md)。</span><span class="sxs-lookup"><span data-stu-id="97354-106">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="97354-107">此範例包含 Secur32 中的函式呼叫，這些函數必須包含在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="97354-107">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_StreamSizes  Sizes;
SECURITY_STATUS            scRet;
SecBufferDesc              Message;
SecBuffer                  Buffers[4];
SecBuffer                  *pDataBuffer;

PBYTE                       pbIoBuffer;
DWORD                       cbIoBuffer;
DWORD                       cbIoBufferLength;
PBYTE                       pbMessage;
DWORD                       cbMessage;

//--------------------------------------------------------------------
// Get the stream encryption sizes. This needs to 
// be done once per connection. 
// phContext must have been initialized during the handshake process.

scRet = QueryContextAttributes(
            phContext,
            SECPKG_ATTR_STREAM_SIZES,
            &Sizes);

if(FAILED(scRet))
{
    MyHandleError("Error reading SECPKG_ATTR_STREAM_SIZES");
}

//--------------------------------------------------------------------
// Allocate a working buffer. The plaintext sent to EncryptMessage
// can never be more than 'Sizes.cbMaximumMessage', so a buffer 
// size of Sizes.cbMaximumMessage plus the header and trailer sizes 
// is sufficient for the longest message.

cbIoBufferLength = Sizes.cbHeader + 
                   Sizes.cbMaximumMessage +
                   Sizes.cbTrailer;

if(!(pbIoBuffer = malloc((BYTE *), cbIoBufferLength)))
{
    MyHandleError("Out of memory");
}

//--------------------------------------------------------------------
// Create a plaintext message to be encrypted offset into the data 
// buffer by "header size" bytes. This allows encryption in place.

pbMessage = pbIoBuffer + Sizes.cbHeader;

StringCbPrintfA(pbMessage,
                cbIoBufferLength - Sizes.cbHeader,
                "This is the plaintext message.");
cbMessage = strlen(pbMessage);

//--------------------------------------------------------------------
// Encrypt the plaintext message.

Buffers[0].pvBuffer     = pbIoBuffer;
Buffers[0].cbBuffer     = Sizes.cbHeader;
Buffers[0].BufferType   = SECBUFFER_STREAM_HEADER;

Buffers[1].pvBuffer     = pbMessage;
Buffers[1].cbBuffer     = cbMessage;
Buffers[1].BufferType   = SECBUFFER_DATA;

Buffers[2].pvBuffer     = pbMessage + cbMessage;
Buffers[2].cbBuffer     = Sizes.cbTrailer;
Buffers[2].BufferType   = SECBUFFER_STREAM_TRAILER;

Buffers[3].BufferType   = SECBUFFER_EMPTY;

Message.ulVersion       = SECBUFFER_VERSION;
Message.cBuffers        = 4;
Message.pBuffers        = Buffers;

scRet = EncryptMessage(phContext, 0, &Message, 0);

if(FAILED(scRet))
{
    MyHandleError("Error returned by EncryptMessage.");
}

//--------------------------------------------------------------------
// Send the encrypted data.

if(!(SendMsg(
     s,
     pbIoBuffer,
     Buffers[0].cbBuffer + Buffers[1].cbBuffer + 
           Buffers[2].cbBuffer)))
{
     MyHandleError("SendMsg failed.");
}
```



 

 



