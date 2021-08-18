---
title: 傳送 SNMP 訊息
description: WinSNMP 應用程式會藉由傳送 SNMP 訊息來起始傳輸要求。 SNMP 訊息包含 SNMP 通訊協定資料單位。 如需詳細資訊，請參閱使用通訊協定資料單位。
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4461c5d554444b2a7a5384a0ca79825b27ebe3c3bc489b6152c81ae71d172f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009066"
---
# <a name="sending-snmp-messages"></a>傳送 SNMP 訊息

WinSNMP 應用程式會藉由傳送 SNMP 訊息來起始傳輸要求。 SNMP 訊息包含 SNMP 通訊協定資料單位。 如需詳細資訊，請參閱 [使用通訊協定資料單位](working-with-protocol-data-units.md)。

WinSNMP 應用程式必須呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式，以要求 Microsoft WinSNMP 執行傳輸 PDU，以及相關 RFC 所定義的其他必要訊息元素。 除了目的地實體之外，應用程式還必須指定來源實體和要求的內容。 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)函式會以非同步方式執行。

WinSNMP 應用程式必須呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式，才能取得 **SnmpSendMsg** 要求的回應。

當應用程式呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)時，此實作為驗證 PDU 和其他訊息元素的有效性。

 

 




