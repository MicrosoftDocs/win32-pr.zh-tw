---
title: 'glAlphaFunc 函式 (Gl) '
description: GlAlphaFunc 函式可讓您的應用程式設定 Alpha 測試函數。
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- glAlphaFunc 函式 OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968767"
---
# <a name="glalphafunc-function"></a>glAlphaFunc 函式

**GlAlphaFunc** 函式可讓您的應用程式設定 Alpha 測試函數。

## <a name="syntax"></a>語法


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*func* 
</dt> <dd>

Alpha 比較函數。 以下是接受的符號常數及其意義。



| 值                                                                                                                                                   | 意義                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ 永不**</dt> </dl>          | 永遠不會通過。<br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | 如果傳入的 Alpha 值小於參考值，則會傳遞。<br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ 相等**</dt> </dl>          | 如果傳入的 Alpha 值等於參考值，則會傳遞。<br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | 如果傳入的 Alpha 值小於或等於參考值，則會傳遞。<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ 更高**</dt> </dl>    | 傳入的 Alpha 值是否大於參考值時傳遞。<br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | 如果傳入的 Alpha 值不等於參考值，則會傳遞。<br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | 如果傳入的 Alpha 值大於或等於參考值，則會傳遞。<br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ 一律**</dt> </dl>       | 一律傳遞。 此為預設值。<br/>                                                 |



 

</dd> <dt>

*ref* 
</dt> <dd>

要比較傳入 Alpha 值的參考值。 此值會壓制至範圍0到1，其中0代表可能的最小 Alpha 值和1個最高的可能值。 預設參考為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *func* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

Alpha 測試會根據傳入片段的 Alpha 值與常數參考值之間的比較結果，來捨棄片段。 **GlAlphaFunc** 函數會指定參考和比較函數。 只有在啟用 Alpha 測試時，才會執行比較。  (如需有關 GL ALPHA 測試的詳細資訊 \_ \_ ，請參閱 [**glEnable**](glenable.md)。 ) 

*Func* 和 *ref* 參數指定圖元繪製時所依據的條件。 使用 *func* 指定的函式，將連入的 Alpha 值與 *ref* 進行比較。 如果比較通過，則會繪製內送片段、後續樣板和深度緩衝區測試的條件。 如果比較失敗，則不會在該圖元位置對畫面格緩衝區進行任何變更。

**GlAlphaFunc** 函式會在所有圖元寫入上運作，包括從點、線條、多邊形和點陣圖的掃描轉換產生的結果，以及從圖元繪製和複製作業產生的結果。 **GlAlphaFunc** 函數不會影響螢幕清除作業。

Alpha 測試只會在 RGBA 模式中完成。

下列函式會取出與 **glAlphaFunc** 函數相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ ALPHA \_ TEST \_ FUNC 的 glGet

具有引數 GL \_ ALPHA \_ TEST \_ REF 的 glGet

[](glisenabled.md)具有引數 GL \_ ALPHA \_ 測試的 glIsEnabled

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





