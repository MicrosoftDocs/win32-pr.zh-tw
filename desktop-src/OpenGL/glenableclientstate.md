---
title: 'glEnableClientState 函式 (Gl) '
description: 'GlEnableClientState 和 glDisableClientState 函數會分別啟用和停用陣列。 |glEnableClientState 函式 (Gl) '
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- glEnableClientState 函式 OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1ebb9b0278ca6a696183da54c40a6463880a24f6a29a7cca3c2fdd9dd1213a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360415"
---
# <a name="glenableclientstate-function"></a>glEnableClientState 函式

**GlEnableClientState** 和 [**glDisableClientState**](gldisableclientstate.md)函數會分別啟用和停用陣列。

## <a name="syntax"></a>語法


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*array* 
</dt> <dd>

您要啟用或停用之陣列的符號常數。 此參數可以採用下列其中一個值。



| 值                                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**GL \_ 色彩 \_ 陣列**</dt> </dl>                          | 如果啟用，請使用色彩陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。<br/> 另請參閱 [**glColorPointer**](glcolorpointer.md)。<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**GL \_ EDGE \_ 旗標 \_ 陣列**</dt> </dl>             | 如果啟用，請使用邊緣旗標陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。<br/> 另請參閱 [**glEdgeFlagPointer**](gledgeflagpointer.md)。<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL \_ 索引 \_ 陣列**</dt> </dl>                          | 如果啟用，請使用索引陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。<br/> 另請參閱 [**glIndexPointer**](glindexpointer.md)。<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**GL \_ 標準 \_ 陣列**</dt> </dl>                       | 如果啟用，請使用一般陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。<br/> 另請參閱 [**glNormalPointer**](glnormalpointer.md)。<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**GL \_ 紋理 \_ COORD \_ 陣列**</dt> </dl> | 若已啟用，請使用紋理座標陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。<br/> 另請參閱 [**glTexCoordPointer**](gltexcoordpointer.md)。<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**GL \_ 頂點 \_ 陣列**</dt> </dl>                       | 如果啟用，請使用頂點陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。<br/> 另請參閱 [**glVertexPointer**](glvertexpointer.md)。<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                             | 意義                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl> | *陣列* 不是可接受的值。<br/> |



## <a name="remarks"></a>備註

**GlEnableClientState** 和 **glDisableClientState** 函式會啟用和停用各種個別的陣列。 使用 [**glIsEnabled**](glisenabled.md) 或 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 來判斷任何功能目前的設定。

在對 [**glBegin**](glbegin.md)的呼叫和 [**glEnd**](glend.md)的對應呼叫之間呼叫 **glEnableClientState** 和 **glDisableClientState** 可能會造成錯誤。 如果未產生任何錯誤，則行為是未定義的。

> [!Note]  
> **GlEnableClientState** 和 **glDisableClientState** 函式僅適用于 OpenGL 1.1 版或更新版本。

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





