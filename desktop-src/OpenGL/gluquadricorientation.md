---
title: 'gluQuadricOrientation 函式 (X.glu 隊) '
description: GluQuadricOrientation 函式會針對 quadrics 指定內部或外部方向。
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- gluQuadricOrientation 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa02c3b6d207cbcc2bf487f51c0e96dc2f2dd98748edc81efb58ac957fac4ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937624"
---
# <a name="gluquadricorientation-function"></a>gluQuadricOrientation 函式

**GluQuadricOrientation** 函式會針對 quadrics 指定內部或外部方向。

## <a name="syntax"></a>語法


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*quadObject* 
</dt> <dd>

Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。

</dd> <dt>

*取向* 
</dt> <dd>

所需的方向。 下列是有效的值。



| 值                                                                                                                                                   | 意義                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**\_外部 X.GLU 隊**</dt> </dl> | 以指向外的法線繪製 quadrics。 這是預設值。<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**X.GLU 隊 \_ 內部**</dt> </dl>    | 繪製具有朝內 quadrics 的法線。<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluQuadricOrientation** 函式會指定以 **quadObject** 轉譯 quadrics 所需的方向類型。 向外和向內的解讀取決於所繪製的 quadric。

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





