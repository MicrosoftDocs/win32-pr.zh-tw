---
description: ConfigurableItem 物件代表 ModuleConfiguration 資料表中的單一資料列。
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: 'ConfigurableItem 物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990810"
---
# <a name="configurableitem-object"></a>ConfigurableItem 物件

**ConfigurableItem 物件** 代表 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的單一資料列。 這是模組中單一可設定的「屬性」。 介面是由唯讀屬性組成，ModuleConfiguration 資料表中的每個資料行各一個。 介面定義如下所示。

## <a name="members"></a>成員

**ConfigurableItem** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ConfigurableItem** 物件具有這些屬性。



| 屬性                                                         | 描述                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**屬性**](configurableitem-attributes.md)<br/>     | 在 ModuleConfiguration 資料表中，傳回這個物件記錄之屬性欄位中的值。<br/>                            |
| [**Context**](configurableitem-context.md)<br/>           | 傳回 ModuleConfiguration 資料表中這個物件記錄的內容欄位中的值。<br/>                               |
| [**DefaultValue**](configurableitem-defaultvalue.md)<br/> | 傳回 ModuleConfiguration 資料表中這個物件記錄的 DefaultValue 欄位中的值。<br/>                          |
| [**描述**](configurableitem-description.md)<br/>   | 在 ModuleConfiguration 資料表中，傳回這個物件記錄之 Description 欄位中的值。<br/>                           |
| [**DisplayName**](configurableitem-displayname.md)<br/>   | 傳回 ModuleConfiguration 資料表中這個物件記錄的 DisplayName 欄位中的值。<br/>                           |
| [**格式**](configurableitem-format.md)<br/>             | 傳回 ModuleConfiguration 資料表中這個物件記錄之格式欄位的值。<br/>                                |
| [**HelpKeyword**](configurableitem-helpkeyword.md)<br/>   | 傳回 ModuleConfiguration 資料表中這個物件記錄之 HelpKeyword 欄位的值。<br/>                           |
| [**HelpLocation**](configurableitem-helplocation.md)<br/> | 傳回 ModuleConfiguration 資料表中這個物件記錄之 HelpLocation 欄位的值。<br/>                          |
| [**Name**](configurableitem-name.md)<br/>                 | 在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中，傳回這個物件記錄之 [名稱] 欄位中的值。<br/> |
| [**類型**](configurableitem-type.md)<br/>                 | 在 ModuleConfiguration 資料表中，傳回這個物件之記錄的類型欄位中的值。<br/>                                  |



 

## <a name="c"></a>C++

介面 **IMsmConfigurableItem： IDispatch**

## <a name="interface-id"></a>介面識別碼



| 常數                      | 值                                  |
|-------------------------------|----------------------------------------|
| **IID \_ IMsmConfigurableItem** | {4D6E6284-D21D-401E-84F6-909E00B50F71} |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 2.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




