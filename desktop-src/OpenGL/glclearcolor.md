---
title: 'glClearColor 函式 (Gl) '
description: GlClearColor 函式會指定色彩緩衝區的明確值。
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glClearColor 函式 OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686017"
---
# <a name="glclearcolor-function"></a>glClearColor 函式

**GlClearColor** 函式會指定色彩緩衝區的明確值。

## <a name="syntax"></a>語法


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*紅* 
</dt> <dd>

[**GlClear**](glclear.md)用來清除色彩緩衝區的紅色值。 預設值為零。

</dd> <dt>

*綠色* 
</dt> <dd>

[**GlClear**](glclear.md)用來清除色彩緩衝區的綠色值。 預設值為零。

</dd> <dt>

*藍色* 
</dt> <dd>

[**GlClear**](glclear.md)用來清除色彩緩衝區的藍色值。 預設值為零。

</dd> <dt>

*阿 爾 法* 
</dt> <dd>

[**GlClear**](glclear.md)用來清除色彩緩衝區的 Alpha 值。 預設值為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlClearColor** 函式會指定 [**glClear**](glclear.md)用來清除色彩緩衝區的紅色、綠色、藍色和 Alpha 值。 **GlClearColor** 所指定的值會壓制至範圍 \[ 0，1 \] 。

下列函式會取出與 **glClearColor** 函數相關的資訊：

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ ACCUM \_ CLEAR \_ 值

具有引數 GL \_ 色彩 \_ 清除 \_ 值的 glGet

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

 

 





