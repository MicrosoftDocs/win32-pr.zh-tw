---
title: 'glGetLightfv 函式 (Gl) '
description: 'GlGetLightfv 和 glGetLightiv 函數會傳回燈光來源參數值。 |glGetLightfv 函式 (Gl) '
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- glGetLightfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetLightfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf90cb9567822ef578bdf01805648a2dabd02db
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853668"
---
# <a name="glgetlightfv-function"></a>glGetLightfv 函式

**GlGetLightfv** 和 [**glGetLightiv**](glgetlightiv.md)函數會傳回燈光來源參數值。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetLightfv(
   GLenum  light,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*light* 
</dt> <dd>

燈光來源。 可能的燈光數目取決於執行，但至少有8個燈支援。 其識別方式是以 GL 燈的符號名稱 \_ 來 *識別，* 其中 0 = *i* < GL \_ 最大 \_ 燈。

</dd> <dt>

*pname* 
</dt> <dd>

*Light* 的光源參數。 接受下列符號名稱。



| 值                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ 環境**</dt> </dl>                                            | *Params* 參數會傳回四個整數或浮點值，代表光線來源的環境濃度。 在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。 如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ 擴散**</dt> </dl>                                            | *Params* 參數會傳回四個整數或浮點值，代表光線來源的擴散濃度。 在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。 如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ 反射**</dt> </dl>                                         | *Params* 參數會傳回四個整數或浮點值，代表光線來源的反射濃度。 在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。 如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**GL \_ 位置**</dt> </dl>                                         | *Params* 參數會傳回四個整數或浮點值，代表光線來源的位置。 在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。 傳回的值是以眼睛座標維持的值。 除非模型矩陣是在呼叫 **glLight** 時所識別，否則它們不會等於使用 [**glLight**](gllight-functions.md)所指定的值。<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**GL \_ 點 \_ 方向**</dt> </dl>                      | *Params* 參數會傳回三個整數或浮點值，代表光線來源的方向。 在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。 傳回的值是以眼睛座標維持的值。 除非模型矩陣是在呼叫 **glLight** 時所識別，否則它們不會等於使用 **glLight** 所指定的值。 雖然在光源方向會在使用於光源方程式之前正規化，但傳回的值是正規化之前所指定值的轉換版本。<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL \_ 點 \_ 指數**</dt> </dl>                         | *Params* 參數會傳回代表光線點指數的單一整數或浮點值。 當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ 點 \_ 截止**</dt> </dl>                               | *Params* 參數會傳回單一整數或浮點值，代表光線的點截止角度。 當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**GL \_ 常數 \_ 衰減**</dt> </dl>    | *Params* 參數會傳回單一整數或浮點值，表示光源的常數 (非距離相關的) 衰減。 當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**GL \_ 線性 \_ 衰減**</dt> </dl>          | *Params* 參數會傳回單一整數或浮點值，代表光線的線性衰減。 當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**GL \_ 二次 \_ 衰減**</dt> </dl> | *Params* 參數會傳回單一整數或浮點值，代表光線的二次衰減。 當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

傳回要求的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GlGetLight** 函式會以 *參數* 值傳回 light 來源參數的值或值。 *Light* 參數會將燈光命名，而且是一種形式的符號名稱，也就是 gl light i 的符號名稱 \_ ，0 = *i* < gl ** \_ 最大光線 \_ ，其中 gl \_ 最大 \_ 光線是大於或等於八的實值相依常數。 *Pname* 參數會以符號名稱再次指定十個光源來源參數的其中一個。

這一律是 GL \_ 燈 = gl ** \_ LIGHT0 + *i* 的情況。

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

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





