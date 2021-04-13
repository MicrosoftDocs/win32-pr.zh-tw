---
title: 'glIsTexture 函式 (Gl) '
description: GlIsTexture 函式會判斷名稱是否對應至材質。
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- glIsTexture 函式 OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466637"
---
# <a name="glistexture-function"></a>glIsTexture 函式

**GlIsTexture** 函式會判斷名稱是否對應至材質。

## <a name="syntax"></a>語法


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*紋理* 
</dt> <dd>

值，這個值是材質的名稱。

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

如果 *材質* 參數目前是材質的名稱， **glIsTexture** 函數會傳回 GL \_ TRUE。 如果材質為零，則 **glIsTexture** 函數會傳回 GL \_ FALSE。  \_如果它是非零值，且不是材質的名稱，或發生錯誤時，它也會傳回 GL FALSE。

您不能在顯示清單中包含 **glIsTexture** 的呼叫。

> [!Note]  
> **GlIsTexture** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





