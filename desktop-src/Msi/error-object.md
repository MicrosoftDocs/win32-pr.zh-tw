---
description: Error 物件會傳回單一合併錯誤的資訊。
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: '錯誤物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 237cf88b2830bf210e84d016b52b7fd0b0183c0c0072ac8f654663e2cd3c12dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947029"
---
# <a name="error-object"></a>Error 物件

**Error** 物件會傳回單一合併錯誤的資訊。

## <a name="members"></a>成員

**Error** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Error** 物件具有這些屬性。



| 屬性                                                | 描述                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**DatabaseKeys**](error-databasekeys.md)<br/>   | 傳回資料庫資料表中造成錯誤之資料列的主鍵。<br/> |
| [**DatabaseTable**](error-databasetable.md)<br/> | 傳回資料庫中造成錯誤之資料表的資料表名稱。<br/>           |
| [**語言**](error-language.md)<br/>           | 傳回錯誤的語言。<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | 傳回模組資料表中造成錯誤之資料列的主鍵。<br/>   |
| [**ModuleTable**](error-moduletable.md)<br/>     | 傳回模組中造成錯誤之資料表的資料表名稱。<br/>             |
| [**路徑**](error-path.md)<br/>                   | 傳回造成錯誤之檔案或目錄的路徑。 目前未使用。<br/>    |
| [**類型**](error-type.md)<br/>                   | 傳回錯誤的類型。<br/>                                                        |



 

## <a name="c"></a>C++

介面 **IMsmError： IDispatch**

## <a name="interface-id"></a>介面識別碼



| 常數           | 值                                  |
|--------------------|----------------------------------------|
| **IID \_ IMsmError** | {0ADDA828-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




