---
title: 註冊 SNMP 代理程式應用程式
description: 除了 SNMP 管理員作業之外，WinSNMP API 版本2.0 也支援 SNMP 代理程式作業。
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3415e511639c7cbbc18455ed93be74e11414c1f442797c8b72f7456092757c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009126"
---
# <a name="registering-an-snmp-agent-application"></a>註冊 SNMP 代理程式應用程式

除了 SNMP 管理員作業之外，WinSNMP API 版本2.0 也支援 SNMP 代理程式作業。

若要將 WinSNMP 應用程式註冊為 SNMP 代理程式，應用程式可以呼叫 [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) 函數。 此函式會通知 Microsoft WinSNMP 執行，SNMP 實體將會扮演 SNMP 代理程式的角色。 當應用程式不再作為代理程式時，應用程式也可以呼叫 **SnmpListen** 來通知執行。

如果應用程式呼叫 [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) 函式，並 \_ 在 *LSTATUS* 參數中傳遞 SNMPAPI 的值，則會發生下列動作：

1.  將在 SNMP 代理程式角色中運作的實體會系結至其指派的埠，並針對傳入的 SNMP 訊息要求進行「接聽」。
2.  代理程式會使用應用程式特定邏輯來處理每個 SNMP 要求。
3.  代理程式會針對每個要求形成適當的回應。
4.  代理程式藉由呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式，將回應傳送給要求的實體。 當代理程式呼叫 **SnmpSendMsg** 時，它會在 *srcEntity* 參數中指定代理程式的位址，並在 *dstEntity* 參數中指定遠端系統管理員實體的位址。  (這些值是 agent 實體在呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式以抓取 SNMP 要求時，在這些參數中收到的值的相反值。 ) 

如需 SNMP 管理應用程式和代理程式應用程式的詳細資訊，請參閱 [關於 snmp](about-snmp.md)。

 

 




