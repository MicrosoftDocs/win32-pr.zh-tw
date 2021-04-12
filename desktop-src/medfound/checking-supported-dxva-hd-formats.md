---
description: .
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: 檢查支援的 DXVA-HD 格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7560d574cee5fca21ab8de78b01b87af1de5a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468648"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="5afe3-103">檢查支援的 DXVA-HD 格式</span><span class="sxs-lookup"><span data-stu-id="5afe3-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="5afe3-104">檢查支援的輸入格式</span><span class="sxs-lookup"><span data-stu-id="5afe3-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="5afe3-105">若要取得 Microsoft DirectX Video 加速 High Definition (DXVA-HD) 裝置支援的輸入格式清單，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="5afe3-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="5afe3-106">呼叫 [**IDXVAHD \_ device：： GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) 來取得裝置功能。</span><span class="sxs-lookup"><span data-stu-id="5afe3-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="5afe3-107">檢查 [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)結構的 **InputFormatCount** 成員。</span><span class="sxs-lookup"><span data-stu-id="5afe3-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="5afe3-108">這個成員會提供支援的輸入格式數目。</span><span class="sxs-lookup"><span data-stu-id="5afe3-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="5afe3-109">配置 **D3DFORMAT** 值的陣列，其大小為 **InputFormatCount**。</span><span class="sxs-lookup"><span data-stu-id="5afe3-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="5afe3-110">將此陣列傳遞至 [**IDXVAHD \_ Device：： GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) 方法。</span><span class="sxs-lookup"><span data-stu-id="5afe3-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="5afe3-111">這些方法會將輸入格式清單填入陣列。</span><span class="sxs-lookup"><span data-stu-id="5afe3-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="5afe3-112">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="5afe3-112">The following code shows these steps:</span></span>


```C++
// Checks whether a DXVA-HD device supports a specified input format.

HRESULT CheckInputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[ caps.InputFormatCount ];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorInputFormats(
        caps.InputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.InputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.InputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="checking-supported-output-formats"></a><span data-ttu-id="5afe3-113">檢查支援的輸出格式</span><span class="sxs-lookup"><span data-stu-id="5afe3-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="5afe3-114">若要取得 DXVA HD 裝置支援的輸出格式清單，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="5afe3-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="5afe3-115">呼叫 [**IDXVAHD \_ device：： GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) 來取得裝置功能。</span><span class="sxs-lookup"><span data-stu-id="5afe3-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="5afe3-116">檢查 [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)結構的 **OutputFormatCount** 成員。</span><span class="sxs-lookup"><span data-stu-id="5afe3-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="5afe3-117">這個成員會提供支援的輸入格式數目。</span><span class="sxs-lookup"><span data-stu-id="5afe3-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="5afe3-118">配置 **D3DFORMAT** 值的陣列，其大小為 **OutputFormatCount**。</span><span class="sxs-lookup"><span data-stu-id="5afe3-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="5afe3-119">將此陣列傳遞至 [**IDXVAHD \_ Device：： GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) 方法。</span><span class="sxs-lookup"><span data-stu-id="5afe3-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="5afe3-120">這些方法會使用輸出格式清單來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="5afe3-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="5afe3-121">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="5afe3-121">The following code shows these steps:</span></span>


```C++
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5afe3-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="5afe3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5afe3-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="5afe3-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



