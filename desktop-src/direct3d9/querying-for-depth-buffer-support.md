---
description: 如同任何功能，您的應用程式所使用的驅動程式可能不支援所有類型的深度緩衝。
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: 查詢 (Direct3D 9) 的深度緩衝區支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687439"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a>查詢 (Direct3D 9) 的深度緩衝區支援

如同任何功能，您的應用程式所使用的驅動程式可能不支援所有類型的深度緩衝。 一律檢查驅動程式的功能。 雖然大部分的驅動程式都支援以 z 為基礎的深度緩衝，但並非全部都支援以 w 為基礎的深度緩衝。 如果您嘗試啟用不支援的配置，驅動程式不會失敗。 相反地，它們會改回另一個深度緩衝處理方法，或有時停用深度緩衝，這可能會導致以極深度排序成品呈現的場景。

您可以針對您的應用程式將在建立 Direct3D 裝置之前使用的顯示裝置，查詢 Direct3D 來檢查深度緩衝區的一般支援。 如果 Direct3D 物件報告它支援深度緩衝，您從這個 Direct3D 物件建立的任何硬體裝置都將支援 z 緩衝。

若要查詢深度緩衝支援，您可以使用 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 方法，如下列程式碼範例所示。


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



[**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 可讓您根據裝置的功能，選擇要建立的裝置。 在此情況下，不支援16位深度緩衝區的裝置將會遭到拒絕。

下列程式碼範例說明使用 [**IDirect3D9：： CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) 來判斷與轉譯目標的深度樣板相容性。


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



當您知道驅動程式支援深度緩衝區時，就可以驗證 w 緩衝區支援。 雖然所有軟體 rasterizers 都支援深度緩衝區，但只有參考轉譯器才支援 w 緩衝區，這不適用於真實世界的應用程式。 無論您的應用程式使用何種類型的裝置，請先確認支援 w 緩衝區，然後再嘗試啟用以 w 為基礎的深度緩衝。

1.  建立您的裝置之後，請呼叫 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/desktop/api) 方法，並傳遞初始化的 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構。
2.  在呼叫之後，LineCaps 成員會包含驅動程式對轉譯基本專案的支援相關資訊。
3.  如果此結構的 RasterCaps 成員包含 D3DPRASTERCAPS \_ WBUFFER 旗標，則此驅動程式會針對該基本型別支援以 w 為基底的深度緩衝。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[深度緩衝區](depth-buffers.md)
</dt> </dl>

 

 
