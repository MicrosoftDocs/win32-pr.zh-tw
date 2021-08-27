---
title: 如何取得介面卡顯示模式
description: 本主題說明如何使用 Microsoft DirectX Graphic Infrastructure (DXGI) 來取得與介面卡相關聯的有效顯示模式。
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921d373a9ff0f79baaf848a55cbab0d08fd4e119d30a0a0cb917832830589dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119568"
---
# <a name="how-to-get-adapter-display-modes"></a>如何：取得介面卡顯示模式

本主題說明如何使用 Microsoft DirectX Graphic Infrastructure (DXGI) 來取得與介面卡相關聯的有效顯示模式。 DirectX 10 和11可以使用 DXGI 來取得有效的顯示模式。 知道有效的顯示模式，可確保您的應用程式能夠正確地選擇有效的全螢幕模式。

**取得介面卡顯示模式**

1.  建立 [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) 物件，並使用它來列舉可用的介面卡。 如需詳細資訊，請參閱 [如何：列舉介面卡](overviews-direct3d-11-devices-enum.md)。
2.  呼叫 IDXGIAdapter：： EnumOutputs 來列舉每個介面卡的輸出。
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  呼叫 IDXGIOutput：： GetDisplayModeList，以抓取 [**DXGI \_ 模式 \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) 結構的陣列，以及陣列中的元素數目。 每個 **DXGI \_ 模式 \_ DESC** 結構代表輸出的有效顯示模式。
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

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 