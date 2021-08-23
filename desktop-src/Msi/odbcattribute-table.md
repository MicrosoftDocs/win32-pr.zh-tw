---
description: ODBCAttribute 資料表包含 (ODBC) 驅動程式和轉譯程式之開放式資料庫連接的屬性相關資訊。
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: ODBCAttribute 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e67cde1625812d1c5b8af7dc3bd24347891d3a769e24deeb02db7cc44396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943176"
---
# <a name="odbcattribute-table"></a>ODBCAttribute 資料表

ODBCAttribute 資料表包含 (ODBC) 驅動程式和轉譯程式之開放式資料庫連接的屬性相關資訊。

ODBCAttribute 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 驅動程式\_  | [識別碼](identifier.md) | Y   | N        |
| 屬性 | [Text](text.md)             | Y   | N        |
| 值     | [格式 化](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>司機\_
</dt> <dd>

驅動程式的內部權杖名稱。 資料表的主鍵。 [ODBCDriver 資料表](odbcdriver-table.md)中的外鍵。

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>屬性
</dt> <dd>

驅動程式屬性的名稱。 資料表的主鍵。

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

 

 



