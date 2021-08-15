---
title: 'gluPickMatrix 函式 (X.glu 隊) '
description: GluPickMatrix 函式會定義挑選區域。
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- gluPickMatrix 函式 OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 394e10c460b406e510b1423f299b4a8724492f5a5b180212ff121f4ad593041e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061576"
---
# <a name="glupickmatrix-function"></a>gluPickMatrix 函式

**GluPickMatrix** 函式會定義挑選區域。

## <a name="syntax"></a>語法


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* 
</dt> <dd>

挑選區域的 x 視窗座標。

</dd> <dt>

*y* 
</dt> <dd>

挑選區域的 y 視窗座標。

</dd> <dt>

*height* (高度) 
</dt> <dd>

視窗座標中挑選區域的高度。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

視窗座標中挑選區域的寬度。

</dd> <dt>

*視窗* 
</dt> <dd>

目前的視口 (為來自 [**glGetIntegerv**](glgetintegerv.md) 呼叫) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluPickMatrix** 函式會建立一個投射矩陣，您可以用來將繪圖限制在一個社區域的區域。

1.  使用 **gluPickMatrix** 將繪圖限制在游標周圍的社區域。
2.  使用 [**glRenderMode**](glrendermode.md)) 進入選取模式 (，然後 rerender 場景。

    所有會在資料指標附近繪製的基本專案都會被識別並儲存在選取範圍緩衝區中。

**GluPickMatrix** 所建立的矩陣會乘以目前的矩陣，就如同使用產生的矩陣來呼叫 [**glMultMatrix**](glmultmatrix.md)一樣。

1.  呼叫 [**glLoadIdentity**](glloadidentity.md) 將識別矩陣載入至透視圖矩陣堆疊。
2.  呼叫 **gluPickMatrix**。
3.  呼叫函數 (例如 [**gluPerspective**](gluperspective.md)) ，以將透視圖矩陣乘以挑選矩陣。

使用 **gluPickMatrix** 挑選非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 時，請小心關閉 NURBS 屬性，x.glu 隊 \_ 自動 \_ 載入 \_ 矩陣。 如果未關閉 X.GLU 隊 \_ 自動 \_ 載入 \_ 矩陣，任何轉譯的 NURBS 介面都會與挑選矩陣的細分方式不同，而不需要挑選矩陣。

## <a name="examples"></a>範例

轉譯場景時，如下所示：


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



下列程式碼會選取部分的部分區：


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>X.glu 隊。h</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Glu32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glGetIntegerv**](glgetintegerv.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





