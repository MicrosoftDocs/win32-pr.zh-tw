---
title: 接收 SNMP 訊息
description: WinSNMP 應用程式必須呼叫 SnmpRecvMsg 函式，才能取得 SnmpSendMsg 要求的回應。
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674908"
---
# <a name="receiving-snmp-messages"></a>接收 SNMP 訊息

WinSNMP 應用程式必須呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式，才能取得 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 要求的回應。

[**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)函式會將應用程式視窗控制碼和通知訊息識別碼傳遞至 Microsoft WinSNMP 執行。 當應用程式視窗接收到此訊息時，它會使用 [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)所傳回的會話控制碼來通知應用程式呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)函數。

[**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)函式會傳回兩個實體控制碼、內容控制碼和 PDU 的控制碼。 建議使用 [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)、 [**SnmpFreeCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)和 [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) 函式，讓 WinSNMP 應用程式釋放這些資源。

如需有關管理呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式和接收對應回應之間時間的詳細資訊，請參閱 [關於重新傳輸](about-retransmission.md)。 如需使用 **要求 \_ 識別碼** PDU 欄位來比對回應 PDU 與其要求 pdu 的詳細資訊，請參閱 [相符的回應和要求](matching-response-and-request-pdus.md)pdu。

 

 




