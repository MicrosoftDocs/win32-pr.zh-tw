---
title: 開啟和關閉重新傳輸
description: 應用程式可以使用 SnmpSetRetransmitMode 函式的呼叫來設定重新傳輸模式。 新的重新傳輸模式會套用至後續呼叫 SnmpSendMsg 函式。
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996552"
---
# <a name="turning-retransmission-on-and-off"></a>開啟和關閉重新傳輸

應用程式可以使用 [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) 函式的呼叫來設定重新傳輸模式。 新的重新傳輸模式會套用至後續呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式。

當應用程式呼叫 **SnmpSetRetransmitMode** 時，SNMPAPI 的重新傳輸模式值為 \_ ON 時，Microsoft WinSNMP 執行會開始執行應用程式的重新傳輸原則。 新的重新傳輸模式不會影響未處理的 SNMP 訊息。 未處理的訊息是指在應用程式變更重新傳輸模式時沒有回應的訊息。

當 WinSNMP 應用程式呼叫 [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) 函式，並將重新傳輸模式值 SNMPAPI \_ 關閉時，該執行會停止執行重新傳輸原則。 此執行會取消對未完成 SNMP 訊息的重新傳輸嘗試。 這是因為在應用程式超時或重試計數器處理事件之前，執行可能無法處理所有未處理的 SNMP 要求和作業加上新的要求。

 

 




