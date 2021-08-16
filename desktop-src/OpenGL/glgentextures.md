---
title: 'glGenTextures 函式 (Gl) '
description: GlGenTextures 函式會產生材質名稱。
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glGenTextures 函式 OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28275bef054b26c2145ab9779ec776297ac7838d0313769123fb1be904a3bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625228"
---
# <a name="glgentextures-function"></a>glGenTextures 函式

**GlGenTextures** 函式會產生材質名稱。

## <a name="syntax"></a>語法


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

要產生的材質名稱數目。

</dd> <dt>

*紋理* 
</dt> <dd>

陣列的第一個元素的指標，其中會儲存產生的材質名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *n* 為負數值。<br/>                                                                                                  |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGenTextures** 函數會在 *材質* 參數中傳回 *n* 個材質名稱。 紋理名稱不一定是連續的整數集合，不過，在呼叫 **glGenTextures** 函式之前，不會立即使用任何傳回的名稱。 產生的材質會假設紋理目標的維度維度會先與 [**glBindTexture**](glbindtexture.md) 函數系結。 後續的 **glGenTextures** 呼叫不會傳回 **glGenTextures** 所傳回的材質名稱，除非先藉由呼叫 [**glDeleteTextures**](gldeletetextures.md)來刪除它們。

您無法在顯示清單中包含 **glGenTextures** 。

> [!Note]  
> **GlGenTextures** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

下列函式會抓取 **glGenTextures** 的相關資訊：

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





