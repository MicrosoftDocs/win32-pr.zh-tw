---
description: 根據預設，Windows Search 引擎和目錄不區分語音符號，也就是新增至字母以改變單字意義或發音的重音符號。
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: 搜尋中的變音符號敏感度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966683"
---
# <a name="diacritic-sensitivity-in-searches"></a><span data-ttu-id="4bb78-103">搜尋中的變音符號敏感度</span><span class="sxs-lookup"><span data-stu-id="4bb78-103">Diacritic Sensitivity in Searches</span></span>

<span data-ttu-id="4bb78-104">根據預設，Windows Search 引擎和目錄不區分語音符號，也就是新增至字母以改變單字意義或發音的重音符號。</span><span class="sxs-lookup"><span data-stu-id="4bb78-104">By default, the Windows Search engine and catalog are insensitive to diacritics, which are accent marks added to letters to alter a word's meaning or pronunciation.</span></span> <span data-ttu-id="4bb78-105">不過，Windows Search 可讓您使用 [目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 為您的目錄變更此設定，以設定變音符號的敏感度。</span><span class="sxs-lookup"><span data-stu-id="4bb78-105">However, Windows Search enables you to change this for your catalog using the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to set diacritic sensitivity.</span></span> <span data-ttu-id="4bb78-106">例如，如果將變音符號敏感度設為 **FALSE**，則目錄會將 "resume" 和 "resumé" 視為相同的文字。</span><span class="sxs-lookup"><span data-stu-id="4bb78-106">For example, with diacritic sensitivity set to **FALSE**, the catalog would treat "resume" and "resumé" as if they were the same word.</span></span>

<span data-ttu-id="4bb78-107">在查詢層中，在 FREETEXT 和 CONTAINS 子句中具有變音符號的查詢詞彙會傳遞至引擎，然後正規化 (，就像在索引時間) 進行比對一樣。</span><span class="sxs-lookup"><span data-stu-id="4bb78-107">At the query layer, query terms with diacritics in FREETEXT and CONTAINS clauses are passed through to the engine and are then normalized (as they would be at index time) for matching.</span></span> <span data-ttu-id="4bb78-108">針對目錄進行比對時，一律會區分變音符號。</span><span class="sxs-lookup"><span data-stu-id="4bb78-108">Matching against the catalog is always diacritic sensitive.</span></span>

> [!Note]  
> <span data-ttu-id="4bb78-109">這不是字元範圍 0x2e81-f8ff 和 0x1100 0x11ff 的情況。</span><span class="sxs-lookup"><span data-stu-id="4bb78-109">This is not the case for the character ranges 0x2e81-f8ff and 0x1100-0x11ff.</span></span>

 

 

 



