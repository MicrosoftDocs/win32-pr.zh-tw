---
title: 'glRectiv 函式 (Gl) '
description: GlRectiv 函式會繪製一個矩形。
ms.assetid: 24db6fc0-9b53-4e72-9b12-18ea65409f12
keywords:
- glRectiv 函式 OpenGL
topic_type:
- apiref
api_name:
- glRectiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6f011748ec66a65511f6cbdcd2342cdf3212d04d3b2ba0507e810eb64293f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036588"
---
# <a name="glrectiv-function"></a>glRectiv 函式

**GlRectiv** 函式會繪製一個矩形。

## <a name="syntax"></a>語法


```C++
void WINAPI glRectiv(
   const GLint *v1,
   const GLint *v2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*v1* 
</dt> <dd>

矩形的一個頂點指標。

</dd> <dt>

*2* 
</dt> <dd>

矩形相對頂點的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlRecti** 函式支援以有效的矩形規格作為兩個角落點。 每個矩形命令都採用四個引數，並以兩個連續的 (*x*、 *y*) 座標，或作為陣列的兩個指標（每個都包含 (*x*、 *y*) 組）進行組織。 產生的矩形是在 *z* = 0 平面中定義。

**GlRecti** (*x1、* *y1、* *x2、* *y2*) 函數完全等同于下列順序：

**glBegin** (GL \_ 多邊形) ;

**glVertex2** ( *x1，* *y1* ) ;

**glVertex2** ( *x2，* *y1* ) ;

**glVertex2** ( *x2，* *y2* ) ;

**glVertex2** ( *x1，* *y2* ) ;

**glEnd** ( ) ;

請注意，如果第二個頂點在第一個頂點的上方和右邊，則會以逆時針繞組來構成矩形。

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

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





