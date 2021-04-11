---
title: 建立系結控制碼
description: 分散式應用程式的用戶端程式需要建立系結控制碼，告知 RPC 執行時間應聯繫的伺服器，以及應如何聯繫伺服器。
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- 遠端程序呼叫 RPC、工作、建立系結控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eddced351642d916f90cd5c127d0e51b764f7ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021152"
---
# <a name="creating-a-binding-handle"></a>建立系結控制碼

分散式應用程式的用戶端程式需要建立系結控制碼，告知 RPC 執行時間應聯繫的伺服器，以及應如何聯繫伺服器。

下列程式碼片段示範建立系結控制碼的常見方法：


```C++
RPC_STATUS status;
unsigned short *StringBinding;
RPC_BINDING_HANDLE BindingHandle;
status = RpcStringBindingCompose(NULL,  // Object UUID
             L"ncacn_ip_tcp",           // Protocol sequence to use
             L"MyServer.MyCompany.com", // Server DNS or Netbios Name
             NULL,
             NULL,
             &StringBinding);
// Error checking ommitted. If no error, we proceed below
status = RpcBindingFromStringBinding(StringBinding, &BindingHandle);

// free string regardless of errors from RpcBindingFromStringBinding
RpcStringFree(&StringBinding);

// Error checking ommitted. If no error, we have a valid binding handle
```



 

 




