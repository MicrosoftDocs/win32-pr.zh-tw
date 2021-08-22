---
title: 'gluSphere 函式 (X.glu 隊) '
description: GluSphere 函式會繪製球體。
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- gluSphere 函式 OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590c4b7335fe0596c5b5b0f3dc709998fafc21f7be78f493a05f6520ed9fd368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488728"
---
# <a name="glusphere-function"></a>gluSphere 函式

**GluSphere** 函式會繪製球體。

## <a name="syntax"></a>語法


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
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

*半徑* 
</dt> <dd>

球體的半徑。

</dd> <dt>

*片* 
</dt> <dd>

圍繞 Z 軸的線段數 (類似于經度) 。

</dd> <dt>

*棧* 
</dt> <dd>

沿著 Z 軸的子分割數目 (類似于緯度) 的線條。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluSphere** 函式會繪製以原點為中心之指定半徑的球體。 球體會以 Z 軸將 Z 軸細分為配量，沿著 Z 軸分割成堆疊 (類似于經度和緯度) 。

如果方向設定為 [X.GLU 隊 \_ 外部] (**gluQuadricOrientation**) ，則會從球體中央開始的任何法線產生點。 否則，它們會指向球體的中心。

如果使用 **gluQuadricTexture**) 來開啟 (的紋理，則會產生材質座標，讓 *t* 範圍從0.0 （z 半徑的 *z* =-*半徑*）到1.0 （ *z*  =  *半徑*） (*t* 在 longitudinal 行之間以線性方式增加) ; 和中的範圍是從0.0 （正 y 軸）到0.25 （正 X 軸）、在負 y 軸的、負 X 軸上的0.75，以及正 y 軸上的1.0。0。5

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

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





