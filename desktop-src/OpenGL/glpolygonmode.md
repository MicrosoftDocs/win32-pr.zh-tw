---
title: 'glPolygonMode 函式 (Gl) '
description: GlPolygonMode 函式會選取多邊形的點陣化模式。
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glPolygonMode 函式 OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966545"
---
# <a name="glpolygonmode-function"></a>glPolygonMode 函式

**GlPolygonMode** 函式會選取多邊形的點陣化模式。

## <a name="syntax"></a>語法


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*臉* 
</dt> <dd>

適用于 *模式* 的多邊形。 必須是上層 \_ 多邊形的 gl 正面、gl \_ 回背面的多邊形，或 \_ \_ \_ 適用于 FRONT 和 back 多邊形的 gl 正面和背面。

</dd> <dt>

*mode* 
</dt> <dd>

多邊形將會被柵格化的方式。 下列模式已定義，可在 *模式* 中指定。 預設值為 \_ front 和 back 多邊形的 GL 填滿。



| 值                                                                                                                                          | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**GL \_ 點**</dt> </dl> | 標示為界限邊緣開頭的多邊形頂點會繪製為點。 點屬性（例如 GL \_ 點 \_ 大小和 gl \_ 點）會 \_ 將點的點陣化順暢地控制。 GL 多邊形模式以外的多邊形點陣化屬性沒有 \_ \_ 任何作用。<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**GL \_ 線**</dt> </dl>    | 多邊形的邊界邊緣會繪製為直線線段。 它們會被視為行 stippling 的連接線區段;在區段之間不會重設 line stipple 計數器和模式 (請參閱 [**glLineStipple**](gllinestipple.md)) 。 生產線屬性（例如 GL \_ 線條 \_ 寬度和 gl \_ 線）會 \_ 順暢地控制線條的點陣化。 GL 多邊形模式以外的多邊形點陣化屬性沒有 \_ \_ 任何作用。<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**GL \_ 填滿**</dt> </dl>    | 多邊形的內部會填滿。 多邊形屬性（例如 GL \_ 多邊形 \_ STIPPLE 和 gl \_ 多邊形）會 \_ 順暢地控制多邊形的點陣化。<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *臉部* 或 *模式* 都不是接受的值。<br/>                                                                         |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlPolygonMode** 函式會控制要進行點陣的多邊形轉譯。 *臉部* 參數描述適用的多邊形 *模式*：正面的多邊形 (gl \_ front) 、背面的多邊形 (GL \_ 回) ，或 (gl \_ 前端 \_ 和 \_ 後端) 。 多邊形模式只會影響多邊形的最終柵格化。 尤其是，多邊形的頂點會發亮，並且在套用這些模式之前裁剪多邊形並可能會挑選。

若要繪製具有已填滿多邊形和空心多邊形的介面，請呼叫

**glPolygonMode** (gl \_ FRONT、gl \_ 行) ;

頂點會標示為界限，或具有邊緣旗標的 nonboundary。 邊緣旗標是在分解多邊形時由 OpenGL 在內部產生的，而且可以使用 [**glEdgeFlag**](gledgeflag-functions.md)明確設定。

下列函式會抓取 **glPolygonMode** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 多邊形 \_ 模式的 glGet

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

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





