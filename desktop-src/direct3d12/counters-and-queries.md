---
title: 計數器、查詢和 predication
description: 串流輸出和 UAV 計數器會在與 Direct3D 11 類似的方法中，在 Direct3D 12 中運作，不過現在計數器的記憶體必須由應用程式佈建，驅動程式並不會這麼做。
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548450"
---
# <a name="counters-queries-and-predication"></a>計數器、查詢和 predication

本主題涵蓋資料流程輸出計數器、UAV 計數器、查詢和 predication。

串流輸出和 UAV 計數器會在與 Direct3D 11 類似的方法中，在 Direct3D 12 中運作，不過現在計數器的記憶體必須由應用程式佈建，驅動程式並不會這麼做。 Direct3D 12 中的查詢與 Direct3D 11 中的查詢更加不同，另外還新增了一些程式來移除某些查詢類型的需求。

## <a name="in-this-section"></a>本節內容



| 主題                                                           | 描述                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [串流輸出計數器](stream-output-counters.md)<br/> | 資料流程輸出是 GPU 將頂點寫入緩衝區的能力。 資料流程輸出計數器會監視進度。<br/>                                                               |
| [UAV 計數器](uav-counters.md)<br/>                     | UAV 計數器可以用來將32位不可部分完成的計數器與未排序的存取權 (UAV) 產生關聯。<br/>                                                                                |
| [查詢](queries.md)<br/>                               | 在 Direct3D 12 中，查詢會分組為稱為查詢堆積的查詢陣列。 查詢堆積有一種類型，可定義可搭配該堆積使用的有效查詢類型。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效能測量](performance-measurement.md)
</dt> </dl>

 

 





