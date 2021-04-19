---
description: SNMP 文字慣例會對應到 CIM 定義的類型。
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: 文字慣例宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982335"
---
# <a name="textual-convention-macro"></a>文字慣例宏

SNMP 文字慣例會對應到 CIM 定義的類型。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

下列對應規則適用于 SNMP 文字慣例：

-   語法子句中的指名型別定義會逐字地對應到 CIM 屬性限定詞 **物件 \_ 語法**。
-   當語法子句明確參考 SNMPv2C 文字慣例宏的文字慣例，或參考隱含的文字慣例時，請使用下表來對應文字慣例。 預設值一律為 **Null**。



| 文字慣例 | CIM 變異類型 | CIM 辨識符號                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DateAndTime        | **VT \_ BSTR**     | **文字 \_ 慣例**： >formatting.dateandtime.custom<br/> **編碼**： OCTETSTRING<br/> **物件 \_ 語法**： >formatting.dateandtime.custom<br/> **cimtype**：字串<br/>       |
| Displaystring      | **VT \_ BSTR**     | **文字 \_ 慣例**： Displaystring<br/> **編碼**： OCTETSTRING<br/> **物件 \_ 語法**： Displaystring<br/> **cimtype**：字串<br/>   |
| MacAddress         | **VT \_ BSTR**     | **文字 \_ 慣例**： MacAddress<br/> **編碼**： OCTETSTRING<br/> **物件 \_ 語法**： MacAddress<br/> **cimtype**：字串<br/>         |
| PhysAddress        | **VT \_ BSTR**     | **文字 \_ 慣例**： PhysAddress<br/> **編碼**： OCTETSTRING<br/> **物件 \_ 語法**： PhysAddress<br/> **cimtype**：字串<br/>       |
| SnmpUDPAddress     | **VT \_ BSTR**     | **文字 \_ 慣例**： SnmpUDPAddress<br/> **編碼**： OCTETSTRING<br/> **物件 \_ 語法**： SnmpUDPAddress<br/> **cimtype**：字串<br/> |
| SnmpOSIAddress     | **VT \_ BSTR**     | **文字 \_ 慣例**： SnmpOSIAddress<br/> **編碼**： OCTETSTRING<br/> **物件 \_ 語法**： SnmpOSIAddress<br/> **cimtype**：字串<br/> |
| SnmpIPXAddress     | **VT \_ BSTR**     | **文字 \_ 慣例**： SnmpIPXAddress<br/> **編碼**： OCTETSTRING<br/> **物件 \_ 語法**： SnmpIPXAddress<br/> **cimtype**：字串<br/> |



 

-   使用基礎基本類型的 CIM 定義變異類型和 CIM 屬性限定詞 **文字 \_ 慣例**、 **編碼**、 **物件 \_ 語法** 和 **cimtype** 對應。
-   SNMPv2C 文字慣例宏的顯示提示子句會逐字對應到 CIM 屬性辨識符號 **顯示 \_ 提示**。 如果沒有文字慣例宏，或宏未包含顯示提示子句，就不會產生這個限定詞。

## <a name="example-code"></a>範例程式碼

下列範例說明 SNMPv1 文字慣例。

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

此範例會產生下列 CIM 限定詞。

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

下列範例說明 SNMPv2 文字慣例。

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

此範例會產生下列 CIM 限定詞。

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




