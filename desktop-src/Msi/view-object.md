---
description: View 物件代表使用資料庫物件的 OpenView 方法處理查詢時所取得的結果集。
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: View 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994122"
---
# <a name="view-object"></a>View 物件

**View** 物件代表使用 [**資料庫**](database-object.md)物件的 [**OpenView**](database-openview.md)方法處理查詢時所取得的結果集。 在可以傳輸任何資料之前，必須使用 [**Execute**](view-execute.md) 方法來執行查詢，並將 SQL 查詢字串中指定的所有可取代參數傳遞給它。 您可以視需要使用不同的參數再次執行查詢，但只在釋放結果集之後，只要提取所有記錄或呼叫 [**Close**](view-close.md) 方法。

## <a name="members"></a>成員

**View** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**View** 物件有這些方法。



| 方法                            | 描述                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**關閉**](view-close.md)       | 終止查詢執行並釋放資料庫資源。<br/>                                                                                                          |
| [**執行**](view-execute.md)   | 使用問號標記來代表 SQL 查詢中的參數。 這些參數的值會傳入做為參數記錄的對應欄位。<br/> |
| [**獲取**](view-fetch.md)       | 如果結果集中有多個資料列可供使用，則傳回包含所要求資料行資料的 [**記錄**](record-object.md) 物件，否則會傳回 null。<br/>      |
| [**GetError**](view-geterror.md) | 傳回發生錯誤的驗證錯誤和資料行名稱。<br/>                                                                                           |
| [**修改**](view-modify.md)     | 使用 [**Fetch**](view-fetch.md)方法取得的修改 [**記錄**](record-object.md)物件來修改資料庫資料列。<br/>                                   |



 

### <a name="properties"></a>屬性

**View** 物件具有這些屬性。



| 屬性                                         | 描述                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**ColumnInfo**](view-columninfo.md)<br/> | 傳回 [**記錄**](record-object.md) 物件，其中包含結果集中每個資料行的要求資訊。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




