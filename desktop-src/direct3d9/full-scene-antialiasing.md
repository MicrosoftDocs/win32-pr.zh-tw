---
description: 全場景消除鋸齒指的是將場景中每個多邊形的邊緣模糊，因為它在單一階段中會進行柵格化;不需要第二次傳遞。
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: 'Full-Scene 的消除鋸齒 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509889"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Full-Scene 的消除鋸齒 (Direct3D 9) 

全場景消除鋸齒指的是將場景中每個多邊形的邊緣模糊，因為它在單一階段中會進行柵格化;不需要第二次傳遞。 全場景消除鋸齒在支援時，只會影響三角形和三角形的群組。 使用 Direct3D 服務無法消除鋸齒的程式碼。 全場景消除鋸齒是在 Direct3D 中使用每個圖元上的交叉取樣來完成。 啟用取樣時，圖元的所有 subsamples 會在一個階段中更新，但用於牽涉到多個轉譯行程的其他效果時，應用程式可以指定只有某些 subsamples 會受到給定轉譯傳遞的影響。 第二種方法可模擬動作模糊、欄位深度焦點效果、反映模糊等等。

在這兩種情況下，為每個圖元記錄的各種樣本會混合在一起，並輸出到畫面。 這可改善消除鋸齒或其他效果的影像品質。

使用 [**IDirect3D9：： CreateDevice**](/windows/desktop/api) 方法建立裝置之前，您必須先判斷是否支援全場景消除鋸齒。 若要這麼做，請呼叫 [**IDirect3D9：： CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) 方法，如下列程式碼範例所示。


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



[**IDirect3D9：： CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)所接受的第一個參數是表示要查詢之顯示配接器的序號。 此範例使用 D3DADAPTER \_ 預設值來指定主顯示器介面卡。 第二個參數是 [**D3DDEVTYPE**](./d3ddevtype.md) 列舉型別中的值，指定裝置類型。 第三個參數指定介面的格式。 第四個參數會告訴 Direct3D 是否 (**TRUE**) 或全場景消除鋸齒 (**FALSE**) 。 此範例會使用 **FALSE** 來告訴 Direct3D，它會詢問如何進行全場景消除鋸齒。 最後一個參數指定您想要測試的取樣技巧。 使用 [**D3DMULTISAMPLE \_ 型**](./d3dmultisample-type.md) 別列舉型別中的值。 此範例會測試是否支援兩種層級的取樣。

如果裝置支援您要使用的取樣層級，則下一個步驟是藉由填入 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md) 結構的適當成員來設定呈現參數，以建立多重程式呈現介面。 之後，您就可以建立裝置。 下列範例程式碼顯示如何使用多取樣轉譯介面來設定裝置。


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



若要使用取樣，必須將 D3DPRESENT 參數的 SwapEffect 成員 \_ 設定為 D3DSWAPEFFECT \_ 捨棄。

最後一個步驟是藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，並將 D3DRS \_ MULTISAMPLEANTIALIAS 設定為 **TRUE**，啟用取樣消除鋸齒。 將此值設定為 **TRUE** 之後，您所做的任何轉譯都會套用至它。 您可能會想要根據所呈現的內容來啟用和停用取樣。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消除鋸齒](antialiasing.md)
</dt> </dl>

 

 
