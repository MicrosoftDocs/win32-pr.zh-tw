---
title: Single-Finger 旋轉
description: 本節說明如何使用 pivot 點來旋轉物件。
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows觸控、旋轉
- Windows觸控、操作
- Windows觸控、單指旋轉
- Windows觸控、資料透視點旋轉
- 操作，旋轉
- 旋轉，pivot 點
- 旋轉，單指
- 手勢，單指旋轉
- 單一手指旋轉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36fe7e92f6d68515e1d13b39c32ee4af5b6b03e675479242210fe302b84e6395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110644"
---
# <a name="single-finger-rotation"></a>Single-Finger 旋轉

本節說明如何使用 pivot 點來旋轉物件。

下圖說明單一手指旋轉。

![顯示兩種類型的單一手指旋轉的圖例：圍繞中心或邊緣的周圍](images/sfrotation.png)

在範例 A 中，會使用旋轉手勢來旋轉物件中心點周圍的物件。 在 B 範例中，物件的旋轉方式是在物件的邊緣周圍移動單一手指。 操作處理器會使用資料透視點和 pivot 半徑值來啟用這項旋轉。 下圖說明單一手指旋轉的元件。

![圖例顯示單一手指旋轉的元件： pivotpointx、pivotpointy 和 pivotradius](images/sfrotation-components.png)

設定 [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)、 [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)和 [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) 值之後，後續的轉譯訊息將會納入旋轉。 Pivot 半徑越大，x 和 y 的變更就必須等於旋轉物件。 下列程式碼顯示如何在操作處理器中設定這些值。


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



在上述範例中，物件的邊緣距離 (調整為 40%) 用來作為 pivot 半徑。 因為物件大小會納入考慮，所以此計算對每個物件差異都有效。 當物件進行調整時，pivot 半徑會成長。 此值和物件的中心 x 和 y 值會傳遞給操作處理器，以在資料透視點周圍旋轉物件。

> [!Note]  
> [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)值絕不能介於0.0 到1.0 之間。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[操作](getting-started-with-manipulations.md)
</dt> <dt>

[**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




