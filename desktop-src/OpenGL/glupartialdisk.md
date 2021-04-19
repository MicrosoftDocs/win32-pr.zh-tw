---
title: 'gluPartialDisk 函式 (X.glu 隊) '
description: GluPartialDisk 函式會繪製磁片的弧形。
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- gluPartialDisk 函式 OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968138"
---
# <a name="glupartialdisk-function"></a>gluPartialDisk 函式

**GluPartialDisk** 函式會繪製磁片的弧形。

## <a name="syntax"></a>語法


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*qobj* 
</dt> <dd>

使用 [**gluNewQuadric**](glunewquadric.md))  (建立的 quadric 物件。

</dd> <dt>

*innerRadius* 
</dt> <dd>

部分磁片 (的內部半徑可以是零) 。

</dd> <dt>

*outerRadius* 
</dt> <dd>

部分磁片的外部半徑。

</dd> <dt>

*片* 
</dt> <dd>

圍繞 Z 軸的細分數目。

</dd> <dt>

*迴圈* 
</dt> <dd>

部分磁片已細分之來源的同心圓環形數目。

</dd> <dt>

*>startangle* 
</dt> <dd>

磁片部分的起始角度（以度為單位）。

</dd> <dt>

*sweepAngle* 
</dt> <dd>

磁片部分的掃描角度（以度為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluPartialDisk** 函式會在 *z* = 0 平面上呈現部分磁片。 部分磁片類似于完整磁片，不同之處在于只會包含從 *>startangle* 到 *>startangle* sweepAngle 的磁片子集，  +   (其中0度沿著正 y 軸，90度是沿著正 X 軸、180度沿著負 y 軸，而270度則沿著負 X 軸) 。

部分磁片的半徑為 *outerRadius* ，且包含半徑為 *innerRadius* 的同心圓迴圈。 如果 *innerRadius* 為零，則不會產生任何洞。 部分磁片會以 Z 軸的形式細分為配量 (例如) 的比薩配量，也會將 Z 軸分割成環形 (*（依配* 量和 *迴圈* 的指定），分別) 。

相對於方向，部分磁片的正面 z 端會被視為外部 (請參閱 [**gluQuadricOrientation**](gluquadricorientation.md)) 。 這表示，如果方向設定為 \_ 外部 x.glu 隊，則為沿著正 Z 軸的任何法線產生點。

如果您已使用 [**gluQuadricTexture**](gluquadrictexture.md)) 開啟紋理 (， **gluPartialDisk** 會以線性方式產生紋理座標，因此 *r*  =  *outerRadius*、 (*r*、0、0) 的值是 (1、0.5) 、 (0、 *r*、0)  (0.5、1) *、 (* r、0、0)  (r、0、0)  (*r*、0、0)  (0.5，0) 。0。5

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

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





