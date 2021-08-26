---
title: 'Rect 類型函數 (D2d1helper .h) '
description: 使用指定的資料類型，建立儲存其座標的矩形結構。
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Rect 型別函式 Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5f56fd9cbcfd576a441d9199e7ec1114cfb9f3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884482"
---
# <a name="rectlttypegt-function"></a>Rect &lt; 類型 &gt; 函數

使用指定的資料類型，建立儲存其座標的矩形結構。

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a>範本參數



| 參數 | 描述                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| 類型      | 用來儲存矩形維度的資料類型。 可能的值為 **FLOAT** 和 **UINT32**。 |



 

## <a name="parameters"></a>參數



| 參數 | 描述                                             |
|-----------|---------------------------------------------------------|
| left      | 矩形左上角的 x 座標。  |
| top       | 矩形左上角的 y 座標。  |
| 向右     | 矩形右下角的 x 座標。 |
| 下    | 矩形右下角的 y 座標。 |



 

## <a name="return-value"></a>傳回值

包含指定座標的矩形結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、Windows vista （含 SP2），以及適用于 Windows Vista \[ desktop apps \| UWP 應用程式的平臺更新\]<br/>                          |
| 最低支援的伺服器<br/> | Windowsserver 2008 R2、Windows server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2d1helper。h</dt> </dl>                                                  |
| 程式庫<br/>                  | <dl> <dt>D2d1 .lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





