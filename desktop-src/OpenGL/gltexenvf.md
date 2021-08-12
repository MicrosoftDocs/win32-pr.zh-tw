---
title: 'glTexEnvf 函式 (Gl) '
description: GlTexEnvf 函式會設定紋理環境參數。
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- glTexEnvf 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4914ae05496c0234adb0b6604f4f75eb630af525b08ccae2825e032d5f97535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613650"
---
# <a name="gltexenvf-function"></a>glTexEnvf 函式

**GlTexEnvf** 函式會設定紋理環境參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

紋理環境。 必須是 GL \_ 紋理 \_ 環境。

</dd> <dt>

*pname* 
</dt> <dd>

單一值紋理環境參數的符號名稱。 必須是 GL \_ 紋理 \_ 環境 \_ 模式。

</dd> <dt>

*param* 
</dt> <dd>

單一符號常數，其中一個 GL \_ lambert、gl \_ DECAL、gl \_ BLEND 或 gl \_ 取代。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *target* 或 *pname* 不是其中一個可接受的定義值，或當 *params* 應該有定義的常數值 (根據 *pname*) 的值而不是時。<br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>                                             |



## <a name="remarks"></a>備註

材質環境指定當片段有紋理時，材質值的轉譯方式。 *目標* 參數必須是 GL \_ 紋理 \_ 環境。 *Pname* 參數為 GL \_ 紋理 \_ 環境 \_ 模式。 已定義三個材質函數： GL \_ lambert、gl \_ DECAL 和 GL \_ BLEND。

材質函式會使用適用于片段的材質影像值，在片段上作用 (查看 [**glTexParameter**](gltexparameter-functions.md)) 並產生該片段的 RGBA 色彩。 下表顯示如何為每個可選擇的材質函數產生 RGBA 色彩。 *C* 是三倍的色彩值 (RGB) ，而 *a* 是相關聯的 Alpha 值。 從材質影像解壓縮的 RGBA 值位於 \[ 0、1的範圍內 \] 。 注標 *f* 指的是傳入片段、紋理影像的注標 *t* 、紋理環境色彩的注標 *c* ，以及注標 *v* 表示紋理函式所產生的值。

材質影像的每個材質元素最多可有四個元件 (查看 [**glTexImage1D**](glteximage1d.md) 和 [**glTexImage2D**](glteximage2d.md)) 。 在一個元件的影像中，Lt 表示單一元件。 雙元件映射使用 *L？*  和 *答？* . 三個元件的影像只有一個色彩值 *C？* . 四個元件的影像同時具有色彩值 *C？*  和 Alpha 值 *A？* .



<table>
<thead>
<tr class="header">
<th>元件數目</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">1 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  = <em>L？</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">未定義 $ {REMOVE} $<br />
</td>
<td><em>C</em> <em><sub>v</sub></em>  =  <em> (1</em> - <em>L？</em> <em>) C<sub>f</sub> </em> + <em>L？</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></td>
<td><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2 $ {移除} $<br />
</td>
<td><em>C<sub>v</sub> </em>  = <em>L？</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">未定義 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  = <em> (1</em> - <em>L？</em> <em>) C<sub>f</sub> </em> + <em>L？</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></td>
<td><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3 $ {移除} $<br />
</td>
<td><em>C<sub>v</sub> </em>  = <em>C？</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  = <em>C？</em></td>
<td rowspan="2">未定義 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em> </td>
<td><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  = <em>C？</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1- <em>A？</em> <em>) C<sub>f</sub> </em> + <em>A？</em> <em>C？</em></td>
<td rowspan="2">未定義 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  = <em>答：</em> <em><sub>F</sub></em> </td>
<td><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></td>


</tr>
</tbody>
</table>



 

GL \_ 紋理 \_ ENV \_ 模式預設為 gl \_ lambert。

下列函式會抓取 **glTexEnvf** 的相關資訊：

[**glTexGetEnvfv**](glgettexenvfv.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





