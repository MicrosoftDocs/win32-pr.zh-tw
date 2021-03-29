---
title: 建立磚集區
description: 磚集區會透過 ID3D11Device CreateBuffer API 來建立，其方式是 \_ \_ \_ \_ 在 \_ D3D11 參數指向之 PDesc 緩衝區 DESC 結構的 MiscFlags 成員中傳遞 D3D11 資源其他磚集區旗標 \_ 。
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990590"
---
# <a name="tile-pool-creation"></a>建立磚集區

磚集區會透過 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API 來建立，其方式是在 *D3D11* 參數指向之 [**PDesc \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)結構的 **MiscFlags** 成員中傳遞 [**D3D11 \_ 資源 \_ 其他 \_ 磚 \_ 集**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)區旗標。

應用程式可以在每一個 Direct3D 裝置建立一個或多個磚集區。 每個磚集區的大小總和限制為 Direct3D 11 的資源大小上限，也就是約為圖形處理器 (GPU) RAM 的 1/4。

磚集區由 64 KB 磚所組成，但作業系統 (顯示驅動程式) 會在幕後將整個集區作為一或多個配置來管理，但應用程式看不到分解過程。 並排顯示的資源會藉由指向磚集區內的磚來定義內容。 將磚指向 **Null**，即可將磚從並排的資源取消對應。 這類未對應的磚具有讀取或寫入行為的相關規則。 如需詳細資訊，請參閱 [危險追蹤與磚集區資源](hazard-tracking-versus-tile-pool-resources.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[對應在磚集區中](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




