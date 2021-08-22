---
description: 成本是指判斷安裝的總磁碟空間需求的過程。
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: 檔案成本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad2dc3ad9da4fab21345e74f3f9db99992445d7cf1e2266806bda55cd6ca638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529578"
---
# <a name="file-costing"></a>檔案成本

成本是指判斷安裝的總磁碟空間需求的過程。 在檔案成本處理常式中計算的元素包括安裝或移除檔案的磁碟空間量，以及由登錄專案、快捷方式和其他檔案所佔用的磁碟空間量。 已排程要覆寫的現有檔案也會以磁片的總成本計算。

總成本會以每個[元件](components-and-features.md) 為基礎累積，並由三個不同的部分組成：本地成本、來源成本和移除成本。 這些元件會對應至元件安裝在本機、安裝從來源媒體執行，或移除時所產生的磁片成本。

所有涉及安裝檔案成本的計算，取決於要安裝或移除檔案的磁片區。 每次與元件相關聯的目錄變更時，都必須重新計算該元件所控制之安裝檔案的成本。 例如，由於目錄變更可能也表示磁片區變更，因此必須重新計算叢集檔案大小。 此外，必須檢查新的目錄，以判斷是否有任何可能覆寫的現有檔案都必須列入考慮。

呼叫 [CostInitialize](costinitialize-action.md) 動作之後，必須呼叫 [FileCost](filecost-action.md) 動作。 CostInitialize 動作會初始化安裝程式的內部常式，以動態計算與標準安裝動作相關的磁片成本。 此時不會進行任何其他動態成本計算。

接下來，必須呼叫 [CostFinalize](costfinalize-action.md) 動作。 此動作會完成所有成本計算，並透過 [元件](component-table.md) 資料表來提供成本資料。

在 [CostFinalize](costfinalize-action.md) 動作完成執行之後， [元件](component-table.md) 資料表就會完全初始化，而且可以視需要起始包含 [SelectionTree](selectiontree-control.md) 控制項的使用者介面對話方塊序列。 使用者介面對話方塊可提供選項，將 [功能](feature-table.md) 資料表中任何功能的選取狀態或目的地目錄變更為使用者。 元件的選取狀態變更時，此程式很類似。不過，在此情況下，只會重新計算已變更元件的動態成本。

使用者在使用者介面中完成選取功能之後，應呼叫 [InstallValidate](installvalidate-action.md) 動作。 此動作會確認成本已屬性化的所有磁片區都有足夠的空間可進行安裝。

 

 



