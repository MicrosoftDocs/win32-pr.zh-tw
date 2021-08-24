---
description: Quality-Control 管理
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control 管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824410b697a29ee73fc269748595fdcae91d054a161561b282536a05dcf92ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747708"
---
# <a name="quality-control-management"></a>Quality-Control 管理

品質控制是一種機制，可透過篩選圖形來調整資料流程的速率，以回應執行時間效能。 如果轉譯器篩選器收到太多資料或太少資料，它可能會傳送 *品質訊息*。 品質訊息會要求資料速率的調整。 根據預設，品質訊息會從轉譯器行進上游，直到到達可回應 (（如果有任何) ）的篩選器為止。 應用程式也可以執行自訂的品質管制員。 在此情況下，轉譯器會將品質訊息直接傳遞至應用程式的品質管制員。

本文包含下列主題。

-   [品質訊息](quality-messages.md)
-   [預設品質控制項](default-quality-control.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選準則開發人員的資料 Flow](data-flow-for-filter-developers.md)
</dt> <dt>

[撰寫 DirectShow 篩選](writing-directshow-filters.md)
</dt> </dl>

 

 



