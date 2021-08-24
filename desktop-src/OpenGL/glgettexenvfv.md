---
title: 'glGetTexEnvfv 函式 (Gl) '
description: 'GlGetTexEnvfv 和 glGetTexEnviv 函數會傳回紋理環境參數。 |glGetTexEnvfv 函式 (Gl) '
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- glGetTexEnvfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnvfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b9b294879711662c67f9ab581e89eaadfa620363e1d19e93f7ea686ba7453a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493868"
---
# <a name="glgettexenvfv-function"></a>glGetTexEnvfv 函式

**GlGetTexEnvfv** 和 [**glGetTexEnviv**](glgettexenviv.md)函數會傳回紋理環境參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetTexEnvfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
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

紋理環境參數的符號名稱。 接受下列值。



| 值                                                                                                                                                                                | 意義                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**GL \_ 紋理 \_ 環境 \_ 模式**</dt> </dl>    | *Params* 參數會傳回單一值紋理環境模式，也就是一個符號常數。<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**GL \_ 紋理 \_ 環境 \_ 色彩**</dt> </dl> | *Params* 參數會傳回四個整數或浮點值，也就是材質環境的色彩。 在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應至最正面的可表示整數，而-1.0 對應至最大的可表示整數。<br/> |



 

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
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *target* 或 *pname* 不是可接受的值。<br/>                                                                             |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetTexEnv** 函式會傳回以 *params* 選取的材質環境值（以 [**glTexEnv**](gltexenv-functions.md)指定）。 *Target* 參數指定紋理環境。 目前只定義並支援一個材質環境： GL \_ 紋理 \_ ENV。

*Pname* 參數會命名特定的材質環境參數。

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

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





