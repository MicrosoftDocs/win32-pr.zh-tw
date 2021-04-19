---
description: 資料庫物件的 Merge 方法會合並參考資料庫與基底資料庫。
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994148"
---
# <a name="databasemerge-method"></a>Database. Merge 方法

[**資料庫**](database-object.md)物件的 **Merge** 方法會合並參考資料庫與基底資料庫。

## <a name="syntax"></a>語法


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*reference* 
</dt> <dd>

要合併到資料庫的必要 [**資料庫**](database-object.md) 物件。

</dd> <dt>

*errorTable* 
</dt> <dd>

資料表的選擇性名稱，包含包含合併衝突之資料表的名稱、資料表中的衝突資料列數目，以及包含合併衝突之資料表的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)函式和 [**資料庫**](database-object.md)物件的 **merge** 方法不能用來合併安裝封裝內所含的模組。 它們不應該用來將 [合併模組](merge-modules.md) 合併成 Windows Installer 套件。 若要在安裝套件中包含合併模組，安裝套件的作者應遵循套用 [合併模組](applying-merge-modules.md) 主題中所述的指導方針。

**Merge** 方法不會將內嵌的封 [包](cabinet-files.md)檔或 [內嵌的轉換](embedded-transforms.md)從參考資料庫複製到目標資料庫。 [二進位資料表](binary-table.md)或[圖示資料表](icon-table.md)中所列的內嵌資料串流，會從參考資料庫複製到目標資料庫。 內嵌于參考資料庫中的儲存體不會複製到目標資料庫。

如果未提供任何資料表，則一般錯誤訊息會提供包含合併衝突的資料表數目。 可以傳入任何資料表，但所有其他資料行都必須是可為 null，因為如果資料行不可為 null，則更新 [錯誤資料表](error-table.md) 的作業會失敗。 您也可以傳入新建立的資料表，因為當找到合併衝突時， **merge** 方法會自動建立所使用的資料行。 有兩個數據行用來呈現合併衝突。 第一個資料行是資料表名稱和主鍵資料行。 第二個數據行是該資料表中有合併失敗的資料列數目。

如果兩個資料庫中相同名稱的資料表不符合主鍵的數目、資料行類型、資料行數目或資料行名稱， **合併** 方法將會失敗，並張貼一則錯誤訊息，指出發生了什麼事。

若要保留錯誤資料表，錯誤處理常式必須認可錯誤資料表所屬的資料庫。 不過，您應該在使用第三個數據行來取得發生合併衝突之資料表的參考之後，進行這種認可。

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




