---
title: Mipmap 封裝
description: 根據並排顯示資源的支援層級，具有特定維度的 mipmap 不會遵循標準磚圖形，而且會被視為以不透明的方式將它們封裝在一起。
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd29098b2668b5b4aab51dd26924d8f166df6fab9a4c5f8c78d0c8f5166b28a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408038"
---
# <a name="mipmap-packing"></a>Mipmap 封裝

根據並排顯示資源的支援 [層級](tiled-resources-features-tiers.md) ，具有特定維度的 mipmap 不會遵循標準磚圖形，而且會被視為以不透明的方式將它們封裝在一起。 較高階層的支援更加保證何種表面維度類型符合標準磚外形 (應用程式可因此個別對應)。

在實值之間有何不同之處，就是在指定並排資源的維度、格式、mipmap 和陣列配量的情況下，每個陣列配量的 mips (的每個數位 M，) 可以封裝成一些 N 個磚。 [**ID3D11Device2：： GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API 存在，可讓驅動程式向應用程式報告 M 和 N (與此 API 所報告的介面相關的其他詳細資料有關，而不會因硬體廠商) 而有所不同。 已封裝的 Mips 的磚組合仍是 64 KB，可以個別對應到磚集區中的不同位置。 但是動態磚的像素形狀，以及 Mipmaps 如何跨過磚組合進行調整因硬體廠商而異，因複雜度過高而無法公開。 因此，應用程式需要每次對應到指定封裝的所有磚，或是都不對應。 否則，用來存取並排資源的行為未定義。

對於陣列式表面，已封裝的 mips 組合以及儲存那些 mips 封裝磚數 (前面描述的 M 和 N)，會針對各陣列配量單獨套用。

用來複製磚的專用 Api ([**ID3D11DeviceCoNtext2：： CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) 和 [**ID3D11DeviceCoNtext2：： UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) 無法存取已封裝的 mips。 想要將資料複製到壓縮的 mips 或從中複製資料的應用程式，可以使用所有非磚資源專屬 Api 來複製和轉譯至表面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚式資源的區域如何並排顯示](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




