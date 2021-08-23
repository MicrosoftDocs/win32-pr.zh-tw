---
title: 使用 MSMQ 做為 RPC 傳輸
description: RPC 子系統支援在同步和非同步模式中使用 MSMQ 做為傳輸。
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab18f4476815929e8a7e6fb4e4a1eef0a4e4e34754ac134f023c8551899e0138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010676"
---
# <a name="using-msmq-as-an-rpc-transport"></a>使用 MSMQ 做為 RPC 傳輸

RPC 子系統支援在同步和非同步模式中使用 MSMQ 做為傳輸。

同步模式使用傳統的遠端程序呼叫。 這些呼叫會使用已知的端點和訊息佇列傳輸（ [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)）作為傳輸通訊協定。 在同步模式中，您的遠端程式可以有 \[ [in](/windows/desktop/Midl/in) \] 和 \[ [out](/windows/desktop/Midl/out-idl) \] 參數，並且可以使用標準的 RPC 安全性服務。 RPC 子系統會針對包含 **\[ out \]** 參數的遠端呼叫建立回復佇列。 同步模式對於用戶端需要從伺服器接收資料的應用程式很有用。 這種模式的主要限制是，如同傳統的遠端程序呼叫，用戶端和伺服器都必須執行，而且在呼叫期間仍維持執行狀態。

非同步模式可讓用戶端應用程式對伺服器進行呼叫，並立即傳回，無論伺服器應用程式或伺服器電腦的狀態為何。 它也會提供可用於管理訊息佇列和資訊流程的 MSMQ 功能子集。 [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)函式可讓您控制服務品質、呼叫優先順序、日誌、安全性，以及伺服器進程佇列的存留期。 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)函數可讓您指定伺服器進程佇列的屬性，例如佇列持續性、驗證和加密。

您可以執行非同步 MSMQ，如同同步 MSMQ 一樣。 您必須使用已知的端點，並定義要 [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)的傳輸通訊協定。 在 IDL 檔案中，將 [message](/windows/desktop/Midl/message) 屬性套用至使用非同步訊息佇列的函數。 請注意，訊息函數 \[ 只能有 in \] 參數。

 

 