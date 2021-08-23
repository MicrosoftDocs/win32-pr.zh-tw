---
title: 'gluPerspective 函式 (X.glu 隊) '
description: GluPerspective 函式會設定透視圖投影矩陣。
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- gluPerspective 函式 OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973040fc9d9f23e6cfba5e30ceea89a1c13cfbaab0071cc7905080cfcdf60f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061586"
---
# <a name="gluperspective-function"></a>gluPerspective 函式

**GluPerspective** 函式會設定透視圖投影矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fovy* 
</dt> <dd>

Y 方向的視圖角度（以度為單位）的欄位。

</dd> <dt>

*aspect* 
</dt> <dd>

以 x 方向決定視圖欄位的外觀比例。 外觀比例是 *x* (寬度) 至 *y* (高度) 的比率。

</dd> <dt>

*zNear* 
</dt> <dd>

從檢視器到接近裁剪平面的距離 (一律為正) 。

</dd> <dt>

*zFar* 
</dt> <dd>

從檢視器到最遠裁剪平面的距離 (一律為正) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluPerspective** 函式會將視圖分割指定為全局座標系統。 一般而言， **gluPerspective** 中的長寬比應該符合相關聯之區的外觀比例。 例如， *外觀* = 2.0 表示檢視器的角度為 *x* 中的寬度兩倍，如同 *y* 一樣。 如果圖區的寬度為高度，則會顯示影像，而不會失真。

**GluPerspective** 所產生的矩陣會乘以目前的矩陣，就像是使用產生的矩陣來呼叫 [**glMultMatrix**](glmultmatrix.md)一樣。 若要改為將透視圖矩陣載入至目前的矩陣堆疊，請在呼叫 **gluPerspective** 之前呼叫 [**glLoadIdentity**](glloadidentity.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>X.glu 隊。h</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Glu32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**gluOrtho2D**](gluortho2d.md)
</dt> </dl>

 

 





