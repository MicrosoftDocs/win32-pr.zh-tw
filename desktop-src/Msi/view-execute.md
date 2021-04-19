---
description: View 物件的 Execute 方法會使用問號標記來代表 SQL 語句中的參數。 如需詳細資訊，請參閱 SQL 語法。 這些參數的值會傳入做為參數記錄的對應欄位。
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exe刻意的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982510"
---
# <a name="viewexecute-method"></a>View.Exe刻意的方法

[**View**](view-object.md)物件的 **Execute** 方法會使用問號標記來代表 SQL 語句中的參數。 如需詳細資訊，請參閱 [SQL 語法](sql-syntax.md)。 這些參數的值會傳入做為參數記錄的對應欄位。

## <a name="syntax"></a>語法


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*記錄* 
</dt> <dd>

選擇性 [**記錄**](record-object.md) 物件，其中包含在 SQL 查詢中 (？ ) 取代參數標記的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

您必須在對 [**Fetch**](view-fetch.md) 方法的任何呼叫之前呼叫這個方法。

如果 SQL 查詢指定具有參數標記 (？ ) 的值，則必須提供包含所有取代值的記錄，而這些取代值必須與參數標記具有相同的順序和相同的資料類型。 當此方法與 INSERT 和 UPDATE 查詢搭配使用時，問號標記必須在所有非參數化的值之前。

例如，以下是有效的查詢：

更新 {資料表清單} 集合 {column} =？ ，{column} = {常數}

插入 {table} ( {column-list} ) 值 (？，{常數清單} ) 

不過，這些查詢無效：

更新 {資料表清單} 集合 {column} = {常數}，{column} =？

插入 {table} ( {column-list} ) 值 ( {常數清單} 中？ )

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




