---
description: 指定索引鍵以選取純量或資料表集合中的唯一資料列。
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: INDEX 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 915cbe1c4bf1da5ccd7fbab881770722b70bc53c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115805"
---
# <a name="index-clause"></a>INDEX 子句

INDEX 子句會指定索引鍵，以選取純量或資料表集合中的唯一資料列。 SNMP 提供者會根據 SNMP 裝置使用的資料表類型，對應至不同類型的 CIM 類別。 因為索引鍵可以是一種以上的物件類型，所以提供者會根據索引鍵內的物件類型，使用不同的對應規則。 如需詳細資訊，請參閱 [索引子句資料類型](#index-clause-data-types)。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

純量集合會對應到 CIM singleton 類別：也就是只能有一個實例的類別。 因為不需要從另一個實例來唯一識別實例，所以單一類別不會將一或多個屬性指定為索引鍵。 從純量集合產生的類別：

-   請勿包含索引 **鍵** 屬性限定詞。
-   確實包含標準 CIM 類別辨識符號 **Singleton**，其為 **Bool** 類型。

資料表集合會對應到可以有一個以上實例的 CIM 類別。 因此，CIM 類別定義必須至少包含一個定義物件索引鍵的屬性;也就是可唯一識別類別實例的屬性。 資料表集合的 [物件類型](object-type-macro.md) 宏的 INDEX 子句會指定集合的索引鍵屬性集。 下列對應規則適用：

-   CIM 辨識符號索引 **鍵**（type **Bool**）會定義索引鍵屬性。
-   資料表集合內的索引資訊順序會定義 CIM 類別定義中索引鍵的順序。

    CIM 辨識符號索引 **鍵 \_ 順序** 會定義索引鍵的順序。 此辨識符號是不帶正負號的32位整數值，基於 MOF 辨識符號語法的目的，必須使用2補數運算，將其轉換為帶正負號的32位整數值。

目前，SNMPv2C INDEX 子句的對應不會處理 **隱含** 辨識符號的使用。 在此情況下，不會產生 CIM 類別定義。

## <a name="index-clause-data-types"></a>INDEX 子句資料類型

由於 [OBJECT TYPE](object-type-macro.md) 宏內的 INDEX 子句有彈性，因此索引鍵屬性的規格並不直接。 相反地，您應該考慮 INDEX 子句可能包含下列一或多個資料類型的可能性：

-   內部可存取的 **indexobject** 值

    **Indexobject** 值是一個名為的值，它會參考出現在包含 INDEX 子句之相同資料表的概念資料列中的 MIB 物件定義。 INDEX 子句中參考的 MIB 物件定義會對應到 CIM 類別定義的索引鍵屬性。

-   外部可存取的 **indexobject** 值

    在此情況下， **indexobject** 是指在不同資料表的概念資料列中所顯示的 MIB 物件定義的命名值。

-   可存取的 **indextype** 值

    **Indextype** 值是參考下列其中一種資料類型的命名類型： **INTEGER**、**八進位字串**、**物件識別碼**、 **networkaddress.cache.ttl** 或 **IpAddress**。 如果 INDEX 子句包含 MIB 型別參考，則適用下列對應規則：

    -   所參照的 MIB 物件會對應至 CIM 類別定義的索引鍵屬性。 其型別語法是以指定的 **indextype** 值為基礎，這會使用標準 [語法子句](syntax-clause.md) 對應程式對應到 CIM 屬性限定詞。
    -   對應進程會串連 MIB 資料表物件描述元、底線 (\_) ，以及 INDEX 子句 **indextype** 值的次序順序，以產生唯一的屬性名稱。 例如，MIB 資料表 **enterpriseIfTable** 的第三個元件 **indextype** 的屬性名稱是 **enterpriseIfTable \_ 3**。
    -   CIM 屬性會以 **虛擬 \_ 金鑰** 辨識符號進行批註。 此辨識符號指定 SNMP 提供者應該根據與類別定義中所有可存取的 MIB 物件定義相關聯之實例資訊的超集合，來計算屬性的值。
    -   CIM 類別定義必須至少包含一個沒有相關聯 **虛擬 \_ 金鑰** 辨識符號的屬性; 無法指定此屬性會讓類別定義失效。

-   固定長度的子類型

    當 SNMP 資料表集合的 INDEX 子句包含 subtyped 為固定長度八位字串的 SNMP 支援型別時，必須使用 CIM 屬性辨識符號 **固定 \_ 長度** 來指定此值。

 

 



