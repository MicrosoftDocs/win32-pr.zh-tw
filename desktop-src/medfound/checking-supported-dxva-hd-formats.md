---
description: 檢查支援的 DXVA-HD 格式
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: 檢查支援的 DXVA-HD 格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07d47043ed200d256e2bef8fa2c9ab6717f3b82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090006"
---
# <a name="checking-supported-dxva-hd-formats"></a>檢查支援的 DXVA-HD 格式

## <a name="checking-supported-input-formats"></a>檢查支援的輸入格式

若要取得 Microsoft DirectX Video 加速 High Definition (DXVA-HD) 裝置支援的輸入格式清單，請執行下列動作：

1.  呼叫 [**IDXVAHD \_ device：： GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) 來取得裝置功能。
2.  檢查 [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)結構的 **InputFormatCount** 成員。 這個成員會提供支援的輸入格式數目。
3.  配置 **D3DFORMAT** 值的陣列，其大小為 **InputFormatCount**。
4.  將此陣列傳遞至 [**IDXVAHD \_ Device：： GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) 方法。 這些方法會將輸入格式清單填入陣列。

下列程式碼顯示這些步驟：


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



## <a name="checking-supported-output-formats"></a>檢查支援的輸出格式

若要取得 DXVA HD 裝置支援的輸出格式清單，請執行下列動作：

1.  呼叫 [**IDXVAHD \_ device：： GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) 來取得裝置功能。
2.  檢查 [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)結構的 **OutputFormatCount** 成員。 這個成員會提供支援的輸入格式數目。
3.  配置 **D3DFORMAT** 值的陣列，其大小為 **OutputFormatCount**。
4.  將此陣列傳遞至 [**IDXVAHD \_ Device：： GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) 方法。 這些方法會使用輸出格式清單來填滿陣列。

下列程式碼顯示這些步驟：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



