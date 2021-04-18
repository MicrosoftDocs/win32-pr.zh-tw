---
title: ID2D1Geometry 大綱方法
description: 計算幾何的外框，並將結果寫入至 ID2D1SimplifiedGeometrySink。
ms.assetid: ec92db79-a1aa-4661-9e75-45a1763af370
keywords:
- 大綱方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 40d4ff1122d4a00e11ea35914f001b6dc9e06e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996393"
---
# <a name="id2d1geometryoutline-methods"></a>ID2D1Geometry：：大綱方法

計算幾何的外框，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                          | 描述                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**大綱 (D2D1 \_ 矩陣 \_ 3X2 \_ F&、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | 計算幾何的外框，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。 <br/> |
| [**大綱 (D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | 計算幾何的外框，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。<br/>  |
| [**大綱 (D2D1 \_ 矩陣 \_ 3X2 \_ F&、FLOAT、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | 計算幾何的外框，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。<br/>  |
| [**大綱 (D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、FLOAT、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | 計算幾何的外框，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。<br/>  |



## <a name="remarks"></a>備註

[**大綱**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))方法可讓呼叫者產生具有對輸入幾何之對等填滿的幾何，並具有下列額外屬性：

-   輸出幾何不包含任何橫向交集;也就是說，區段可以接觸，但永遠不會交叉。
-   輸出幾何中的最外層圖形都是逆時針方向的。
-   輸出幾何為填滿模式不變;也就是說，幾何的填滿不依賴填滿模式的選擇。 如需填滿模式的詳細資訊，請參閱 [**D2D1 \_ 填滿 \_ 模式**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode)。

此外， [**外框**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) 方法可能有助於移除已被提到幾何的多餘部分，以簡化複雜的幾何。 它也可以與 [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) 搭配使用，以同時在多個幾何之間建立聯集。

## <a name="examples"></a>範例

下列程式碼示範如何使用 **外框** 來建立沒有自我交集的相等幾何。 它會使用預設的簡維容錯功能，因此不應該與非常小的幾何一起使用。


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
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

 

