---
description: ModuleConfiguration 資料表會識別模組的可設定屬性。 這個資料表不會合並到資料庫中。
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: ModuleConfiguration 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193310"
---
# <a name="moduleconfiguration-table"></a>ModuleConfiguration 資料表

ModuleConfiguration 資料表會識別模組的可設定屬性。 這個資料表不會合並到資料庫中。

ModuleConfiguration 資料表具有下列資料行。



| Column       | 類型                         | 答案 | Nullable |
|--------------|------------------------------|-----|----------|
| Name         | [識別碼](identifier.md) | Y   | N        |
| 格式       | [整數](integer.md)       | N   | N        |
| 類型         | [Text](text.md)             | N   | Y        |
| CoNtextData  | [Text](text.md)             | N   | Y        |
| DefaultValue | [Text](text.md)             | N   | Y        |
| 屬性   | [整數](integer.md)       | N   | Y        |
| DisplayName  | [Text](text.md)             | N   | Y        |
| Description  | [Text](text.md)             | N   | Y        |
| HelpLocation | [Text](text.md)             | N   | Y        |
| HelpKeyword  | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

此欄位定義可設定專案的名稱。 這個名稱會在 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中的格式化範本中參考。

</dd> <dt>

<span id="Format"></span><span id="format"></span><span id="FORMAT"></span>格式
</dt> <dd>

此資料行指定要變更的資料格式。



| 格式                                       | 值 |
|----------------------------------------------|-------|
| [Text](text-format-types.md)                | 0     |
| [金鑰](key-format-types.md)                  | 1     |
| [整數](integer-format-types.md)          | 2     |
| [位位格式](bitfield-format-types.md) | 3     |



 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型
</dt> <dd>

這個資料行會指定變更資料的類型。 此類型是用來提供任何使用者介面的內容，而且不會用於合併進程。 此資料行的有效值取決於 Format 資料行中的值。

</dd> <dt>

<span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>CoNtextData
</dt> <dd>

這個資料行會指定所要求資料的語義內容。 類型是用來提供任何使用者介面的內容，而且不會用於合併處理。 此資料行的有效值取決於 [格式] 和 [類型] 資料行中的值。

</dd> <dt>

<span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>值
</dt> <dd>

如果合併工具拒絕提供值，此資料行會指定此記錄中專案的預設值。 這個值必須具有專案的格式、類型和內容。 如果這是「金鑰」格式專案，外鍵必須是模組資料表中的有效索引鍵。 根據專案而定，Null 可能是此資料行的有效值。 針對「金鑰」格式專案，此值採用 [CMSM 的特殊格式](cmsm-special-format.md)。 若為所有其他類型，則會將值視為字面處理。

模組作者必須確保模組在其預設狀態中是有效的。 這可確保2.0 版之前的 Mergemod.dll 版本仍可使用其預設狀態中的模組。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

此資料行是一個位欄位，其中包含這個可設定專案的屬性。 Null 相當於0。 此資料行中的所有其他位都保留供日後使用，且必須為0。



| Name                             | Decimal | 十六進位 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msmConfigurableOptionKeyNoOrphan | 1       | 0x00000001  | 這個屬性只適用于在其 DefaultValue 欄位中列出模組資料表外鍵的記錄。 合併工具會忽略索引 [鍵格式類型](key-format-types.md)以外之任何格式的屬性。 下列檢查會排除未列在 [ModuleSubstitution 資料表](modulesubstitution-table.md) 中的專案。 如果在完成所有設定選項之後滿足下列條件，則合併工具不會將 DefaultValue 資料行所參考的資料列合併到目標資料庫。<br/> ModuleConfiguration 資料表中具有相同 DefaultValue 的每個資料列都會設定 msmConfigurationItemsKeyNoOrphan。<br/> 沒有任何資料列使用 DefaultValue，因為 authoring tool 已拒絕提供值。<br/> 如果符合下列任一條件，則合併工具會合並資料列。<br/> 合併工具會尋找未設定 msmConfigItemsKeyNoOrphan 的任何資料列。<br/> 如果合併工具使用 DefaultValue 找到任何資料列，因為 authoring tool 已拒絕提供值。<br/> |
| msmConfigurableOptionNonNullable | 2       | 0x00000002  | 當設定這個屬性時，null 不是此專案的有效回應。 這個屬性不會影響 [整數格式類型](integer-format-types.md) 或位欄位 [格式類型](bitfield-format-types.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName
</dt> <dd>

本資料行提供 authoring tool 可能在使用者介面中使用之這個專案的簡短描述。 此資料行可能尚未當地語系化。 將此資料行設定為 null，讓模組要求 authoring tool 不會在 UI 中公開此屬性。 此工具可能會忽略此欄位中的值。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

此資料行提供 authoring tool 可在 UI 元素中使用的這個專案的描述。 這個字串可能會由模組的語言轉換所當地語系化。 此資料行可以是 null。

</dd> <dt>

<span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation
</dt> <dd>

此資料行提供說明檔的名稱 (不含 .chm 副檔名) 或以分號分隔的說明命名空間清單。 如果沒有可用的說明，此資料行可以是 null。 只有當 HelpKeyword 資料行是 null 時，這個資料行才可以是 null。

</dd> <dt>

<span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword
</dt> <dd>

這個資料行會從 HelpLocation 資料行提供說明檔或命名空間中的關鍵字。 此關鍵字的解讀取決於 HelpLocation 資料行。 此資料行可以是 null。

</dd> </dl>

## <a name="remarks"></a>備註

ModuleConfiguration 資料表是由可設定的 [合併模組](configurable-merge-modules.md)所使用。 需要 Mergemod.dll 2.0 或更新版本，才能建立可設定的合併模組。

為了確保與舊版 Mergemod.dll 的相容性，ModuleConfiguration 資料表和 [ModuleSubstitution 資料表](modulesubstitution-table.md) 應該加入至每個模組的 [ModuleIgnoreTable 資料表](moduleignoretable-table.md) 。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
[ICE45](ice45.md)  
</dl>

 

 




