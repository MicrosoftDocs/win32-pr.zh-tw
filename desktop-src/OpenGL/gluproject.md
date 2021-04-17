---
title: 'gluProject 函式 (X.glu 隊) '
description: GluProject 函式會將物件座標組應至視窗座標。
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluProject 函式 OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466180"
---
# <a name="gluproject-function"></a>gluProject 函式

**GluProject** 函式會將物件座標組應至視窗座標。

## <a name="syntax"></a>語法


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*objx* 
</dt> <dd>

X 物件座標。

</dd> <dt>

*objy* 
</dt> <dd>

Y 物件座標。

</dd> <dt>

*objz* 
</dt> <dd>

Z 物件座標。

</dd> <dt>

*modelMatrix* 
</dt> <dd>

目前的模型矩陣 (為 [**glGetDoublev**](glgetdoublev.md) 呼叫) 。

</dd> <dt>

*projMatrix* 
</dt> <dd>

目前的投射矩陣 (從 **glGetDoublev** 呼叫) 。

</dd> <dt>

*視窗* 
</dt> <dd>

目前的視口 (為來自 [**glGetIntegerv**](glgetintegerv.md) 呼叫) 。

</dd> <dt>

*winx* 
</dt> <dd>

計算的 x 視窗座標。

</dd> <dt>

*winy* 
</dt> <dd>

計算的 y 視窗座標。

</dd> <dt>

*winz* 
</dt> <dd>

計算的 z 視窗座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 GL \_ TRUE。

如果函式失敗，則傳回值為 GL \_ FALSE。

## <a name="remarks"></a>備註

**GluProject** 函式會使用 *modelMatrix*、 *projMatrix* 和 *視口*，將指定的物件座標轉換成視窗座標。 結果會儲存在 *winx*、 *winy* 和 *winz* 中。

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

[**glGetDoublev**](glgetdoublev.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluUnProject**](gluunproject.md)
</dt> </dl>

 

 





