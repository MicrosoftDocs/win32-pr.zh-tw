---
description: 資料庫物件會存取安裝程式資料庫。
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: 資料庫物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3dcdb2c4098905d7e6a410e786d4af254732bc80cee4b760870a7c1c44a8ec26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086198"
---
# <a name="database-object"></a>資料庫物件

**資料庫** 物件會存取安裝程式資料庫。

當 **資料庫** 物件被移出範圍，或與其相關聯的物件變數設定為 null 時，就會釋放該物件。 您必須在釋放 **資料庫** 物件之前呼叫 [**Commit**](database-commit.md)方法，以寫出所有持續性變更。 如果未呼叫 **Commit** 方法，安裝程式會在物件終結時執行隱含復原。

用戶端可以使用下列程式進行資料存取。

**若要查詢 API 排序**

1.  藉由呼叫 [**OpenDatabase**](installer-opendatabase.md)或 [**安裝程式**](installer-object.md)物件來取得 **資料庫** 物件。
2.  藉由呼叫 **Database** 物件的 [**OpenView**](database-openview.md)方法，使用 SQL 字串起始查詢。
3.  在 [**記錄**](record-object.md)物件中設定查詢參數，並藉由呼叫 [**View**](view-object.md)物件的 [**execute**](view-execute.md)方法來執行資料庫查詢。 這會產生可提取或更新的結果。
4.  重複呼叫 [**View**](view-object.md)物件的 [**Fetch**](view-fetch.md)方法，以傳回 [**記錄**](record-object.md)物件。
5.  使用 [**View**](view-object.md)物件的 [**Modify**](view-modify.md)方法，更新 [**Fetch**](view-fetch.md)方法所取得之 [**記錄**](record-object.md)物件的資料庫資料列。
6.  藉由呼叫 [**View**](view-object.md)物件的 [**Close**](view-close.md)方法來釋放查詢和任何 unfetched 記錄。
7.  藉由呼叫 **database** 物件的 [**Commit**](database-commit.md)方法，保存任何資料庫更新。

## <a name="members"></a>成員

**資料庫** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**資料庫** 物件有這些方法。



| 方法                                                                    | 描述                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyTransform**](database-applytransform.md)                         | 將轉換套用至這個資料庫。<br/>                                                                                                                        |
| [**認可**](database-commit.md)                                         | 完成資料庫的持續性形式。<br/>                                                                                                                 |
| [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) | 建立並填入現有轉換檔案的摘要資訊資料流程。<br/>                                                                            |
| [**EnableUIPreview**](database-enableuipreview.md)                       | 藉由提供所需的支援來查看儲存在安裝程式資料庫中的使用者介面對話方塊，以加速撰寫對話方塊和公告欄。<br/> |
| [**匯出**](database-export.md)                                         | 將指定資料表中的結構和資料複製到文字封存檔案。<br/>                                                                                   |
| [**基表**](database-generatetransform.md)                   | 建立轉換。<br/>                                                                                                                                           |
| [**匯入**](database-import.md)                                         | 從文字保存檔案匯入資料庫資料表。<br/>                                                                                                             |
| [**合併**](database-merge.md)                                           | 合併參考資料庫與基底資料庫。<br/>                                                                                                          |
| [**OpenView**](database-openview.md)                                     | 傳回 [**View**](view-object.md)物件，代表 SQL 字串所指定的查詢。<br/>                                                                 |



 

### <a name="properties"></a>屬性

**資料庫** 物件具有這些屬性。



| 屬性                                                                               | 描述                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DatabaseState**](database-databasestate.md)<br/>                             | 傳回資料庫的持續性狀態。<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | 傳回包含資料表名稱和資料行名稱的 [**記錄**](record-object.md) 物件， (將主鍵組成) 。<br/>                        |
| [**SummaryInformation (資料庫物件)**](database-summaryinformation.md)<br/> | 傳回 [**SummaryInfo**](summaryinfo-object.md) 物件，這個物件可以用來檢查、更新和加入屬性至摘要資訊資料流程。<br/> |
| [**TablePersistent**](database-tablepersistent.md)<br/>                         | 傳回資料表的持續性狀態。<br/>                                                                                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows安裝程式腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




