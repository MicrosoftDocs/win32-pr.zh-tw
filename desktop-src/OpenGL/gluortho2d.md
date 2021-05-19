---
title: 'gluOrtho2D 函式 (X.glu 隊) '
description: GluOrtho2D 函式會定義2D 正向投射矩陣。
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D 函式 OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153551"
---
# <a name="gluortho2d-function"></a>gluOrtho2D 函式

**GluOrtho2D** 函式會定義2d 正向投射矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*離開* 
</dt> <dd>

左方垂直裁剪平面的座標。

</dd> <dt>

*對* 
</dt> <dd>

右垂直裁剪平面的座標。

</dd> <dt>

*top* 
</dt> <dd>

上方水準裁剪平面的座標。

</dd> <dt>

*底部* 
</dt> <dd>

底部水準裁剪平面的座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluOrtho2D** 函式會設定二維正交的視圖區域。 這相當於呼叫 [**glOrtho**](glortho.md) 搭配 zNear =-1 和 zFar = 1。

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

[**glOrtho**](glortho.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





