---
title: 'glClearIndex 函式 (Gl) '
description: GlClearIndex 函數會指定色彩索引緩衝區的清除值。
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- glClearIndex 函式 OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465657"
---
# <a name="glclearindex-function"></a>glClearIndex 函式

**GlClearIndex** 函數會指定色彩索引緩衝區的清除值。

## <a name="syntax"></a>語法


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*c* 
</dt> <dd>

清除色彩索引緩衝區時使用的索引。 預設值為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlClearIndex** 函數會指定 [**glClear**](glclear.md)用來清除色彩索引緩衝區的索引。 *C* 參數不是壓制。 相反地， *c* 會轉換成具有二進位點右邊未指定精確度的固定點值。 然後，此值的整數部分會以 2 <sup>m</sup>  -1 遮罩，其中 *m* 是儲存在畫面格緩衝區中之色彩索引的位數。

下列函式會取出與 **glClearIndex** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 索引 \_ 清除 \_ 值的 glGet

具有引數 GL \_ 索引 \_ 位的 glGet

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

 

 





