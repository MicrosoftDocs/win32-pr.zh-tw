---
description: 這個範例示範如何初始化安全性緩衝區的陣列。
ms.assetid: f8196a9c-786a-49a3-85a4-1bd5f414a653
title: 之 secbuffer 和 SecBufferDesc 範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7d28e885d6eec65c209caeda299b2f7e5f2ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974437"
---
# <a name="secbuffer-and-secbufferdesc-example-code"></a><span data-ttu-id="05ad0-103">之 secbuffer 和 SecBufferDesc 範例程式碼</span><span class="sxs-lookup"><span data-stu-id="05ad0-103">SecBuffer and SecBufferDesc Example Code</span></span>

<span data-ttu-id="05ad0-104">這個範例示範如何初始化安全性緩衝區的陣列。</span><span class="sxs-lookup"><span data-stu-id="05ad0-104">This example demonstrates how to initialize an array of security buffers.</span></span> <span data-ttu-id="05ad0-105">它會顯示連接之伺服器端初始化的輸入安全性緩衝區，以準備 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="05ad0-105">It shows input security buffers initialized by the server side of a connection to prepare for a call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span> <span data-ttu-id="05ad0-106">請注意，最後一個緩衝區包含用戶端接收到的不透明安全性權杖，且之 SECBUFFER \_ READONLY 旗標是在 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)上設定的。</span><span class="sxs-lookup"><span data-stu-id="05ad0-106">Note that the last buffer contains the opaque security token received by the client and that the SECBUFFER\_READONLY flag is set on [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).</span></span>


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



 

 
