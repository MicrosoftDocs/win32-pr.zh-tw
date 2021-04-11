---
title: 'gluQuadricDrawStyle 函式 (X.glu 隊) '
description: GluQuadricDrawStyle 函式會指定 quadrics 所需的繪製樣式。
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluQuadricDrawStyle 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934757"
---
# <a name="gluquadricdrawstyle-function"></a>gluQuadricDrawStyle 函式

**GluQuadricDrawStyle** 函式會指定 quadrics 所需的繪製樣式。

## <a name="syntax"></a>語法


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*quadObject* 
</dt> <dd>

Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。

</dd> <dt>

*drawStyle* 
</dt> <dd>

所需的繪製樣式。 下列是有效的值。



| 值                                                                                                                                                            | 意義                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**X.GLU 隊 \_ 填滿**</dt> </dl>                   | Quadrics 是以多邊形基本專案轉譯。 多邊形是以逆時針方式繪製，與 [**gluQuadricOrientation**](gluquadricorientation.md)) 所定義的法線 (有關。<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**X.GLU 隊 \_ 行**</dt> </dl>                   | Quadrics 會轉譯為一組線。<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**X.GLU 隊 \_ 側面**</dt> </dl> | Quadrics 會轉譯為一組線，不同之處在于不會繪製分隔共面的臉部的邊緣。<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**X.GLU 隊 \_ 點**</dt> </dl>                | Quadrics 會轉譯為一組點。<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluQuadricDrawStyle** 函式會指定使用 **quadObject** 轉譯之 quadrics 的繪製樣式。

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

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





