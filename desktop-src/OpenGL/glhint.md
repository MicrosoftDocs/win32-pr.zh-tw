---
title: 'glHint 函式 (Gl) '
description: GlHint 函式會指定實作為特定的提示。
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glHint 函式 OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7602b4f0af35c8bc9aeb38cdcb613e30ded907ced75e2241c8ed9e23b57fd98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359644"
---
# <a name="glhint-function"></a>glHint 函式

**GlHint** 函式會指定實作為特定的提示。

## <a name="syntax"></a>語法


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

指出要控制之行為的符號常數。 接受下列符號常數以及建議的語法。



| 值                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**GL \_ 霧化 \_ 提示**</dt> </dl>                                                           | 表示霧化計算的精確度。 如果 OpenGL 執行不能有效率地支援每個圖元的霧化計算，則提示 GL 不 \_ \_ 在意或 GL \_ 最快可能會導致每個頂點的霧化效果計算。<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**GL \_ 行 \_ 平滑 \_ 提示**</dt> </dl>                                  | 指出反鋸齒線條的取樣品質。 如果套用 \_ 較大的篩選函式，提示 GL 最好可能會導致在點陣化期間產生更多圖元片段。<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**GL \_ 透視圖 \_ 校正 \_ 提示**</dt> </dl> | 指出色彩和材質座標插補的品質。 如果 OpenGL 修正程式未有效率地支援以觀點校正的參數插補，則提示 GL 不 \_ \_ 在意或 GL 最快的方式， \_ 會導致色彩和/或紋理座標的簡單線性插補。<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**GL \_ 點 \_ 平滑 \_ 提示**</dt> </dl>                               | 指出反鋸齒點的取樣品質。 如果套用 \_ 較大的篩選函式，提示 GL 最好可能會導致在點陣化期間產生更多圖元片段。<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**GL \_ 多邊形 \_ 平滑 \_ 提示**</dt> </dl>                         | 指出反鋸齒多邊形的取樣品質。 如果套用 \_ 較大的篩選函式，提示 GL 最好可能會導致在點陣化期間產生更多圖元片段。<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

表示所需行為的符號常數。 接受下列符號常數。



| 值                                                                                                                                                       | 意義                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ 最快**</dt> </dl>        | 您應該選擇最有效率的選項。<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL \_ 最好**</dt> </dl>           | 您應該選擇最正確或最高品質的選項。<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**GL \_ 別 \_ 在意**</dt> </dl> | 用戶端沒有喜好設定。<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 或 *模式* 不是可接受的值。<br/>                                                                              |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

當有足夠的解讀空間時，您可以使用提示來控制 OpenGL 行為的特定層面。 您可以指定具有兩個引數的提示。 *目標* 參數是指出要控制之行為的符號常數，而 *模式* 則是另一個指出所需行為的符號常數。

雖然可以提示的實方面是妥善定義的，但提示的解讀取決於執行。

可以忽略 **glHint** 函數。

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
</dt> </dl>

 

 





