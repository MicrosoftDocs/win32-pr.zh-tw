---
title: 指派要求識別碼
description: WinSNMP 應用程式可以呼叫 SnmpCreatePdu 函式或 SnmpSetPduData 函數，將應用程式產生的要求識別碼指派給 PDU。 應用程式必須傳遞要求識別碼參數中的值 \_ 。
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671079"
---
# <a name="assigning-request-identifiers"></a>指派要求識別碼

WinSNMP 應用程式可以呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函式或 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函數，將應用程式產生的要求識別碼指派給 PDU。 應用程式必須傳遞 *要求 \_ 識別碼* 參數中的值。

應用程式可以藉由在 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)函式的 *request \_ id* 參數中傳遞零，要求 Microsoft WinSNMP 執行產生並將要求識別碼指派給 PDU。 應用程式可以透過呼叫 [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) 函式來取得指派的要求識別碼。

若要指派等於特定值（包括零）的要求識別碼，應用程式必須在 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)函數的 *request \_ id* 參數中傳遞該值。

當執行執行應用程式的重新傳輸原則時，它會在每個重新傳輸的 SNMP 訊息中包含原始 PDU 的 **要求 \_ 識別碼** 欄位。 如需詳細資訊，請參閱 [關於重新傳輸](about-retransmission.md) 和 [管理重新傳輸原則](managing-the-retransmission-policy.md)。

> [!Note]  
> 當實值從 SNMPv1 實體收到陷阱時，它會將非零值指派給 PDU 的 **要求 \_ 識別碼** 欄位。 此值可能會複製應用程式在要求 PDU 中所使用的要求識別碼。 應用程式必須檢查是否有重複。

 

 

 




