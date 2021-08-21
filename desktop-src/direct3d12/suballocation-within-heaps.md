---
title: 堆積中的子分配
description: 資源堆積會將資料從 CPU 傳輸到 GPU (上傳) ，然後從 GPU 到 CPU (讀回) 。
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bdda33f1db1b0f798e9c3d18d8b3f33f7fbc30638ae6d62d38c0d5e2767463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912134"
---
# <a name="suballocation-within-heaps"></a>堆積中的子分配

資源堆積會將資料從 CPU 傳輸到 GPU (上傳) ，然後從 GPU 到 CPU (讀回) 。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [記憶體別名和資料繼承](memory-aliasing-and-data-inheritance.md)<br/> | 放置和保留的資源可能會在堆積內為實體記憶體加上別名。 當堆積已設定共用旗標，或當別名的資源有完整定義的記憶體配置時，放置的資源可提供比保留資源更多的資料繼承案例。 <br/> |
| [共用堆積](shared-heaps.md)<br/>                                                 | 共用適用于多進程和多介面卡架構。<br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID3D12Device::CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[記憶體管理](memory-management.md)
</dt> </dl>

 

 





