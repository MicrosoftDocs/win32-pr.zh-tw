---
title: 'glStencilOp 函式 (Gl) '
description: GlStencilOp 函數會設定樣板測試動作。
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glStencilOp 函式 OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da899207456cece58216874c7540a032326e4180e9484590e2effd619eea72f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614332"
---
# <a name="glstencilop-function"></a>glStencilOp 函式

**GlStencilOp** 函數會設定樣板測試動作。

## <a name="syntax"></a>語法


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*失敗* 
</dt> <dd>

樣板測試失敗時所要採取的動作。 接受下列六個符號常數。



| 值                                                                                                                                                | 意義                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**GL \_ 保留**</dt> </dl>          | 保留目前的值。<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**GL \_ 零**</dt> </dl>          | 將樣板緩衝區值設定為零。<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**GL \_ 取代**</dt> </dl> | 將樣板緩衝區值設定為 *ref*（如 **glStencilFunc** 所指定）。<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**GL \_ 增量**</dt> </dl>          | 遞增目前的樣板緩衝區值。 個至可表示的最大不帶正負號值。<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**GL \_ OPERATORS.DECR**</dt> </dl>          | 遞減目前的樣板緩衝區值。 個為零。<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ 反轉**</dt> </dl>    | 以位反轉目前的樣板緩衝區值。<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

樣板測試通過時的樣板動作，但深度測試會失敗。 接受與失敗相同的符號常數 *。*

</dd> <dt>

*zpass* 
</dt> <dd>

樣板測試和深度測試成功時，或樣板測試通過，而且沒有啟用深度緩衝區或深度測試時的樣板動作。 接受與 *失敗* 相同的符號常數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *fail*、 *zfail* 或 *zpass* 是六個定義常數值以外的任何值。<br/>                                      |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

Stenciling，例如 *z* 緩衝，可啟用和停用以每圖元為基礎的繪圖。 您可以使用 OpenGL 繪圖基本專案來繪製到樣板平面，然後轉譯幾何和影像，使用樣板平面來遮蔽畫面的部分。 Stenciling 通常用於 multipass 轉譯演算法，以達成特殊效果，例如 decals、大綱和具建設性的純幾何呈現。

樣板測試會根據樣板緩衝區中的值與參考值之間的比較結果，有條件地消除圖元。 測試會以具有引數 GL 樣板測試的 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 呼叫來啟用 \_ \_ ，並使用 [**glStencilFunc**](glstencilfunc.md)來控制。

**GlStencilOp** 函式會採用三個引數，指出啟用 stenciling 時，儲存的樣板值會發生什麼事。 如果樣板測試失敗，則不會對圖元的色彩或深度緩衝區進行任何變更，而且 *會* 指定樣板緩衝區內容會發生什麼事。

樣板緩衝區值會被視為不帶正負號的整數。 遞增和遞減時，值會壓制為0和 2 *n* 1，其中 *n* 是查詢 GL 樣板位所傳回的值 \_ \_ 。

**GlStencilOp** 指定樣板緩衝區動作的其他兩個引數，應該 (*zpass*) 或 (*zfail*) 失敗，才能執行後續深度緩衝區測試。  (請參閱 [**glDepthFunc**](gldepthfunc.md)。 ) 使用相同的六個符號常數來指定 *失敗*。 請注意，當沒有深度緩衝區或未啟用深度緩衝區時，就會忽略 *zfail* 。 在這些情況下，當樣板測試失敗並分別傳遞時，fail 和 *zpass* *會* 指定樣板動作。

範本測試一開始會停用。 如果沒有任何樣板緩衝區，則不會發生任何樣板修改，也就像樣板測試一律通過，而不考慮任何 **glStencilOp** 呼叫。

下列函式會取出與 **glStencilOp** 相關的資訊：

具有引數 GL 樣板的 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ 失敗

具有引數 GL \_ 樣板 \_ 通過 \_ 深度 \_ 傳遞的 glGet

具有引數 GL \_ 樣板 \_ 通過 \_ 深度 \_ 失敗的 glGet

具有引數 GL \_ 樣板 \_ 位的 glGet

[](glisenabled.md)具有引數 GL \_ 樣板 \_ 測試的 glIsEnabled

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





