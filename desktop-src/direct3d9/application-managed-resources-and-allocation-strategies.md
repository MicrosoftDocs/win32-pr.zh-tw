---
description: Managed 頂點緩衝區或索引緩衝區資源無法在建立時指定 D3DUSAGE 動態宣告為動態 \_ 。
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed (Direct3D 9) 的資源和配置策略
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991627"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Application-Managed (Direct3D 9) 的資源和配置策略

Managed 頂點緩衝區或索引緩衝區資源無法在建立時指定 D3DUSAGE 動態宣告為動態 \_ 。 這需要針對頂點緩衝區內容的每次修改進行額外的複製。 動態頂點緩衝區適用于轉譯動態幾何，以及從二進位空間分割樹狀結構或其他可視性資料結構提取的資料。 這可以透過預先配置所需格式的緩衝區來完成。 然後 parceled 這些資源，以支援應用程式內的資源管理員所需的應用程式需求。 動態頂點緩衝區總數很小，因為應用程式只會使用幾個不同的頂點進展，而且因為唯一的進展需要不同的頂點緩衝區。 以這種方式管理動態資源時，請確定對資源的高頻率需求不會大幅降低應用程式的效能。

使用 Direct3D 和應用程式所管理的資源時，請在 \_ 建立 direct3d 管理的資源之前，先在 D3DPOOL 預設記憶體中配置應用程式管理的資源。 這可讓記憶體管理員維持準確的可用記憶體計數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 資源](direct3d-resources.md)
</dt> </dl>

 

 



