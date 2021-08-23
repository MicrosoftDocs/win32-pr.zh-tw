---
title: 'gluCylinder 函式 (X.glu 隊) '
description: GluCylinder 函式會繪製圓柱。
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluCylinder 函式 OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a09ff92aec17a13f03ecb1cbaaf118398b2b88dea76936454d527bb9c37032f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061606"
---
# <a name="glucylinder-function"></a>gluCylinder 函式

**GluCylinder** 函式會繪製圓柱。

## <a name="syntax"></a>語法


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*qobj* 
</dt> <dd>

Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。

</dd> <dt>

*baseRadius* 
</dt> <dd>

位於 *z* = 0 之圓柱的半徑。

</dd> <dt>

*topRadius* 
</dt> <dd>

以 *z* 高度為圓柱的半徑半徑  =  **。

</dd> <dt>

*height* (高度) 
</dt> <dd>

圓柱的高度。

</dd> <dt>

*片* 
</dt> <dd>

圍繞 Z 軸的細分數目。

</dd> <dt>

*棧* 
</dt> <dd>

沿著 Z 軸的子分割數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluCylinder** 函式會繪製沿著 Z 軸方向的圓柱。 圓柱的基底位於 *z* = 0，而頂端是 *z*  =  *高度*。 如同球體，圓柱會以 Z 軸的形式細分為配量，並沿著 Z 軸細分為堆疊。

請注意，如果 *topRadius* 設為零，則此常式會產生一個錐形。

如果方向設定為 \_ 使用 [**gluQuadricOrientation**](gluquadricorientation.md))  (外部 x.glu 隊，則任何產生的法線點都不會出現在 Z 軸上。 否則，它們會指向 Z 軸。

如果使用 [**gluQuadricTexture**](gluquadrictexture.md)) 開啟 (的紋理：系統會產生紋理座標，讓 *t* 範圍從0.0 （以 *z 為單位*）到1.0 （以 *z*  =  *高度* 為單位），以及從位於正 y 軸的0.0 到位於正 y 軸的0.25、從正 y 軸到、從正 y 軸到0.5、在負 y 軸的0.75，以及從正 y 軸回到1.0。 

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

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





