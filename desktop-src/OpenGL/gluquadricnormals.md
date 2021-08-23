---
title: 'gluQuadricNormals 函式 (X.glu 隊) '
description: GluQuadricNormals 函式會指定要針對 quadrics 使用何種法線。
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- gluQuadricNormals 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d535a90f21b88b26c3afd245b2f6350a443fd8915a4cd806df79236484c36d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554178"
---
# <a name="gluquadricnormals-function"></a>gluQuadricNormals 函式

**GluQuadricNormals** 函式會指定要針對 quadrics 使用何種法線。

## <a name="syntax"></a>語法


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*quadObject* 
</dt> <dd>

Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。

</dd> <dt>

*法線* 
</dt> <dd>

所需的法線類型。 下列是有效的值。



| 值                                                                                                                                                | 意義                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <dt>**X.GLU 隊 \_ 無**</dt> </dl>       | 不會產生任何法線。<br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <dt>**X.GLU 隊 \_ 平面**</dt> </dl>       | Quadric 的每個 facet 都會產生一個正常情況。<br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <dt>**X.GLU 隊 \_ 順暢**</dt> </dl> | Quadric 的每個頂點都會產生一個正常情況。 這是預設值。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluQuadricNormals** 函式會指定要針對以 **quadObject** 轉譯的 quadrics 使用何種法線。

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

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





