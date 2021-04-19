---
description: Direct3D 提供下列功能來判斷硬體支援。
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: 判斷 (Direct3D 9) 的硬體支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971927"
---
# <a name="determining-hardware-support-direct3d-9"></a>判斷 (Direct3D 9) 的硬體支援

Direct3D 提供下列功能來判斷硬體支援。

-   [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    用來驗證介面格式是否可作為材質、表面格式是否可作為材質和轉譯目標，或是介面格式是否可做為深度樣板緩衝區來使用。 此外，這個方法是用來驗證深度緩衝區格式支援和深度樣板緩衝區格式支援。

-   [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    用來確認裝置是否能夠執行硬體加速、裝置是否能夠建立簡報的交換鏈，或可轉譯為目前顯示格式的裝置功能。

-   [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    用來驗證深度樣板緩衝區格式是否與轉譯目標格式相容。 請注意，在呼叫這個方法之前，應用程式應該在深度樣板和轉譯目標格式上呼叫 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 裝置](direct3d-devices.md)
</dt> </dl>

 

 
