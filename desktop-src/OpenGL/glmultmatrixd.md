---
title: 'glMultMatrixd 函式 (Gl) '
description: 'GlMultMatrixd 函式會將目前的矩陣乘以任意矩陣。 |glMultMatrixd 函式 (Gl) '
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- glMultMatrixd 函式 OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd31b3f84bbc8c75a3622b7b87f7a7577a33927bd489a06b8691377badaf0b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358794"
---
# <a name="glmultmatrixd-function"></a>glMultMatrixd 函式

**GlMultMatrixd** 和 [**glMultMatrixf**](glmultmatrixf.md)函數會將目前的矩陣乘以任意矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*m* 
</dt> <dd>

以資料行主要順序儲存為16個連續值之4x4 矩陣的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlMultMatrix** 函式會將目前的矩陣乘以 *m* 中指定的矩陣。 也就是說，如果 M 是目前的矩陣，而 T 是傳遞給 **glMultMatrix** 的矩陣，則 m 會取代為 m T。

目前的矩陣是投射矩陣、模型矩陣或紋理矩陣，由目前的矩陣模式決定 (查看 [**glMatrixMode**](glmatrixmode.md)) 。

*M* 參數指向以資料行主要順序儲存之單精確度或雙精確度浮點值的4x4 矩陣。 也就是說，矩陣的儲存方式如下圖所示。

![![顯示 m 參數所指向之4x4 矩陣的圖表]。](images/multi01.png)

下列函式會取出與 **glMultMatrix** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet

具有引數 GL \_ 模型 \_ 矩陣的 glGet

具有引數 GL \_ 投射 \_ 矩陣的 glGet

具有引數 GL \_ 材質 \_ 矩陣的 glGet

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





