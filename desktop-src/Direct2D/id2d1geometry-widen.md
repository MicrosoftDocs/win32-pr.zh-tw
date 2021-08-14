---
title: ID2D1Geometry 加寬方法
description: 依指定的筆觸擴大幾何，並將結果寫入至 ID2D1SimplifiedGeometrySink。
ms.assetid: c951ab85-7980-41e3-95c4-291d2fb046c8
keywords:
- 擴大方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: ebdae7ba4fd9eca96e422ae62274b4b9934040d4c4249bc9e1c78b81b62589dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342808"
---
# <a name="id2d1geometrywiden-methods"></a>ID2D1Geometry：：加寬方法

依指定的筆觸擴大幾何，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                          | 描述                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**加寬 (FLOAT、ID2D1StrokeStyle \* 、D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))             | 依指定的筆觸擴大幾何，並在指定的矩陣轉換結果之後，將結果寫入 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ，並使用預設的容錯值壓平合併。<br/>   |
| [**加寬 (FLOAT、ID2D1StrokeStyle \* 、D2D1 \_ 矩陣 \_ 3X2 \_ F&、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))              | 依指定的筆觸擴大幾何，並在指定的矩陣轉換結果之後，將結果寫入 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ，並使用預設的容錯值壓平合併。<br/>   |
| [**加寬 (FLOAT、ID2D1StrokeStyle \* 、D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、FLOAT、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | 依指定的筆觸擴大幾何，並在指定的矩陣轉換結果之後，將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ，並使用指定的容忍度壓平合併。<br/> |
| [**加寬 (FLOAT、ID2D1StrokeStyle \* 、D2D1 \_ 矩陣 \_ 3X2 \_ F&、FLOAT、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))  | 依指定的筆觸擴大幾何，並在指定的矩陣轉換結果之後，將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ，並使用指定的容忍度壓平合併。<br/> |



## <a name="examples"></a>範例

下列程式碼範例示範如何使用 **加寬** 依指定的筆觸來加寬幾何，然後將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) 物件。


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

 

