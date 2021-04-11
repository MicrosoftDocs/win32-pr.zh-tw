---
title: 'glTranslatef 函式 (Gl) '
description: GlTranslatef 函式會將目前的矩陣與轉譯矩陣相乘。
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- glTranslatef 函式 OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5b52c3890b70ecb931211af1788afe2b8e6ad4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103853272"
---
# <a name="gltranslatef-function"></a>glTranslatef 函式

[**GlTranslatef**](gltranslate.md)函式會將目前的矩陣與轉譯矩陣相乘。

## <a name="syntax"></a>語法


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* 
</dt> <dd>

平移向量的 *x* 座標。

</dd> <dt>

*y* 
</dt> <dd>

平移向量的 *y* 座標。

</dd> <dt>

*Z* 
</dt> <dd>

平移向量的 *z* 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GlTranslatef** 函式會產生由 (*x*、 *y*、 *z*) 指定的平移。 轉譯向量用來計算4x4 平移矩陣：

![顯示 x、y、z 所指定之4x4 平移矩陣的圖表。](images/trans01.png)

目前的矩陣 (查看 [**glMatrixMode**](glmatrixmode.md)) 乘以此平移矩陣，並將產品取代為目前的矩陣。 也就是說，如果 M 是目前的矩陣，而 T 是轉譯矩陣，則 M 會取代為 M T。

如果矩陣模式是 GL \_ 模型或 gl \_ 投射，則會轉譯 **glTranslatef** 之後繪製的所有物件。 使用 [**glPushMatrix**](glpushmatrix.md) 和 **glPopMatrix** 來儲存及還原未轉譯的座標系統。

下列函式會取出 [**glTranslated**](gltranslate.md) 和 **glTranslatef** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet

具有引數 GL \_ 模型 \_ 矩陣的 glGet

具有引數 GL \_ 投射 \_ 矩陣的 glGet

具有引數 GL \_ 材質 \_ 矩陣的 glGet

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

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> </dl>

 

 





