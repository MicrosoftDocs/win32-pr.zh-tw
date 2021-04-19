---
description: Quality-Control 管理
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control 管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971090"
---
# <a name="quality-control-management"></a>Quality-Control 管理

品質控制是一種機制，可透過篩選圖形來調整資料流程的速率，以回應執行時間效能。 如果轉譯器篩選器收到太多資料或太少資料，它可能會傳送 *品質訊息*。 品質訊息會要求資料速率的調整。 根據預設，品質訊息會從轉譯器行進上游，直到到達可回應 (（如果有任何) ）的篩選器為止。 應用程式也可以執行自訂的品質管制員。 在此情況下，轉譯器會將品質訊息直接傳遞至應用程式的品質管制員。

本文包含下列主題。

-   [品質訊息](quality-messages.md)
-   [預設品質控制項](default-quality-control.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選開發人員的資料流程](data-flow-for-filter-developers.md)
</dt> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



