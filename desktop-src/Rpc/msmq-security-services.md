---
title: MSMQ 安全性服務
description: 同步 RPC 訊息可以使用 RPC 執行時間所提供的任何安全性功能。 如需詳細資訊，請參閱安全性。
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092944"
---
# <a name="msmq-security-services"></a>MSMQ 安全性服務

同步 RPC 訊息可以使用 RPC 執行時間所提供的任何安全性功能。 如需詳細資訊，請參閱 [安全性](security.md) 。

非同步 \[ [訊息](/windows/desktop/Midl/message) \] 呼叫無法使用 RPC 安全性，因為用戶端與伺服器之間沒有信號交換。 事實上，伺服器可能甚至不會在呼叫時執行。 若要存取訊息佇列服務 (MSMQ) 所提供的安全性服務，用戶端應用程式應該呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 來控制其對伺服器之呼叫的驗證層級和隱私權。

伺服器應用程式可以從遠端程序呼叫內呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) ，以判斷該呼叫的安全性層級。 下表顯示 RPC 安全性常數與 MSMQ 安全性之間的對應。



| RPC 安全性層級                | Description                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| RPC \_ 驗證 \_ 層級 \_ 無           | 呼叫未經過驗證或加密。                                                |
| RPC \_ 驗證 \_ 層級的 \_ PKT \_ 完整性 | 呼叫是使用 MSMQ 安全性進行驗證。                                             |
| RPC \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權   | 呼叫會在用戶端和伺服器佇列之間傳輸時進行驗證和加密。 |



 

伺服器也可以藉由呼叫 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) 和設定 rpc \_ c \_ mq \_ 驗證 \_ 層級 \_ NONE、rpc \_ c \_ mq \_ 驗證 \_ 層級 \_ \_ 的 pkt 完整性和 rpc \_ c \_ mq \_ 驗證 \_ level \_ pkt \_ [**rpc \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) 結構中的隱私權旗標，來強制執行呼叫驗證和加密。

 

 