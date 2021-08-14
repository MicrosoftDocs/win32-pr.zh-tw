---
description: 這個範例示範如何初始化安全性緩衝區的陣列。
ms.assetid: f8196a9c-786a-49a3-85a4-1bd5f414a653
title: 之 secbuffer 和 SecBufferDesc 範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b60b776dd85e29c3f91d2840849d18e48d100dada6037bff556074b1041bdb8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918445"
---
# <a name="secbuffer-and-secbufferdesc-example-code"></a>之 secbuffer 和 SecBufferDesc 範例程式碼

這個範例示範如何初始化安全性緩衝區的陣列。 它會顯示連接之伺服器端初始化的輸入安全性緩衝區，以準備 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)的呼叫。 請注意，最後一個緩衝區包含用戶端接收到的不透明安全性權杖，且之 SECBUFFER \_ READONLY 旗標是在 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)上設定的。


```C++
SecBuffer  Buffers[3];
SecBufferDesc BufferDesc;
BYTE *pHeader;
BYTE *pMessage;
BYTE *pTrailer;

//--------------------------------------------------------------------
// pHeader, pMessage, and pTrailer are BYTE strings.
// In a working program, they would be assigned string values.

BufferDesc.ulVersion = SECBUFFER_VERSION;
BufferDesc.cBuffers = 3;
BufferDesc.pBuffers = Buffers;

Buffers[0].cbBuffer = sizeof(pHeader);
Buffers[0].BufferType = SECBUFFER_READONLY | SECBUFFER_DATA;
Buffers[0].pvBuffer = pHeader;

Buffers[1].cbBuffer = sizeof(pMessage);
Buffers[1].BufferType = SECBUFFER_DATA;
Buffers[1].pvBuffer = pMessage;

Buffers[2].cbBuffer = sizeof(pTrailer);
Buffers[2].BufferType = SECBUFFER_READONLY | SECBUFFER_TOKEN;
Buffers[2].pvBuffer = pTrailer;
```



 

 
