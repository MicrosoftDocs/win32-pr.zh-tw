---
title: 'glRotatef 函式 (Gl) '
description: GlRotatef 函式會將目前的矩陣乘以旋轉矩陣。
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- glRotatef 函式 OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f466ca73a826d9a12f97093c90c41cd1c753b01f25853096dd3f3219628654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937928"
---
# <a name="glrotatef-function"></a>glRotatef 函式

**GlRotatef** 函式會將目前的矩陣乘以旋轉矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*角度* 
</dt> <dd>

旋轉的角度（以度為單位）。

</dd> <dt>

*x* 
</dt> <dd>

向量的 *x* 座標。

</dd> <dt>

*y* 
</dt> <dd>

向量的 *y* 座標。

</dd> <dt>

*z* 
</dt> <dd>

向量的 *z* 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlRotatef** 函式會計算矩陣，此矩陣會執行從原點到 (*x*、 *y*、 *z*) 點之向量的旋轉 *角度* 度數。

目前的矩陣 (查看 [**glMatrixMode**](glmatrixmode.md)) 乘以這個旋轉矩陣，並將產品取代為目前的矩陣。 也就是說，如果 M 是目前的矩陣，而 R 是轉譯矩陣，則 M 會取代為 M R。

如果矩陣模式是 GL \_ 模型或 gl \_ 投射，則會呼叫 **glRotatef** 之後繪製的所有物件。 使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) 來儲存及還原未旋轉的座標系統。

下列函式會取出與 **glRotatef** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 轉譯 \_ 模式的 glGet

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

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





