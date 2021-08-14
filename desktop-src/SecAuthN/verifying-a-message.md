---
description: 下列範例顯示用來接收和驗證已簽署訊息的程式碼。 此範例會在 SignatureBuffer 和 SignatureBufferSize 中接收簽章緩衝區和其大小，並在 MessageBuffer 和 MessageBufferSize 中接收訊息緩衝區及其大小。
ms.assetid: 3e71aa0f-d135-4311-96f3-305762543627
title: 驗證訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90850a88ede875ae41549bca79aceb2d7bdea17db6f50eeb1a3a5e6dfb9a921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915087"
---
# <a name="verifying-a-message"></a>驗證訊息

下列範例顯示用來接收和驗證已簽署訊息的程式碼。 此範例會在 SignatureBuffer 和 SignatureBufferSize 中接收簽章緩衝區和其大小，並在 MessageBuffer 和 MessageBufferSize 中接收訊息緩衝區及其大小。

此範例假設名為 phCoNtext 的 **SecHandle** 變數和名為 s 的 **通訊端** 結構已初始化。 如需這些變數的宣告和連線，請參閱搭配使用[sspi 與 Windows 通訊端用戶端](using-sspi-with-a-windows-sockets-client.md)，以及搭配[Windows 通訊端伺服器使用 sspi](using-sspi-with-a-windows-sockets-server.md)。 這段程式碼包含 Secur32 中的函式呼叫，這些函式必須包含在程式庫中。


```C++
//--------------------------------------------------------------------
//  Declare and initialize local variables.
#include <windows.h>
#include <stdio.h>
#include <sspi.h>

#define SECURITY_WIN32
#define MaxMessageLength 1024
#define BUFSIZ 512

void main()
{
    BYTE MessageBuffer[BUFSIZ];
    BYTE SignatureBuffer[BUFSIZ];
    DWORD MessageBufferSize;
    DWORD SignatureBufferSize;
    SECURITY_STATUS SecStatus;
    SecBufferDesc InputBufferDescriptor;
    SecBuffer InputSecurityToken[2];
    ULONG fQOP;

    //------------------------------------------------------------------
    //    Receive the message.

    if(!(ReceiveMsg(
         s,
         MessageBuffer,
         MaxMessageLength,
         &MessageBufferSize)))
    {
         MyHandleError("Error. Message not received.");
    }

    //------------------------------------------------------------------
    //    Receive the signature.

    if(!(ReceiveMsg(
         s,
         SignatureBuffer,
         MaxMessageLength,
         &SignatureBufferSize)))
    {
         MyHandleError("Error. Signature not received.");
    }

    //------------------------------------------------------------------
    // Build the input buffer descriptor.

    InputBufferDescriptor.cBuffers = 2;
    InputBufferDescriptor.pBuffers = InputSecurityToken;
    InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

    //-------------------------------------------------------------------
    // Build the security buffer for the message.

    InputSecurityToken[0].BufferType = SECBUFFER_DATA;
    InputSecurityToken[0].cbBuffer = MessageBufferSize;
    InputSecurityToken[0].pvBuffer = MessageBuffer;

    //-------------------------------------------------------------------
    // Build the security buffer for the signature.

    InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
    InputSecurityToken[1].cbBuffer = SignatureBufferSize;
    InputSecurityToken[1].pvBuffer = SignatureBuffer;

    //--------------------------------------------------------------------
    // Call VerifySignature. 

    SecStatus = VerifySignature(
          &phContext,
          &InputBufferDescriptor,  // input message descriptor
          0,                       // no sequence number
          &fQOP                    // quality of protection
          );
    if(SecStatus == SEC_E_OK)
    {
         printf("The signature verified the message.\n");
    }
    else
         if(SecStatus == SEC_E_MESSAGE_ALTERED)
         {
              printf("The message was altered in transit.\n");
         }
         else
              if(SecStatus == SEC_E_OUT_OF_SEQUENCE )
              {
                  printf("The message is out of sequence.\n");
              }
              else
              {
                  printf("An unknown error occurred in VerifyMessage.\n");
              }
}
```



 

 



