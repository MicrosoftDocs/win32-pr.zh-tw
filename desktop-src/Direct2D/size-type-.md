---
title: '大小類型函式 (D2d1helper .h) '
description: 使用指定的資料類型，建立儲存其寬度和高度的大小結構。
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- 大小類型函式 Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf2bac3b43cf083d4f2d3588fed41d55380a435cc10c56cdfdb5cae1929d12c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292778"
---
# <a name="sizetype-function"></a>Size <Type> 函數

使用指定的資料類型，建立儲存其寬度和高度的大小結構。

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>範本參數



| 參數 | 描述                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| 類型      | 資料類型，用來儲存大小的寬度和高度。 可能的值為 FLOAT 和 UINT32。 |



 

## <a name="parameters"></a>參數



| 參數 | 描述        |
|-----------|--------------------|
| width     | 大小的寬度。  |
| 身高    | 大小的高度。 |



 

## <a name="return-value"></a>傳回值

包含指定之寬度和高度的大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、Windows vista （含 SP2），以及適用于 Windows Vista \[ desktop apps \| UWP 應用程式的平臺更新\]<br/>                          |
| 最低支援的伺服器<br/> | Windowsserver 2008 R2、Windows server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2d1helper。h</dt> </dl>                                                  |
| 程式庫<br/>                  | <dl> <dt>D2d1 .lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





