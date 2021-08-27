---
title: 'glAccum 函式 (Gl) '
description: GlAccum 函數會在累積緩衝區上運作。
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glAccum 函式 OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0820d27bf6aff05916eb179e4dfd0b51a0746e2c6e5a6f4e5f3bdfe8f3e6d91a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082258"
---
# <a name="glaccum-function"></a>glAccum 函式

**GlAccum** 函數會在累積緩衝區上運作。

## <a name="syntax"></a>語法


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*op* 
</dt> <dd>

累積緩衝區作業。 接受的符號常數如下所示。



| 值                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**GL \_ ACCUM**</dt> </dl>    | 從目前選取要讀取的緩衝區取得 R、G、B 和值 (參閱 [**glReadBuffer**](glreadbuffer.md)) 。 每個元件值都除以 2 *n*  1，其中 *n* 是配置給目前所選緩衝區中每個色彩元件的位數。 結果是範圍0，1的浮點值， \[ \] 會乘以 *值* 並加入至累積緩衝區中的對應圖元元件，藉此更新累積緩衝區。<br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**GL \_ 負載**</dt> </dl>       | 類似于 GL \_ ACCUM，不同之處在于累積緩衝區中的目前值不會用於計算新值。 也就是說，R、G、B 和目前所選緩衝區的值會除以 2 *n*  1、乘以 *值*，然後儲存在對應的累積緩衝區資料格中，以覆寫目前的值。<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**GL \_ 新增**</dt> </dl>          | 將 *值* 加入至累積緩衝區中的每個 R、G、B 和 A。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**GL \_ MULT**</dt> </dl>       | 以傳 *值* 方式將累積緩衝區中的每個 R、G、B 和 A 相乘，並將縮放的元件傳回至其對應的累積緩衝區位置。<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**GL \_ 退貨**</dt> </dl> | 將累積的緩衝區值傳輸到目前選取要寫入的色彩緩衝區或緩衝區。 每個 R、G、B 和 A 元件都會乘以 *value*，然後乘以 2 *n*  1，壓制至範圍 \[ 0，2 *n*  1 \] ，並儲存在對應的顯示緩衝區資料格中。 套用到此傳輸的唯一片段作業是圖元擁有權、剪下、遞色和色彩 writemasks。<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

在累積緩衝區作業中使用的浮點值。 *Op* 參數會決定 *值* 的使用方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *op* 不是可接受的值。<br/>                                                                                                                                            |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 沒有累積緩衝區，或呼叫 [**glBegin**](glbegin.md)和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數 **glAccum** 。<br/> |



## <a name="remarks"></a>備註

累積緩衝區是延伸範圍的色彩緩衝區。 影像不會轉譯到其中。 相反地，轉譯成其中一個色彩緩衝區的影像會在轉譯之後加入累積緩衝區的內容中。 您可以藉由使用不同的轉換矩陣產生的影像累積，來建立點、線條和多邊形的消除鋸齒 (、曲線) 、運動模糊和欄位深度等效果。

累積緩衝區中的每個圖元都是由紅色、綠色、藍色和 Alpha 值所組成。 累積緩衝區中每個元件的位數取決於執行量。 您可以藉由呼叫 [**glGetIntegerv**](glgetintegerv.md) 四次，分別使用引數 GL \_ ACCUM RED \_ bit \_ 、GL \_ ACCUM \_ 綠 BIT \_ 、gl \_ ACCUM \_ BLUE \_ bits 和 gl \_ ACCUM \_ ALPHA \_ bit 來檢查此數目。 但是，不論每個元件的位數為何，每個元件儲存的值範圍都是 \[ 1，？ 1 \] 。 累積的緩衝區圖元會以畫面格緩衝區圖元為一對一對應。

**GlAccum** 函數會在累積緩衝區上運作。 第一個引數 *op* 是選取累積緩衝區作業的符號常數。 第二個引數（ *value*）是要在該作業中使用的浮點值。 指定了五個作業： GL \_ ACCUM、gl \_ LOAD、gl \_ ADD、GL \_ MULT 和 gl \_ 退回。

所有累積的緩衝區作業僅限於目前剪下方塊的區域，並與每個圖元的紅色、綠色、藍色和 Alpha 元件相同套用。 如果 **glAccum** 作業產生的值超出範圍 \[ 1，1，則會定義累積緩衝區圖元元件的內容 \] 。

若要清除累積緩衝區，請使用 [**glClearAccum**](glclearaccum.md) 函式來指定 R、G、B 和值，以將其設定為，併發出 [**glClear**](glclear.md) 函數並啟用累積緩衝區。

任何 **glAccum** 作業都只會更新目前剪式方塊內的圖元。

下列函式會取出與 **glAccum** 函數相關的資訊：

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)與引數 GL \_ ACCUM \_ RED bit \_

**glGet** 與引數 GL \_ ACCUM \_ 綠 \_ 位

**glGet** 與引數 GL \_ ACCUM \_ BLUE \_ BITS

**glGet** 與引數 GL \_ ACCUM \_ ALPHA \_ 位

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

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





