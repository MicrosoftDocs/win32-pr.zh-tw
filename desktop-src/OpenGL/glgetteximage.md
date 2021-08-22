---
title: 'glGetTexImage 函式 (Gl) '
description: GlGetTexImage 函式會傳回材質影像。
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glGetTexImage 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b116bc4ae517d0767d794767ad5232d8537033d62a099a3906f9f2ca96a7166c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493748"
---
# <a name="glgetteximage-function"></a>glGetTexImage 函式

**GlGetTexImage** 函式會傳回材質影像。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

指定要取得的材質。 \_ \_ 已接受 gl 材質1D 和 gl \_ 材質 \_ 2d。

</dd> <dt>

*level* 
</dt> <dd>

所需影像的詳細層級編號。 層級0是基底映射層級。 層級 *n* 是第 *n* 個 mipmap 縮減影像。

</dd> <dt>

*format* 
</dt> <dd>

傳回資料的像素格式。 支援的格式為 GL \_ RED、gl \_ 綠、gl \_ BLUE、GL \_ ALPHA、gl \_ RGB、gl \_ RGBA、gl \_ 亮度、gl \_ BGR \_ EXT、gl \_ BGRA \_ ext 和 gl \_ 亮度 \_ ALPHA。

</dd> <dt>

*type* 
</dt> <dd>

傳回資料的圖元型別。 支援的類型為 GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、gl 不 \_ 帶正負號的 \_ SHORT、gl \_ short、gl 不 \_ 帶正負號 \_ int、gl \_ int 和 gl \_ FLOAT。

</dd> <dt>

*圖元* 
</dt> <dd>

傳回材質影像。 應為 *類型* 所指定之類型陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標*、 *格式* 或 *類型* 不是可接受的值。<br/>                                                                    |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *層級* 小於零或大於 *log* 2 (*max*) ，其中 *max* 是 GL \_ 最大 \_ 紋理大小的傳回值 \_ 。<br/>      |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md) 呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetTexImage** 函式會將材質影像傳回到 *圖元*。 *目標* 參數會指定所需的材質影像是由 [**glTexImage1D**](glteximage1d.md) **(** GL \_ 材質 \_ 1d **)** 或 [**glTexImage2D**](glteximage2d.md) **(** GL \_ 材質 \_ 2d **)** 所指定。 *Level* 參數會指定所需影像的詳細層級數目。 *Format* 和 *type* 參數會指定所需影像陣列的格式和類型。 如需適用于 *格式* 和 *類型* 參數的可接受值的描述，請參閱 **glTexImage1D** 和 [**glDrawPixels**](gldrawpixels.md)。

將選取的內部四元件紋理影像視為映射大小的 RGBA 色彩緩衝區，可充分瞭解 **glGetTexImage** 的作業。 然後， **glGetTexImage** 的語義會與使用相同 *格式* 和 *類型* 呼叫的 [**glReadPixels**](glreadpixels.md)相同。如果 *x* 和 *y* 設定為零，則寬度設定為材質影像的寬度 (包括框線（如果有指定的話）) ，以及將 *寬度* 設定為 1-d 影像 *的高度，* 或是材質影像的高度（如果指定了2d 影像) ，則會包含框線）。 (

因為內部紋理影像是 RGBA 影像，所以不接受像素格式的 GL \_ 色彩 \_ 索引、gl 樣板 \_ \_ 索引和 gl \_ 深度 \_ 元件，而且不接受圖元類型 gl \_ 點陣圖。

如果選取的材質影像未包含四個元件，則會套用下列對應。 單一元件紋理會被視為 RGBA 緩衝區，並將紅色設定為單一元件值，綠色、藍色和 Alpha 設定為零。

雙元件紋理會視為 RGBA 緩衝區，並將紅色設定為元件零的值、將 Alpha 設定為元件1的值，而綠色和藍色設定為零。 最後，會將三個元件的材質視為 RGBA 緩衝區，並將紅色設定為 [元件零]、綠色設定為 [元件 1]、[藍色設定為第二個]、[Alpha] 設定為零。

若要判斷所需的 *圖元* 大小，請使用 [**glGetTexLevelParameter**](glgettexlevelparameter.md) 來確定內部紋理影像的維度，然後根據 *格式* 和 *類型*，根據每個圖元所需的儲存體來調整所需的圖元數目。 務必將圖元儲存體參數納入考慮，特別是 GL \_ 套件 \_ 對齊。

如果產生錯誤，則不會對 *圖元* 的內容進行任何變更。

下列函式會取出與 **glGetTexImage** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 套件 \_ 對齊和其他專案的 glGet

[](glgettexlevelparameter.md)具有引數 GL \_ 材質 \_ 寬度的 glGetTexLevelParameter

具有引數 GL \_ 材質 \_ 高度的 glGetTexLevelParameter

具有引數 GL \_ 紋理 \_ 框線的 glGetTexLevelParameter

具有引數 GL \_ 材質 \_ 元件的 glGetTexLevelParameter

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





