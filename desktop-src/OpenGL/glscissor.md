---
title: 'glScissor 函式 (Gl) '
description: GlScissor 函式會定義剪式方塊。
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glScissor 函式 OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466917"
---
# <a name="glscissor-function"></a>glScissor 函式

**GlScissor** 函式會定義剪式方塊。

## <a name="syntax"></a>語法


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* 
</dt> <dd>

垂直軸的 x (垂直軸) 座標（剪下方塊的左下角）。

</dd> <dt>

*y* 
</dt> <dd>

[剪下] 方塊左上角的 y (水準軸) 座標。 同時，x 和 y 會指定剪下方塊的左下角。 一開始 (0，0) 。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

剪式方塊的寬度。

</dd> <dt>

*height* (高度) 
</dt> <dd>

剪式方塊的高度。 當 OpenGL 內容 *第一次* 附加至視窗時，會將 *寬度* 和 *高度* 設定為該視窗的維度。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 或 *高度* 都是負數。<br/>                                                                                   |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlScissor** 函式會在視窗座標中定義稱為剪下方塊的矩形。 前兩個參數 *x* 和 *y* 指定方塊左下角。 *寬度* 和 *高度* 參數會指定方塊的寬度和高度。

使用 [**glEnable**](glenable.md) 和 **glDisable** 搭配引數 GL 剪下測試，可啟用和停用剪式測試 \_ \_ 。 當剪下測試啟用時，繪製命令只能修改位於剪下方塊內的圖元。 視窗座標在畫面格緩衝區圖元的共用角落具有整數值，因此 **glScissor** (0、0、1、1) 只允許修改視窗中的左下圖元，而 **glScissor** (0、0、0、0) 不允許修改視窗中的所有圖元。

當剪式測試停用時，就如同剪下方塊包含整個視窗一樣。

下列函式會取出與 **glScissor** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 剪狀方塊的 glGet \_

[](glisenabled.md)具有引數 GL \_ 剪式測試的 glIsEnabled \_

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





