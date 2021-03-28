---
title: 如何取得介面卡顯示模式
description: 本主題說明如何使用 Microsoft DirectX Graphic Infrastructure (DXGI) 來取得與介面卡相關聯的有效顯示模式。
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c2602fcd4e1baa4476bb89273eda676f444e38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315208"
---
# <a name="how-to-get-adapter-display-modes"></a><span data-ttu-id="8e0dc-103">如何：取得介面卡顯示模式</span><span class="sxs-lookup"><span data-stu-id="8e0dc-103">How To: Get Adapter Display Modes</span></span>

<span data-ttu-id="8e0dc-104">本主題說明如何使用 Microsoft DirectX Graphic Infrastructure (DXGI) 來取得與介面卡相關聯的有效顯示模式。</span><span class="sxs-lookup"><span data-stu-id="8e0dc-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to get the valid display modes associated with an adapter.</span></span> <span data-ttu-id="8e0dc-105">DirectX 10 和11可以使用 DXGI 來取得有效的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="8e0dc-105">DirectX 10 and 11 can use DXGI to get the valid display modes.</span></span> <span data-ttu-id="8e0dc-106">知道有效的顯示模式，可確保您的應用程式能夠正確地選擇有效的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="8e0dc-106">Knowing the valid display modes ensures that your application can properly choose a valid full-screen mode.</span></span>

<span data-ttu-id="8e0dc-107">**取得介面卡顯示模式**</span><span class="sxs-lookup"><span data-stu-id="8e0dc-107">**To get adapter display modes**</span></span>

1.  <span data-ttu-id="8e0dc-108">建立 [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) 物件，並使用它來列舉可用的介面卡。</span><span class="sxs-lookup"><span data-stu-id="8e0dc-108">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object and use it to enumerate the available adapters.</span></span> <span data-ttu-id="8e0dc-109">如需詳細資訊，請參閱 [如何：列舉介面卡](overviews-direct3d-11-devices-enum.md)。</span><span class="sxs-lookup"><span data-stu-id="8e0dc-109">For more information, see [How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md).</span></span>
2.  <span data-ttu-id="8e0dc-110">呼叫 IDXGIAdapter：： EnumOutputs 來列舉每個介面卡的輸出。</span><span class="sxs-lookup"><span data-stu-id="8e0dc-110">Call IDXGIAdapter::EnumOutputs to enumerate the outputs for each adapter.</span></span>
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  <span data-ttu-id="8e0dc-111">呼叫 IDXGIOutput：： GetDisplayModeList，以抓取 [**DXGI \_ 模式 \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) 結構的陣列，以及陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="8e0dc-111">Call IDXGIOutput::GetDisplayModeList to retrieve an array of [**DXGI\_MODE\_DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) structures and the number of elements in the array.</span></span> <span data-ttu-id="8e0dc-112">每個 **DXGI \_ 模式 \_ DESC** 結構代表輸出的有效顯示模式。</span><span class="sxs-lookup"><span data-stu-id="8e0dc-112">Each **DXGI\_MODE\_DESC** structure represents a valid display mode for the output.</span></span>
    ```
    UINT numModes = 0;
    DXGI_MODE_DESC* displayModes = NULL;
    DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;

        // Get the number of elements
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, NULL);

        displayModes = new DXGI_MODE_DESC[numModes]; 

        // Get the list
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, displayModes);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="8e0dc-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e0dc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e0dc-114">裝置</span><span class="sxs-lookup"><span data-stu-id="8e0dc-114">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="8e0dc-115">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="8e0dc-115">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 