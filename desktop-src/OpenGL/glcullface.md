---
title: 'glCullFace 函式 (Gl) '
description: GlCullFace 函式會指定是否可以挑選正面或後端面向的 facet。
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glCullFace 函式 OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934027"
---
# <a name="glcullface-function"></a>glCullFace 函式

**GlCullFace** 函式會指定是否可以挑選正面或後端面向的 facet。

## <a name="syntax"></a>語法


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

指定正面或後端面向是否為剔除的候選項目。 接受符號常數 GL \_ 前端、gl \_ 背面和 gl \_ 前端 \_ 和 \_ 後端。 預設值為 [GL \_ 回]。

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

**GlCullFace** 函式會指定在啟用 Facet 剔除時，) 由 *模式* 所指定 (的正面或後端 facet 是否為挑選。 您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配引數 GL 剔除臉部來啟用和停用 facet 剔除 \_ \_ 。 Facet 包括三角形、quadrilaterals、多邊形和矩形。

[**GlFrontFace**](glfrontface.md)函式會指定順向和逆時針的 facet 為正面和反向的面向。

如果 *模式* 是 GL \_ 前端 \_ 和 \_ 後端，則不會繪製任何 facet，但會繪製其他基本專案，例如點和線條。

下列函式會取出與 **glCullFace** 相關的資訊：

具有引數 GL 的 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)會 \_ 挑選 \_ 臉部 \_ 模式

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 挑選 \_ 臉部

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFrontFace**](glfrontface.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





