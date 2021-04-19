---
description: View 物件的 Modify 方法會使用 Fetch 方法取得的修改記錄物件來修改資料庫資料列。
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: View. Modify 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Modify
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4dc97f2e3b5f85d472cfcbfad6017ce4e051e4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999264"
---
# <a name="viewmodify-method"></a>View. Modify 方法

[**View**](view-object.md)物件的 **Modify** 方法會使用 [**Fetch**](view-fetch.md)方法取得的修改 [**記錄**](record-object.md)物件來修改資料庫資料列。

## <a name="syntax"></a>語法


```JScript
View.Modify(
  action,
  record
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*action* 
</dt> <dd>

需要在資料庫資料列上執行的動作。 這是下表所示的動作之一。



| 動作名稱                                                                                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiViewModifySeek**</dt> <dt>– 1</dt> </dl>                                            | 重新整理提供記錄中的資訊，而不變更結果集中的位置，而不會影響後續的提取作業。 然後，記錄可以用於後續的更新、刪除和重新整理。 資料表的所有主鍵資料行都必須在查詢中，而且記錄至少必須有與查詢相同的欄位數目。Seek 無法與 multitable 查詢搭配使用。 請參閱備註。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiViewModifyRefresh**</dt> <dt>0</dt> </dl>                                 | 重新整理記錄中的資訊。 必須先呼叫具有相同記錄的 [**Fetch**](view-fetch.md) 方法。 刪除的資料列失敗。 適用于讀寫和唯讀記錄。<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiViewModifyInsert**</dt> <dt>1</dt> </dl>                                     | 插入記錄。 如果存在具有相同主鍵的資料列，則會失敗。 使用唯讀資料庫失敗。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiViewModifyUpdate**</dt> <dt>2</dt> </dl>                                     | 更新現有的記錄。 僅限非主要索引鍵。 必須先呼叫具有相同記錄的 [**Fetch**](view-fetch.md) 方法。 失敗並刪除記錄。 只適用于讀寫記錄。<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiViewModifyAssign**</dt> <dt>3</dt> </dl>                                     | 將資料指標中的目前資料寫入至資料表資料列。 如果主鍵符合現有的資料列，則會更新記錄，如果它們不相符，則會插入。 使用唯讀資料庫失敗。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiViewModifyReplace**</dt> <dt>4</dt> </dl>                                 | 更新或刪除記錄，並將記錄插入資料表中。 必須先呼叫具有相同記錄的 [**Fetch**](view-fetch.md) 方法。 如果主鍵未變更，則會更新記錄。 刪除舊資料列，並在主要索引鍵變更時插入新的。 使用唯讀資料庫失敗。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiViewModifyMerge**</dt> <dt>5</dt> </dl>                                         | 在資料表中插入或驗證記錄。 如果主鍵不符合任何資料列，則會插入，並驗證是否有相符的。 如果記錄與資料表中的資料不相符，則會失敗。 如果有重複索引鍵不相同的記錄，則會失敗。 只適用于讀寫記錄。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiViewModifyDelete**</dt> <dt>6</dt> </dl>                                     | 從資料表中移除資料列。 必須先呼叫具有相同記錄的 [**Fetch**](view-fetch.md) 方法。 如果資料列已刪除，則會失敗。 只適用于讀寫記錄。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiViewModifyInsertTemporary**</dt> <dt>7</dt> </dl> | 插入暫存記錄。 這項資訊不是持續性的。 如果存在具有相同主鍵的資料列，則會失敗。 只適用于讀寫記錄。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiViewModifyValidate**</dt> <dt>8</dt> </dl>                             | 驗證記錄。 不會跨聯結進行驗證。 必須先呼叫具有相同記錄的 [**Fetch**](view-fetch.md) 方法。 使用 [**GetError**](view-geterror.md) 方法取得驗證錯誤。 適用于讀寫和唯讀記錄。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiViewModifyValidateNew**</dt> <dt>9</dt> </dl>                 | 驗證新的記錄。 不會跨聯結進行驗證。 檢查是否有重複的索引鍵。 藉由呼叫 [**GetError**](view-geterror.md) 方法來取得驗證錯誤。 需要使用修改值來呼叫 [**MsiDatabase。**](database-openview.md) 適用于讀寫和唯讀記錄。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiViewModifyValidateField**</dt> <dt>10</dt> </dl>        | 驗證提取或新記錄的欄位。 可以驗證一或多個不完整記錄的欄位。 藉由呼叫 [**GetError**](view-geterror.md) 方法來取得驗證錯誤。 適用于讀寫和唯讀記錄。 此模式無法與包含聯結的視圖一起使用。<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiViewModifyValidateDelete**</dt> <dt>11</dt> </dl>    | 驗證稍後將刪除的記錄。 必須先呼叫具有相同記錄的 [**Fetch**](view-fetch.md) 方法。 如果另一個資料列參考此資料列的主鍵，則會失敗。 驗證不會在屬性或字串中檢查此資料列的主鍵是否存在。 不會檢查資料行是否為多個資料表的外鍵。 藉由呼叫 [**GetError**](view-geterror.md) 方法來取得驗證錯誤。 適用于讀寫和唯讀記錄。 此模式無法與包含聯結的視圖一起使用。<br/> |



 

</dd> <dt>

*記錄* 
</dt> <dd>

必要。 [**Fetch**](view-fetch.md)方法透過修改過的欄位資料所取得的 [**記錄**](record-object.md)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

您必須在 [**Execute**](view-execute.md) 方法之後呼叫這個方法。

若要執行任何 SQL 語句，您必須建立一個 view。 但是，不會建立結果集的視圖（例如 CREATE TABLE 或 INSERT INTO）無法與 **Modify** 方法搭配使用，以透過視圖來更新資料表。

**Modify** 方法的 MsiViewModifyValidate、MsiViewModifyValidateNew、MsiViewModifyValidateField 和 msiViewModifyValidateDelete 值不會執行實際的更新;它們可確保記錄中的資料是有效的。 若要使用這些動作，資料庫必須包含[ \_ 驗證資料表](-validation-table.md)。

您無法從某個資料庫提取包含二進位資料的記錄，然後使用該記錄，將資料插入至完全不同的資料庫。 若要將二進位資料從某個資料庫移到另一個資料庫，您應該將資料匯出至檔案，然後使用 [**Record**](record-object.md)物件的 [**SetStream**](record-setstream.md)方法，將資料匯入至新的資料庫。 這可確保每個資料庫都有自己的二進位資料複本。

> [!Note]  
> 自訂動作只能加入、修改或移除資料庫中的暫存資料列、資料行或資料表。 自訂動作無法修改資料庫中的持續性資料，例如儲存在磁片上的資料庫中的資料。 如需詳細資訊，請參閱 [從自訂動作內部存取目前的安裝程式會話](accessing-the-current-installer-session-from-inside-a-custom-action.md)。

 

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




