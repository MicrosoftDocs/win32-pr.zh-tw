---
title: 'gluDisk 函式 (X.glu 隊) '
description: GluDisk 函式會繪製磁片。
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gluDisk 函式 OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025064"
---
# <a name="gludisk-function"></a>gluDisk 函式

**GluDisk** 函式會繪製磁片。

## <a name="syntax"></a>語法


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*qobj* 
</dt> <dd>

Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。

</dd> <dt>

*innerRadius* 
</dt> <dd>

磁片 (的內部半徑可能是零) 。

</dd> <dt>

*outerRadius* 
</dt> <dd>

磁片的外部半徑。

</dd> <dt>

*片* 
</dt> <dd>

圍繞 Z 軸的細分數目。

</dd> <dt>

*迴圈* 
</dt> <dd>

磁片正在細分之來源的同心圓環形數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluDisk** 函式會在 *z* = 0 平面上呈現磁片。 磁片的半徑為 *outerRadius*，並包含半徑為 *innerRadius* 的同心圓圓形孔。 如果 *innerRadius* 為0，則不會產生任何漏洞。 磁片會以 Z 軸的形式細分為配量 (例如比薩配量) 以及依配量和 *迴圈* 所 *指定的環形* (，分別) 。

相對於方向，磁片的正 *z* 端會被視為 *外部* (請參閱 [**gluQuadricOrientation**](gluquadricorientation.md)) 。 這表示，如果方向設定為 \_ 外部 x.glu 隊，則為沿著正 Z 軸的任何法線產生點。

如果 (使用 [**gluQuadricTexture**](gluquadrictexture.md)) 來開啟紋理座標，則會以線性方式產生紋理座標，使 *r*  =  *outerRadius*、在 (*r*、0、0) 的值是 (1、0.5) ; 在 (0、 *r*、0)  (0.5、1) 、在 (-r *、* 0、0) ， (0、-r *、* 0)  (0.5，0) 。0。5

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

[**gluCylinder**](glucylinder.md)
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

 

 





