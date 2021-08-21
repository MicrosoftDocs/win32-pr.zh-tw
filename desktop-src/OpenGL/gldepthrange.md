---
title: 'glDepthRange 函式 (Gl) '
description: GlDepthRange 函式會指定從正規化裝置座標到視窗座標的 z 值對應。
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- glDepthRange 函式 OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac72155449e70a59265e4ffd2576245059a547906092df2a932e84f221e48fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081648"
---
# <a name="gldepthrange-function"></a>glDepthRange 函式

**GlDepthRange** 函式會指定從正規化裝置座標到視窗座標的 *z* 值對應。

## <a name="syntax"></a>語法


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*zNear* 
</dt> <dd>

接近裁剪平面與視窗座標的對應。 預設值為零。

</dd> <dt>

*zFar* 
</dt> <dd>

最遠裁剪平面到視窗座標的對應。 預設值為 1。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

在裁剪和除以 *w* 之後， *z* 座標的範圍從0.0 到1.0，對應至接近或遠裁剪的平面。 **GlDepthRange** 函式會將此範圍中正規化 *z* 座標的線性對應指定為視窗 *z* 座標。 無論實際深度緩衝區的執行程度為何，都可以將視窗座標深度值視為範圍從0.0 到 1.0 (例如色彩元件) 。 因此， **glDepthRange** 所接受的值在被接受之前，都會壓制到這個範圍。

 (0，1) 的預設對應會將接近的平面對應到0，而將最遠的平面對應至1。 透過此對應，深度緩衝區範圍會完全使用。

*ZNear* 小於 *zFar* 是不必要的。 反向對應，例如 (1、0) 是可接受的。

下列函式會抓取 **glDepthRange** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 深度 \_ 範圍的 glGet

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





