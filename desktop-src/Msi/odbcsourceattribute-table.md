---
description: ODBCSourceAttribute 資料表包含資料來源屬性的相關資訊。
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: ODBCSourceAttribute 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d84ca19dfd059df4ff8f79d9409ef23288800f09e84d45e1b55d81bc8641e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082708"
---
# <a name="odbcsourceattribute-table"></a>ODBCSourceAttribute 資料表

ODBCSourceAttribute 資料表包含資料來源屬性的相關資訊。

ODBCSourceAttribute 資料表具有下列資料行。



| Column       | 類型                         | 答案 | Nullable |
|--------------|------------------------------|-----|----------|
| DataSource\_ | [識別碼](identifier.md) | Y   | N        |
| 屬性    | [Text](text.md)             | Y   | N        |
| 值        | [格式 化](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>資料來源\_
</dt> <dd>

資料來源的內部 token 名稱。 資料表的主鍵。

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>屬性
</dt> <dd>

資料來源屬性的名稱。 資料表的主鍵。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

屬性的可當地語系化字串值。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



