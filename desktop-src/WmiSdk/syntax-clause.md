---
description: 包含定義 MIB 物件的資料和類型的語法子句。
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: 語法子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989036"
---
# <a name="syntax-clause"></a>語法子句

[物件類型](object-type-macro.md)宏包含語法子句，此子句會定義 MIB 物件的資料和類型。 雖然 SNMP 提供者會觀察對應語法子句的一般規則，但是提供者也會遵循數種資料類型的特定規則。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

下列對應規則適用于下表所述的所有資料類型：

-   語法子句的文字標記法會對應到 CIM 屬性辨識符號 **文字 \_ 慣例**。
-   語法子句中的指名型別定義會對應到 CIM 屬性限定詞 **物件 \_ 語法**。 這個對應會根據資料類型而有所不同。 如需詳細資訊，請參閱對應描述。
-   將 SNMPv1 和 SNMPv2C 通訊協定框架編碼時，所使用的 SNMP 類型會對應至 CIM 屬性限定詞 **編碼**。
-   CIM 屬性限定詞 **cimtype** 包含格式化基礎 CIM 通訊協定值的文字標記法。

下表列出具有管理提供者對應行為之特定規則的資料類型。



| SNMP 資料類型                                     | Description                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [基本型別](#primitive-type)                  | 管理資訊的結構中定義的其中一個基本資料類型 (SMI-S) 檔 RFC 1213 和 RFC 1903。                                                                                                                            |
| [文字慣例](textual-convention-macro.md) | 透過明確使用 SNMPv2C **文字慣例** 宏所產生的型別定義，或是透過使用命名的型別所產生的型別定義。 文字慣例會指派名稱，而在某些情況下會將某個範圍的值指派給現有的資料類型。 |
| [命名類型](#named-type)                          | 基本類型、文字慣例或受限型別的命名參考。                                                                                                                                                                    |
| [條件約束類型](#constrained-type)              | 已受限於 SMI-S 檔 RFC 1213 和 RFC 1903 中所定義之某些 subtyping 機制的基本類型、命名類型或文字慣例。                                                                                      |



 

## <a name="primitive-type"></a>基本類型

基本型別是 (SMI-S) 檔 RFC 1213 和 RFC 1903 的管理資訊結構中所定義的其中一個基本資料類型。 SNMP 基本型別對應到 CIM 定義的類型。 下表列出語法子句明確參考 SNMPv1 的基本類型時所發生的對應。 **文字 \_ 慣例**、**編碼方式** 和 **物件 \_ 語法** 辨識符號一律與 MIB 類型相同，且預設值一律為 **Null**。



| MIB 類型         | CIM 變異類型 | cimtype 值 |
|------------------|------------------|---------------|
| INTEGER          | VT \_ I4           | **sint32**    |
| OCTETSTRING      | VT \_ BSTR         | **string**    |
| OBJECTIDENTIFIER | VT \_ BSTR         | **string**    |
| NULL             | VT \_ Null         | 不支援 |
| IpAddress        | VT \_ BSTR         | **string**    |
| 計數器          | VT \_ I4           | **uint32**    |
| 量測計            | VT \_ I4           | **uint32**    |
| TimeTicks        | VT \_ I4           | **uint32**    |
| Opaque           | VT \_ BSTR         | **string**    |
| Networkaddress.cache.ttl   | VT \_ BSTR         | **string**    |



 

當語法子句參考 **Null**（明確地或透過命名類型指派）時，提供者會忽略物件類型宏。 下表列出語法子句明確參考 SNMPv2 的基本類型時所發生的對應。 **文字 \_ 慣例**、**編碼方式** 和 **物件 \_ 語法** 辨識符號一律與 MIB 類型相同，且預設值一律為 **Null**。



| MIB 類型          | CIM 變異類型 | cimtype 值 |
|-------------------|------------------|---------------|
| INTEGER           | VT \_ I4           | **sint32**    |
| 八位字串      | VT \_ BSTR         | **string**    |
| 物件識別碼 | VT \_ BSTR         | **string**    |
| IpAddress         | VT \_ BSTR         | **string**    |
| Counter32         | VT \_ I4           | **uint32**    |
| Gauge32           | VT \_ I4           | **uint32**    |
| Unsigned32        | VT \_ I4           | **uint32**    |
| Integer32         | VT \_ I4           | **sint32**    |
| Counter64         | VT \_ BSTR         | **uint64**    |
| TimeTicks         | VT \_ I4           | **uint32**    |
| Opaque            | VT \_ BSTR         | **string**    |



 

## <a name="named-type"></a>命名類型

SNMP 命名類型會對應至 CIM 定義類型。 當語法子句透過型別指派衍生來參考基本型別、[文字慣例](textual-convention-macro.md)或[限制型](#constrained-type)別時，請使用[這些型別](#primitive-type)來判斷哪些對應程式適用。

-   如果透過衍生類型指派規則，則會遇到限制型別定義：

    -   此外，如果透過進一步的衍生，您就會遇到 [文字慣例宏](textual-convention-macro.md)中所列的其中一種文字慣例，然後套用適用于限制類型和文字慣例的對應規則。
    -   否則，如果您遇到基本類型資料表中所列的其中一個基本類型，請套用基本型別和條件約束類型的對應規則。

-   如果您遇到 [文字慣例 \_ 宏](textual-convention-macro.md)中所列的其中一個文字慣例，請套用文字慣例的對應規則。
-   如果您遇到任何一個基本類型資料表中所列的其中一個基本類型，請套用基本類型的對應規則。

> [!Note]  
> 包含不符合上述對應之屬性類型的類別無效。 在此情況下，當提供者在執行實例抓取函式時要求抓取類別定義時，提供者會傳回錯誤。

 

## <a name="constrained-type"></a>條件約束類型

受限型別是一種基本類型、命名類型或文字慣例，受限於 SMI-S 檔 RFC 1213 和 RFC 1903 中所定義的部分 subtyping 機制。 發生 subtyping 時，需要額外的 CIM 限定詞來指定子類型值。 語法子句中的指名型別定義會逐字對應到 CIM 屬性限定詞 **物件 \_ 語法** （最多），但不包括子類型的條件約束。

子類型可以遵循下列任何格式：

-   列舉整數

    CIM 屬性辨識符號 **列舉** 會指定列舉值。 此辨識符號會以字串表示，其中包含帶正負號的32位整數值清單（以逗號分隔）。 下表列出對應類型。 預設值一律為 **Null**。



| 受限的 MIB 類型 | CIM 變異類型 | CIM 限定詞                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| 列舉整數   | VT \_ BSTR         | **文字 \_ 慣例**： enumeratedinteger<br/> **編碼**：整數<br/> **cimtype**：字串<br/> |



 

-   BITS

    CIM 屬性辨識符號 **位** 會指定列舉值。 此辨識符號會以字串表示，其中包含帶正負號的32位整數值清單（以逗號分隔）。 下表列出對應類型。 預設值一律為 **Null**。



| 受限的 MIB 類型 | CIM 變異類型      | CIM 限定詞                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| BITS                 | VT \_ 陣列 \| VT \_ BSTR | **文字 \_ 慣例**：位<br/> **編碼**： OCTETSTRING<br/> **cimtype**：字串<br/> |



 

-   Variable-length

    當語法子句參考 subtyped 為可變長度八進位字串或不透明的基本類型、命名類型或文字慣例時，CIM 屬性辨識符號的 **\_ 長度** 會指定與類型定義相關聯的最小值、最大值和固定長度值。 此限定詞會實作為下列格式的字串，其中的可變長度值會以不帶正負號的32位整數表示。

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   Fixed-length

    當語法子句參考 subtyped 為固定長度八進位字串或不透明的基本類型、命名類型或文字慣例時，CIM 屬性辨識符號 **固定 \_ 長度** 會指定固定長度的值。 此辨識符號會表示為不帶正負號的32位整數值。

-   範圍

    當語法子句參考 subtyped 為範圍值或固定值整數或量測計的基本類型、命名類型或文字慣例時，CIM 屬性辨識符號 **變數 \_ 值** 會指定與類型定義相關聯的範圍和固定值。 此限定詞會實作為下列格式的字串，其中範圍和固定長度的值會以不帶正負號的32位整數表示。

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a>範例程式碼

下列範例描述列舉整數子類型。

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

此範例對應至：

``` syntax
enumeration("up(1),down(2),testing(3)")
```

下列程式碼範例描述位子類型。

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

下列程式碼範例會對應至：

``` syntax
bits("up(1),down(2),testing(3)")
```

下列程式碼範例描述可變長度的子類型。

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

此範例對應至：

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

下列範例描述固定長度的子類型。

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

此範例對應至：

``` syntax
fixed_length(6)
```

下列範例說明範圍子類型。

``` syntax
Status := INTEGER (10..20|8)
```

此範例對應至：

``` syntax
variable_value("10..20,8")
```

 

 




