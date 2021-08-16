---
title: 'glMateriali 函式 (Gl) '
description: TheglMateriali 函數會指定光源模型的材質參數。
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- glMateriali 函式 OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d850bac6b27672c00dca9b1cafa7b4664dbde5fca0085381b4b166e2106b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358862"
---
# <a name="glmateriali-function"></a>glMateriali 函式

**GlMateriali** 函數會指定光源模型的材質參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
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

要更新之臉部或臉部的單一值材質參數。 必須是 GL \_ 的反光。



| 值                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ 反光**</dt> </dl> | *Param* 參數是單一整數，可指定材質的 RGBA 反射指數。 整數值會直接對應。 只 \[ 接受範圍0，128中的值 \] 。 正面和背面材質的預設反射指數為0。 <br/> |



 

</dd> <dt>

*param* 
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

**GlMateriali** 函式會將值指派給材質參數。 有兩組相符的材質參數。 其中一個是 *front* 的集合，用來將點、線條、點陣圖和所有多邊形 (在停用雙面光源時，) ，或只是在) 啟用雙面光源 (時的多邊形。 另一組 [ *回溯*] 則是在啟用雙面光源的情況下，用來為向下多邊形加上陰影。 如需單面和雙面光源計算的詳細資料，請參閱 [**glLightModel**](gllightmodel-functions.md) 。

**GlMateriali** 函式會採用三個引數。 第一個是 *臉部*，指定是否 \_ 要修改 gl FRONT 教材、gl \_ 回材料，或 gl \_ 正面 \_ 和 \_ 背面材質。 第二個 *pname*，則會指定一或兩個集合中的哪一個參數將會被修改。 第三個 *參數* 會指定將指派給指定參數的值。

材質參數用於光源方程式，可選擇性地套用至每個頂點。 此方程式會在 [**glLightModel**](gllightmodel-functions.md)中討論。

您可以隨時更新材質參數。 尤其是，在呼叫 [**glBegin**](glbegin.md)和對應的 [**glEnd**](glend.md)呼叫之間，可以呼叫 **glMateriali** 。 不過，如果每個頂點只會變更單一材質參數，則 [**glColorMaterial**](glcolormaterial.md) 優先于 **glMateriali**。

下列函式會抓取 **glMateriali** 的相關資訊：

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

 

 





