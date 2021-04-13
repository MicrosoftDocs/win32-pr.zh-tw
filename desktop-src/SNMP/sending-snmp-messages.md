---
title: 傳送 SNMP 訊息
description: WinSNMP 應用程式會藉由傳送 SNMP 訊息來起始傳輸要求。 SNMP 訊息包含 SNMP 通訊協定資料單位。 如需詳細資訊，請參閱使用通訊協定資料單位。
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301552"
---
# <a name="sending-snmp-messages"></a>傳送 SNMP 訊息

WinSNMP 應用程式會藉由傳送 SNMP 訊息來起始傳輸要求。 SNMP 訊息包含 SNMP 通訊協定資料單位。 如需詳細資訊，請參閱 [使用通訊協定資料單位](working-with-protocol-data-units.md)。

WinSNMP 應用程式必須呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式，以要求 Microsoft WinSNMP 執行傳輸 PDU，以及相關 RFC 所定義的其他必要訊息元素。 除了目的地實體之外，應用程式還必須指定來源實體和要求的內容。 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)函式會以非同步方式執行。

WinSNMP 應用程式必須呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式，才能取得 **SnmpSendMsg** 要求的回應。

當應用程式呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)時，此實作為驗證 PDU 和其他訊息元素的有效性。

 

 




