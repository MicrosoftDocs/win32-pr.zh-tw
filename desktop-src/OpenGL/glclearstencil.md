---
title: 'glClearStencil 函式 (Gl) '
description: GlClearStencil 函數會指定樣板緩衝區的清除值。
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- glClearStencil 函式 OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4749a8d9c4844bd95181a7353bb0ce4559001fa47164fec3dbab5c188de8d994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618028"
---
# <a name="glclearstencil-function"></a>glClearStencil 函式

**GlClearStencil** 函數會指定樣板緩衝區的清除值。

## <a name="syntax"></a>語法


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*s* 
</dt> <dd>

清除樣板緩衝區時使用的索引。 預設值為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlClearStencil** 函數會指定 [**glClear**](glclear.md)用來清除樣板緩衝區的索引。 *S* 參數的遮罩是 2 <sup>m</sup> -1，其中 *m* 是樣板緩衝區中的位數。

下列函式會取出與 **glClearStencil** 函數相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 樣板 \_ CLEAR \_ 值的 glGet

具有引數 GL \_ 樣板 \_ 位的 glGet

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





