---
title: 如何列舉介面卡
description: 本主題說明如何使用 Microsoft DirectX Graphic Infrastructure (DXGI) 來列舉電腦上可用的圖形配接器。
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af16aba0131d93a5f72732931a68f132126b5d48
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990963"
---
# <a name="how-to-enumerate-adapters"></a>如何：列舉介面卡

本主題說明如何使用 Microsoft DirectX Graphic Infrastructure (DXGI) 來列舉電腦上可用的圖形配接器。 Direct3D 10 和11可以使用 DXGI 來列舉介面卡。

基於下列原因，您通常需要列舉介面卡：

-   判斷電腦上安裝的圖形配接器數目。
-   協助您選擇要用來建立 Direct3D 裝置的介面卡。
-   取出 [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) 物件，您可以使用此物件來取得裝置功能。

**列舉介面卡**

1.  藉由呼叫 [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory)函數來建立 [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory)物件。 下列程式碼範例示範如何初始化 **IDXGIFactory** 物件。
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  藉由呼叫 [**IDXGIFactory：： EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) 方法來列舉每個介面卡。 *介面卡* 參數可讓您指定要列舉的介面卡之以零為基底的索引編號。 如果指定的索引處沒有任何可用的介面卡，則方法會傳回 [**\_ \_ 未 \_ 找到的 DXGI 錯誤**](/windows/desktop/direct3ddxgi/dxgi-error)。

    下列程式碼範例示範如何列舉電腦上的介面卡。

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

下列程式碼範例示範如何列舉電腦上所有的介面卡。

> [!Note]  
> 針對 Direct3D 11.0 和更新版本，建議應用程式一律改用 [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) 和 [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) 。

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 