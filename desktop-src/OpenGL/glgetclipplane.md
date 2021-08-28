---
title: 'glGetClipPlane 函式 (Gl) '
description: GlGetClipPlane 函數會傳回指定裁剪平面的係數。
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glGetClipPlane 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf551356088db2b99b79a28a396be785ab60f2196cc3e27353cb867d4b151dd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742036"
---
# <a name="glgetclipplane-function"></a>glGetClipPlane 函式

**GlGetClipPlane** 函數會傳回指定裁剪平面的係數。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*飛機* 
</dt> <dd>

裁剪平面。 裁剪平面的數目取決於執行，但至少支援六個裁剪平面。 它們是以 [GL 的格式] 剪輯平面的符號名稱來識別 \_ \_ ，其中 0 = *i* < GL  \_ 最大 \_ 剪輯 \_ 平面。

</dd> <dt>

*方程* 
</dt> <dd>

傳回四個雙精確度值，這是眼睛座標 *平面* 的平面方程式係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *平面* 不是可接受的值。<br/>                                                                                         |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetClipPlane** 函 *式* 會在方程式中傳回 *平面* 的平面方程式四個係數。

GL \_ 剪輯 \_ 平面 *i* = gl \_ 剪輯 \_ PLANE0 + *i* 是永遠的情況。

如果產生錯誤，則不會對方程式內容進行任何變更 *。*

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

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





