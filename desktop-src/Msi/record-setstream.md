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
ms.openlocfilehash: de443f2d6802fb74e4b0f05b90ca8d3b3f97e328991fde50ec05ff37c203943c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626968"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




