---
title: 'glClear 函式 (Gl) '
description: GlClear 函式會清除緩衝區來設定預設值。
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- glClear 函式 OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb48a1b2832a5f9c046bb450b7cfba9ec4f83a759b093df91f3ec2064f23a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082098"
---
# <a name="glclear-function"></a>glClear 函式

**GlClear** 函式會清除緩衝區來設定預設值。

## <a name="syntax"></a>語法


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*面具* 
</dt> <dd>

遮罩的位 OR 運算子，表示要清除的緩衝區。 四個遮罩如下所示。



| 值                                                                                                                                                                                   | 意義                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**GL \_ 色彩 \_ 緩衝區 \_ 位**</dt> </dl>       | 目前已啟用色彩寫入的緩衝區。<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**GL \_ 深度 \_ 緩衝區 \_ 位**</dt> </dl>       | 深度緩衝區。<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**GL \_ ACCUM \_ 緩衝區 \_ 位**</dt> </dl>       | 累積緩衝區。<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**GL \_ 樣板 \_ 緩衝區 \_ 位**</dt> </dl> | 樣板緩衝區。<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | 在 *遮罩* 中設定四個定義位以外的任何位。<br/>                                                                |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlClear** 函式會將視窗的 bitplane 區域設定為先前由 [**glClearColor**](glclearcolor.md)、 [**glClearIndex**](glclearindex.md)、 [**glClearDepth**](glcleardepth.md)、 [**glClearStencil**](glclearstencil.md)和 [**glClearAccum**](glclearaccum.md)所選取的值。 您可以使用 [**glDrawBuffer**](gldrawbuffer.md)一次選取一個以上的緩衝區，以同時清除多個色彩緩衝區。

圖元擁有權測試、剪下測試、遞色和緩衝區 writemasks 都會影響 **glClear** 的作業。 剪式方塊會將已清除的區域界限。 **GlClear** 函式會忽略 Alpha 函數、blend 函式、邏輯運算、stenciling、材質對應和 *z* 緩衝。

**GlClear** 函式會採用單一引數 (*mask*) 這是數個值的位 or，表示要清除的緩衝區。

每個緩衝區清除的值取決於該緩衝區的清除值設定。

如果緩衝區不存在，則在該緩衝區導向的 **glClear** 呼叫不會有任何作用。

下列函式會取出與 **glClear** 相關的資訊：

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ ACCUM \_ CLEAR \_ 值

具有引數 GL \_ 深度 \_ 清除 \_ 值的 glGet

具有引數 GL \_ 索引 \_ 清除 \_ 值的 glGet

具有引數 GL \_ 色彩 \_ 清除 \_ 值的 glGet

具有引數 GL \_ 樣板 \_ CLEAR \_ 值的 glGet

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

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glClearColor**](glclearcolor.md)
</dt> <dt>

[**glClearDepth**](glcleardepth.md)
</dt> <dt>

[**glClearIndex**](glclearindex.md)
</dt> <dt>

[**glClearStencil**](glclearstencil.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> </dl>

 

 





