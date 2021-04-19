---
description: SNMP 事件提供者會從 WINSNMP 堆疊接收 SNMP 事件封包，並將封包中包含的資訊轉譯成 WMI 事件。
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: 在 SNMP 事件提供者之間進行選擇
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979955"
---
# <a name="choosing-between-snmp-event-providers"></a>在 SNMP 事件提供者之間進行選擇

SNMP 事件提供者會從 WINSNMP 堆疊接收 SNMP 事件封包，並將封包中包含的資訊轉譯成 WMI 事件。

WMI 包含下列兩個 SNMP 事件提供者：

-   SNMP 封裝事件提供者 (滲入) 

    封裝的布建表示事件實例有簡單的屬性，描述直接從 SNMP 陷阱對應的資訊。

-   SNMP 對等事件提供者 (SREP) 

    參照布建會將 SNMP 陷阱內出現的資訊抽象化，讓共用相同類別與實例的屬性以内嵌物件的形式呈現。 這可讓相關聯的唯一實例在事件接收之後，使用 SNMP RELPATH 進行抓取 \_ \_ 。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

無論 SNMP 事件是 SNMPv1 陷阱或 SNMPv2C 通知，堆疊都會將它報告為 SNMPv2 通知。 因此，事件提供者會以 SNMPv2 通知的方式處理所有 SNMP 事件。

為了向 WMI 取用者描述 SNMP 事件，每個事件提供者都支援衍生自 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)系統類別的類別階層架構。 [SNMPNotification](snmpnotification.md)類別是滲入階層的父類別;[SNMPExtendedNotification](snmpextendednotification.md)類別是 SREP 階層的父類別。

 

 



