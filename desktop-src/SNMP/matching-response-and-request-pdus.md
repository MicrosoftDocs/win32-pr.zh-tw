---
title: 符合回應和要求 Pdu
description: WinSNMP 應用程式接收 SNMP 回應的順序可能不符合應用程式提交 SNMP 作業要求的順序。
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e669b3e15652b8df68cb8fc27437106e644909e99bf0b7aee21a128194cf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009316"
---
# <a name="matching-response-and-request-pdus"></a>符合回應和要求 Pdu

WinSNMP 應用程式接收 SNMP 回應的順序可能不符合應用程式提交 SNMP 作業要求的順序。 為了符合要求的回應，應用程式必須使用要求識別碼欄位 (回應的要求識別碼 **) \_** 。

[ **要求 \_ 識別碼** ] 欄位是識別 PDU 的唯一數位值。 應用程式可以藉由呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函數或 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函數來指派要求識別碼。 呼叫 [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) 函式來取出 PDU 的 **要求 \_ 識別碼**。

 

 




