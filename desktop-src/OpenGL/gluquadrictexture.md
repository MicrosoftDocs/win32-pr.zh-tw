---
title: 'gluQuadricTexture 函式 (X.glu 隊) '
description: GluQuadricTexture 函數會指定是否要將 quadrics 設為紋理。
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluQuadricTexture 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbde88e0a878fd59e01ad0a450cf4cbe9831c4ad867c8029373586a8efe830eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937479"
---
# <a name="gluquadrictexture-function"></a>gluQuadricTexture 函式

**GluQuadricTexture** 函數會指定是否要將 quadrics 設為紋理。

## <a name="syntax"></a>語法


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*quadObject* 
</dt> <dd>

Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。

</dd> <dt>

*textureCoords* 
</dt> <dd>

指出是否要產生紋理座標的旗標。 下列是有效的值。



| 值                                                                                                                                          | 意義                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <dt>**GL \_ TRUE**</dt> </dl>    | 產生材質座標。<br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <dt>**GL \_ FALSE**</dt> </dl> | 不要產生材質座標。 這是預設值。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluQuadricTexture** 函式會指定是否要針對以 **quadObject** 轉譯的 quadrics 產生材質座標。

材質座標產生的方式取決於轉譯的特定 quadric。

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
</dt> </dl>

 

 





