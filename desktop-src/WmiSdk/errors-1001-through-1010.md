---
description: 描述 WMI SNMP 提供者錯誤1001到1010。
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: 錯誤1001到1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fac32553e345dfe2f011d6294ff045db58c681b49dc127bd0da8e5afabf0757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411938"
---
# <a name="errors-1001-through-1010"></a>錯誤1001到1010

描述 WMI SNMP 提供者錯誤1001到1010。

[嚴重錯誤1001](#fatal-error-1001)

[嚴重錯誤1002](#fatal-error-1002)

[嚴重錯誤1003](#fatal-error-1003)

[警告1004](#warning-1004)

[警告1005](#warning-1005)

[嚴重錯誤1006](#fatal-error-1006)

[嚴重錯誤1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>嚴重錯誤1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001，嚴重>： " <fileName> ： <行 \#>：物件類型的語法子句無法解析為允許的類型"
</dt> <dd>

物件類型宏調用模組語意錯誤。 物件類型宏的語法子句必須解析為類型或子類型，使用 SNMPv1 或 SNMPv2C SMI-S 允許的大小或範圍規格來形成。 如果不是這種情況，則會報告嚴重錯誤1001。

編譯 SNMPv1 或 SNMPv2C MIB 時，會發生此錯誤。

SNMPv1 SMI-S 允許的類型為：

-   INTEGER
-   NULL
-   八位字串
-   物件識別碼
-   Networkaddress.cache.ttl
-   IpAddress
-   計數器
-   量測計
-   TimeTicks
-   Opaque
-   DisplayString
-   PhysAddress

SNMPv2C SMI-S 允許的類型為：

-   INTEGER
-   八位字串
-   物件識別碼
-   BITS
-   Integer32
-   IpAddress
-   Counter32
-   TimeTicks
-   Opaque
-   Counter64
-   Unsigned32
-   DisplayString
-   PhysAddress
-   MacAddress
-   TruthValue
-   TestAndIncr
-   AutonomousType
-   InstancePointer
-   VariablePointer
-   RowPointer
-   RowStatus
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   Tdomain
-   Taddress

</dd> </dl>

## <a name="fatal-error-1002"></a>嚴重錯誤1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002，嚴重>： " <fileName> ： <行 \#>：不正確存取子句 <clause> "
</dt> <dd>

物件類型宏調用模組語意錯誤。 若為 SNMPv1，則物件類型宏的存取子句必須是「唯讀」、「僅限寫入」、「讀取/寫入」或「不可存取」。

針對 SNMPv2C，MAX 存取子句必須是「唯讀」、「讀取-建立」、「讀取/寫入」或「無法存取」。

</dd> </dl>

## <a name="fatal-error-1003"></a>嚴重錯誤1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003、嚴重>： " <fileName> ： <行 \#>：不正確 STATUS 子句 <clause> "
</dt> <dd>

物件類型宏調用模組語意錯誤。 若為 SNMPv1，則物件類型宏調用的 STATUS 子句必須是「強制性」、「選擇性」、「已淘汰」或「已淘汰」。

若為 SNMPv2C，則物件類型宏調用的 STATUS 子句必須是「目前」、「已淘汰」或「過時」。

</dd> </dl>

## <a name="warning-1004"></a>警告1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004，警告>： " <fileName> ： <行 \#>：物件類型 <identifier> ，其語法解析為其中一個計數器類型時，不是以字母 '" 結尾
</dt> <dd>

物件類型宏調用模組語義警告。 語法計數器 (SNMPv1) 或 Counter32 和 Counter64 (SNMPv2C) 的物件識別碼必須是複數。

編譯 SNMPv1 或 SNMPv2C MIB 時可能會發生這個警告。

</dd> </dl>

## <a name="warning-1005"></a>警告1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005，警告>： " <fileName> ： <行 \#>：具有" SEQUENCE OF "順序的物件類型，則應該有存取子句「無法存取」
</dt> <dd>

物件類型宏調用模組語義警告。 資料表或概念資料列 (序列的或序列物件類型，分別) 必須是「不可存取」。

此警告可能會在 SNMPv1 或 SNMPv2C 中發生。

</dd> </dl>

## <a name="fatal-error-1006"></a>嚴重錯誤1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006，嚴重>： " <fileName> ： <行 \#> 物件類型 <identifier> （這是語法順序）沒有索引或增強子句"
</dt> <dd>

物件類型宏調用模組語意錯誤。 針對 SNMPv1，其語法會解析為序列類型的物件類型定義必須有 INDEX 子句。

針對 SNMPv2C，概念資料列宣告必須有索引或增強子句。

</dd> </dl>

## <a name="fatal-error-1008"></a>嚴重錯誤1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008，嚴重>： " <fileName> ： <行 \#>：物件類型 <identifier> ，也就是" SEQUENCE "的語法未被參考"
</dt> <dd>

物件類型宏調用模組語意錯誤。 以語法子句作為序列類型的物件類型，必須在只是一個代表資料表宣告的物件類型調用的語法子句中，也就是使用語法子句作為類型序列的物件。 <行 \#> 參數參考第二個點參考。

這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。

</dd> </dl>

 

 



