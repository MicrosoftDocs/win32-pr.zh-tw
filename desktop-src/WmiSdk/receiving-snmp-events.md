---
description: SNMP 事件提供者支援 SNMPv1 陷阱和 SNMPv2 通知。
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: 接收 SNMP 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f718d2bcea85d0ee942050108f337f8ecb78e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980540"
---
# <a name="receiving-snmp-events"></a>接收 SNMP 事件

SNMP 事件提供者支援 SNMPv1 陷阱和 SNMPv2 通知。

支援下列三種類型的 SNMPv1 陷阱和 SNMPv2 通知：

-   泛型

    泛型陷阱和通知會對應到已命名的事件，例如連結和冷啟動。 泛型陷阱和通知會以類別（例如 **SnmpLinkUpNotification** 和 **SnmpWarmStartExtendedNotification**）來表示，而這些類別會在類別名稱中包含陷阱的名稱。 這些類別是 [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md)的子類別。

-   企業專用

    企業特定的陷阱和通知會對應至 WMI 類別所代表的事件，而該 WMI 類別不是 [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md)的子類別。 若要支援企業特定的陷阱和通知，取用者必須藉由使用 SNMP MIB 編譯器編譯 MIB 定義來定義類別。

-   企業-非特定

    Nonenterprise 特定的陷阱和通知不會對應到任何一般事件種類或企業特定的事件種類。 Nonenterprise 特定的陷阱和通知未將其 MIB 定義編譯成 SMIR。 它們是由衍生自 SnmpNotification 和 [SnmpExtendedNotification](snmpextendednotification.md)的 [SnmpNotification](snmpnotification.md)、 **SnmpV2Notification**、 **SnmpV1ExtendedNotification** 和 **SnmpV2ExtendedNotification** 類別表示。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

本主題將討論下列各節：

-   [接收一般 SNMP 事件](#receiving-generic-snmp-events)
-   [接收 Enterprise-Specific 事件](#receiving-enterprise-specific-events)
-   [接收 Enterprise-Nonspecific 事件](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>接收一般 SNMP 事件

滲入和 SREP 支援所有類型的泛型 SNMPv1 陷阱和 SNMPv2 通知。 一般 SNMP 事件是以 [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md) 類別的子類別表示。

每個事件種類都是以一個滲入類別和一個 SREP 類別來表示。 滲入類別衍生自 [SnmpNotification](snmpnotification.md);SREP 類別衍生自 [SnmpExtendedNotification](snmpextendednotification.md)。 事件提供者需要不同的類別，因為它們在 SNMP 事件資料的呈現方式中使用不同的機制。

滲入會將 SNMP 事件資料直接轉換成 WMI 類別屬性，而 SREP 則不會。 SREP 會將間接取值層級新增至使用 WMI 屬性所需的解讀。 SREP [SnmpExtendedNotification](snmpextendednotification.md) 子類別的屬性是 SNMP 類別的實例;滲入 [SnmpNotification](snmpnotification.md) 子類別的屬性是整數和字串。

下表列出一般 SNMP 事件和相關事件類別的類型。



| 簡易網路管理通訊協定 (SNMP) 事件                                    | 滲入類別                                | SREP 類別                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| 驗證失敗                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| 外部閘道協定 (EGP) 鄰居遺失 | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| 冷啟動                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| 暖開機                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| 連結                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| 連結下移                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

例如， **SnmpLinkUpNotification** 和 **SnmpLinkUpExtendedNotification** 類別會描述連結事件。 這兩個類別都包含 **ifIndex**、 **ifAdminStatus** 和 **ifOperStatus** 屬性，但它們的類型非常不同。 **SnmpLinkUpNotification** 類別中的屬性是 SINT32 和 STRING 類型。 **SnmpLinkUpExtendedNotification** 類別中的屬性是內嵌物件類型 IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable。

## <a name="receiving-enterprise-specific-events"></a>接收 Enterprise-Specific 事件

滲入和 SREP 支援您已編譯到 SMIR 中的任何企業特定陷阱和通知。

下列程式描述如何接收企業特定的事件。

**接收企業特定事件**

1.  從負責產生事件的裝置編譯 MIB 定義。

    您可以使用 SNMP MIB 編譯器編譯 MIB 定義。 如需詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

2.  決定您想要對應至事件的類別類型。

    當您針對企業特定事件編譯 MIB 定義時，您可以決定編譯器所產生的類別類型。 具體來說，您可以指示編譯器建立下列其中一個選項：

    -   從定義[SnmpNotification](snmpnotification.md)子類別。
    -   從定義[SnmpExtendedNotification](snmpextendednotification.md)子類別。
    -   [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md) 定義中的子類別。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

如果 SNMP 事件提供者收到沒有類別的特定陷阱或通知，則提供者會產生 nonenterprise 特定的事件。 如需詳細資訊，請參閱 [接收企業非特定事件](#receiving-enterprise-nonspecific-events)。

## <a name="receiving-enterprise-nonspecific-events"></a>接收 Enterprise-Nonspecific 事件

企業非明確事件是指不會將 SNMPv1 陷阱或 SNMPv2 通知對應到 [SnmpNotification](snmpnotification.md) 或 [SnmpExtendedNotification](snmpextendednotification.md) 的任何子類別或代表企業事件的任何類別的事件。

滲入會針對未明確的事件使用 **SNMPV1Notification** 或 **SNMPV2Notification** 類別，而 SREP 會使用 **SNMPv1ExtendedNotification** 和 **SNMPV2ExtendedNotification** 類別。

所有四個企業明確的類別都衍生自 [SnmpNotification](snmpnotification.md) 或 [SnmpExtendedNotification](snmpextendednotification.md) 類別，而且具有相同的格式。 這兩個類別都具有單一屬性 **VarBindList**。 **VarBindList** 是 **SnmpVarBind** 類別的實例陣列。 **SnmpVarBind** 是 snmp 事件提供者所支援的基類，用以代表 snmp 變數系結的實例。 下表列出 **SnmpVarBind** 的屬性。



| 屬性         | 描述                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| 編碼         | 字串，指出 **值** 屬性中變數的抽象語法標記法 (一)  (asn.1) 類型。 |
| ObjectIdentifier | 在 **Value** 屬性中識別變數的字串。                                                 |
| 值            | 位元組中的原始資料。                                                                                            |



 

在 **SnmpV1Notification** 和 **SnmpV2Notification** 類別中，除了前兩個變數系結（TimeStamp 和 SnmpTrapOID）之外，已保留 SNMP 事件的變數系結順序。 這些系結已移除，並儲存在 [SnmpNotification](snmpnotification.md)或 [SnmpExtendedNotification](snmpextendednotification.md)父類別的 **TimeStamp** 和 **id** 屬性中。

 

 



