---
title: 'glLogicOp 函式 (Gl) '
description: GlLogicOp 函式會指定色彩索引呈現的邏輯圖元運算。
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- glLogicOp 函式 OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509450"
---
# <a name="gllogicop-function"></a>glLogicOp 函式

**GlLogicOp** 函式會指定色彩索引呈現的邏輯圖元運算。

## <a name="syntax"></a>語法


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*opcode* 
</dt> <dd>

選取邏輯運算的符號常數。 接受下列符號，其中 s 等於來源位的值，而 d 是目的地位的值。



| 值                                                                                                                                                                   | 意義              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**GL \_ 清除**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**GL \_ 設定**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**GL \_ 複製**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**GL \_ 複製 \_ 反轉**</dt> </dl> | ！ s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**GL \_ NOOP**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ 反轉**</dt> </dl>                       | ！ d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ 和**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**GL \_ N**</dt> </dl>                             | ！ (s & d) <br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ 或**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ 或**</dt> </dl>                                | ！ (s \| d) <br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**GL \_ XOR**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**GL \_ HTTP-EQUIV**</dt> </dl>                          | ！ (s ^ d) <br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ 和 \_ 反向**</dt> </dl>       | s &！ d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ 和 \_ 倒轉**</dt> </dl>    | ！ s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ 或 \_ 反轉**</dt> </dl>          | s \| ！ d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ 或 \_ 反轉**</dt> </dl>       | ！ s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *opcode* 不是可接受的值。<br/>                                                                                        |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlLogicOp** 函式會指定在已啟用時，于畫面格緩衝區中對應位置的內送色彩索引和色彩索引之間套用的邏輯運算。 使用符號常數 GL 邏輯 OP 來啟用或停用 [**glEnable**](glenable.md) 和 **glDisable** 的邏輯 \_ 作業 \_ 。

*Opcode* 參數是從下列清單中選擇的符號常數。 在邏輯作業的說明中， *s* 代表傳入的色彩索引，而 *d* 代表畫面格緩衝區中的索引。 使用標準 C 語言運算子。 如同這些位運算子的建議，邏輯作業會獨立套用至來源和目的地索引的每個位配對。

邏輯圖元作業不會套用到 RGBA 色彩緩衝區。

當有一個以上的色彩索引緩衝區啟用繪圖時，會針對每個啟用的緩衝區個別完成邏輯作業，使用目的地索引的緩衝區內容 (查看 [**glDrawBuffer**](gldrawbuffer.md)) 。

*Opcode* 參數必須是16個接受值的其中一個。 其他值會導致錯誤。

下列函式會取出與 **glLogicOp** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 邏輯 \_ OP \_ 模式的 glGet

[](glisenabled.md)具有引數 GL \_ 邏輯 \_ OP 的 glIsEnabled

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

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





