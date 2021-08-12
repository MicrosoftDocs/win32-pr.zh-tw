---
title: 'glClipPlane 函式 (Gl) '
description: GlClipPlane 函式會指定用來裁剪所有幾何的平面。
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glClipPlane 函式 OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb55edd88b8c8dcd6b4481e60dfc05a012bb79f4f484fde8987e9ed23239d837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618038"
---
# <a name="glclipplane-function"></a>glClipPlane 函式

**GlClipPlane** 函式會指定用來裁剪所有幾何的平面。

## <a name="syntax"></a>語法


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*飛機* 
</dt> <dd>

正在放置的裁剪平面。 表單 GL 剪輯平面 i 的符號名稱，在這種情況下， \_ \_ 會接受0到 GL **  \_ 最大 \_ 剪輯 \_ 平面-1 之間的整數。

</dd> <dt>

*方程* 
</dt> <dd>

四個雙精確度浮點值陣列的位址。 這些值會被視為平面方程式。

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

幾何一律會根據 *x*、 *y* 和 *z* 的六平面錐迭界進行裁剪。 **GlClipPlane** 函式可讓您指定其他平面的規格，而不一定是垂直于 *x* 軸、 *y* 軸或 *z* 軸，以裁剪所有幾何。 最高可指定最高 GL 的 \_ \_ 剪輯 \_ 平面平面，其中 GL \_ 最大 \_ 剪輯 \_ 平面在所有的執行中至少為六個。 因為產生的裁剪區域是所定義之半空格的交集，所以一律為凸間距。

**GlClipPlane** 函式會使用四個元件的平面方程式來指定半個空格。 當您呼叫 **glClipPlane** 時 *，會* 由模型矩陣的反向轉換方程式，並儲存在產生的眼睛座標中。 模型矩陣的後續變更對預存的平面方程式元件沒有任何影響。 如果具有預存平面方程式元件之頂點的眼睛座標的點乘積為正數或零，則頂點會與該裁剪平面有關。 否則，就會退出。

使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 函數來啟用和停用裁剪平面。 使用引數 GL 的 [剪下] 剪輯平面來呼叫裁剪平面 \_ \_ ，其中 *i* 是平面編號。**

依預設，所有裁剪平面都會定義為眼睛座標中的 (0、0、0、0) ，而且會停用。

GL \_ 剪輯 \_ 平面 *i* = gl \_ 剪輯 \_ PLANE0 + *i* 是永遠的情況。

下列函式會取出與 **glClipPlane** 相關的資訊：

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 剪輯 \_ 平面 *i*

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

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





