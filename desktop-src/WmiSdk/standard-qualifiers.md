---
description: 所有符合 CIM 規範的執行都必須處理一組標準的限定詞。
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: 標準限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997509"
---
# <a name="standard-qualifiers"></a>標準限定詞

所有符合 CIM 規範的執行都必須處理一組標準的限定詞。 任何特定的物件都未列出所有的限定詞。 通常，擴充類別會提供額外的限定詞，以促進類別實例的布建和其他作業。

提供者必須負責強制執行限定詞。 WMI 不會強制執行限定詞，但只會使用它們來通知使用者屬性的使用方式。

> [!Note]  
> WMI 符合 CIM 2.5 規格的規範。

 

限定詞有下列限制：

-   並非所有標準限定詞都可以一起使用。
-   並非所有的限定詞都可以套用至所有的結構，例如關聯或參考。 這些限制是在 [適用于] 清單中所識別。
-   針對特定的結構（例如關聯或參考），使用合法限定詞可能會進一步限制，因為某些限定詞是互斥的，使用一個限定詞可能表示對另一個限定詞的值有一些限制，依此類推。 這些使用規則已記載。
-   合法限定詞只會由屬性、方法、實例或子類別的實體（而不是透過關聯或參考）所繼承。 例如，參考不會繼承套用至屬性的 **MaxLen** 限定詞。

以下列出 WMI 標準限定詞。

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**抽象**
</dt> <dd>

資料類型： **布林值**

適用于：類別、關聯、指示

指出類別是否為抽象，而且只作為新類別的基底。 預設值為 **FALSE**。 您無法建立抽象類別的實例。 缺少這個辨識符號表示類別不是抽象的，因此，所有抽象類別都需要此限定詞。

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**骨料**
</dt> <dd>

資料類型： **布林值**

適用于：參考

指出參考是否為匯總關聯的父元件。 預設值為 **FALSE**。

使用方式： **匯總** 和 **匯總** 限定詞會一起使用   **，匯總會符合關聯** ，而 **Aggregate** 則會指定父系參考。

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**聚集**
</dt> <dd>

資料類型： **布林值**

適用于：關聯

指出關聯是否為匯總。 預設值為 **FALSE**。 搭配 **Aggregate** 使用。 所有匯總關聯都需要此限定詞。

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**別名**
</dt> <dd>

資料類型： **字串**

適用物件：屬性、參考、方法

架構中屬性或方法的替代名稱。 預設值為 **Null**。

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**
</dt> <dd>

資料類型： **字串**

適用物件：屬性、參數

限定陣列的型別。

有效值為：

-   包 (預設) 
-   索引
-   排序

使用方式：僅將這種類型的限定詞套用至屬性和參數，這些屬性和參數是使用括弧語法) 所定義 (陣列。

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**點陣圖**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性、方法、參數

每個重要位置都可以是「開啟」或「關閉」的重要位位置對應。 每個 "on" 位會對應至 **BitValues** 陣列中的對應值。 藉由將多個位「開啟」，則會指出 **BitValues** 陣列中的多個並行值。 預設值為 **Null**。

如需詳細資訊，請參閱 [點陣圖和 BitValues](bitmap-and-bitvalues.md)。

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性、方法、參數

將位位置值轉譯為相關聯的 **字串**。 預設值為 **Null**。

如需詳細資訊，請參閱 [點陣圖和 BitValues](bitmap-and-bitvalues.md)。

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**構造 函數**
</dt> <dd>

資料類型： **布林值**

適用于：方法

指出方法是否建立實例。 這些方法不會限制為單一實例或單一類別的作用。 例如，函式可以建立關聯實例，以及定義此函式之類別的實例。

「函式 **辨識符號」** 僅供資訊之用，不應該是由物件管理員處理。 物件管理員不需要在建立物件時呼叫此方法。 此外，呼叫函式時，物件管理員不需要叫用針對原始類別之任何父類別所定義的任何方法。 預設值為 **FALSE**。

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**
</dt> <dd>

資料類型： **字串**

適用于：類別

用來建立此類別之實例的方法名稱。 值可以是 "PutInstance" 或另一個建立實例的方法名稱。 預設值為 **Null**。

使用方式：只有在 **SupportsCreate** 限定詞存在時，才能使用這個限定詞。

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**
</dt> <dd>

資料類型： **字串**

適用于：類別

用來刪除這個類別之實例的方法名稱。 值為 "DeleteInstance" 或另一個刪除實例之方法的名稱。 預設值為 **Null**。

使用方式：只有在 **SupportsDelete** 限定詞存在時，才能使用這個限定詞。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

資料類型： **字串**

適用于： any

命名元素的描述。 預設值為 **Null**。

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**析 構 函數**
</dt> <dd>

資料類型： **布林值**

適用于：方法

指出方法是否刪除實例。 使用「 **函** 式」限定詞辨識符號的方法會刪除套用了「函式」 () 的實例，而不會限制在單一實例或類別上的作用。 例如，函式可能會刪除關聯實例，以及定義此函式之類別的實例。

「 **函** 式辨識符號」僅供資訊之用，不應該是由物件管理員處理。 當刪除實例時，物件管理員不會呼叫具有「 **函** 式」限定詞的方法。 此外，呼叫函式時，物件管理員不需要叫用針對原始類別之任何父類別所定義的任何析構函數方法。 預設值為 **FALSE**。

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**
</dt> <dd>

資料類型： **字串**

適用于： any

在 UI 中顯示的名稱，而非元素的實際名稱。 預設值為 **Null**。

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**
</dt> <dd>

資料類型： **字串**

適用于： any

限定的字串類型元素包含內嵌的實例。 限定詞值會在與擁有限定專案之類別相同的命名空間中，指定 CIM 類別的名稱。 內嵌實例是指定類別的實例，包括其子類別的實例。 預設值為 **Null**。

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**表**
</dt> <dd>

資料類型： **布林值**

適用于： any

指出屬性是否代表非負整數，這可能會增加或減少，但絕不會超過最大值。 預設值為 **FALSE**。

屬性的最大值不能大於 2 ^*n* -1。 *N* 可以是8、16、32或64，這取決於套用此限定詞之屬性的資料類型。 當模型化的資訊大於或等於最大值時，量測計的值會有其最大值。 如果隨後將模型化的資訊減少到最大值，量測計也會減少。 此限定詞只適用于具有不帶正負號的整數資料類型的屬性。

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**在**
</dt> <dd>

資料類型： **布林值**

適用于：參數

指出參數是否用來將值傳遞給方法。 預設值為 **TRUE**。

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In、Out**
</dt> <dd>

資料類型： **布林值**

適用于：參數

指出參數是否為輸入和輸出參數。

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**關鍵**](key-qualifier.md)
</dt> <dd>

資料類型： **布林值**

適用物件：屬性、參考

指出屬性是否為命名空間控制碼的一部分。 如果有一個以上的屬性具有索引 [**鍵**](key-qualifier.md) 限定詞，則所有這類屬性統稱 (複合索引鍵) 。 在一起時，索引鍵屬性必須提供每個類別實例的唯一參考。 如果將這個限定詞放置在屬性上，則只允許值 **TRUE** 。

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**懶惰**
</dt> <dd>

適用物件：屬性

指出屬性需要大量資源才能傳回，而且需要大量的處理器時間和記憶體。 WMI 藉由不嘗試傳回以 **延遲** 辨識符號標記的屬性，來改善查詢的效能。

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**
</dt> <dd>

資料類型： **字串陣列**

適用物件：類別、屬性、關聯、指示、參考

值的集合，表示位置的路徑，您可以在這裡找到有關屬性、類別、關聯、指示或參考之來源的詳細資訊。 對應字串可以是目錄路徑、URL、登錄機碼、包含檔、CIM 類別的參考，或是其他格式。 預設值為 **Null**。

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**麥克斯**
</dt> <dd>

資料類型： **int**

適用于：參考

在關聯中，指定參考可以有每一組其他參考值的最大值數目。 預設值為 **Null**。 例如，如果關聯將實例與 B 實例相關聯，而且每個 B 實例最多隻能有一個實例，則的參考最多應該有一個限定詞。

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**
</dt> <dd>

資料類型： **int**

適用物件：屬性、方法、參數

**字串** 資料項目的字元) 長度上限 (，並指出固定長度陣列的支援。

如果遇到固定長度的陣列， **MaxLen** 限定詞會包含剖析期間所找到的固定長度。 如果遇到可變長度的陣列，則不會使用這個限定詞。 **MaxLen** 可用來建議應儲存在陣列中的元素數目上限。 覆寫預設值時，可以指定任何不帶正負號的整數值 (**uint32**) 。 **Null** 值 (預設值) 表示不限長度。

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**Timespan.maxvalue**
</dt> <dd>

資料類型： **int**

適用物件：屬性、方法、參數

物件的最大值。 預設值為 **Null**。

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**化**
</dt> <dd>

資料類型： **int**

適用于：參考

參考的最小基數 (指定的參考可對關聯) 中的每個其他參考值設定的最小值數目。 預設值是 0。

例如，如果關聯將實例與 B 實例相關聯，而且每個 B 實例至少必須有一個實例，則的參考應該至少有一個限定詞。

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**
</dt> <dd>

資料類型： **int**

適用物件：屬性、方法、參數

指出物件的最小值。 預設值為 **Null**。

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性

值的集合，指出物件的屬性和 CIM 架構中的其他屬性之間的對應。 預設值為 **Null**。

物件屬性會使用下列語法來識別。

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**外地**
</dt> <dd>

資料類型： **字串**

適用于：參考

實例的位置，其值為 <*namespacetype*>：//<*namespacehandle*> 預設值為 **Null**。

使用方式：此限定詞不能與 **NonlocalType** 限定詞搭配使用。

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**
</dt> <dd>

資料類型： **字串**

適用于：參考

實例的位置類型。 其值為 <namespacetype> 。 預設值為 **Null**。

使用方式：此辨識符號不能與 **非本機** 辨識符號一起使用。

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**
</dt> <dd>

資料類型： **字串**

適用物件：屬性

值，表示相關聯的屬性為 **Null** (屬性沒有有效或有意義的值) 。 預設值為 **Null**。

用來定義 **Null** 值的慣例和限制與適用于 **ValueMap** 辨識符號的慣例和限制相同。 注意：無法覆寫此限定詞。 允許子類別傳回不同于父類別的 **Null** 值是不合理的。

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**擴展**
</dt> <dd>

資料類型： **布林值**

適用于：參數

指出參數是否會從方法傳回值。 預設值為 **FALSE**。

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**覆蓋**
</dt> <dd>

資料類型： **字串**

適用物件：屬性、方法、參考

父類別或次級結構 (屬性、方法或參考) 由衍生類別中相同名稱的屬性、方法或參考所覆寫。 預設值為 **Null**。

其格式為：

\[<*類別*>。 \] <*從屬結構*>

如果省略類別名稱，則會將覆寫套用至類別階層中父類別的從屬結構。

使用方式：覆 **寫** 辨識符號只能根據相同的中繼模型來參考結構。 在覆寫操作期間，不允許變更結構名稱或簽章。

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**
</dt> <dd>

適用于：類別

指出子類別上的屬性值是否會覆寫父類別中的值。 這項功能的含意是，如果您針對父類別執行查詢，而 **WHERE** 子句包含這個屬性，則父系必須傳回具有覆寫值的實例。 因此，Windows 管理會調整傳送至父類別的查詢 **WHERE** 子句，以排除這個屬性的參考。

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**傳播**
</dt> <dd>

資料類型： **字串**

適用物件：屬性

要傳播之金鑰的名稱。 預設值為 **Null**。

使用這個辨識符號時，會假設具有包含類別做為其目標的參考上只存在一個弱式限定詞。 相關聯的屬性必須與弱式關聯另一端之類別中的限定詞所命名的屬性具有相同的值。 其格式為：

\[<*類別*>。 \] <*從屬結構*>

使用方式：使用 **傳播** 的辨識符號時，必須使用值 **TRUE** 指定 [**金鑰**](key-qualifier.md)限定詞。

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**讀**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性

指出屬性是否可讀取。 預設值為 **TRUE**。

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**必填**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性

指出屬性是否需要非 null 值。 預設值為 **FALSE**。

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**修訂**
</dt> <dd>

資料類型： **字串**

適用于：類別、關聯、指示、架構

架構物件的次要修訂編號。 預設值為 **Null**。

使用方式：使用 **修訂** 限定詞時，必須要有 **版本** 限定詞才能提供主要版本號碼。

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**模式**
</dt> <dd>

資料類型： **字串**

適用物件：屬性、方法

定義功能的架構名稱。 預設值為 **Null**。

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**源**
</dt> <dd>

資料類型： **字串**

適用物件：類別、關聯、指示、參考

實例的位置。 預設值為 **Null**。

限定詞的值是 <*namespacetype*>：//<*namespacehandle*>。

使用方式： **來源** 辨識符號不能與 **SourceType** 限定詞搭配使用。

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**
</dt> <dd>

資料類型： **字串**

適用物件：類別、關聯、指示、參考

實例的位置類型。 此辨識符號的值是 <*namespacetype*>。 預設值為 **Null**。

使用方式： **SourceType** 限定詞不能與 **來源** 辨識符號一起使用。

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**
</dt> <dd>

資料類型： **布林值**

適用于：類別

指出類別是否支援建立實例。 預設值為 **FALSE**。

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

資料類型： **布林值**

適用于：類別

指出類別是否支援刪除實例。 預設值為 **FALSE**。

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**
</dt> <dd>

資料類型： **布林值**

適用于：類別

指出類別是否支援修改 (更新實例) 。 預設值為 **FALSE**。

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**終端**
</dt> <dd>

資料類型： **布林值**

適用于：類別

指出類別是否可以有子類別。 預設值為 **FALSE**。

如果已宣告子類別，則編譯器會產生錯誤。

使用方式：此限定詞不能與 **抽象** 辨識符號並存。 如果同時指定了 **終端** 機和 **抽象** 限定詞，則編譯器會產生錯誤。

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**單位**
</dt> <dd>

資料類型： **字串**

適用物件：屬性、方法、參數

用來表示相關聯資料項目的單位類型。 預設值為 **Null**。

例如，大小資料項目的 **單位** 值可能為 "bytes"。

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性、方法、參數

屬性、方法傳回型別或方法參數允許的值集。 預設值為 **Null**。

使用方式：此限定詞可以單獨使用，也可以與 **值** 限定詞組合使用。 搭配 **values** 辨識符號使用時，在 **ValueMap** 陣列中的值位置會提供 **值** 陣列中對應專案的位置。 請僅使用具有字串和整數值的 **ValueMap** 限定詞。 在值地圖陣列中表示整數值的語法是 \[ + \| = \] 數位 \[ \* 數位 \] 。 內容、最大位數和表示值會受限於相關聯屬性的型別。 例如，uint8 可能未簽署、必須小於四位數，且必須代表小於256的值。

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**值**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性、方法、參數

將整數值轉譯為相關聯字串的一組值。 預設值為 **Null**。

這個屬性也會指定要對應至列舉屬性的字串值陣列。 這個限定詞可以套用至整數屬性或字串屬性，而且對應可以是隱含或明確。 如果對應是隱含的，則整數或字串屬性值代表 **值** 陣列中的序數位置。 如果對應是明確的，則屬性必須是整數，而且有效的屬性值會列在由 **ValueMap** 辨識符號定義的陣列中。 如需詳細資訊，請參閱 [值對應](value-map.md)。

如果不存在 **ValueMap** 辨識符號，則會使用相關聯的屬性、方法傳回型別或方法參數中的值，將 **值** 陣列索引 (零相對的) 。 如果有 **ValueMap** 辨識符號，則值索引是由值對應中的屬性值位置所定義。

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**版本**
</dt> <dd>

資料類型： **字串**

適用物件：類別、架構、關聯、指示

架構物件的主要版本號碼。 預設值為 **Null**。 變更介面的架構進行變更時，版本號碼會遞增。

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**弱**
</dt> <dd>

資料類型： **布林值**

適用于：參考

指出參考類別的索引鍵是否包含關聯中其他參與者的索引鍵。 預設值為 **FALSE**。

當參考類別的識別相依于關聯中其他參與者的身分識別時，會使用這個限定詞。 任何一個指定類別的參考都不能是弱式。 關聯中的其他類別必須定義索引鍵。 關聯中其他類別的索引鍵會在參考的類別中重複，並以 **傳播** 的辨識符號標記。

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**寫**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性

表示應用程式或腳本可以變更屬性值。 執行應用程式的帳戶必須能夠存取包含類別實例的命名空間。 提供者的執行也可能會限制對提供者資料的存取。 **TRUE** 值表示屬性可由 WMI 和提供者允許存取的取用者讀取和寫入。 預設值為 **FALSE**。

缺少 **寫入** 限定詞的屬性仍可寫入。 提供者的執行可能會讓提供者類別中的任何屬性變更，不論 **寫入** 限定詞是否存在。

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性

表示在建立實例時，是否可寫入屬性。 此限定詞可與 **WriteAtCreate** 限定詞搭配使用。 預設值為 **FALSE**。

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**
</dt> <dd>

資料類型： **布林值**

適用物件：屬性

指出屬性在實例更新時是否可寫入。 此限定詞可與 **WriteAtCreate** 限定詞搭配使用。 預設值為 **FALSE**。

</dd> </dl>

## <a name="examples"></a>範例

如需有關如何抓取限定詞的詳細資訊，請參閱 TechNet 資源庫上的 [WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell 程式碼範例。

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

 

 




