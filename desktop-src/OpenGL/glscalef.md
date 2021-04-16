---
title: 'glScalef 函式 (Gl) '
description: 'GlScaled 和 glScalef 函數會將目前的矩陣乘以一般調整矩陣。 |glScalef 函式 (Gl) '
ms.assetid: bf039bbc-7669-4282-b629-71440b798cb1
keywords:
- glScalef 函式 OpenGL
topic_type:
- apiref
api_name:
- glScalef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eda183b763f22736370dd5c9ea13ca8793243e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104563309"
---
# <a name="glscalef-function"></a>glScalef 函式

[**GlScaled**](glscaled.md)和 **glScalef** 函數會將目前的矩陣乘以一般調整矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI glScalef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* 
</dt> <dd>

沿著 *x* 軸的縮放比例。

</dd> <dt>

*y* 
</dt> <dd>

沿著 *y* 軸的縮放因數。

</dd> <dt>

*Z* 
</dt> <dd>

沿著 *z* 軸的縮放因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlScalef** 函式會沿著 *x*、 *y* 和 *z* 軸產生一般調整。 三個引數會指出所需的縮放比例，以及三個軸的每一個。 產生的矩陣如下圖所示。

![此圖顯示沿著 x、y 和 Z 軸的縮放因數矩陣。](images/scale01.png)

目前的矩陣 (查看 [**glMatrixMode**](glmatrixmode.md)) 乘以此尺規矩陣，並將產品取代為目前的矩陣。 也就是說，如果 M 是目前的矩陣，而 S 是尺規矩陣，則 M 會取代為 M S。

如果矩陣模式是 GL \_ 模型或 gl \_ 投射，則會呼叫 **glScalef** 之後繪製的所有物件。 使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) 來儲存及還原未縮放的座標系統。

如果將1.0 以外的縮放因數套用至模型矩陣且已啟用光源，則應該也要啟用法線的自動正規化 ([**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) ，並將引數 GL \_ 標準化) 。

下列函式會取出與 **glScalef** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 模型 \_ 矩陣的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 投射 \_ 矩陣的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 材質 \_ 矩陣的 glGet

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotated**](glrotated.md)
</dt> <dt>

[**glRotatef**](glrotatef.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





