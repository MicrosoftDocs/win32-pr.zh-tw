---
description: 讓您追蹤讀者內的牌。 這些常式通常會 \_ 在陣列中使用捨棄 READERSTATE 結構。
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: 智慧卡追蹤功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851340"
---
# <a name="smart-card-tracking-functions"></a><span data-ttu-id="5d8a7-104">智慧卡追蹤功能</span><span class="sxs-lookup"><span data-stu-id="5d8a7-104">Smart Card Tracking Functions</span></span>

<span data-ttu-id="5d8a7-105">下列函數可讓您追蹤讀者內的卡片。</span><span class="sxs-lookup"><span data-stu-id="5d8a7-105">The following functions let you track cards within readers.</span></span> <span data-ttu-id="5d8a7-106">這些常式通常會在陣列中使用 [**捨棄 \_ READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) 結構。</span><span class="sxs-lookup"><span data-stu-id="5d8a7-106">These routines typically use the [**SCARD\_READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) structure within an array.</span></span>



| <span data-ttu-id="5d8a7-107">主題</span><span class="sxs-lookup"><span data-stu-id="5d8a7-107">Topic</span></span>                                                | <span data-ttu-id="5d8a7-108">描述</span><span class="sxs-lookup"><span data-stu-id="5d8a7-108">Description</span></span>                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d8a7-109">**SCardLocateCards**</span><span class="sxs-lookup"><span data-stu-id="5d8a7-109">**SCardLocateCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | <span data-ttu-id="5d8a7-110">搜尋其 [*ATR 字串*](../secgloss/a-gly.md) 符合所提供卡片名稱的卡片。</span><span class="sxs-lookup"><span data-stu-id="5d8a7-110">Search for a card whose [*ATR string*](../secgloss/a-gly.md) matches a supplied card name.</span></span> |
| [<span data-ttu-id="5d8a7-111">**SCardGetStatusChange**</span><span class="sxs-lookup"><span data-stu-id="5d8a7-111">**SCardGetStatusChange**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | <span data-ttu-id="5d8a7-112">封鎖執行，直到卡片目前的可用性變更為止。</span><span class="sxs-lookup"><span data-stu-id="5d8a7-112">Block execution until the current availability of cards changes.</span></span>                                                                       |
| [<span data-ttu-id="5d8a7-113">**SCardCancel**</span><span class="sxs-lookup"><span data-stu-id="5d8a7-113">**SCardCancel**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | <span data-ttu-id="5d8a7-114">終止未完成的動作。</span><span class="sxs-lookup"><span data-stu-id="5d8a7-114">Terminate outstanding actions.</span></span>                                                                                                         |



 

 

 
