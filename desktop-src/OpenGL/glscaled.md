---
title: 'glScaled 函式 (Gl) '
description: 'GlScaled 和 glScalef 函數會將目前的矩陣乘以一般調整矩陣。 |glScaled 函式 (Gl) '
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- glScaled 函式 OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46742831eaa0a014de0f6ae50271b28c922893133588758119cbf5bff7ba628b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491788"
---
# <a name="glscaled-function"></a>glScaled 函式

**GlScaled** 和 [**glScalef**](glscalef.md)函數會將目前的矩陣乘以一般調整矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
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

*z* 
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

**GlScaled** 函式會沿著 *x*、 *y* 和 *z* 軸產生一般調整。 三個引數會指出所需的縮放比例，以及三個軸的每一個。 產生的矩陣是

![此圖顯示沿著 x、y 和 Z 軸的縮放因數矩陣。](images/scale01.png)

目前的矩陣 (查看 [**glMatrixMode**](glmatrixmode.md)) 乘以此尺規矩陣，並將產品取代為目前的矩陣。 也就是說，如果 M 是目前的矩陣，而 S 是尺規矩陣，則 M 會取代為 M S。

如果矩陣模式是 GL \_ 模型或 gl \_ 投射，則會呼叫 **glScaled** 之後繪製的所有物件。 使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) 來儲存及還原未縮放的座標系統。

如果將1.0 以外的縮放因數套用至模型矩陣且已啟用光源，則應該也要啟用法線的自動正規化 ([**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) ，並將引數 GL \_ 標準化) 。

下列函式會取出與 **glScaled** 相關的資訊：

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

 

 





