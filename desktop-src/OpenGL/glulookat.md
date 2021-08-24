---
title: 'gluLookAt 函式 (X.glu 隊) '
description: GluLookAt 函式會定義「查看」轉換。
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- gluLookAt 函式 OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b21d0cb2fac6573ab2999eb96b2af8b1ecb670f4e51d1ffd2ad91ba001c9ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675298"
---
# <a name="glulookat-function"></a>gluLookAt 函式

**GluLookAt** 函式會定義「查看」轉換。

## <a name="syntax"></a>語法


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*eyex* 
</dt> <dd>

眼睛點的位置。

</dd> <dt>

*eyey* 
</dt> <dd>

眼睛點的位置。

</dd> <dt>

*eyez* 
</dt> <dd>

眼睛點的位置。

</dd> <dt>

*system.windows.media.rotatetransform.centerx* 
</dt> <dd>

參考點的位置。

</dd> <dt>

*centery* 
</dt> <dd>

參考點的位置。

</dd> <dt>

*centerz* 
</dt> <dd>

參考點的位置。

</dd> <dt>

*upx* 
</dt> <dd>

向上向量的方向。

</dd> <dt>

*upy* 
</dt> <dd>

向上向量的方向。

</dd> <dt>

*upz* 
</dt> <dd>

向上向量的方向。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluLookAt** 函式會建立衍生自眼睛點的視圖矩陣、指出場景中心的參考點，以及向上向量。 矩陣會將參考點對應至負 Z 軸，並將眼睛點對應至原點，如此當您使用一般投射矩陣時，場景的中心就會對應到此區的中心。 同樣地，上傳至「觀看」平面的向上向量所描述的方向，會對應至正 y 軸，使其在視口中向上指向。 向上向量不能平行至從眼睛到參考點的可見線。

**GluLookAt** 所產生的矩陣會 postmultiplies 目前的矩陣。

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





