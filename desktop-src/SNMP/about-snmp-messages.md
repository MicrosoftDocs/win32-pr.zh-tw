---
title: 關於 SNMP 訊息
description: 簡易網路管理通訊協定會使用訊息來進行通訊，並在遠端 SNMP 實體之間交換資訊。
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90c8e6aba33384ddaf16fbe847f20488f0be4d584c70563a34d052a37e80a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009946"
---
# <a name="about-snmp-messages"></a>關於 SNMP 訊息

簡易網路管理通訊協定會使用訊息來進行通訊，並在遠端 SNMP 實體之間交換資訊。 SNMP 訊息包含通訊協定資料單位 (的 Pdu) 再加上相關 RFC 所定義的其他訊息標頭元素。 PDU 是包含 SNMP 資料元件 (或欄位) 的資料封包。

SNMPv1 和 SNMPv2C 的 SNMP 訊息格式都相同。 不過，SNMPv2C 支援額外的 PDU 類型。 例如，它支援 [SNMP \_ PDU \_ GETBULK](snmp-variable-types-and-request-pdu-types.md) 要求類型，可讓應用程式有效率地從目標實體中取出大型資料區塊。

 

 




