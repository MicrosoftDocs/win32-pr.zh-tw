---
title: 計數器、查詢和效能測量
description: 下列各節說明在效能測試和改進（例如查詢、計數器、計時和 predication）中使用的功能。
ms.assetid: C7AEF1A0-36FB-4026-9CCF-ED0206961A58
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4940f6c32ac8754a8a8d41fd7c849d6023775e833988611988d3a6979bd3cace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631988"
---
# <a name="counters-queries-and-performance-measurement"></a>計數器、查詢和效能測量

下列各節說明在效能測試和改進（例如查詢、計數器、計時和 predication）中使用的功能。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [資料流程-輸出計數器、UAV 計數器、查詢和 Predication](counters-and-queries.md)<br/> | 串流輸出和 UAV 計數器會在與 Direct3D 11 類似的方法中，在 Direct3D 12 中運作，不過現在計數器的記憶體必須由應用程式佈建，驅動程式並不會這麼做。 Direct3D 12 中的查詢與 Direct3D 11 中的查詢更加不同，另外還新增了一些程式來移除某些查詢類型的需求。<br/> |
| [計時](timing.md)<br/>                                                                       | 本節涵蓋查詢時間戳記，以及校準 GPU 和 CPU 時間戳計數器。<br/>                                                                                                                                                                                                                                                            |
| [預測](predication.md)<br/>                                                             | Predication 是一項功能，可啟用 GPU 而非 CPU 來決定不繪製、複製或分派物件。<br/>                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 程式設計指南](directx-12-programming-guide.md)
</dt> </dl>

 

 





