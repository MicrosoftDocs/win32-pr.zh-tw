---
title: 'glMaterialiv 函式 (Gl) '
description: GlMaterialiv 函數會指定光源模型的材質參數。
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
keywords:
- glMaterialfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95f12a5d34357a3436ffd6725ad2f1d56901e700
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384466"
---
# <a name="glmaterialiv-function"></a>glMaterialiv 函式

**GlMaterialiv** 函數會指定光源模型的材質參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glMaterialfv(
         GLenum face,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*臉* 
</dt> <dd>

正在更新的臉部或臉部。 必須是下列其中一項： GL \_ front、gl \_ BACK 或 gl \_ front 和 gl \_ 回來。

</dd> <dt>

*pname* 
</dt> <dd>

要更新之臉部或臉部的材質參數。 您可以使用 [**glMaterialiv**](glmaterialfv.md)來指定參數，並以光源方程式進行解讀，如下所示。



| 值                                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ 環境**</dt> </dl>                                       | Params 參數包含四個整數值，可指定材質的環境 RGBA 反射率。 整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。 浮點值會直接對應。 整數和浮點值都不是壓制。 適用于 front 和後端材質的預設環境反射率是 (0.2、0.2、0.2、1.0) 。 <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ 擴散**</dt> </dl>                                       | Params 參數包含四個整數值，可指定材質的擴散 RGBA 反射率。 整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。 浮點值會直接對應。 整數和浮點值都不是壓制。 適用于 front 和後端材質的預設擴散反射率是 (0.8、0.8、0.8、1.0) 。 <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ 反射**</dt> </dl>                                    | Params 參數包含四個整數值，可指定材質的反射 RGBA 反射率。 整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。 浮點值會直接對應。 整數和浮點值都不是壓制。 適用于 front 和後端材質的預設反射反射率是 (0.0、0.0、0.0、1.0) 。 <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**GL \_ 排放**</dt> </dl>                                    | Params 參數包含四個整數值，可指定針對材質發出的 RGBA 濃度。 整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。 浮點值會直接對應。 整數和浮點值都不是壓制。 正面和後端材質的預設發射濃度是 (0.0、0.0、0.0、1.0) 。 <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ 反光**</dt> </dl>                                 | *Param* 參數是單一整數，可指定材質的 RGBA 反射指數。 整數值會直接對應。 只 \[ 接受範圍0，128中的值 \] 。 正面和背面材質的預設反射指數為0。 <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**GL \_ 環境 \_ 和 \_ 擴散**</dt> </dl> | 相當於使用相同的參數值呼叫 [**glMaterial**](glmaterial-functions.md) 兩次，一次使用 gl \_ 環境，一次使用 gl \_ 擴散。 <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**GL \_ 色彩 \_ 索引**</dt> </dl>                    | Params 參數包含三個整數值，可指定環境、擴散和反射光源的色彩索引。 這三個值，以及 GL \_ 反光，是色彩索引模式光源方程式所使用的唯一材質值。 如需色彩索引光源的討論，請參閱 [**glLightModel**](gllightmodel-functions.md) 。<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

將設定參數 GL 反光的值 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                              | 意義                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>  | *臉部* 或 *pname* 都不是可接受的值。<br/>                |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | \[已指定0、128範圍以外的反射指數 \] 。<br/> |



## <a name="remarks"></a>備註

[**GlMaterialiv**](glmaterialf.md)函式會將值指派給材質參數。 有兩組相符的材質參數。 其中一個是 *front* 的集合，用來將點、線條、點陣圖和所有多邊形 (在停用雙面光源時，) ，或只是在) 啟用雙面光源 (時的多邊形。 另一組 [ *回溯*] 則是在啟用雙面光源的情況下，用來為向下多邊形加上陰影。 如需單面和雙面光源計算的詳細資料，請參閱 [**glLightModel**](gllightmodel-functions.md) 。

[**GlMaterialiv**](glmaterialf.md)函式會採用三個引數。 第一個是 *臉部*，指定是否 \_ 要修改 gl FRONT 教材、gl \_ 回材料，或 gl \_ 正面 \_ 和 \_ 背面材質。 第二個 *pname*，則會指定一或兩個集合中的哪一個參數將會被修改。 第三個 *參數* 會指定將指派給指定參數的值。

材質參數用於光源方程式，可選擇性地套用至每個頂點。 此方程式會在 [**glLightModel**](gllightmodel-functions.md)中討論。

您可以隨時更新材質參數。 尤其是，在呼叫 [**glBegin**](glbegin.md)和對應的 [**glEnd**](glend.md)呼叫之間，可以呼叫 [**glMaterialiv**](glmaterialf.md) 。 不過，如果每個頂點只會變更單一材質參數，則 [**glColorMaterial**](glcolormaterial.md) 優先于 **glMaterialiv**。

下列函式會抓取 [**glMaterialiv**](glmaterialf.md)的相關資訊：

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





