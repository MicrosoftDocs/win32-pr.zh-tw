---
title: 'glGetMaterialiv 函式 (Gl) '
description: 'GlGetMaterialfv 和 glGetMaterialiv 函數會傳回材質參數。 |glGetMaterialiv 函式 (Gl) '
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- glGetMaterialiv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df6babcac908d59c5a5a51b0a23736b760ed25ec542f58339182d3a7536050be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360072"
---
# <a name="glgetmaterialiv-function"></a>glGetMaterialiv 函式

[**GlGetMaterialfv**](glgetmaterialfv.md)和 **glGetMaterialiv** 函數會傳回材質參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetMaterialiv(
   GLenum face,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*臉* 
</dt> <dd>

指定要查詢的兩個材質中的哪一個。 \_已接受 GL 前或 gl \_ 回，分別代表 front 和 BACK 教材。

</dd> <dt>

*pname* 
</dt> <dd>

要傳回的材質參數。 接受下列值。



| 值                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ 環境**</dt> </dl>                    | *Params* 參數會傳回四個整數或浮點值，代表材質的環境反射率。 在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。 如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ 擴散**</dt> </dl>                    | *Params* 參數會傳回四個整數或浮點值，代表材質的擴散反射率。 在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。 如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ 反射**</dt> </dl>                 | *Params* 參數會傳回四個整數或浮點值，代表材質的反射反射率。 在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。 如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**GL \_ 排放**</dt> </dl>                 | *Params* 參數會傳回四個整數或浮點值，代表所發出之材質的亮度。 在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。 如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ 反光**</dt> </dl>              | *Params* 參數會傳回代表材質反射指數的一個整數或浮點值。 在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**GL \_ 色彩 \_ 索引**</dt> </dl> | *Params* 參數會傳回三個整數或浮點值，代表材質的環境、擴散和反射索引。 這些索引只能用於色彩索引光源。  (其他參數都只用于 RGBA 光源。在要求時，) 整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。<br/>                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

傳回要求的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 或 *查詢* 不是可接受的值。<br/>                                                                             |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetMaterial** 函式會以 *params* *傳回材質的* 參數 *pname* 值或值。

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

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





