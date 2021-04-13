---
title: IAccessible 設計考慮
description: 本節將討論伺服器開發人員在根據 IAccessible 介面設計類別時所面臨的問題。
ms.assetid: 240cdff1-a4c3-477a-b146-2ac295d7a148
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb8648bd0398117f1d3da895ff4b4288aa5e7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301159"
---
# <a name="iaccessible-design-considerations"></a><span data-ttu-id="51875-103">IAccessible 設計考慮</span><span class="sxs-lookup"><span data-stu-id="51875-103">IAccessible Design Considerations</span></span>

<span data-ttu-id="51875-104">本節將討論伺服器開發人員在根據 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面設計類別時所面臨的問題。</span><span class="sxs-lookup"><span data-stu-id="51875-104">This section discusses the issues that server developer face when designing classes based on the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51875-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="51875-105">In this section</span></span>

-   [<span data-ttu-id="51875-106">選擇建立可存取物件的時機</span><span class="sxs-lookup"><span data-stu-id="51875-106">Choosing When to Create Accessible Objects</span></span>](choosing-when-to-create-accessible-objects.md)
-   [<span data-ttu-id="51875-107">選擇要支援的屬性</span><span class="sxs-lookup"><span data-stu-id="51875-107">Choosing Which Properties to Support</span></span>](choosing-which-properties-to-support.md)
-   [<span data-ttu-id="51875-108">選擇描述性屬性的內容</span><span class="sxs-lookup"><span data-stu-id="51875-108">Choosing the Content for Descriptive Properties</span></span>](choosing-the-content-for-descriptive-properties.md)
-   [<span data-ttu-id="51875-109">設定動畫或移動物件的屬性</span><span class="sxs-lookup"><span data-stu-id="51875-109">Setting Properties for Animated or Moving Objects</span></span>](setting-properties-for-animated-or-moving-objects.md)
-   [<span data-ttu-id="51875-110">產生適當的 WinEvents</span><span class="sxs-lookup"><span data-stu-id="51875-110">Generating Appropriate WinEvents</span></span>](generating-appropriate-winevents.md)
-   [<span data-ttu-id="51875-111">公開 IAccessible 介面未涵蓋的其他資訊</span><span class="sxs-lookup"><span data-stu-id="51875-111">Exposing Additional Information Not Covered by IAccessible Interface</span></span>](exposing-additional-information-not-covered-by-iaccessible-interface.md)

 

 




