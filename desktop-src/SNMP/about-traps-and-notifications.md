---
title: 關於陷阱和通知
description: SNMP 代理程式應用程式可以傳送至 WinSNMP 應用程式的一種訊息，就是通知應用程式有重大事件的非同步訊息。
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60739041237dad462e516e43c71d552446357f3ddc188d6609de2eef508b9658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009806"
---
# <a name="about-traps-and-notifications"></a>關於陷阱和通知

SNMP 代理程式應用程式可以傳送至 WinSNMP 應用程式的一種訊息，就是通知應用程式有重大事件的非同步訊息。 重大事件的一個範例是當網路連結關機或發生驗證失敗時。

這些類型的訊息在 SNMPv1 和 SNMPv2C 底下的通知下稱為「陷阱」。 Microsoft 的 WinSNMP 實行一律會將 SNMPv1 陷阱轉譯為 SNMPv2C 格式，如 RFC 1908 所定義。

當您呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函式來建立陷印 pdu 時，您只能建立 SNMPV2C 陷阱 pdu。 您可以使用 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函式的呼叫來更新的唯一類型的陷阱 Pdu 是 SNMPv2C 的陷阱 pdu。

如需詳細資訊，請參閱下列主題。



| 主題                                                                                    | 描述 |
|------------------------------------------------------------------------------------------|-------------|
| [將 SNMPv1 的陷阱翻譯為 SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [補漏設格式](trap-formats.md)                                                         |             |



 

 

 




