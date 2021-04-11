---
description: ModuleSubstitution 資料表會指定模組資料庫的可設定欄位，並為每個欄位的設定提供範本。
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: ModuleSubstitution 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e27789f723af87e228bada91b79a16d7dc4d2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195281"
---
# <a name="modulesubstitution-table"></a>ModuleSubstitution 資料表

ModuleSubstitution 資料表會指定模組資料庫的可設定欄位，並為每個欄位的設定提供範本。 使用者或合併工具可能會查詢此資料表，以判斷要進行的設定作業。 此資料表不會合並到目標資料庫。

下列資料表不能包含可設定的欄位，而且不得列在此資料表中：

ModuleSubstitution 資料表

[ModuleConfiguration 資料表](moduleconfiguration-table.md)

[ModuleExclusion 資料表](moduleexclusion-table.md)

[ModuleSignature 資料表](modulesignature-table.md)

ModuleSubstitution 資料表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| 資料表  | [識別碼](identifier.md) | Y   | N        |
| 資料列    | [Text](text.md)             | Y   | N        |
| Column | [識別碼](identifier.md) | Y   | N        |
| 值  | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

此資料行指定要在模組資料庫中修改的資料表名稱。

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>行
</dt> <dd>

此欄位會在資料表資料行中指定的資料表中，指定目標資料列的主鍵。 多個主鍵會以分號分隔。 在對目標資料表進行任何變更之前，已選取要修改的目標資料列。 如果 ModuleSubstitution 資料表中的一筆記錄變更目標資料列的主鍵欄位，則會根據原始主鍵資料套用 ModuleSubstitution 資料表中的其他記錄，而不是主鍵替代的結果。 資料列替代的順序未定義。

本資料行中的值一律為 [CMSM 的特殊格式](cmsm-special-format.md)。 常值分號 ( '; '您可以在字元前面加上反斜線來新增 ) 或等號 ( ' = ' ) 。 '\\'. 索引鍵的 null 值會以 null、前置分號、兩個連續分號或尾端分號表示，視 null 值為唯一、第一個、中間或最後一個索引鍵資料行值而定。

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>列
</dt> <dd>

此欄位會在 [資料列] 資料行中指定名為的資料列中的目標資料行。 如果 ModuleSubstitution 資料表中的多個資料列變更相同目標資料列的不同資料行，則會在將修改的資料列插入資料庫之前，先執行所有資料行替換。 資料行替換順序未定義。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

此資料行包含字串，可針對要取代為數據表、資料列和資料行所指定之目標欄位的資料，提供格式化範本。 當遇到 form = ItemA 的替代字串時 \[ \] ，會以可設定的 "ItemA" 的值取代字串（包括括弧字元）。 可設定的專案 "ItemA" 是在 [ModuleConfiguration 資料表](moduleconfiguration-table.md) 的 Name 資料行中指定的，而它的值是由合併工具所提供。 如果合併工具拒絕在取代字串中提供任何專案的值，則會替代 ModuleConfiguration 資料表的 DefaultValue 資料行中指定的預設值。 如果字串參考不在 ModuleConfiguration 資料表中的專案，則合併會失敗。

-   此資料行使用 [CMSM 特殊格式](cmsm-special-format.md)。 常值分號 ( '; '您可以在字元前面加上反斜線，以將 ) 或等號 ( ' = ) ' 新增至資料表。 '\\'.
-   值欄位可能包含多個替代字串。 例如，"Food1" 和 "Food2" 字串在字串中的設定： " \[ = Food1 \] 是不錯的，但 \[ = Food2 較 \] 好，因為 \[ = Food2 \] 更營養。」
-   取代字串不得進行嵌套。 範本 " \[ = AB \[ = CDE \] \] " 無效。
-   如果 [值] 欄位評估為 null，而且目標欄位不可為 null，則合併會失敗，並會建立 msmErrorBadNullSubstitution 類型的錯誤物件，並將其加入至錯誤清單。 如需詳細資訊，請參閱 [**get \_ Type 函數**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type)中所述的錯誤類型。
-   如果 [值] 欄位評估為 null GUID： {00000000-0000-0000-0000-000000000000} ，則在將資料列合併至模組之前，會以功能的名稱取代 Null guid。 如需詳細資訊，請參閱 [合併模組中的參考功能](referencing-features-in-merge-modules.md)。
-   值欄位中的範本會在插入目標欄位之前進行評估。 取代任何功能之前，請先完成資料列的替代。
-   如果 [值] 資料行評估為唯一的整數位符字串 (有選擇性的 + 或-) ，則會將字串轉換成整數格式，然後再將其取代為 [整數格式類型](integer-format-types.md)的目標欄位。 如果範本評估為不只包含整數個字元的字串 (以及選擇性的 + 或-) 則結果無法替代為整數目標欄位。 嘗試在整數位段中插入非整數會導致合併失敗，並將 msmErrorBadSubstitutionType 錯誤物件加入至錯誤清單。
-   如果 [資料表] 和 [資料行] 欄位中指定的目標資料行是 [文字格式類型](text-format-types.md)，而 [值] 欄位的評估結果為 [整數格式類型](integer-format-types.md)，則會在目標文字欄位中插入數位的十進位標記法。
-   如果目標欄位是 [整數格式類型](integer-format-types.md)，[值] 欄位包含以位 [格式](bitfield-format-types.md)表示的非分隔專案清單、[目標] 欄位中的值會結合使用位 **and** 運算子與專案中所有遮罩值的反位 **or** ，然後使用位 **or** 運算子搭配其對應的遮罩值進行遮罩處理時，結合每個整數或位專案。 基本上，這會將屬性中的位明確設定為提供的值，但會保留儲存格中的所有其他位。
-   如果 [值] 欄位評估為索引 [鍵格式類型](key-format-types.md)，而且在使用多個主鍵的資料表中是索引鍵，則專案名稱後面可能會接著分號和整數值，指出以1為基礎的索引，並將組成主鍵的一組值一起組成。 如果未指定整數，則會使用值1。 例如， [控制資料表](control-table.md) 有兩個主鍵資料行： Dialog \_ 和 Control。 專案 "Item1" 的值是控制資料表中的索引鍵，其格式為 "DialogName;Controlnameinrow "，其中 DialogName 是對話方塊資料表中的值， \_ 而 controlnameinrow 是控制項資料行中的值。 若要以單純的 Controlnameinrow 替代， \[ 應使用替代字串 = Item1; 2 \] 。

</dd> </dl>

## <a name="remarks"></a>備註

ModuleSubstition 資料表是由可設定的 [合併模組](configurable-merge-modules.md)所使用。 需要 Mergemod.dll 版本2.0 或更新版本，才能建立可設定的合併模組。

為了確保相容于2.0 版之前的 Mergemod.dll 版本， [ModuleConfiguration 資料表](moduleconfiguration-table.md) 和 ModuleSubstitution 資料表應該包含在每個模組的 [ModuleIgnoreTable 資料表](moduleignoretable-table.md) 中。

 

 
