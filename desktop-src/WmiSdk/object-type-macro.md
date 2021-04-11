---
description: 物件類型宏包含必要的和選擇性子句，可描述 MIB 物件的基本特性。 SNMP 提供者會將 MIB 轉換成物件類型宏的對應部分。
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: OBJECT 類型宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111961"
---
# <a name="object-type-macro"></a>OBJECT 類型宏

物件類型宏包含必要的和選擇性子句，可描述 MIB 物件的基本特性。 SNMP 提供者會將 MIB 轉換成物件類型宏的對應部分。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

## <a name="components"></a>單元

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB 物件
</dt> <dd>

物件，其中包含大部分有問題的資料。

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>物件描述元
</dt> <dd>

識別每個 MIB 物件的唯一名稱或物件描述元。 每個 MIB 物件描述項會完全對應至 CIM 屬性名稱。 例如， **ifIndex** 會轉譯成 **ifIndex**。

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[語法子句](syntax-clause.md)
</dt> <dd>

定義 MIB 物件的資料和類型。

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX 子句](index-clause.md)
</dt> <dd>

定義用來選取唯一資料表資料列的索引鍵。

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>增強子句
</dt> <dd>

指出它所指定的資料表集合可以視為另一個資料表集合的延伸，並且可以取代 SNMPv2 中的 INDEX 子句。 增強型子句所參考的集合可以與其他資料表集合結合，以形成一個集合。 產生的集合會共用在鏈中最後一個資料表集合中指定的主要索引鍵屬性。

在此情況下，為 INDEX 子句指定的先前對應規則會套用至鏈中的最後一個資料表集合。 接著，物件的集合會對應到一個 CIM 類別定義。

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>物件識別碼子句
</dt> <dd>

包含 MIB 物件的唯一物件識別碼。 此物件識別碼會對應至 CIM 屬性辨識符號 **物件 \_ 識別碼**。

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[存取和最大存取權子句](access-and-max-access-clauses.md)
</dt> <dd>

定義 MIB 物件的存取權限。

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION 子句
</dt> <dd>

提供物件的文字描述，該物件會對應至 CIM 屬性辨識符號 **描述**。 這個子句可能是空的。

SNMP 資料表定義中的每個 **資料表** 和 **專案** 物件也包含 DESCRIPTION 子句，也可能是空的。 資料表和專案描述子句會串連在一起，且結果會對應至 CIM 類別限定詞 **描述**。

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS 子句
</dt> <dd>

指出是否必須支援此物件。 當 STATUS 子句的值 **過時** 時，提供者會從對應中捨棄 MIB 物件。 否則，STATUS 子句會對應到 CIM 屬性限定詞的 **狀態**。

針對 SNMPv1，[ **狀態** ] 的慣用值是 [ **強制** ] 或 [ **選擇性**]，但辨識符號可以包含其他一些值。 若為 SNMPv2C，則 [ **狀態** ] 的慣用值為 [ **目前** ] 或 [已 **淘汰**]，但辨識符號可以包含其他一些值。

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL 子句
</dt> <dd>

將預設值指派給邏輯資料表資料列中的變數，並對應至字串 CIM 屬性辨識符號 **Defval**。

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE 子句
</dt> <dd>

指的是包含物件之詳細資訊的另一份檔。 這個子句會對應到 CIM 屬性辨識符號 **參考**，它是字串類型。

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>單位子句
</dt> <dd>

提供物件所代表內容的精確定義。 這個子句會對應到 CIM 屬性限定詞 **單位**，這是字串類型。

</dd> </dl>

## <a name="remarks"></a>備註

物件類型宏描述個別 MIB 物件的基本特性。 一組物件類型宏可視為相關物件的群組。 在 SNMPv2C 中，使用物件群組宏將相關物件的集合正式分組到集合中。 不過，在 SNMPv1 中建立集合沒有正式的機制。 基於 SNMP 提供者的目的，會忽略物件群組宏，但您可以建立群組關聯性和製作集合。

 

 



