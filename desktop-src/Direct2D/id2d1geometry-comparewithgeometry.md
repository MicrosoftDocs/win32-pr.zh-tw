---
title: ID2D1Geometry CompareWithGeometry 方法
description: 描述這個幾何與指定幾何之間的交集。
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- CompareWithGeometry 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09978c38c3e4be7ad8a86ccfccb43387ed4ac48232e39e1ed19001d806362c88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119304798"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>ID2D1Geometry：： CompareWithGeometry 方法

描述這個幾何與指定幾何之間的交集。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                            | 描述                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompareWithGeometry (ID2D1Geometry \* 、D2D1 \_ MATRIX \_ 3X2 \_ F&、D2D1 \_ GEOMETRY \_ 關聯 \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | 描述這個幾何與指定幾何之間的交集。 比較是使用預設的簡維容錯來執行。<br/>      |
| [**CompareWithGeometry (ID2D1Geometry \* 、D2D1 \_ MATRIX \_ 3X2 \_ F \* 、D2D1 \_ GEOMETRY \_ 關聯 \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | 描述這個幾何與指定幾何之間的交集。 比較是使用預設的簡維容錯來執行。<br/>      |
| [**CompareWithGeometry (ID2D1Geometry \* 、D2D1 \_ MATRIX \_ 3X2 \_ F&、FLOAT、D2D1 \_ GEOMETRY \_ 關聯 \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | 描述這個幾何與指定幾何之間的交集。 使用指定的簡維容錯來執行比較。<br/>    |
| [**CompareWithGeometry (ID2D1Geometry \* 、D2D1 \_ MATRIX \_ 3X2 \_ F \* 、FLOAT、D2D1 \_ GEOMETRY \_ 關聯 \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | 描述這個幾何與指定幾何之間的交集。 使用指定的簡維容錯來執行比較。<br/> |



## <a name="remarks"></a>備註

在解讀傳回的 *關聯* 值時，請務必記住，成員 [**D2D1 \_ GEOMETRY \_ 關聯 \_ 是 \_ 包含**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) 在 **D2D1 \_ geometry \_ 關聯** 列舉型別中，這表示此幾何包含在 *inputGeometry* 中，而不是這個幾何包含 *inputGeometry*。

如需有關如何解讀其他可能傳回值的詳細資訊，請參閱 [**D2D1 \_ GEOMETRY \_ 關聯**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation)性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

