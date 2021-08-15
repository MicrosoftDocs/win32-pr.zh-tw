---
title: 元組索引的運作方式
description: 元組索引是用來優化有0個或更多字串中間詞搜尋字串的搜尋，以及0或1個最終搜尋字串。 如果沒有任何一般索引可在該屬性上使用，它們也可以用來將初始搜尋字串的搜尋優化。
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- 元組索引編制
- 搜尋 Active Directory Active Directory，優化
- Active Directory，搜尋優化 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9d15bad8de15e4f559123d2d3cb3b6b9ec6446328e6ed4c4c52cf18355d634
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188031"
---
# <a name="how-tuple-indexing-works"></a>元組索引的運作方式

元組索引是用來優化有0個或更多 [字串中間詞搜尋字串](search-string-types.md) 的搜尋，以及0或1個最終搜尋字串。 如果沒有任何一般索引可在該屬性上使用，它們也可以用來將初始搜尋字串的搜尋優化。

您可以在 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) 屬性中，設定與值32對應的 bit 5，來開啟屬性的元組索引編制。 這個屬性是在代表需要元組索引之屬性的架構物件中所設定。 開啟元組索引的效能影響，是針對該屬性所設定的任何字串值，將會擴充到元組索引中的大量片段。 當屬性展開時，它會在目錄資訊樹狀目錄中耗用較大量的磁碟空間，而且更新速度也會變慢。

元組索引是設計來加速搜尋表單 `*string*` 。 加速可能很大，因為這種形式的搜尋無法以任何其他方式進行優化，而且在其未優化的表單中，它會強制 Active Directory 伺服器在搜尋範圍中的每個物件上執行查詢。 因此，基底搜尋只會搜尋一個物件（這會使用較少的資源），而立即的子系搜尋則只會搜尋物件的子系， (可以使用較少的資源或更多資源（視容器) 大小而定），而子樹搜尋將會逐步解說基底物件下的整個子樹，因為子樹大小的關係

元組索引會藉由將字串分成 *元組* 來運作。 例如，字串 "Active Directory" 會分成下列元組：

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> 當擴充元組索引的字串時，目錄將會在32767個字元停止。

 

元組索引會包含每一個元組的專案。 因此，如果使用者搜尋 `*cto*` ，Active Directory 伺服器將會在索引中尋找 "cto" 的所有相符專案，在此情況下，請尋找具有 (元組索引) 屬性值為 "Directory" 之記錄的指標。

如果 `*cto*` 上一個範例中 (的搜尋字串) 特定，則搜尋將會相當有效率，因為它可大幅減少 Active Directory 伺服器必須檢查以執行查詢的物件數目。

 

 