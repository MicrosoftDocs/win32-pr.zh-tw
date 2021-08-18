---
title: 'glTexGeniv 函式 (Gl) '
description: '控制材質座標的產生。 |glTexGeniv 函式 (Gl) '
ms.assetid: e95f2844-414a-4fb2-944e-4d0b6e51bdd2
keywords:
- glTexGeniv 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexGeniv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7caffbcf71b09f31fd05c1252471f7da2a66e5bc01e532dfb6c71563545779e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519748"
---
# <a name="gltexgeniv-function"></a>glTexGeniv 函式

控制材質座標的產生。

## <a name="syntax"></a>語法


```C++
void WINAPI glTexGeniv(
         GLenum coord,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*coord* 
</dt> <dd>

材質座標。 必須是下列其中一項： GL \_ S、gl \_ T、gl \_ R 或 GL \_ Q。

</dd> <dt>

**pname** 
</dt> <dd>

紋理座標產生函數的符號名稱。

</dd> <dt>

*params* 
</dt> <dd>

陣列，其中包含對應材質產生函數的係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *coord* 或 *pname* 不是接受的定義值，或 *pname* 是 GL \_ 材質 \_ GEN \_ 模式，而 *params* 不是接受的定義值。<br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。 <br/>                 |



## <a name="remarks"></a>備註

**GlTexGen** 函式會選取材質座標產生函數或提供其中一個函數的係數。 *Coord* 參數會命名其中一個 (s、t、r、q) 材質座標，而且必須是下列其中一個符號： GL \_ s、GL \_ t、gl \_ r 或 gl \_ q。 *Pname* 參數必須是三個符號常數的其中一種： gl \_ 紋理內 \_ 代 \_ 模式、gl \_ 物件 \_ 平面或 gl \_ 眼 \_ 平面。 如果 *pname* 是 gl \_ 物件 \_ 平面或 gl \_ 眼 \_ 平面， *param* 就會包含對應材質產生函數的係數。

如果材質產生函數是 GL \_ 物件 \_ 線性，函式

![當材質產生函數 GL_OBJECT_LINEAR 時，顯示 glTexGen 函式的方程式。]

會使用，其中 g 是針對以 coord 命名的座標計算的值;p1、p2、p3 和 p4 是在 params 中提供的四個值;和 x？、y？、z？以及 w？是頂點的物件座標。 您可以使用此函式來紋理對應地形，方法是使用海平面作為參考平面， (p1、p2、p3 和 p4) 所定義。 GL \_ 物件 \_ 線性座標產生函數會將地形頂點的高度計算為其與海平面之間的距離，而該海拔高度則是用來編制紋理影像的索引，以將白色的上階對應到尖峰，而將綠色草對應至 foothills。

如果材質產生函式為 GL \_ 眼 \_ 線性，則函式會

![當材質產生函數 GL_EYE_LINEAR 時，顯示 glTexGen 函式的方程式。]

使用

![顯示頂點眼睛座標的方程式。](images/tex03.png)

和 x？、y？、z？以及 w？頂點、p1、p2、p3 和 p4 的眼睛座標是在 *param* 中提供的值，而當您呼叫 **GlTexGen** 時，M 是模型矩陣。 如果 M 的條件式或單數不佳，則產生的函式所產生的材質座標可能不正確或未定義。

請注意， *param* 中的值會以眼睛座標定義參考平面。 當多邊形頂點轉換時，套用至它們的模型矩陣可能不會是相同的結果。 此函式會建立可在移動物件上產生動態輪廓線的材質座標欄位。

如果 *pname* 為 gl \_ 球體 \_ 地圖，而 *COORD* 為 gl \_ S 或 gl \_ T，則會產生 S 和 T 紋理座標，如下所示。 讓 u 成為從原點指向多邊形頂點的單位向量)  (眼睛座標。 在轉換為眼睛座標之後，讓 n 成為目前的正常情況。 讓 f = (fx ( ) 年度 ( ) fz) T 是反映向量，

![顯示反映向量作為單位向量和目前一般標準函式的方程式。](images/tex05.png)

最後，讓我們

![顯示 m 的方程式，表示為反映向量的函式。](images/tex07.png)

然後，指派給 i 和 t 紋理座標的值為

![顯示指派給 i 和 t 材質座標之值的方程式。](images/tex06.png)

您可以使用 [**glEnable**](glenable.md) 或 [**glDisable**](gldisable.md) 搭配其中一個符號材質座標名稱 (GL \_ 材質 \_ gen \_ 、gl \_ 材質 \_ gen \_ T、GL \_ 材質 \_ gen \_ R 或 gl \_ 材質 \_ gen \_ Q) 作為引數，以啟用或停用材質座標產生函數。 啟用此函式時，會根據與該座標相關聯的產生函數來計算指定的材質座標。 停用此函式時，後續頂點會從目前的材質座標集合取得指定的材質座標。 一開始，所有材質產生函數都會設定為 GL \_ 眼 \_ 線性，並停用。 這兩個平面方能 (1、0、0、0) ;這兩個 t 平面方能 (0、1、0、0) ;和所有 r 和 q 平面方能 (0、0、0、0) 。

下列函式會取出與 glTexGen 相關的資訊：

<dl>

[**glGetTexGen**](glgettexgen.md)  
[](glisenabled.md)具有引數 GL \_ 材質 \_ GEN \_ S 的 glIsEnabled  
[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 材質 \_ GEN \_ T  
[](glisenabled.md)具有引數 GL \_ 材質 \_ GEN \_ R 的 glIsEnabled  
[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 材質 \_ GEN 的 \_ Q  
</dl>

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

[**glEnd**](glend.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[glTexParameter](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





