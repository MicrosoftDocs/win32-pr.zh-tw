---
title: 描述項
description: 描述項是 D3D12 中單一資源的系結主要單位。
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104692"
---
# <a name="descriptors"></a>描述項

描述項是 D3D12 中單一資源的系結主要單位。

## <a name="in-this-section"></a>本節內容



| 主題                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [描述項總覽](descriptors-overview.md)<br/> | 描述元是由 API 呼叫所建立，並識別資源。<br/>                                                                                                                                                                                                                                                                                                                   |
| [建立描述項](creating-descriptors.md)<br/> | 描述並顯示建立索引、頂點和常數緩衝區視圖的範例;著色器資源、轉譯目標、未排序的存取、資料流程輸出和深度樣板視圖;和取樣器。 建立描述項的所有方法都是無限制執行緒。<br/>                                                                                                                             |
| [複製描述項](copying-descriptors.md)<br/>   | 裝置介面上的 [**ID3D12Device：： CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) 和 [**ID3D12Device：： CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) 方法會使用 CPU 來立即複製描述項。 只要 CPU 或 GPU 上的多個執行緒不會執行任何可能衝突的寫入，就可以將它們稱為「自由執行緒」。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[描述元堆積](descriptor-heaps.md)
</dt> <dt>

[描述中繼資料表](descriptor-tables.md)
</dt> <dt>

[資源系結](resource-binding.md)
</dt> <dt>

[根簽章](root-signatures.md)
</dt> </dl>

 

 





