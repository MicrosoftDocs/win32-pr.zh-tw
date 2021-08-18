---
title: 建立 PDU
description: 若要建立及初始化 PDU，則會呼叫 SnmpCreatePdu 函式的 WinSNMP 應用程式。
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef0598c08c27d988825b3f0db3d8172362e9e6daf2ed4dbad049e2808b01034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009596"
---
# <a name="creating-a-pdu"></a>建立 PDU

若要建立及初始化 PDU，則會呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函式的 WinSNMP 應用程式。 應用程式必須先呼叫 **SnmpCreatePdu** ，然後再呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式，以要求 MICROSOFT WinSNMP 執行傳輸 PDU。 應用程式也必須先呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ，然後再呼叫 [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) 函式來要求 SNMP 訊息的編碼。

應用程式必須呼叫 [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) 函式，以釋放 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函式為新的 pdu 配置的資源。

 

 




