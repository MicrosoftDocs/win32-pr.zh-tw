---
title: 'glStencilFunc 函式 (Gl) '
description: GlStencilFunc 函數會設定樣板測試的函數和參考值。
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glStencilFunc 函式 OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e529bd83cff8ffb25c8853b7d896926e63982370387f7e2fb5d2ca30a394c1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491508"
---
# <a name="glstencilfunc-function"></a>glStencilFunc 函式

**GlStencilFunc** 函數會設定樣板測試的函數和參考值。

## <a name="syntax"></a>語法


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*func* 
</dt> <dd>

測試函數。 下列八個權杖都有效。



| 值                                                                                                                                                   | 意義                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ 永不**</dt> </dl>          | 一律會失敗。<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | 如果 (*ref*  &  *mask*) < (樣板  &  *遮罩*) ，則傳遞。<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | 如果 (*ref*  &  *mask*) = (樣板  &  *遮罩*) ，則傳遞。<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ 更高**</dt> </dl>    | 如果 (*ref*  &  *mask*) > (樣板  &  *遮罩*) ，則傳遞。<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | 如果 (*ref*  &  *mask*) = (樣板  &  *遮罩*) ，則傳遞。<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ 相等**</dt> </dl>          | 如果 (*ref*  &  *mask*) = (樣板  &  *遮罩*) ，則傳遞。<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | 如果 (*ref*  &  *遮罩*) ，則傳遞？  (*樣板*  &  *遮罩*) 。<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ 一律**</dt> </dl>       | 一律傳遞。<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

樣板測試的參考值。 *Ref* 參數壓制至範圍 \[ 0，2 *n* 1 \] ，其中 *n* 是樣板緩衝區中的 bitplanes 數目。

</dd> <dt>

*面具* 
</dt> <dd>

當測試完成時 **，同時** 具有參考值和儲存的樣板值的遮罩。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *func* 不是八個接受值的其中一個。<br/>                                                                           |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

Stenciling，例如 *z* 緩衝，可啟用和停用以每圖元為基礎的繪圖。 您可以使用 OpenGL 繪圖基本專案來繪製到樣板平面，然後轉譯幾何和影像，使用樣板平面來遮蔽畫面的部分。 Stenciling 通常用於 multipass 轉譯演算法，以達成特殊效果，例如 decals、大綱和具建設性的純幾何呈現。

樣板測試會根據參考值與樣板緩衝區中的值之間的比較結果，有條件地排除圖元。 [**GlEnable**](glenable.md)和 [**glDisable**](gldisable.md)會使用引數 GL 樣板測試來啟用測試 \_ \_ 。 根據樣板測試結果所採取的動作會以 [**glStencilOp**](glstencilop.md)指定。

*Func* 參數是決定樣板比較函數的符號常數。 它會接受上面所示的八個值之一。 *Ref* 參數是用於樣板比較的整數參考值。 它會壓制至範圍 \[ 0，2 *n* 1 \] ，其中 *n* 是樣板緩衝區中的 bitplanes 數目。 *Mask* 參數是使用參考值和預存樣板值的位 **And** ed，並參與比較的 **和** ed 值。

如果樣板表示儲存在對應之樣板緩衝區位置的值 *，則上述* 清單會顯示 *func* 可指定之每個比較函式的效果。 只有在比較成功時，才會將圖元傳遞給點陣化進程中的下一個階段 (請參閱 [**glStencilOp**](glstencilop.md)) 。 所有測試都會將 *樣板值視為* 範圍 \[ 0，2 *n* 1 的不帶正負號的整數， \] 其中 *n* 是樣板緩衝區中的 bitplanes 數目。

一開始，樣板測試已停用。 如果沒有樣板緩衝區，則不會進行任何樣板修改，如同樣板測試一律會通過。

下列函式會取出與 **glStencilFunc** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 樣板 \_ FUNC 的 glGet

具有引數 GL \_ 範本 \_ 值 \_ 遮罩的 glGet

具有引數 GL \_ 樣板 \_ REF 的 glGet

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

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





