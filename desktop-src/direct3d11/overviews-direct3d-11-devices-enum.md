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
# <a name="how-to-enumerate-adapters"></a><span data-ttu-id="4b032-103">如何：列舉介面卡</span><span class="sxs-lookup"><span data-stu-id="4b032-103">How To: Enumerate Adapters</span></span>

<span data-ttu-id="4b032-104">本主題說明如何使用 Microsoft DirectX Graphic Infrastructure (DXGI) 來列舉電腦上可用的圖形配接器。</span><span class="sxs-lookup"><span data-stu-id="4b032-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to enumerate the available graphics adapters on a computer.</span></span> <span data-ttu-id="4b032-105">Direct3D 10 和11可以使用 DXGI 來列舉介面卡。</span><span class="sxs-lookup"><span data-stu-id="4b032-105">Direct3D 10 and 11 can use DXGI to enumerate adapters.</span></span>

<span data-ttu-id="4b032-106">基於下列原因，您通常需要列舉介面卡：</span><span class="sxs-lookup"><span data-stu-id="4b032-106">You generally need to enumerate adapters for these reasons:</span></span>

-   <span data-ttu-id="4b032-107">判斷電腦上安裝的圖形配接器數目。</span><span class="sxs-lookup"><span data-stu-id="4b032-107">To determine how many graphics adapters are installed on a computer.</span></span>
-   <span data-ttu-id="4b032-108">協助您選擇要用來建立 Direct3D 裝置的介面卡。</span><span class="sxs-lookup"><span data-stu-id="4b032-108">To help you choose which adapter to use to create a Direct3D device.</span></span>
-   <span data-ttu-id="4b032-109">取出 [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) 物件，您可以使用此物件來取得裝置功能。</span><span class="sxs-lookup"><span data-stu-id="4b032-109">To retrieve an [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) object that you can use to retrieve device capabilities.</span></span>

<span data-ttu-id="4b032-110">**列舉介面卡**</span><span class="sxs-lookup"><span data-stu-id="4b032-110">**To enumerate adapters**</span></span>

1.  <span data-ttu-id="4b032-111">藉由呼叫 [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory)函數來建立 [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory)物件。</span><span class="sxs-lookup"><span data-stu-id="4b032-111">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object by calling the [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) function.</span></span> <span data-ttu-id="4b032-112">下列程式碼範例示範如何初始化 **IDXGIFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="4b032-112">The following code example demonstrates how to initialize an **IDXGIFactory** object.</span></span>
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  <span data-ttu-id="4b032-113">藉由呼叫 [**IDXGIFactory：： EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) 方法來列舉每個介面卡。</span><span class="sxs-lookup"><span data-stu-id="4b032-113">Enumerate through each adapter by calling the [**IDXGIFactory::EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) method.</span></span> <span data-ttu-id="4b032-114">*介面卡* 參數可讓您指定要列舉的介面卡之以零為基底的索引編號。</span><span class="sxs-lookup"><span data-stu-id="4b032-114">The *Adapter* parameter allows you to specify a zero-based index number of the adapter to enumerate.</span></span> <span data-ttu-id="4b032-115">如果指定的索引處沒有任何可用的介面卡，則方法會傳回 [**\_ \_ 未 \_ 找到的 DXGI 錯誤**](/windows/desktop/direct3ddxgi/dxgi-error)。</span><span class="sxs-lookup"><span data-stu-id="4b032-115">If no adapter is available at the specified index, the method returns [**DXGI\_ERROR\_NOT\_FOUND**](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>

    <span data-ttu-id="4b032-116">下列程式碼範例示範如何列舉電腦上的介面卡。</span><span class="sxs-lookup"><span data-stu-id="4b032-116">The following code example demonstrates how to enumerate through the adapters on a computer.</span></span>

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

<span data-ttu-id="4b032-117">下列程式碼範例示範如何列舉電腦上所有的介面卡。</span><span class="sxs-lookup"><span data-stu-id="4b032-117">The following code example demonstrates how to enumerate all adapters on a computer.</span></span>

> [!Note]  
> <span data-ttu-id="4b032-118">針對 Direct3D 11.0 和更新版本，建議應用程式一律改用 [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) 和 [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) 。</span><span class="sxs-lookup"><span data-stu-id="4b032-118">For Direct3D 11.0 and later, we recommend that apps always use [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) and [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) instead.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="4b032-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b032-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b032-120">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4b032-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 