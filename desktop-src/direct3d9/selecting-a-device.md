---
description: 應用程式可以查詢硬體來偵測支援的 Direct3D 裝置類型。 本節包含有關列舉顯示配接器和選取 Direct3D 裝置的主要工作資訊。
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: 選取 (Direct3D 9) 的裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63428e15948e15790364f310d55989a9bbc7339846f7db5d301e316bee4d872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044246"
---
# <a name="selecting-a-device-direct3d-9"></a>選取 (Direct3D 9) 的裝置

應用程式可以查詢硬體來偵測支援的 Direct3D 裝置類型。 本節包含有關列舉顯示配接器和選取 Direct3D 裝置的主要工作資訊。

應用程式必須執行一系列的工作，才能選取適當的 Direct3D 裝置。 請注意，下列步驟適用于全螢幕應用程式，在大部分情況下，視窗型應用程式可以略過這些步驟。

1.  一開始，應用程式必須列舉系統上的顯示器介面卡。 介面卡是一種實體硬體。 請注意，圖形配接器可能包含一個以上的介面卡，如同雙指標顯示器。 不在意多重監視器支援的應用程式可以忽略此步驟，並將 D3DADAPTER \_ 預設值傳遞至步驟2中的 [**IDirect3D9：： EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) 方法。
2.  針對每個介面卡，應用程式會藉由呼叫 [**IDirect3D9：： EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)來列舉支援的顯示模式。
3.  如有需要，應用程式會藉由呼叫 [**IDirect3D9：： CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)，在每個列舉顯示模式中檢查硬體加速是否存在，如下列程式碼範例所示。 請注意，這只是 **IDirect3D9：： CheckDeviceType**; 的其中一種可能用途如需詳細資訊，請參閱 [判斷 (Direct3D 9) 的硬體支援](determining-hardware-support.md)。
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  應用程式會藉由呼叫 [**IDirect3D9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) 方法，在此介面卡上檢查裝置的所需功能層級。 透過 [**IDirect3D9：： CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)驗證，在所有顯示模式中，此方法所傳回的功能保證會是固定的裝置。
5.  裝置一律會轉譯成裝置所支援之列舉顯示模式的格式表面。 如果應用程式需要轉譯成不同格式的介面，則可以呼叫 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)。 如果裝置可以轉譯成格式，則保證 [**IDirect3D9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) 所傳回的所有功能都適用。
6.  最後，應用程式可以使用 [**IDirect3D9：： CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) 方法，判斷是否支援轉譯格式的取樣技術，例如全場景消除鋸齒。

完成上述步驟之後，應用程式應該會有可運作的顯示模式清單。 最後一個步驟是確認有足夠的可用裝置可存取記憶體，以容納所需的緩衝區和消除鋸齒數目。 這是必要的測試，因為模式和取樣率組合的記憶體耗用量無法進行預測，而不需要進行驗證。 此外，某些顯示器介面卡架構可能不會有固定數量的裝置可存取記憶體。 這表示，應用程式應該能夠在進入全螢幕模式時，回報非影片記憶體失敗。 一般而言，應用程式應該從它提供給使用者的模式清單中移除全螢幕模式，或者應該藉由減少背景緩衝區的數目或使用較不復雜的多層式技術來嘗試消耗較少的記憶體。

視窗型應用程式會執行一組類似的工作。

1.  它會決定視窗的工作區所涵蓋的桌面矩形。
2.  它會列舉介面卡，並尋找其監視器涵蓋用戶端區域的介面卡。 如果用戶端區域是由一個以上的介面卡所擁有，則應用程式可以選擇獨立驅動每個介面卡，或驅動單一介面卡，並讓 Direct3D 在簡報時將圖元從一個裝置傳輸到另一個裝置。 應用程式也可以略過兩個先前的步驟，並使用 D3DADAPTER \_ 預設介面卡。 請注意，當視窗放置於次要監視器時，這可能會導致較慢的作業。
3.  應用程式應該呼叫 [**IDirect3D9：： CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) ，以判斷裝置是否可以在桌面圖案中支援轉譯為指定格式的背景緩衝區。 您可以使用 [**IDirect3D9：： GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)來判斷桌面顯示格式，如下列程式碼範例所示。
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 裝置](direct3d-devices.md)
</dt> </dl>

 

 
