---
title: 補漏設格式
description: 陷阱 Pdu 的格式與其他 Pdu 的格式不同。 SNMPv1 陷阱和 SNMPv2C 陷阱的格式也不同。
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021103"
---
# <a name="trap-formats"></a>補漏設格式

陷阱 Pdu 的格式與其他 Pdu 的格式不同。 SNMPv1 陷阱和 SNMPv2C 陷阱的格式也不同。

在 SNMPv2C 架構下，PDU 陷印格式是以下列方式組織的 *n* 個變數系結專案的變數系結清單：

-   第一個變數系結專案包含時間戳記。
-   第二個變數系結專案是識別陷阱的物件識別碼。
-   第三個到 *n* 個變數系結專案（如果有的話）會包含與該陷阱相關聯的其他資訊。

在 SNMPv1 架構下，PDU 陷印格式如下所示。

| 欄位                      | 描述                                                      |
|----------------------------|------------------------------------------------------------------|
| 企業                 | 識別產生陷阱的裝置類型。           |
| 代理程式-addr                 | 識別產生陷阱的裝置 IP 位址。 |
| 一般-陷阱/特定-陷阱 | 識別預先定義的陷阱類型。                               |
| 時間戳記                 | 識別產生陷阱的時間。                          |
| 變數系結          | 包含與陷阱相關聯的其他資訊。        |



 

[**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)函數一律會傳回 SNMPv2C 格式的訊息。 如果訊息包含「 **SNMP \_ PDU \_ 陷阱**」作業類型，應用程式可以讀取訊息的變數系結專案，並取得與該陷阱相關聯的資訊。

 

 




