---
title: 'glMapGrid2d 函式 (Gl) '
description: '定義一維網格。 |glMapGrid2d 函式 (Gl) '
ms.assetid: 5e5887d1-e137-434b-a1f3-b3f10d462823
keywords:
- glMapGrid2d 函式 OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6992a904528cf961f27335e7241c50fbd14f058b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981769"
---
# <a name="glmapgrid2d-function"></a>glMapGrid2d 函式

定義一維網格。

## <a name="syntax"></a>語法


```C++
void WINAPI glMapGrid2d(
   GLint    un,
   GLdouble u1,
   GLdouble u2,
   GLint    vn,
   GLdouble v1,
   GLdouble v2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*聯合國* 
</dt> <dd>

方格範圍間隔 u1，u2 的資料分割數目 \[ \] 。 這個值必須是正數。

</dd> <dt>

*u1* 
</dt> <dd>

用來當做整數方格定義域值 i = 0 之對應的值。

</dd> <dt>

*u2* 
</dt> <dd>

值，用來當做整數方格定義域值 i = un 的對應。

</dd> <dt>

*vn* 
</dt> <dd>

方格範圍間隔 v1、v2 中的資料分割數目 \[ \] 。

</dd> <dt>

*v1* 
</dt> <dd>

用來當做整數方格定義域值 j = 0 對應的值。

</dd> <dt>

*v2* 
</dt> <dd>

用來當做整數方格定義域值 j = vn 之對應的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *Un* 或 *vn* 不是正數。<br/>                                                                                      |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlMapGrid** 和 [glEvalMesh](glevalmesh-functions.md)函式會以串聯方式使用，以有效率地產生和評估一連串的平均地圖定義域值。 GlEvalMesh 函式會逐步執行一維或二維方格的整數定義域，其範圍是 [**glMap1**](glmap1.md) 和 [**glMap2**](glmap2.md)所指定之評估對應的定義域。

[**GlMapGrid1**](glmapgrid1d.md)和 **glMapGrid2** 函式會指定在 i (或 i 和 j) 整數格線座標之間的線性方格對應、u (或您和 v) 浮點數評估對應座標。 如需如何評估您和 v 座標的詳細資訊，請參閱 [**glMap1**](glmap1.md) 和 [**glMap2**](glmap2.md) 。

[**GlMapGrid1**](glmapgrid1d.md)函式會指定單一線性對應，讓整數格線座標0完全對應至 u1，而整數網格 *線座標則* 完全不會對應到 *u2*。 所有其他的整數網格 *線座標都* 有對應，如下所示：

*u = i (u2 u1) /un + u1*

**GlMapGrid2** 函式會指定兩個這類線性對應。 一個將整數格線座標 *i = 0* 精確地對應至 *u1*，而整數格線座標 *i =* 完全不是 *u2*。 另一個會將整數格線座標 *j = 0* 精確對應至 *v1*，而整數格線座標 *j = vn* 精確至 *v2*。 其他整數格線座標 i 和 j 會對應到

*u = i (u2 u1) /un + u1*

*v = j (v2 v1) /vn + v1*

[**GlMapGrid**](glmapgrid1d.md)所指定的對應會使用 [glEvalMesh](glevalmesh-functions.md)和 [**glEvalPoint**](glevalpoint.md)的相同方式。

下列函式會取出與 [**glMapGrid**](glmapgrid1d.md)相關的資訊：

<dl>

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 網域的 glGet  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ list.map2 \_ 方格 \_ 網域的 glGet  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 區段的 glGet  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ list.map2 \_ 方格 \_ 區段的 glGet  
</dl>

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[glEvalMesh](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





