---
title: 'glDeleteTextures 函式 (Gl) '
description: GlDeleteTextures 函式會刪除已命名的材質。
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- glDeleteTextures 函式 OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408019d3bfe226c9e7ecdc2ea00182a0b11c78fa64a0210be658ded4556850cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617043"
---
# <a name="gldeletetextures-function"></a>glDeleteTextures 函式

**GlDeleteTextures** 函式會刪除已命名的材質。

## <a name="syntax"></a>語法


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

要刪除的材質數目。

</dd> <dt>

*紋理* 
</dt> <dd>

要刪除之材質的陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *n* 為負數值。<br/>                                                                                                  |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlDeleteTextures** 函式會刪除由陣列 *紋理* 的元素所命名的 *n* 紋理。 在刪除材質之後，它沒有任何內容或維度，而且其名稱可自由重複使用 (例如， **glGenTextures**) 。 **GlDeleteTextures** 函式會忽略未對應至現有材質的零和名稱。

如果刪除目前系結的材質，系結會還原為零 (預設材質) 。

您不能在顯示清單中包含 **glDeleteTextures** 的呼叫。

> [!Note]  
> **GlDeleteTextures** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

下列函式會抓取 **glDeleteTextures** 的相關資訊：

-   [**glIsTexture**](glistexture.md)

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





