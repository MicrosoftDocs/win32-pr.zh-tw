---
title: ID2D1Geometry ComputePointAtLength 方法
description: 沿著指定的距離，以 \ 160; geometry 計算點和正切向量。
ms.assetid: b76aa3db-2967-4baa-a449-f664b080fb74
keywords:
- ComputePointAtLength 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 6665d5317b5359228f2e27803a8fee443ed8233e893cf7e8986e3af1c21a9373
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342828"
---
# <a name="id2d1geometrycomputepointatlength-methods"></a>ID2D1Geometry：： ComputePointAtLength 方法

計算沿著幾何之指定距離的點和正切向量。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                        | 描述                                                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputePointAtLength (浮點數、D2D1 \_ 矩陣 \_ 3X2 \_ F&、D2D1 \_ 點 \_ 2f \* 、D2D1 \_ 點 \_ 2f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f__d2d1_point_2f_d2d1_point_2f))              | 依指定的矩陣轉換之後，以指定的距離計算點和正切向量，並使用預設的容錯值壓平合併。<br/>   |
| [**ComputePointAtLength (FLOAT、D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、D2D1 \_ 點 \_ 2f \* 、D2D1 \_ POINT \_ 2f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_d2d1_point_2f_d2d1_point_2f))             | 依指定的矩陣轉換之後，以指定的距離計算點和正切向量，並使用預設的容錯值壓平合併。<br/>   |
| [**ComputePointAtLength (FLOAT、D2D1 \_ 矩陣 \_ 3X2 \_ F&、FLOAT、D2D1 \_ POINT \_ 2f \* 、D2D1 \_ POINT \_ 2f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))  | 依指定的矩陣轉換之後，在幾何的指定距離上計算點和正切向量，並使用指定的容錯值進行壓平合併。<br/> |
| [**ComputePointAtLength (FLOAT、D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、FLOAT、D2D1 \_ POINT \_ 2f \* 、D2D1 \_ POINT \_ 2f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_float_d2d1_point_2f_d2d1_point_2f)) | 依指定的矩陣轉換之後，在幾何的指定距離上計算點和正切向量，並使用指定的容錯值進行壓平合併。<br/> |



## <a name="examples"></a>範例

下列程式碼範例示範如何使用 **ComputePointAtLength** ，在幾何的指定距離計算點和正切向量。


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;
```




```C++
// Ask the geometry to give us the point that corresponds with the
// length at the current time.
hr = m_pPathGeometry->ComputePointAtLength(
    length, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

