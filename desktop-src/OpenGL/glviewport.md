---
title: 'glViewport 函式 (Gl) '
description: GlViewport 函式會設定此功能區。
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- glViewport 函式 OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70fc727265ce4af1db2be808ae7eee3f59246874659a815c66292bcab3d7ecfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035401"
---
# <a name="glviewport-function"></a>glViewport 函式

**GlViewport** 函式會設定此功能區。

## <a name="syntax"></a>語法


```C++
void WINAPI glViewport(
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

以圖元為單位的區式矩形左下角。 預設值為 (0,0)。

</dd> <dt>

*y* 
</dt> <dd>

以圖元為單位的區式矩形左下角。 預設值為 (0,0)。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

區的寬度。 當 OpenGL 內容第一次附加至視窗時，會將 *寬度* 和 *高度* 設定為該視窗的維度。

</dd> <dt>

*height* (高度) 
</dt> <dd>

視口的高度。 當 OpenGL 內容第一次附加至視窗時，會將 *寬度* 和 *高度* 設定為該視窗的維度。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 或 *高度* 都是負數。<br/>                                                                                   |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlViewport** 函式會指定從標準化裝置座標到視窗座標之 *x* 和 *y* 的仿射轉換。 讓 (*x*<sub>nd</sub> ， *y*<sub>nd</sub> ) 為標準化裝置座標。 視窗座標 (*x*<sub>w</sub> ， *y*<sub>w</sub> ) 接著計算如下：

![顯示視窗座標計算的方程式。](images/view01.png)

當區寬度和高度以無訊息方式壓制至相依于執行的範圍時。 藉由呼叫 **glGet** 與引數 GL \_ 最大值區變暗，即可查詢此範圍 \_ \_ 。

下列函式會取出與 **glViewport** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 區的 glGet

具有引數 GL \_ 最大區的 glGet 變 \_ \_ 暗

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

[**glDepthRange**](gldepthrange.md)
</dt> </dl>

 

 





