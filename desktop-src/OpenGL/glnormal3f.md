---
title: 'glNormal3f 函式 (Gl) '
description: '設定目前的一般向量。 |glNormal3f 函式 (Gl) '
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- glNormal3f 函式 OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e83b874b1588ad8bd91da9e5c9f831062de9cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982840"
---
# <a name="glnormal3f-function"></a>glNormal3f 函式

設定目前的一般向量。

## <a name="syntax"></a>語法


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Nx* 
</dt> <dd>

指定新目前標準向量的 x 座標。

</dd> <dt>

*紐約* 
</dt> <dd>

指定新目前標準向量的 y 座標。

</dd> <dt>

*紐西蘭* 
</dt> <dd>

指定新目前標準向量的 z 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

當您呼叫 **glNormal3f** 函式時，目前的一般會設定為指定的座標。

Byte、short 或 integer 引數會轉換成浮點數格式，其具有將最正面可表示的整數值對應至1.0 的線性對應，以及最大的負向-1.0 的可表示整數值。

使用 **glNormal3f** 指定的法線不需要單位長度。 如果啟用正規化，則在轉換之後會正規化以 **glNormal3f** 指定的法線。 您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配引數 GL 標準化來控制正規化 \_ 。 預設會停用正規化。 您可以隨時更新目前的正常情況。 尤其是，您可以呼叫 [**glBegin**](glbegin.md)的呼叫與 [**glEnd**](glend.md)的對應呼叫之間的 **glNormal3f** 。 下列函式會取出與 **glNormal3f** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 標準的 glGet

具有引數 GL 正規化的 [**glIsEnable**](glisenabled.md) \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





