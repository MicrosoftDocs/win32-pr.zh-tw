---
description: 通知型別宏的 OBJECTS 子句會列舉與通知物件相關聯的物件集合。
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: OBJECTS 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e25848e0fc98ca79ef96e25423ba7872296e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191109"
---
# <a name="objects-clause"></a>OBJECTS 子句

[通知](notification-type-macro.md)型別宏的 objects 子句會列舉與通知物件相關聯的物件集合。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

對應至 CIM 類別時，適用下列規則：

-   OBJECTS 子句的每個成員都會對應至 CIM 類別定義的屬性。 成員的物件描述項會逐字對應到 CIM 屬性名稱。 例如， **ifIndex** 會轉譯成 **ifIndex**。
-   對應進程所產生的每個 CIM 屬性都包含 **VarBindIndex** 限定詞。

    **VarBindIndex** 是 **uint32** 的強制辨識符號，描述物件在 [TRAP 類型](trap-type-macro.md) 或 [通知類型](notification-type-macro.md) 宏的物件子句中出現的位置。 整數也會指定屬性在 SNMPv1 或 SNMPv2C 陷阱 PDU 的變數系結清單中的位置，分別 (通訊協定資料單位) 。  (，因為前兩個變數系結一律為 TimeStamp 和識別，所以任何其他變數都是在值2之後編號 ) 

    從 SNMPv1 的 [TRAP](trap-type-macro.md) 型別宏產生 CIM 事件類別時， **VarBindIndex** 辨識符號的初始值為1，代表變數系結清單中的第一個變數。

    從 SNMPv2C [通知類型](notification-type-macro.md) 宏產生 CIM 事件類別時， **VarBindIndex** 辨識符號的初始值為3，代表變數系結清單中的第一個變數。

當對應封裝的 CIM 類別時，OBJECTS 子句的每個成員都會對應到一個 CIM 屬性，以反映對應之 MIB 物件的名稱、類型和值。 使用的對應程式是在下列主題中指定：

-   [語法子句](syntax-clause.md)
-   [文字慣例宏](textual-convention-macro.md)
-   [存取和最大存取權子句](access-and-max-access-clauses.md)

使用引用 CIM 類別時，OBJECTS 子句的每個成員會對應如下：

-   OBJECTS 子句的每個成員都會對應到 CIM 類別的單一屬性。 屬性是強型別，做為内嵌物件。
-   内嵌物件的類別是透過標準物件對應程式產生的。 如需詳細資訊，請參閱 [OBJECT TYPE 宏](object-type-macro.md)。 例如， **ifTable** 會對應到名為 **SNMP \_ RFC1213 \_ MIB \_ ifTable** 的內嵌類別。
-   與設陷 PDU 之變數系結相關聯的值，會具現化為引用類別之物件的内嵌物件。 每個内嵌物件都包含物件之索引鍵屬性的值，以及所對應之變數系結中的屬性值。

 

 



