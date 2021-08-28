---
title: 磚資源
description: 您可以將已平平的資源視為大型邏輯資源，其使用少量的實體記憶體。
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73835d6603d1d8d7e708cd422e3991bb88ac1f91cebf016ccce36f2466270c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124086"
---
# <a name="tiled-resources"></a>磚資源

您可以將已平平的資源視為大型邏輯資源，其使用少量的實體記憶體。

本節說明為何需要並排顯示的資源，以及如何建立和使用並排顯示的資源。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                   | 描述                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [為何需要磚資源？](why-are-tiled-resources-needed-.md)<br/>       | 需要有並排的資源，因此 (GPU) 記憶體會浪費儲存應用程式知道將無法存取的介面區域，而且硬體可以瞭解如何在連續的磚之間進行篩選。<br/>     |
| [建立磚資源](creating-tiled-resources.md)<br/>                     | 建立資源時，藉由指定 [**D3D11 \_ 資源的「 \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示」旗標來建立並排顯示的資源。<br/>                                                                                          |
| [磚資源 Api](tiled-resource-apis.md)<br/>                               | 本節所述的 Api 適用于磚化的資源和磚集區。<br/>                                                                                                                                                              |
| [磚資源的管線存取](pipeline-access-to-tiled-resources.md)<br/> | 磚資源可用於著色器資源檢視 (SRV) 、轉譯目標視圖 (RTV) 、深度樣板視圖 (DSV) 和未排序的存取權視圖 (UAV) ，以及某些未使用視圖的系結點，例如頂點緩衝區系結。 <br/> |
| [磚資源功能層級](tiled-resources-features-tiers.md)<br/>         | Direct3D 11.2 會以 D3D11 並排顯示的 [**\_ \_ 資源 \_ 層級**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) 值，來公開兩個層級的並排資源支援。 <br/>                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





