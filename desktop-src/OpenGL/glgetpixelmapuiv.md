---
title: 'glGetPixelMapuiv 函式 (Gl) '
description: 'GlGetPixelMapfv、glGetPixelMapuiv 和 glGetPixelMapusv 函數會傳回指定的圖元對應。 |glGetPixelMapuiv 函式 (Gl) '
ms.assetid: a49f5fd2-c350-4acc-8f61-ecb92b0164cc
keywords:
- glGetPixelMapuiv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c017e7601e074c588aa534b6ea90aef79325ed4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992677"
---
# <a name="glgetpixelmapuiv-function"></a>glGetPixelMapuiv 函式

[**GlGetPixelMapfv**](glgetpixelmapfv.md)、 **glGetPixelMapuiv** 和 [**glGetPixelMapusv**](glgetpixelmapusv.md)函數會傳回指定的圖元對應。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetPixelMapuiv(
   GLenum map,
   GLuint *values
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*map* 
</dt> <dd>

要傳回的圖元對應名稱。 接受的值為 GL \_ 圖元 \_ 地圖 \_ i \_ 至 \_ i、gl \_ 圖元 \_ 地圖 \_ s \_ 、到 s、 \_ gl \_ 圖元 \_ 對應 \_ i \_ 到 \_ R、gl \_ 圖元 \_ 地圖 i 到 \_ \_ \_ G、gl 圖元對應 i \_ \_ \_ \_ 到 \_ b、gl 圖元對應 i 到 \_ \_ \_ \_ \_ a、gl 圖元地圖 \_ \_ \_ r \_ 至 R、 \_ gl 圖元地圖 \_ \_ \_ G \_ 至 \_ G、gl 圖元地圖 \_ \_ \_ b \_ 到 \_ b，而 gl 圖元會將 \_ \_ A 對應 \_ \_ 至 \_ 。

</dd> <dt>

*值* 
</dt> <dd>

傳回圖元地圖內容。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *地圖* 不是可接受的值。<br/>                                                                                           |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

如需 *map* 參數可接受值的描述，請參閱 [**glPixelMap**](glpixelmap.md) 。 **GlGetPixelMap** 函式會傳回 *map* 中所指定圖元地圖內容的 *值*。 在執行 [**glReadPixels**](glreadpixels.md)、 [**glDrawPixels**](gldrawpixels.md)、 [**glCopyPixels**](glcopypixels.md)、 [**glTexImage1D**](glteximage1d.md)和 [**glTexImage2D**](glteximage2d.md) 期間使用圖元地圖，以將色彩索引、樣板索引、色彩元件和深度元件對應至其他值。

不帶正負號的整數值（如有要求）會以線性方式從內部固定或浮點表示對應，使1.0 對應到最大的可表示整數值，0.0 則對應至零。 如果對應值不在0到1的範圍內，則不會定義傳回不帶正負號的整數值 \[ \] 。

若要判斷所需的 *地圖* 大小，請使用適當的符號常數來呼叫 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 。

如果產生錯誤，則不會對 *值* 的內容進行任何變更。

下列函式會取出與 **glGetPixelMap** 相關的資訊：

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 圖元 \_ 對應 \_ 我 \_ 的 \_ \_ 大小

將引數 GL \_ 圖元 \_ 對應 \_ \_ 到 \_ s \_ 大小的 glGet

使用引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ R \_ 大小的 glGet

使用引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ G \_ 大小的 glGet

**glGet** 與引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 B 的 \_ \_ 大小

**glGet** 與引數 GL \_ 圖元 \_ 對應 \_ I \_ 至 \_ \_ 大小

使用引數 GL \_ 圖元 \_ 地圖 \_ r \_ 至 \_ r \_ 大小的 glGet

具有引數 GL \_ 圖元 \_ 地圖 \_ g \_ 至 \_ g \_ 大小的 glGet

具有引數 GL \_ 圖元 \_ 地圖 \_ b \_ 到 \_ b \_ 大小的 glGet

具有引數 GL \_ 圖元 \_ 的 glGet 對應 \_ \_ 至 \_ \_ 大小

具有引數 GL \_ 最大 \_ 圖元 \_ 地圖 \_ 資料表的 glGet

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





