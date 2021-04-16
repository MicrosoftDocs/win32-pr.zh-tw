---
title: 'glRectf 函式 (Gl) '
description: GlRectf 函式會繪製一個矩形。
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
keywords:
- glRectf 函式 OpenGL
topic_type:
- apiref
api_name:
- glRectf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0c7036ae7395dce66d88f52c30631be801c4af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464332"
---
# <a name="glrectf-function"></a>glRectf 函式

[**GlRectf**](glrectd.md)函式會繪製一個矩形。

## <a name="syntax"></a>語法


```C++
void WINAPI glRectf(
   GLfloat x1,
   GLfloat y1,
   GLfloat x2,
   GLfloat y2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x1* 
</dt> <dd>

矩形頂點的 *x* 座標。

</dd> <dt>

*y1* 
</dt> <dd>

矩形頂點的 *y* 座標。

</dd> <dt>

*x2* 
</dt> <dd>

矩形相對頂點的 *x* 座標。

</dd> <dt>

*y2* 
</dt> <dd>

矩形相對頂點的 *y* 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlRectf** 函式支援以有效的矩形規格作為兩個角落點。 每個矩形命令都採用四個引數，並以兩個連續的 (*x*、 *y*) 座標，或作為陣列的兩個指標（每個都包含 (*x*、 *y*) 組）進行組織。 產生的矩形是在 *z* = 0 平面中定義。

**GlRectf** (*x1、* *y1、* *x2、* *y2*) 函數完全等同于下列順序：

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

 

 





