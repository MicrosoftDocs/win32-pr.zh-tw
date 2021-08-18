---
title: 關於重新傳輸
description: WinSNMP 應用程式可以透過各種方式進行 SNMP 作業要求。
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade0b2d58f371de87be5da855f26686a18518454c787c6a09e9701afbb731757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009956"
---
# <a name="about-retransmission"></a>關於重新傳輸

WinSNMP 應用程式可以透過各種方式進行 SNMP 作業要求。 應用程式可以在不等候回應的情況下，對 SNMP 代理程式發出數個要求，也可以發出單一要求並等候回應。 由於 SNMP 可以在多個傳輸通訊協定上執行，因此傳遞機制和可靠性特性可能會有所不同。

當您撰寫「WinSNMP」應用程式的程式碼時，您必須根據應用程式發出作業要求的方式，判斷通訊作業需要的可靠性層級。 然後，您必須選取重新傳輸策略，並執行重新傳輸原則。

重新傳輸原則包含超時時間和重試計數。 超時期間是指應用程式在 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 要求的發行和收到的對應訊息之間，所經過的時間（百分之一秒）。 應用程式會在呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式時收到訊息。 超時值是 Microsoft 的 WinSNMP 執行等候實體回應通訊要求的一段時間。 如果在超時期間內沒有任何回應，則會在 [重試計數] 值指定重新傳輸嘗試，或無法呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)時，將要求重新傳輸。 重試計數是當 SNMP 傳輸要求失敗時，執行所進行的重新傳輸嘗試次數上限。

此實值會在應用程式的資料庫中儲存超時值和重試計數。 此實值會儲存每個目的地實體的個別值。

應用程式必須建立自己的輪詢頻率，且必須管理計時器變數。 如需詳細資訊，請參閱 [管理重新傳輸原則](managing-the-retransmission-policy.md)。

 

 




