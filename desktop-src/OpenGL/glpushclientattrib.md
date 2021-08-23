---
title: 'glPushClientAttrib 函式 (Gl) '
description: 'GlPushClientAttrib 和 glPopClientAttrib 函式會在用戶端屬性堆疊上儲存和還原用戶端狀態變數的群組。 |glPushClientAttrib 函式 (Gl) '
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- glPushClientAttrib 函式 OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f378ec3ff735ed916567ea91e211a1d8a1685580b1f1ea80d448b92203b39a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492608"
---
# <a name="glpushclientattrib-function"></a>glPushClientAttrib 函式

**GlPushClientAttrib** 和 [**glPopClientAttrib**](glpopclientattrib.md)函式會在用戶端屬性堆疊上儲存和還原用戶端狀態變數的群組。

## <a name="syntax"></a>語法


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*面具* 
</dt> <dd>

表示要儲存哪些屬性的遮罩。 以下是符號遮罩常數及其相關聯的 OpenGL 用戶端狀態。



| 值                                                                                                                                                                                                                                            | 意義                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <dt>**GL \_ 用戶端 \_ 圖元 \_ 存放區 \_ 位**</dt> </dl>                                             | 圖元儲存模式屬性。<br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <dt>**GL \_ 用戶端 \_ 頂點 \_ 陣列 \_ 位**</dt> </dl>                                          | 頂點陣列屬性。<br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <dt>**GL \_ 用戶端 \_ 所有的 \_ ATTRIB \_ 位**</dt> </dl> | 所有堆疊的用戶端狀態屬性。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                               | 意義                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 堆疊 \_ 溢位**</dt> </dl> | 當用戶端屬性堆疊已滿時，就會呼叫此函數。<br/> |



## <a name="remarks"></a>備註

**GlPushClientAttrib** 函式會使用其 mask 參數，來判斷要將哪些用戶端狀態變數群組儲存在用戶端屬性堆疊上。 您可以使用位 OR 運算子將已接受的符號常數聯結在一起，以設定位並建立遮罩。

[**GlPopClientAttrib**](glpopclientattrib.md)函式會還原上次與 **glPushclientAttrib** 儲存之用戶端狀態變數的值。 先前未儲存的用戶端狀態變數會保持不變。 將屬性推送至完整的用戶端屬性堆疊，或將屬性從空的堆疊中取出，會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。 用戶端屬性堆疊預設為空白。

某些 OpenGL 用戶端狀態值無法儲存在用戶端屬性堆疊上。 例如，您無法在用戶端屬性堆疊上儲存選取或意見反應狀態。 用戶端屬性堆疊的深度至少為16。

**GlPushclientAttrib** 和 **glPopClientAttrib** 函式不會編譯成顯示清單，但是會立即執行。

**GlPushClientAttrib** 和 **glPopClientAttrib** 函式只能推送和 pop 圖元儲存模式，以及頂點陣列用戶端狀態。 您必須使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 來推送和保留在伺服器上的 pop 狀態。

> [!Note]  
> **GlPushClientAttrib** 和 **glPopClientAttrib** 函式僅適用于 OpenGL 1.1 版或更新版本。

 

下列函式會取出 **glPushClientAttrib** 和 **glPopClientAttrib** 的相關資訊：

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 用戶端 ATTRIB 用戶端 \_ ATTRIB \_ 堆疊 \_ 深度

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ 用戶端 \_ ATTRIB \_ 堆疊 \_ 深度的 glGet

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





