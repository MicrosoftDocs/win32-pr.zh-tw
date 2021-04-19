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
# <a name="signing-a-message"></a>簽署訊息

當用戶端和伺服器完成 [*安全性內容*](../secgloss/s-gly.md)的設定時，就可以使用訊息支援函式。 用戶端和伺服器使用建立會話時所建立的安全性內容權杖，以呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函數。 內容權杖可以搭配 [**EncryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) 和 [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) 以進行通訊 [*隱私權*](../secgloss/p-gly.md)。

下列範例顯示用戶端產生簽署的訊息，以傳送至伺服器。 在呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)之前，用戶端會使用 [**SecPkgCoNtext \_ 大小**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes)結構來呼叫 [**QueryCoNtextAttributes (一般)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) ，以決定保存訊息簽章所需的緩衝區長度。 如果 **cbMaxSignature** 成員為零，則 [*安全性封裝*](../secgloss/s-gly.md) 不支援簽章訊息。 否則，此成員會指出要配置以接收簽章的緩衝區大小。

此範例假設名為 *phCoNtext* 的 **SecHandle** 變數和名為 *s* 的 **通訊端** 結構已初始化。 如需這些變數的宣告和連線，請參閱搭配 [使用 sspi 與 Windows 通訊端用戶端](using-sspi-with-a-windows-sockets-client.md) ，以及搭配 [Windows 通訊端伺服器使用 sspi](using-sspi-with-a-windows-sockets-server.md)。 此範例包含 Secur32 中的函式呼叫，這些函數必須包含在程式庫中。


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



如果內容已設定為允許簽署訊息，且輸入緩衝區描述項的格式正確， [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)會傳回 **TRUE** 。 簽署訊息之後，訊息及其長度的簽章會傳送至遠端電腦。

> [!Note]  
> [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構的資料內容會被傳送，而不是 **之 secbuffer** 結構本身或 [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc)結構。 接收應用程式會建立新的 **之 secbuffer** 結構和新的 **SecBufferDesc** 結構，以驗證簽章。

 

 

 
