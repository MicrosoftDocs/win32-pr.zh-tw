---
title: 'gluUnProject 函式 (X.glu 隊) '
description: GluUnProject 函式會將視窗座標組應到物件座標。
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- gluUnProject 函式 OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969621"
---
# <a name="gluunproject-function"></a>gluUnProject 函式

**GluUnProject** 函式會將視窗座標組應到物件座標。

## <a name="syntax"></a>語法


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*winx* 
</dt> <dd>

要對應的 x 視窗座標。

</dd> <dt>

*winy* 
</dt> <dd>

要對應的 y 視窗座標。

</dd> <dt>

*winz* 
</dt> <dd>

要對應的 z 視窗座標。

</dd> <dt>

*modelMatrix* 
</dt> <dd>

模型矩陣 (為 [**glGetDoublev**](glgetdoublev.md) 呼叫) 。

</dd> <dt>

*projMatrix* 
</dt> <dd>

投射矩陣 (從 **glGetDoublev** 呼叫) 。

</dd> <dt>

*視窗* 
</dt> <dd>

從 [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 呼叫)  (的區。

</dd> <dt>

*objx* 
</dt> <dd>

計算的 x 物件座標。

</dd> <dt>

*objy* 
</dt> <dd>

計算的 y 物件座標。

</dd> <dt>

*objz* 
</dt> <dd>

計算的 z 物件座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 GL \_ TRUE。

如果函式失敗，則傳回值為 GL \_ FALSE。

## <a name="remarks"></a>備註

**GluUnProject** 函式會使用 *modelMatrix*、 *projMatrix* 和 *視窗* 圖將指定的視窗座標組應到物件座標。 結果會儲存在 *objx*、 *objy* 和 *objz* 中。

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetDoublev**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluProject**](gluproject.md)
</dt> </dl>

 

 





