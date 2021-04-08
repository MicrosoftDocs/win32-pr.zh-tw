---
title: 符合回應和要求 Pdu
description: WinSNMP 應用程式接收 SNMP 回應的順序可能不符合應用程式提交 SNMP 作業要求的順序。
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932391"
---
# <a name="matching-response-and-request-pdus"></a>符合回應和要求 Pdu

WinSNMP 應用程式接收 SNMP 回應的順序可能不符合應用程式提交 SNMP 作業要求的順序。 為了符合要求的回應，應用程式必須使用要求識別碼欄位 (回應的要求識別碼 **) \_** 。

[ **要求 \_ 識別碼** ] 欄位是識別 PDU 的唯一數位值。 應用程式可以藉由呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函數或 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函數來指派要求識別碼。 呼叫 [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) 函式來取出 PDU 的 **要求 \_ 識別碼**。

 

 




