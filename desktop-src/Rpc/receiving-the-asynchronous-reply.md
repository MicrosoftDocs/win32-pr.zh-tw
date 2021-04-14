---
title: 接收非同步回復
description: 在通知伺服器已傳送回復之後，用戶端會以非同步控制碼呼叫 RpcAsyncCompleteCall，以便接收回複。
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382617"
---
# <a name="receiving-the-asynchronous-reply"></a>接收非同步回復

在通知伺服器已傳送回復之後，用戶端會以非同步控制碼呼叫 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) ，以便接收回複。 當 **RpcAsyncCompleteCall** 成功完成時， *回復* 參數會指向包含遠端函式之傳回值的緩衝區。 用戶端程式提供的任何緩衝區做為 \[ [**out**](/windows/desktop/Midl/out-idl) \] 或 \[ [**in**](/windows/desktop/Midl/in)，非同步遠端函式的 **out** \] 參數包含有效的資料。 如果用戶端在伺服器傳送回復之前呼叫 **RpcAsyncCompleteCall** ，該呼叫將會失敗，並傳回 RPC \_ S \_ 非同步呼叫的值 \_ 擱置中 \_ 。

如果您的用戶端程式使用 i/o 完成埠或事件來通知，它必須呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) ，以在不再需要時釋放埠或處理。

 

 