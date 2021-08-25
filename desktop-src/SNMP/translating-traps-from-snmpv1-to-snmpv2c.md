---
title: 將 SNMPv1 的陷阱翻譯為 SNMPv2C
description: 當 Microsoft WinSNMP 的執行從 SNMPv1 架構下的實體接收到陷阱時，會將陷阱轉譯為 SNMPv2C 格式。
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f70ddbdfb779f6b06f8ed26490c6fabd2421ae96f0006b4af5b7f1ab18f7d5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885858"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a>將 SNMPv1 的陷阱翻譯為 SNMPv2C

當 Microsoft WinSNMP 的執行從 SNMPv1 架構下的實體接收到陷阱時，會將陷阱轉譯為 SNMPv2C 格式。 因此，當 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 傳遞時，它一律會採用 SNMPv2C 格式。 RFC 1908：「在第1版與第2版的網際網路標準網路管理架構之間共存」中，指定從 SNMPv1 轉譯為 SNMPv2C 陷阱格式的規則。

WinSNMP 應用程式可以檢查變數系結清單中的最後一個變數系結專案，以判斷專案是否為從 SNMPv1 轉譯為 SNMPv2C 格式的設陷。 如果是的話，最後一個變數系結永遠等於值 "snmpTrapEnterpriseOID. 0"。

如需詳細資訊，請參閱 [管理陷阱和通知](managing-traps-and-notifications.md)。

 

 




