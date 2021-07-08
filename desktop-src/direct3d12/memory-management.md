---
title: Direct3D 12 中的記憶體管理
description: 移至 D3D12 牽涉到適當的同步處理和管理記憶體存放區。
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481803"
---
# <a name="memory-management-in-direct3d-12"></a>Direct3D 12 中的記憶體管理

移至 D3D12 牽涉到適當的同步處理和管理記憶體存放區。 管理記憶體存放區表示需要進行更多的同步處理。 本節涵蓋記憶體管理原則，以及在堆積和緩衝區內的子分配。

-   [本節內容](#in-this-section)
-   [相關主題](#related-topics)

## <a name="in-this-section"></a>本節內容



| 主題                                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [記憶體管理原則](memory-management-strategies.md)<br/> | 適用于 Direct3D 12 的記憶體管理員可能會因為所有不同的支援層級（適用于 UMA 或離散 (非 UMA) 介面卡）而變得非常複雜，並且在 GPU 介面卡之間有很大的架構差異。<br/> 本章節所述之 Direct3D 12 記憶體管理的建議策略是「分類、預算和串流」。<br/> |
| [在緩衝區內進行子分配](large-buffers.md)<br/>                | 緩衝區具有 D3D12 for applications 中所需的所有功能，以將大量暫時性資料從 CPU 傳送至 GPU。 本節涵蓋使用和管理資源和緩衝區的四個常見案例。<br/>                                                                                                                                     |
| [堆積中的子分配](suballocation-within-heaps.md)<br/>     | 資源堆積會將資料從 CPU 傳輸到 GPU (上傳) ，然後從 GPU 到 CPU (讀回) 。 <br/>                                                                                                                                                                                                                                                                  |
| [居住](residency.md)<br/>                                       | 當 GPU 可存取物件時，會將物件視為 *駐留* 。<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 程式設計指南](directx-12-programming-guide.md)
</dt> <dt>

[資源系結](resource-binding.md)
</dt> </dl>

 

 





