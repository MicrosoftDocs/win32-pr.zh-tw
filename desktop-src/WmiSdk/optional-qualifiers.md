---
description: 選擇性的限定詞可解決所有符合 CIM 規範的執行情況，這些都不是解讀這些限定詞的必要項。
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: 選用限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996964"
---
# <a name="optional-qualifiers"></a>選用限定詞

選擇性的限定詞可解決所有符合 CIM 規範的執行情況，這些都不是解讀這些限定詞的必要項。 規格中提供選擇性的限定詞，以避免在這些週期性情況下可能會發生的隨機使用者定義限定詞。

<dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**刪除**
</dt> <dd>

資料類型： **布林值**

適用于：關聯、參考

針對 [關聯]，指出當關聯中參考的任何物件被刪除，以及關聯中參考的個別物件是否以 **IfDeleted** 限定時，是否必須刪除限定的關聯。 預設值為 **FALSE**。

若為參考，此辨識符號會指出是否必須刪除參考的物件（如果包含參考的關聯已刪除並以 **IfDeleted** 限定），或者如果關聯中參考的任何物件被刪除，而且關聯中參考的個別物件是以 **IfDeleted** 限定。

使用方式：應用程式必須追蹤以 **Delete** 限定詞標記的關聯和參考，並適當地刪除關聯或參考。 如果關聯中的物件已經刪除，但是未標示為 **IfDeleted**，則不應該刪除關聯。

此使用規則必須在定義 CIM 安全性模型時進行驗證。

</dd> <dt>

<span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**昂貴**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性、參考、類別、關聯、方法

指出隱含的動作是否需要大量的計算。 預設值為 **FALSE**。

</dd> <dt>

<span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**
</dt> <dd>

資料類型： **布林值**

適用于：關聯和參考

指出如果參考的物件或關聯已刪除，是否必須刪除以 **Delete** 限定之關聯內的所有物件。 預設值為 **FALSE**。

</dd> <dt>

<span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**索引**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性、方法

指出是否應該為類別屬性編制索引。 當套用至存放庫所裝載之類別中的屬性時，這只具有在建立類別時建立 (的意義) 該屬性的快速次要查詢查閱。

只允許值 **TRUE** (預設) 。

</dd> <dt>

<span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**無形**
</dt> <dd>

資料類型： **布林值**

適用于：關聯、屬性、方法、參考、類別

指出此關聯是否僅針對內部用途而定義 (例如，相依性語義的定義) ，而且不應該顯示 (例如對應) 中。 預設值為 **FALSE**。

</dd> <dt>

<span id="Large"></span><span id="large"></span><span id="LARGE"></span>**大**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性、類別

指出屬性或類別是否需要大量儲存空間。 預設值為 **FALSE**。

</dd> <dt>

<span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**非 \_ Null**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性

指出類別屬性是否不能採用 **Null** 值 (**VT \_ null**) 。 只允許值 **TRUE** (預設) 。

如果指定了此限定詞，則 WMI 不允許建立屬性設為 **null** 的實例，而且 **Null** 屬性會傳回 **WBEM E 不 \_ \_ 合法的 \_ Null** 錯誤碼。

請注意，索引 [**鍵**](standard-qualifiers.md) 和 **索引** 限定詞已表示此行為。

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**供應商**
</dt> <dd>

資料類型： **字串**

適用于： Any

指出架構元素是動態的，因此是由提供者填入。 預設值為 **Null**。 此辨識符號是檢測的特定執行控點。

</dd> <dt>

<span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**實驗**
</dt> <dd>

資料類型： **布林值**

適用于： any

指出已將指定的專案建議為未來版本的 CIM 架構，但還不是標準架構的一部分。 相反地，專案可供使用者進行實驗、執行並提供意見反應。 根據意見反應，元素可能會新增至提供、修改或移除的標準。 預設值為 **FALSE**。 執行不需要支援具有此辨識符號的元素。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

資料類型： **字串**

適用物件：屬性、參考、方法、參數

指派給資料項目的特定類型。 預設值為 **Null**。

使用方式：您必須使用 **SyntaxType** 限定詞搭配此限定詞。

</dd> <dt>

<span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**
</dt> <dd>

資料類型： **字串**

適用物件：屬性、參考、方法、參數

**語法** 辨識符號的格式。 預設值為 **Null**。

使用方式：您必須使用 **語法** 辨識符號搭配此限定詞。

</dd> <dt>

<span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**
</dt> <dd>

資料類型： **字串**

適用物件：類別、屬性、方法、關聯、指示、參考

引發觸發程式的情況。 預設值為 **Null**。 觸發程式類型會依中繼模型結構而有所不同。

若為類別和關聯，合法值為：

建立

刪除

更新

Access

針對屬性和參考，合法值為： Update 和 Access。

針對方法，合法的值會在之前和之後。

如果是指示，則會擲回合法值。

</dd> <dt>

<span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性

值的集合，表示相關聯屬性的值是未知的 (無法將屬性視為具有有效或有意義的值) 。 預設值為 **Null**。

用來定義未知值的慣例和限制與適用于 [**ValueMap**](standard-qualifiers.md) 辨識符號的慣例和限制相同。

請注意，無法覆寫此限定詞。 當某個子類別視為某個父類別的未知值時，允許子類別將該值視為已知值是不合理的。

</dd> <dt>

<span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性

值的集合，表示不支援相關聯屬性的值 (無法將屬性視為具有有效或有意義的值) 。 預設值為 **Null**。

用來定義不支援值的慣例和限制與適用于 [**ValueMap**](standard-qualifiers.md) 辨識符號的慣例和限制相同。

注意：無法覆寫此限定詞。 允許子類別將值視為支援的值（由某些父類別視為未知）是不合理的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 限定詞](wmi-qualifiers.md)
</dt> <dt>

[新增限定詞](adding-a-qualifier.md)
</dt> </dl>

 

 




