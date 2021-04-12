---
description: 管理智慧卡資料庫，使用指定的 resource manager 內容來更新資料庫。
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: 智慧卡資料庫管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319899"
---
# <a name="smart-card-database-management-functions"></a><span data-ttu-id="e7ad4-103">智慧卡資料庫管理功能</span><span class="sxs-lookup"><span data-stu-id="e7ad4-103">Smart Card Database Management Functions</span></span>

<span data-ttu-id="e7ad4-104">下列函式會管理 [*智慧卡資料庫*](../secgloss/s-gly.md)，並使用指定的 [*resource manager 內容*](../secgloss/r-gly.md)來更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-104">The following functions manage the [*smart card database*](../secgloss/s-gly.md), updating the database by using a specified [*resource manager context*](../secgloss/r-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="e7ad4-105">藉由在資料庫上放置存取限制，而不是將安全性機制新增至 [*智慧卡子系統*](../secgloss/s-gly.md)，來維護資料庫安全性。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-105">Database security is maintained by placing access restrictions on the database, rather than by adding security mechanisms to the [*smart card subsystem*](../secgloss/s-gly.md).</span></span>

 



| <span data-ttu-id="e7ad4-106">主題</span><span class="sxs-lookup"><span data-stu-id="e7ad4-106">Topic</span></span>                                                            | <span data-ttu-id="e7ad4-107">描述</span><span class="sxs-lookup"><span data-stu-id="e7ad4-107">Description</span></span>                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7ad4-108">**SCardAddReaderToGroup**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-108">**SCardAddReaderToGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | <span data-ttu-id="e7ad4-109">將 [*讀者*](../secgloss/r-gly.md) 新增至 [*讀者群組*](../secgloss/r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-109">Add a [*reader*](../secgloss/r-gly.md) to a [*reader group*](../secgloss/r-gly.md).</span></span> |
| [<span data-ttu-id="e7ad4-110">**SCardForgetCardType**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-110">**SCardForgetCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | <span data-ttu-id="e7ad4-111">從系統移除智慧卡。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-111">Remove a smart card from the system.</span></span>                                                                                                                                    |
| [<span data-ttu-id="e7ad4-112">**SCardForgetReader**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-112">**SCardForgetReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | <span data-ttu-id="e7ad4-113">移除系統中的讀取器。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-113">Remove a reader from the system.</span></span>                                                                                                                                        |
| [<span data-ttu-id="e7ad4-114">**SCardForgetReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-114">**SCardForgetReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | <span data-ttu-id="e7ad4-115">從系統移除讀取器群組。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-115">Remove a reader group from the system.</span></span>                                                                                                                                  |
| [<span data-ttu-id="e7ad4-116">**SCardIntroduceCardType**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-116">**SCardIntroduceCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | <span data-ttu-id="e7ad4-117">將新的卡片引進系統。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-117">Introduce a new card to the system.</span></span>                                                                                                                                     |
| [<span data-ttu-id="e7ad4-118">**SCardIntroduceReader**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-118">**SCardIntroduceReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | <span data-ttu-id="e7ad4-119">為系統引進新的讀取器。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-119">Introduce a new reader to the system.</span></span>                                                                                                                                   |
| [<span data-ttu-id="e7ad4-120">**SCardIntroduceReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-120">**SCardIntroduceReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | <span data-ttu-id="e7ad4-121">為系統引進新的讀取器群組。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-121">Introduce a new reader group to the system.</span></span>                                                                                                                             |
| [<span data-ttu-id="e7ad4-122">**SCardRemoveReaderFromGroup**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-122">**SCardRemoveReaderFromGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | <span data-ttu-id="e7ad4-123">從讀取器群組移除讀取器。</span><span class="sxs-lookup"><span data-stu-id="e7ad4-123">Remove a reader from a reader group.</span></span>                                                                                                                                    |



 

 

 
