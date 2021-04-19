---
title: ID2D1Geometry ComputeArea 方法
description: 計算幾何的區域。
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- ComputeArea 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997750"
---
# <a name="id2d1geometrycomputearea-methods"></a>ID2D1Geometry：： ComputeArea 方法

計算幾何的區域。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                      | 描述                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputeArea (D2D1 \_ 矩陣 \_ 3X2 \_ F&，FLOAT \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))              | 當指定的矩陣轉換之後，並使用預設容錯壓平合併時，計算幾何的區域。<br/>    |
| [**ComputeArea (D2D1 \_ 矩陣 \_ 3X2 \_ F \* ，FLOAT \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))             | 使用預設容錯值，在指定的矩陣轉換並壓平合併之後，計算幾何的區域。<br/> |
| [**ComputeArea (D2D1 \_ 矩陣 \_ 3X2 \_ F&，float，float \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))  | 當指定的矩陣轉換之後，以及使用指定的容錯壓平合併時，計算幾何的區域。<br/>  |
| [**ComputeArea (D2D1 \_ 矩陣 \_ 3X2 \_ F \* ，float，float \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float)) | 當指定的矩陣轉換之後，以及使用指定的容錯壓平合併時，計算幾何的區域。<br/>  |



## <a name="examples"></a>範例

下列程式碼範例會使用 **ComputeArea** 來計算指定之圓形的區域 (**m \_ pCircleGeometry1**) 。


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
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

 

