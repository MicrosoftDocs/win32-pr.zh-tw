---
description: 根據預設，Windows Search 引擎和目錄不區分語音符號，也就是新增至字母以改變單字意義或發音的重音符號。
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: 搜尋中的變音符號敏感度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fcde4eb6cde6fe7a0b25a1d58f8026176de2fe30b6b0e2f020275821891a404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863681"
---
# <a name="diacritic-sensitivity-in-searches"></a>搜尋中的變音符號敏感度

根據預設，Windows Search 引擎和目錄不區分語音符號，也就是新增至字母以改變單字意義或發音的重音符號。 不過，Windows Search 可讓您使用[目錄管理員](-search-3x-wds-mngidx-catalog-manager.md)為您的目錄變更此設定，以設定變音符號的敏感度。 例如，如果將變音符號敏感度設為 **FALSE**，則目錄會將 "resume" 和 "resumé" 視為相同的文字。

在查詢層中，在 FREETEXT 和 CONTAINS 子句中具有變音符號的查詢詞彙會傳遞至引擎，然後正規化 (，就像在索引時間) 進行比對一樣。 針對目錄進行比對時，一律會區分變音符號。

> [!Note]  
> 這不是字元範圍 0x2e81-f8ff 和 0x1100 0x11ff 的情況。

 

 

 



