---
description: 下列範例顯示已接收和解密的加密訊息。
ms.assetid: 4858a43b-3084-4a03-8b6f-4a788cdb3dd5
title: 解密訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3598025564e607bf25241def4171eba84aa1dbbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512008"
---
# <a name="decrypting-a-message"></a><span data-ttu-id="fc2f7-103">解密訊息</span><span class="sxs-lookup"><span data-stu-id="fc2f7-103">Decrypting a Message</span></span>

<span data-ttu-id="fc2f7-104">下列範例顯示已接收和解密的加密訊息。</span><span class="sxs-lookup"><span data-stu-id="fc2f7-104">The following example shows an encrypted message being received and decrypted.</span></span>

<span data-ttu-id="fc2f7-105">此範例假設名為的 **SecHandle** 變數 `phContext` 和名為的 **通訊端** 結構 `s` 已初始化。</span><span class="sxs-lookup"><span data-stu-id="fc2f7-105">The example assumes that a **SecHandle** variable named `phContext` and a **SOCKET** structure named `s` are initialized.</span></span> <span data-ttu-id="fc2f7-106">如需這些變數的宣告和連線，請參閱搭配 [使用 sspi 與 Windows 通訊端用戶端](using-sspi-with-a-windows-sockets-client.md) ，以及搭配 [Windows 通訊端伺服器使用 sspi](using-sspi-with-a-windows-sockets-server.md)。</span><span class="sxs-lookup"><span data-stu-id="fc2f7-106">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="fc2f7-107">此範例包含 Secur32 中的函式呼叫，這些函數必須包含在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="fc2f7-107">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


```C++
SecPkgContext_StreamSizes   Sizes;
SECURITY_STATUS             scRet;
SecBufferDesc               Message;
SecBuffer                   Buffers[4];
SecBuffer                   *pDataBuffer;
SecBuffer                   *pExtraBuffer;
SecBuffer                    ExtraBuffer;

PBYTE                        pbIoBuffer;
DWORD                        cbIoBuffer;
DWORD                        cbIoBufferLength;

//--------------------------------------------------------------------
// Get stream encryption properties.

scRet = QueryContextAttributes(
       phContext,
       SECPKG_ATTR_STREAM_SIZES,
       &Sizes);

if(scRet != SEC_E_OK)
{
    MyHandleError("Error reading SECPKG_ATTR_STREAM_SIZES\n");
}

//--------------------------------------------------------------------
// Allocate a working buffer. The plaintext sent to EncryptMessage
// should never be more than 'Sizes.cbMaximumMessage', so a buffer 
// size of this plus the header and trailer sizes should be safe.

cbIoBufferLength = Sizes.cbHeader + 
                   Sizes.cbMaximumMessage +
                   Sizes.cbTrailer;

pbIoBuffer = LocalAlloc(LMEM_FIXED, cbIoBufferLength);
if(pbIoBuffer == NULL)
{
    MyHandleError("Error: Out of memory");
}

//--------------------------------------------------------------------
// Attempt to decrypt the data in the i/o buffer.

Buffers[0].pvBuffer     = pbIoBuffer;
Buffers[0].cbBuffer     = cbIoBuffer;
Buffers[0].BufferType   = SECBUFFER_DATA;

Buffers[1].BufferType   = SECBUFFER_EMPTY;
Buffers[2].BufferType   = SECBUFFER_EMPTY;
Buffers[3].BufferType   = SECBUFFER_EMPTY;

Message.ulVersion       = SECBUFFER_VERSION;
Message.cBuffers        = 4;
Message.pBuffers        = Buffers;

scRet = DecryptMessage(
     phContext, 
     &Message, 
     0, 
     NULL);

if(scRet == SEC_E_INCOMPLETE_MESSAGE)
{
//--------------------------------------------------------------------
// The input buffer contains only a fragment of an
// encrypted record. Read some more data from the server 
// and then try the decryption again.
     continue;
}

if(scRet != SEC_E_OK && scRet != SEC_I_RENEGOTIATE)
{
    MyHandleError("Error returned by DecryptMessage");
}

//--------------------------------------------------------------------
// Locate data.

pDataBuffer  = NULL;
pExtraBuffer = NULL;
while(!pDataBuffer && i < 4)
{
    if(Buffers[i].BufferType == SECBUFFER_DATA)
    {
        pDataBuffer = &Buffers[i];
    }
    i++;
}

if(pDataBuffer)
{
//--------------------------------------------------------------------
// Display or otherwise process the decrypted data.
//        ...
}
```



 

 



