---
description: 資料庫物件的 ApplyTransform 方法會將轉換套用至這個資料庫。
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: ApplyTransform 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9c3424dab82b6981af033b40b33481937fd7c36d3c00dcf3ddfcba5f13f56ec7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289618"
---
# <a name="databaseapplytransform-method"></a>ApplyTransform 方法

[**資料庫**](database-object.md)物件的 **ApplyTransform** 方法會將轉換套用至這個資料庫。

## <a name="syntax"></a>語法


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*儲存體* 
</dt> <dd>

要套用之轉換檔的路徑。 此為必要參數。

</dd> <dt>

*errorConditions* 
</dt> <dd>

指定要隱藏的錯誤條件。 指定為下列整數值的組合。



| 錯誤狀況                                                                                                                                                                                                                                                                                                                                                  | 意義                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt> </dl>                                 | 加入已經存在的資料列。<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt> </dl>         | 刪除不存在的資料列。<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt> </dl>                         | 加入已經存在的資料表。<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt> </dl> | 刪除不存在的資料表。<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt> </dl>         | 更新不存在的資料列。<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt> </dl>                                 | 轉換和資料庫字碼頁不相符，且沒有中性的字碼頁。<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt> </dl>                                     | 建立暫存的[ \_ TransformView 資料表](-transformview-table.md)。<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**ApplyTransform** 方法會延遲轉換資料表，直到最後一個可能的時間為止。 **ApplyTransform** 中所採取的步驟，是立即轉換資料庫的資料表和資料行目錄。 資料表和資料行目錄會根據新增或刪除的資料表，以及要加入的資料行來更新 () 不允許刪除資料行。 如果資料表目前已載入記憶體，且需要轉換，則會轉換。 否則，資料表狀態會設定為，需要進行轉換，以便在載入資料表時或認可資料庫時，套用轉換。 此實例中的轉換表示會新增、刪除或更新資料表的實際 (資料列) 資料。

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**資料庫**](database-object.md)
</dt> <dt>

[資料庫轉換](database-transforms.md)
</dt> </dl>

 

 




