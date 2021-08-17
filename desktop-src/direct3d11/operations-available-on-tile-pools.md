---
title: 磚集區可用的作業
description: 此區段會列出您可以在磚集區上執行的作業。
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c72e15ebe9a8fd2f6725451268d3d03fb7b181442907248d0db44860560aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098320"
---
# <a name="operations-available-on-tile-pools"></a>磚集區可用的作業

此區段會列出您可以在磚集區上執行的作業。

-   磚集區的存留期與任何其他 Direct3D 資源的運作方式相同，它是由參考計數所支援，包括在此案例中追蹤來自並排顯示資源的對應。 當應用程式不再參考磚集區以及對於記憶體的任何磚對應消失，並且圖形處理單元 (GPU) 的存取完成時，作業系統便會解除配置磚集區。
-   與介面共用相關的 Api 以及磚集區的同步處理工作， (但不直接在) 的磚資源上。 類似于所提供之磚集區的行為，如果磚集區已共用且目前由其他裝置和處理常式取得，則會卸載可存取指向磚集區之磚化資源的 Direct3D 命令。
-   [**ID3D11DeviceCoNtext2：： ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) 作業
-   [**IDXGIDevice2：： OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) 和 [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) 作業-這些 api 可讓您暫時將記憶體提供給系統， (，且不適用於個別的並排資源) 。 如果已並排的資源指向所提供磚集區中的圖格，則並排顯示的資源行為會如同 (所提供的一樣，例如執行時間會卸載參考它的命令) 。

資料無法直接在磚集區記憶體中來回複製。 記憶體的存取一律是透過並排顯示的資源來完成。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立磚資源](creating-tiled-resources.md)
</dt> </dl>

 

 