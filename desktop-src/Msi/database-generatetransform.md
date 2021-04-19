---
description: 資料庫物件的轉換方法會建立一個轉換，在套用至物件資料庫時，會產生參考資料庫。 轉換會儲存在儲存物件中。
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: 資料庫. 此方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995265"
---
# <a name="databasegeneratetransform-method"></a>資料庫. 此方法

[**資料庫**](database-object.md)物件的轉換 **方法會** 建立一個 [*轉換*](t-gly.md)，在套用至物件資料庫時，會產生參考資料庫。 轉換會儲存在儲存物件中。

如果要在安裝期間套用轉換，您必須使用 [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) 方法來填入摘要資訊串流。

## <a name="syntax"></a>語法


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*reference* 
</dt> <dd>

不包含變更的必要資料庫。

</dd> <dt>

*儲存體* 
</dt> <dd>

產生之轉換檔案的名稱。 這是選擇性的。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

轉換可以將非主鍵資料行加入至資料表的結尾。 無法建立轉換，將主鍵資料行加入至資料表。 無法建立變更資料行順序、名稱或定義的轉換。

這個方法會傳回布林值。 如果產生轉換，則會傳回 TRUE。 如果未產生轉換，則會傳回 FALSE，因為兩個資料庫之間沒有任何差異。 如果方法失敗，則會產生錯誤。

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**資料庫**](database-object.md)
</dt> <dt>

[資料庫轉換](database-transforms.md)
</dt> </dl>

 

 




