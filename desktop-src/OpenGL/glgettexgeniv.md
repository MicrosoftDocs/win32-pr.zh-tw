---
title: 'glGetTexGeniv 函式 (Gl) '
description: 'GlGetTexGendv、glGetTexGenfv 和 glGetTexGeniv 函數會傳回材質座標產生參數。 |glGetTexGeniv 函式 (Gl) '
ms.assetid: 62c481d1-4862-43bb-9319-5a282c4e47d3
keywords:
- glGetTexGeniv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexGeniv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6eb9fbca41f8ad9fe9564c45f3ece21af58e5e16b7bb4ac85d0f6b1d2b428bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493768"
---
# <a name="glgettexgeniv-function"></a>glGetTexGeniv 函式

[**GlGetTexGendv**](glgettexgendv.md)、 [**glGetTexGenfv**](glgettexgenfv.md)和 **glGetTexGeniv** 函數會傳回材質座標產生參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetTexGeniv(
   GLenum coord,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*coord* 
</dt> <dd>

材質座標。 必須是 GL \_ S、gl \_ T、gl \_ R 或 gl \_ Q。

</dd> <dt>

*pname* 
</dt> <dd>

值 (s 的符號名稱，) 要傳回的值。 必須是 GL \_ 材質 \_ \_ 產生模式或其中一個材質產生平面方程式的名稱： GL \_ 物件 \_ 平面或 gl \_ 眼 \_ 平面。 這些值如下所示。



| 值                                                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**GL \_ 材質 \_ 產生 \_ 模式**</dt> </dl> | *Params* 參數會傳回單一值紋理產生函數（符號常數）。<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**GL \_ 物件 \_ 平面**</dt> </dl>              | *Params* 參數會傳回四個平面方程式係數，以指定物件線性座標產生。 整數值在要求時，會直接從內部浮點標記法對應。<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**GL \_ 眼 \_ 平面**</dt> </dl>                       | *Params* 參數會傳回四個平面方程式係數，以指定眼睛線性座標產生。 整數值在要求時，會直接從內部浮點標記法對應。 傳回的值是以眼睛座標維持的值。 除非模型矩陣是在呼叫 **glTexGen** 時所識別，否則它們不等於使用 [**glTexGen**](gltexgen-functions.md)所指定的值。<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

傳回要求的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *coord* 或 *pname* 不是可接受的值。<br/>                                                                              |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetTexGen** 函式會傳回您使用 **glTexGen** 指定之材質座標產生函數的 *params* 選取參數。 *Coord* 參數會使用符號常數 GL、 ** gl t **、   \_ \_ gl \_ r 或 gl q 來命名其中一個 (s、t、r、q) 材質座標 \_ 。

如果產生錯誤，則不會對 *參數* 的內容進行任何變更。

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

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





