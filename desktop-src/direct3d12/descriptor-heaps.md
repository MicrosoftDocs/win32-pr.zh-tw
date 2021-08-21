---
title: 描述元堆積
description: 描述元堆積是描述項連續配置的集合，每個描述項的一個配置。
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd883436954cb6e1f0270646f1a57d564f3d51d29b6023bec749d1728fda40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807550"
---
# <a name="descriptor-heaps"></a>描述元堆積

描述元堆積是描述項連續配置的集合，每個描述項的一個配置。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                             | 描述                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [描述元堆積總覽](descriptor-heaps-overview.md)<br/>                             | 描述元堆積包含許多不屬於管線狀態物件的物件類型 (PSO) ，例如著色器資源查看 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器。 <br/>                |
| [硬體層](hardware-support.md)<br/>                                                 | 第1層到第3層的硬體層級已增加管線的可用資源。 <br/>                                                                                                                              |
| [著色器可見的描述元堆積](shader-visible-descriptor-heaps.md)<br/>                 | 著色器可見的描述元堆積是可透過描述中繼資料表來參考著色器的描述元堆積。<br/>                                                                                                              |
| [非著色器可見描述元堆積](non-shader-visible-descriptor-heaps.md)<br/>         | 部分描述元堆積無法透過描述項資料表來參考著色器，但存在於記錄命令清單之前，或因為不需要著色器可見的堆積，以協助應用程式暫存描述項。<br/> |
| [建立描述元堆積](creating-descriptor-heaps.md)<br/>                             | 若要建立和設定描述元堆積，您必須選取描述項堆積類型、判斷它包含多少個描述元，以及設定旗標，指出它是否為 CPU 可見和/或著色器可見。 <br/>                    |
| [設定和填入描述元堆積](setting-descriptor-heaps.md)<br/>                | 可以在命令清單上設定的描述項堆積型別，也就是包含描述項資料表的描述項，其中每一次最多隻能使用 (的描述中繼資料表) 。 <br/>                                                        |
| [描述元堆積的配置摘要](descriptor-heap-configurability-summary.md)<br/> | 下表摘要說明著色器和非著色器可見堆積支援的相關資訊。<br/>                                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[描述項](descriptors.md)
</dt> <dt>

[描述中繼資料表](descriptor-tables.md)
</dt> <dt>

[**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[資源系結](resource-binding.md)
</dt> <dt>

[根簽章](root-signatures.md)
</dt> </dl>

 

 





