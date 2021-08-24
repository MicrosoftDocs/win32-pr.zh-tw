---
title: 'Point2 類型函式 (D2d1helper .h) '
description: 使用指定的資料類型，建立儲存其座標的點。
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Point2 型別函數 Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d925cc5676e6f0c9a8fb27a3ba2a12591ee87a5a72d5937e365fa57179e47ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160374"
---
# <a name="point2type-function"></a>Point2 <Type> 函式

使用指定的資料類型，建立儲存其座標的點。

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a>範本參數



| 參數 | 描述                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| 類型      | 用來儲存點之 x 座標和 y 座標的資料型別。 可能的值為 FLOAT 和 UINT32。 |



 

## <a name="parameters"></a>參數



| 參數 | 描述                    |
|-----------|--------------------------------|
| x         | 點的 X 座標。 |
| y         | 點的 Y 座標。 |



 

## <a name="return-value"></a>傳回值

包含指定之 x 座標和 y 座標的點。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、Windows vista （含 SP2），以及適用于 Windows Vista \[ desktop apps \| UWP 應用程式的平臺更新\]<br/>                          |
| 最低支援的伺服器<br/> | Windowsserver 2008 R2、Windows server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2d1helper。h</dt> </dl>                                                  |
| 程式庫<br/>                  | <dl> <dt>D2d1 .lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





