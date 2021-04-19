---
description: View 物件的 ColumnInfo 屬性會傳回包含結果集中每個資料行之要求資訊的記錄物件。
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: ColumnInfo 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994253"
---
# <a name="viewcolumninfo-property"></a>ColumnInfo 屬性

[**View**](view-object.md)物件的 **ColumnInfo** 屬性會傳回包含結果集中每個資料行之要求資訊的 [**記錄**](record-object.md)物件。 可以要求資料行名稱或資料行定義。 選取清單中提供的常數沒有名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>屬性值

每個資料行所需的必要資訊。



| 參數名稱                                                                                                                                                                                                                                                          | 意義                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | 傳回結果集內所有非常數資料行的名稱。<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | 傳回結果集內所有非常數資料行的類型。<br/> |



 

## <a name="remarks"></a>備註

**ColumnInfo** 屬性所傳回的資料行描述採用資料 [行定義格式](column-definition-format.md)所述的格式。 每個資料行都是由對應的 [記錄] 欄位中的字串所描述。 定義字串是由代表資料類型的單一字母，以及資料行的寬度 (（如果適用的話）或其他位元組) 。 寬度為零會指定未系結的寬度 (長文字欄位和資料流程) 。 大寫字母表示資料行中允許 Null 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




