---
title: 'glStencilMask 函式 (Gl) '
description: GlStencilMask 函數控制樣板平面中個別位的寫入。
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- glStencilMask 函式 OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106398"
---
# <a name="glstencilmask-function"></a>glStencilMask 函式

**GlStencilMask** 函數控制樣板平面中個別位的寫入。

## <a name="syntax"></a>語法


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*面具* 
</dt> <dd>

用來啟用和停用在樣板平面中寫入個別位的位元遮罩。 一開始，遮罩就是所有的遮罩。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlStencilMask** 函數控制樣板平面中個別位的寫入。 最不重要的 *n* 位 *遮罩*，其中 *n* 是樣板緩衝區中的位數，指定遮罩。 當遮罩中出現一個時，會讓樣板緩衝區中的對應位成為可寫入的位置。 如果出現零，則位為寫入保護。 一開始，所有位都會啟用寫入。

下列函式會取出與 **glStencilMask** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 樣板 \_ WRITEMASK 的 glGet

具有引數 GL 樣板位的 glGet \_ \_

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





