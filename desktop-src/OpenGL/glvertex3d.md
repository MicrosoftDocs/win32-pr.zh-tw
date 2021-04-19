---
title: 'glVertex3d 函式 (Gl) '
description: '指定頂點。 |glVertex3d 函式 (Gl) '
ms.assetid: 531a552d-7979-4994-ad28-73c2d3987bae
keywords:
- glVertex3d 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608ab02bf2cd41b7f2ffcc8fa3fe8cb2dea0ca89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988150"
---
# <a name="glvertex3d-function"></a>glVertex3d 函式

指定頂點。

## <a name="syntax"></a>語法


```C++
void WINAPI glVertex3d(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* 
</dt> <dd>

指定頂點的 x 座標。

</dd> <dt>

*y* 
</dt> <dd>

指定頂點的 y 座標。

</dd> <dt>

*Z* 
</dt> <dd>

指定頂點的 z 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

GlVertex 函數命令會在 [**glBegin**](glbegin.md) / [**glEnd**](glend.md)配對中用來指定點、線條和多邊形頂點。 當呼叫 glVertex 時，目前的色彩、標準和材質座標會與頂點相關聯。 當僅指定 *x* 和 *y* 時， *z* 的預設值為0.0， *w* 預設值為1.0。 當指定 *x*、 *y* 和 *z* 時， *w* 預設為1.0。 在 **glBegin** / **glEnd** 配對之外叫用 glVertex 會導致未定義的行為。

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glRect**](glrect-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> </dl>

 

 





