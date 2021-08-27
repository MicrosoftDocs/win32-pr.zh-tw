---
title: 'glDrawBuffer 函式 (Gl) '
description: GlDrawBuffer 函式會指定要繪製的色彩緩衝區。
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- glDrawBuffer 函式 OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5bc715aad24198031ed096d53f1a468b6672532e4df4ae1ef66b416002a65b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081608"
---
# <a name="gldrawbuffer-function"></a>glDrawBuffer 函式

**GlDrawBuffer** 函式會指定要繪製的色彩緩衝區。

## <a name="syntax"></a>語法


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

使用下列可接受的符號常數，指定要繪製的最多四個色彩緩衝區。



| 值                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ 無**</dt> </dl>                                 | 不會寫入任何色彩緩衝區。<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL \_ FRONT \_ 左方**</dt> </dl>              | 只會寫入 front 左色緩衝區。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**GL \_ 正面 \_**</dt> </dl>           | 只會寫入右上方的色彩緩衝區。<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**GL \_ 向 \_ 左復原**</dt> </dl>                 | 只會寫入向左色彩緩衝區。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**GL \_ 向 \_ 右**</dt> </dl>              | 只會寫入向右色彩緩衝區。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**GL \_ FRONT**</dt> </dl>                              | 只會寫入左上角和右上角的色彩緩衝區。 如果沒有右邊的色彩緩衝區，則只會寫入 front 左色緩衝區。<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**GL \_ 回**</dt> </dl>                                 | 只會寫入向左和向右色彩緩衝區。 如果沒有右邊的色彩緩衝區，則只會寫入向左色彩緩衝區。<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL \_ 剩餘**</dt> </dl>                                 | 只會寫入左上角和左邊的色彩緩衝區。 如果沒有上一頁的色彩緩衝區，則只會寫入左上角的色彩緩衝區。<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**GL \_ 右邊**</dt> </dl>                              | 只會寫入左右和右邊的色彩緩衝區。 如果沒有右邊的色彩緩衝區，則只會寫入右上方的色彩緩衝區。<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**GL \_ 正面 \_ 和 \_ 背面**</dt> </dl> | 所有前端和背景色彩緩衝區都 (由左上角、右上角、左上角、右) 書寫。 如果沒有背面的色彩緩衝區，則只會寫入左上角和右上角的色彩緩衝區。 如果沒有正確的色彩緩衝區，則只會寫入左上角和左邊的色彩緩衝區。 如果沒有右邊或背面的色彩緩衝區，則只會寫入左上角的色彩緩衝區。<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**GL \_ AUXi**</dt> </dl>       | 只寫入輔助 *顏色緩衝區，**i* 介於0和 GL \_ AUX \_ 的緩衝區-1 之間。  (GL \_ AUX \_ 緩衝區不是上限; 請使用 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 來查詢可用輔助緩衝區的數目。 ) <br/>                                                                                                                            |



 

預設值為單一緩衝內容的 GL \_ 前端，而 \_ 針對雙重緩衝的內容則會傳回 gl。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | *模式* 所指出的緩衝區都不存在。<br/>                                                                           |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |


## <a name="remarks"></a>備註

當色彩寫入至畫面格緩衝區時，會將其寫入至 **glDrawBuffer** 所指定的色彩緩衝區。

如果選取了一個以上的色彩緩衝區來進行繪製，則會針對每個顏色緩衝區個別計算並套用混合或邏輯運算，而且可能會在每個緩衝區中產生不同的結果。

Monoscopic 內容只會包含左邊的緩衝區，而 stereoscopic 內容則包含左邊和右邊的緩衝區。 同樣地，單一緩衝的內容只會包含前端緩衝區，而雙重緩衝的內容則包含前端和後端緩衝區。 內容會在 OpenGL 初始化時選取。

這一律是 GL \_ AUX *i* = gl \_ AUX0 + *i*。

下列函式會取出與 **glDrawBuffer** 函數相關的資訊：

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 繪圖 \_ 緩衝區

具有引數 GL \_ AUX \_ 緩衝區的 glGet

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





