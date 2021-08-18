---
title: ID2D1Geometry Tessellate 方法
description: 建立一組順時針彎曲的三角形，這組三角形在使用指定的矩陣轉換並且使用指定的容錯扁平化之後，將涵蓋幾何。
ms.assetid: 4e0af188-d14b-43c0-be11-16577f054b90
keywords:
- Tessellate 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: b40602fb38ec2a0834ba202252114f7c0c34a4948e4473703ff4daf8bf2ee97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917888"
---
# <a name="id2d1geometrytessellate-methods"></a>ID2D1Geometry：： Tessellate 方法

建立一組順時針彎曲的三角形，這組三角形在使用指定的矩陣轉換並且使用指定的容錯扁平化之後，將涵蓋幾何。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                    | 描述                                                                                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Tessellate (D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、ID2D1TessellationSink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__id2d1tessellationsink))             | 建立一組順時針纏繞三角形，以在使用指定的矩陣轉換之後，以及使用預設容錯壓平合併的幾何。 <br/>   |
| [**Tessellate (D2D1 \_ 矩陣 \_ 3X2 \_ F&、ID2D1TessellationSink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_id2d1tessellationsink))              | 建立一組順時針纏繞三角形，以在使用指定的矩陣轉換之後，以及使用預設容錯壓平合併的幾何。 <br/>   |
| [**Tessellate (D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、FLOAT、ID2D1TessellationSink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_float_id2d1tessellationsink)) | 建立一組順時針彎曲的三角形，這組三角形在使用指定的矩陣轉換並且使用指定的容錯扁平化之後，將涵蓋幾何。 <br/> |
| [**Tessellate (D2D1 \_ 矩陣 \_ 3X2 \_ F&、FLOAT、ID2D1TessellationSink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__float_id2d1tessellationsink))  | 建立一組順時針彎曲的三角形，這組三角形在使用指定的矩陣轉換並且使用指定的容錯扁平化之後，將涵蓋幾何。<br/>  |



## <a name="examples"></a>範例

下列程式碼範例示範如何使用 Tessellate 來建立一組涵蓋幾何的順向纏繞三角形。


```C++
 ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry->Open(&pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry->Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink->Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT->CreateMesh(&pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh->Open(&pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry->Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink->Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink->Release();
                 }
                 pMesh->Release();
             }
         }
     }
     pGeometrySink->Release();
 }
 pPathGeometry->Release();
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

 

