---
description: Record 物件的 SetStream 方法會將指定之檔案的內容複寫到指定的記錄欄位中，做為資料流程資料。 資料流程資料無法插入暫存欄位。
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: SetStream 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987880"
---
# <a name="recordsetstream-method"></a>SetStream 方法

[**Record**](record-object.md)物件的 **SetStream** 方法會將指定之檔案的內容複寫到指定的記錄欄位中，做為資料流程資料。 資料流程資料無法插入暫存欄位。

## <a name="syntax"></a>語法


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*領域* 
</dt> <dd>

記錄中值的必要欄位編號（以1為基礎）。

</dd> <dt>

*filePath* 
</dt> <dd>

要複製之檔案的位置。 不會執行任何類型的轉譯。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




