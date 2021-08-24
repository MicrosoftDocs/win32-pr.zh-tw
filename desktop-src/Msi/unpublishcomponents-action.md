---
description: UnpublishComponents 動作會管理 PublishComponent 資料表中所列元件的 unadvertisement。
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: UnpublishComponents 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1feaca4449ffa344eeda828334f879ebc12905406446dd14623e3b9c4474c6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810258"
---
# <a name="unpublishcomponents-action"></a>UnpublishComponents 動作

UnpublishComponents 動作會管理 PublishComponent 資料表中所列元件的 unadvertisement。 這些是其他產品可能發生錯誤的元件。 此動作會從 [PublishComponent 資料表](publishcomponent-table.md) 中移除已發行之元件的相關資訊，而此資料表目前已選取要卸載的對應功能。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID，代表已公告功能的元件識別碼。 |
| \[2\] | 元件識別碼的辨識符號。                               |



 

