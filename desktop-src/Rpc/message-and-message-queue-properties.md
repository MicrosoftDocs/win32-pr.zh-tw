---
title: 訊息和訊息佇列屬性
description: 訊息具有屬性，可指定標籤、訊息主體和數個選項。
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c18b3a4751cd3be4473067dd9ca5aca17717672e6b67b559c10c502513fa2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928107"
---
# <a name="message-and-message-queue-properties"></a>訊息和訊息佇列屬性

訊息具有屬性，可指定標籤、訊息主體和數個選項。 訊息屬性選項可以包含服務品質、優先順序、日誌、隱私權和驗證層級，以及訊息的存留期。 在傳統 (非 RPC) 訊息佇列應用程式中，您可以藉由呼叫 MSMQ SDK 檔中所述的 MSMQ API 函數或 COM 物件方法來指定這些屬性。 RPC 用戶端應用程式可以藉由呼叫 [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) 和 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)，來設定遠端程序呼叫的特定屬性。 一旦設定之後，這些屬性會在用戶端應用程式重設之前，對每個訊息保持有效狀態。

訊息佇列有自己的一組屬性，除了訊息之外。 這些屬性會唯一識別佇列，並定義佇列提供的服務類別、此佇列中訊息所需的隱私權和驗證層級，以及訊息是否為分散式交易的一部分。 如同訊息屬性，您可以藉由呼叫 MSMQ API 函數或 COM 物件方法（如 MSMQ 檔中所述）來指定訊息佇列的屬性。 不過，RPC 伺服器應用程式在呼叫 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) 來建立系結時，可以指定其專屬接收佇列的屬性。

 

 




