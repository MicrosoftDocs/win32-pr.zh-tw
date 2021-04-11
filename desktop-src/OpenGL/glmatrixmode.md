---
title: 'glMatrixMode 函式 (Gl) '
description: GlMatrixMode 函數會指定哪一個矩陣是目前的矩陣。
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- glMatrixMode 函式 OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104681"
---
# <a name="glmatrixmode-function"></a>glMatrixMode 函式

**GlMatrixMode** 函數會指定哪一個矩陣是目前的矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

矩陣堆疊，也就是後續矩陣作業的目標。 *Mode* 參數可以採用三個值的其中一個。



| 值                                                                                                                                                         | 意義                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <dt>**GL \_ 模型**</dt> </dl>    | 將後續矩陣作業套用至模型矩陣堆疊。<br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <dt>**GL \_ 投射**</dt> </dl> | 將後續矩陣作業套用至投射矩陣堆疊。<br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <dt>**GL \_ 材質**</dt> </dl>          | 將後續矩陣作業套用至材質矩陣堆疊。<br/>    |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlMatrixMode** 函數會設定目前的矩陣模式。

下列函式會抓取 **glMatrixMode** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet

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

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





