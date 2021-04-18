---
title: 'glBlendFunc 函式 (Gl) '
description: GlBlendFunc 函數會指定圖元算術。
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glBlendFunc 函式 OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965728"
---
# <a name="glblendfunc-function"></a>glBlendFunc 函式

**GlBlendFunc** 函數會指定圖元算術。

## <a name="syntax"></a>語法


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sfactor* 
</dt> <dd>

指定如何計算紅色、綠色、藍色和 Alpha 來源混合因數。 接受九個符號常數： GL \_ 零、gl \_ 1、GL \_ DST \_ 色彩、gl \_ 1 \_ 減去 \_ DST \_ 色彩、gl \_ 來源 \_ Alpha、GL \_ 1 \_ 減去 \_ SRC \_ Alpha、gl \_ DST \_ Alpha、gl \_ 1 \_ 減去 \_ dst \_ Alpha，以及 GL \_ SRC \_ Alpha \_ 飽和。

</dd> <dt>

*dfactor* 
</dt> <dd>

指定如何計算紅色、綠色、藍色和 Alpha 目的地混合因數。 接受八個符號常數： GL \_ 零、gl \_ 1、gl \_ SRC \_ 色彩、gl \_ 1 \_ 減去 \_ SRC \_ 色彩、gl \_ src \_ Alpha、gl \_ \_ 減去 \_ src \_ Alpha、gl \_ DST \_ Alpha 和 gl \_ 1 \_ 減去 \_ DST \_ Alpha。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *Sfactor* 或 *dfactor* 都不是可接受的值。<br/>                                                                   |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

在 RGB 模式中，可以使用混合傳入 (來源) RGBA 值的函式，以及已在目的地值) 的 (畫面格緩衝區中的 RGBA 值來繪製圖元。 依預設，會停用混色。 使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配 GL \_ BLEND 引數來啟用和停用混合。

啟用時， **glBlendFunc** 會定義混合的運算。 *Sfactor* 參數會指定使用九種方法來調整來源色彩元件的大小。 *Dfactor* 參數會指定用來調整目的地色彩元件的八種方法。 下表說明了11種可能的方法。 每個方法都會定義四個縮放因數，分別用於紅色、綠色、藍色和 Alpha。

在資料表和後續的方商中，來源和目的地色彩元件稱為 (*R*？ ， *G*？ ， *B*？ ， *答*： ) 和 (*R*<sub>d</sub> 、 *G*<sub>d</sub> 、 *B*<sub>d</sub> 、 ** <sub>d</sub> ) 。 其可理解的整數值介於零和 (*k*<sub>r</sub> 、 *k*<sub>G</sub> 、 *k*<sub>r</sub> 、 *k*<sub>A</sub> ) ，其中

*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1

*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1

*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1

*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1

和 (*m*<sub>R</sub> 、 *m*<sub>G</sub> 、 *m*<sub>B</sub> 、 *m*<sub>A</sub> ) 是紅色、綠色、藍色和 Alpha bitplanes 的數目。

來源和目的縮放比例稱為 (*s*<sub>r</sub> 、 *s*<sub>G</sub> 、 *s*<sub>B</sub> 、 *s*<sub>) 和</sub> (*d*<sub>r</sub> 、 *d*<sub>G</sub> 、 *d*<sub>B</sub> 、 *d*<sub>A</sub> ) 。 表格中描述的比例因素（表示 (*f*<sub>R</sub> 、 *f*<sub>G</sub> 、 *f*<sub>B</sub> 、 *f*<sub>A</sub> ) ）代表來源或目的地因素。 所有比例因素的範圍為 \[ 0、1 \] 。



| 參數                  |  (*f*<sub>R</sub>  、 *f*<sub>G</sub>  、 *f*<sub>B</sub>  、 *f*<sub>A</sub>  )                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ 零                   | (0,0,0,0)                                                                                                                                                    |
| GL \_ 1                    |  (1，1，1，1)                                                                                                                                                     |
| GL \_ SRC \_ 色彩             |  (*R*？ / *k*<sub>R</sub> 、 *G*？ / *k*<sub>G</sub> 、 *B*？ / *k*<sub>B</sub> ， *A*？ / *k*<sub>)</sub>                                                         |
| GL \_ 1 \_ 減去 \_ SRC \_ 色彩 |  (1，1，1，1)  (*R*？ / *k*<sub>R</sub> 、 *G*？ / *k*<sub>G</sub> 、 *B*？ / *k*<sub>B</sub> ， *A*？ / *k*<sub>)</sub>                                             |
| GL \_ DST \_ 色彩             |  (*r*<sub>d</sub>  /  *k*<sub>R</sub> 、 *g*<sub>d</sub>  /  *k*<sub>G</sub> 、 *B*<sub>d</sub>  /  *k*<sub>B</sub> 、 *a*<sub>d</sub>  /  *k*<sub>a</sub> )              |
| GL \_ 1 \_ 減去 \_ DST \_ 色彩 |  (1，1，1，1)  (*R*<sub>d</sub>  /  *k*<sub>r</sub> 、 *G*<sub>d</sub>  /  *k*<sub>G</sub> 、 *B*<sub>d</sub>  /  *k*<sub>b</sub> 、 ** <sub>d</sub>  /  *k*<sub>a</sub> )  |
| GL \_ SRC \_ ALPHA             |  (*嗎*？ / *k*<sub>a</sub> ， *答*？ / *k*<sub>a</sub> ， *答*？ / *k*<sub>a</sub> ， *答*？ / *k*<sub>)</sub>                                                         |
| GL \_ 1 \_ 減去 \_ SRC \_ ALPHA |  (1，1，1，1)  (*A*？ / *k*<sub>a</sub> ， *答*？ / *k*<sub>a</sub> ， *答*？ / *k*<sub>a</sub> ， *答*？ / *k*<sub>)</sub>                                             |
| GL \_ DST \_ ALPHA             |  (** <sub>d</sub>  /  *k*<sub>a</sub> 、 *a*<sub>d</sub>  /  *k*<sub>a</sub> 、 ** <sub>d</sub>  /  *k*<sub>a</sub> 、 *a*<sub>d</sub>  /  *k*<sub>a</sub> )              |
| GL \_ 1 \_ 減去 \_ DST \_ ALPHA |  (1，1，1，1)  (*A*<sub>d</sub>  /  *k*<sub>a</sub> 、 *a*<sub>d</sub>k a、d  /   <sub></sub>  <sub></sub>  /  *k*<sub>a</sub> 、 *a*<sub>d</sub>  /  *k*<sub>a</sub> )  |
| GL \_ SRC \_ ALPHA \_ 飽和   |  (*i、i、i、* 1)                                                                                                                                                  |



 

在表格中，

*i* = 最小 (*A*？ ， *k*<sub>a</sub>   -  *a*<sub>d</sub> ) / *k*<sub>a</sub>

若要在以 RGBA 模式繪製時判斷圖元的混合 RGBA 值，系統會使用下列方程式：

*R* (*d*) = min ( *k*<sub>r</sub> 、 *r*？*s*<sub>r</sub>  +  *r*<sub>d</sub> ** <sub>r</sub> ) 

*G* (*d*) = min ( *k*<sub>g g</sub> *？**s*<sub>g</sub>  +  *g*<sub>d</sub> *d*<sub>g</sub> ) 

*B* (*d*) = min ( *k*<sub>b</sub> *，b*？*s*<sub>b</sub>  +  *b*<sub>d</sub> *d*<sub>b</sub> ) 

*(* *d*) = min ( *k*<sub>a</sub> *？**s*<sub>a a</sub>  +  *a*<sub>d</sub> *a* <sub></sub> ) 

儘管上述方程式有明顯的精確度，但不會完全指定混合算術，因為混合的運算會以不精確的整數色彩值來運作。 不過，應該等於1的 blend 因數保證不會修改其被乘數，而 blend 因數等於零則會將其被乘數減少為零。 因此，例如，當 *sfactor* 為 gl \_ src Alpha 時 \_ ， *dfactor* 是 gl \_ 1 \_ 減去 \_ SRC \_ ALPHA，而 *A*？等於 *k*<sub>A</sub>，則方程式會減少為簡單的取代：

*R*<sub>d</sub>  =  *r*？

*G*<sub>d</sub>  =  *g*？

B <sub>d</sub>  =  *b*？

*A*<sub>d</sub>  =  *a*？

## <a name="examples"></a>範例

透明度最適合使用 **glBlendFunc** (GL \_ SRC \_ Alpha、gl \_ 1 \_ 減去 \_ SRC \_ Alpha) ，基本專案從最遠到最接近。 請注意，這個透明度計算不需要在畫面格緩衝區中出現 Alpha bitplanes。

您也可以使用 **glBlendFunc** (GL \_ SRC \_ Alpha、gl \_ 1 \_ 減去 \_ SRC \_ Alpha) ，以任意順序呈現反鋸齒的點和線條。

若要將多邊形消除鋸齒優化，請使用 **glBlendFunc** (GL \_ SRC \_ \_ \_) ALPHA  (查看 \_ glEnable 中的 GL 多邊形 \_ 平滑[](glenable.md)引數，以取得有關多邊形消除鋸齒的資訊 ) 。必須要有這個 blend 函式的 bitplanes 目的地 Alpha，才能正常運作，請儲存累積的涵蓋範圍。

傳入的 (來源) Alpha 是一種材質不透明度，範圍從 1.0 (*K*<sub>) ，</sub> 代表完整的不透明度，到 0.0 (0) ，代表完整的透明度。

當您為繪圖啟用一個以上的色彩緩衝區時，每個啟用的緩衝區都會個別混合，而緩衝區的內容會用於目的地色彩。  (參閱 [**glDrawBuffer**](gldrawbuffer.md)。 ) 

混色只會影響 RGBA 轉譯。 色彩索引轉譯器會忽略它。

下列函式會取出與 **glBlendFunc** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ BLEND \_ SRC 的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ BLEND \_ DST 的 glGet

[](glisenabled.md)具有引數 GL \_ BLEND 的 glIsEnabled

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

[**glClear**](glclear.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





