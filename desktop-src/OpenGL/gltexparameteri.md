---
title: 'glTexParameteri 函式 (Gl) '
description: '設定材質參數。 |glTexParameteri 函式 (Gl) '
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
keywords:
- glTexParameteri 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexParameteri
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bcc269c92d2d233f8c0dae89438232830539c3f8f59c3f8e28ef2be6ba42e54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613235"
---
# <a name="gltexparameteri-function"></a>glTexParameteri 函式

設定材質參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glTexParameteri(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

目標材質，必須是 GL \_ 材質 \_ 1D 或 gl \_ 紋理 \_ 2d。

</dd> <dt>

*pname* 
</dt> <dd>

單一值材質參數的符號名稱。 *Pname* 接受下列符號。



| 值                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**GL \_ 材質 \_ 最小 \_ 篩選**</dt> </dl> | 紋理縮小函式會在每次有紋理的圖元對應到一個以上的材質專案區域時使用。 有六個定義的縮小函數。 其中兩個會使用最接近的一個或最接近的四個材質元素來計算紋理值。 其他四個使用 mipmap。 <br/> Mipmap 是一組已排序的陣列，代表以漸進較低解析度表示的相同影像。 如果材質的維度為 2nx2<sup>m</sup> ，則 (n，m) + 1 mipmap 的上限。 第一個 mipmap 是原始材質，維度為 2nx2<sup>m</sup>。 每個後續的 mipmap 都有維度 2<sup>k</sup>1x2<sup>l</sup>1，其中 2<sup>k</sup>x2<sup>l</sup> 是前一個 mipmap 的維度，直到 k = 0 或 l = 0 為止。 屆時，後續的 mipmap 會有維度 1x2<sup>l</sup>1 或 2<sup>k</sup>1x1，直到最後一個 mipmap，其維度為1x1。 Mipmap 是使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md) 來定義，並以詳細程度的引數來指出 mipmap 的順序。 層級0是原始紋理;水準粗體最大 (n，m) 是最後 1x1 mipmap。<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**GL \_ 紋理 \_ MAG \_ 篩選**</dt> </dl> | 當材質的圖元對應到小於或等於一個材質元素的區域時，就會使用材質放大功能。 它會將材質放大函式設定為 \_ 最接近的 gl 或 gl \_ 線性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ 材質 \_ 換行 \_**</dt> </dl>             | 將材質座標 s 的 wrap 參數設定為 GL \_ 夾具或 gl \_ 重複。 GL \_ 夾具會將 s 座標壓制至範圍 \[ 0，1， \] 以便在將單一影像對應至物件時防止包裝成品。 GL \_ 重複會忽略 s 座標的整數部分。OpenGL 只會使用小數部分，藉此建立重複的模式。 只有當換行設定為 GL 夾具時，才會存取框線材質元素 \_ 。 一開始， \_ \_ 會將 gl 材質換行 \_ 設定為 gl \_ 重複。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ 紋理 \_ WRAP \_ T**</dt> </dl>             | 將材質座標 t 的 wrap 參數設定為 GL \_ 夾具或 gl \_ 重複。 請參閱 GL \_ 材質 WRAP S 下的討論 \_ \_ 。 一開始，GL \_ 紋理 \_ WRAP \_ T 會設定為 gl \_ REPEAT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

*param* 
</dt> <dd>

*Pname* 的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_不正確 \_ 列舉**</dt> </dl>     | *target* 或 *pname* 不是其中一個接受的定義值，或是當 *param* 應該有定義的常數值 (根據 *pname*) 的值而不是時。<br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>                                            |



## <a name="remarks"></a>備註

材質對應是一種技術，可將影像套用至物件的介面，就像影像是 decal 或 cellophane 壓縮包裝一樣。 影像會在材質空間中建立，其中包含 (*s*， *t*) 座標系統。 材質是一或兩維度的影像，而一組參數會決定如何從影像衍生樣本。

**GlTexParameter** 函式會將 params 中的值或值指派給指定為 pname 的材質參數。 目標參數會定義目標材質，也就是 GL \_ 材質 \_ 1D 或 gl \_ 材質 \_ 2d。

在縮制程式中取樣更多紋理專案時，會有較少的別名成品。 雖然 \_ 最接近的 gl 和 gl \_ 線性縮制函式可以比其他四個函式更快，但它們只會取樣一或四個材質元素，以判斷所轉譯圖元的材質值，而且可以產生 moire 模式或不完全的轉換。 GL \_ 紋理 \_ 最小篩選的預設值 \_ 為 gl \_ 最接近 \_ MIPMAP 的 \_ 線性。

假設 (藉由使用引數 GL [](glenable.md) \_ 紋理 \_ 1d 或 gl \_ 材質 2d) 來呼叫 glEnable \_ ，並 \_ 將 gl 材質 \_ MIN \_ 篩選設定為需要 mipmap 的其中一個函式，以啟用紋理。 如果目前定義的材質影像維度 (與先前對 [**glTexImage1D**](glteximage1d.md) 或) [**glTexImage2D**](glteximage2d.md) 的呼叫不遵循正確的 mipmap 順序，或者定義的材質影像數目小於所需的材質影像，或紋理影像集合的材質元件數目不同，則會如同材質對應已停用一樣。 線性篩選只會存取2D 材質中四個最接近的材質元素。 在立體材質中，線性篩選會存取兩個最接近的材質元素。 下列函式會抓取 **glTexParameterf**、 **glTexParameteri**、 **glTexParameterfv** 和 **glTexParameteriv** 的相關資訊：

[**glGetTexParameter**](glgettexparameter.md)

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





