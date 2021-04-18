---
description: UnpublishComponents 動作會管理 PublishComponent 資料表中所列元件的 unadvertisement。
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: UnpublishComponents 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104386414"
---
# <a name="unpublishcomponents-action"></a><span data-ttu-id="5e248-103">UnpublishComponents 動作</span><span class="sxs-lookup"><span data-stu-id="5e248-103">UnpublishComponents Action</span></span>

<span data-ttu-id="5e248-104">UnpublishComponents 動作會管理 PublishComponent 資料表中所列元件的 unadvertisement。</span><span class="sxs-lookup"><span data-stu-id="5e248-104">The UnpublishComponents action manages the unadvertisement of components listed in the PublishComponent table.</span></span> <span data-ttu-id="5e248-105">這些是其他產品可能發生錯誤的元件。</span><span class="sxs-lookup"><span data-stu-id="5e248-105">These are components that may be faulted in by other products.</span></span> <span data-ttu-id="5e248-106">此動作會從 [PublishComponent 資料表](publishcomponent-table.md) 中移除已發行之元件的相關資訊，而此資料表目前已選取要卸載的對應功能。</span><span class="sxs-lookup"><span data-stu-id="5e248-106">This action removes information about published components from the [PublishComponent table](publishcomponent-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5e248-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="5e248-107">Sequence Restrictions</span></span>

<span data-ttu-id="5e248-108">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="5e248-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5e248-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="5e248-109">ActionData Messages</span></span>



| <span data-ttu-id="5e248-110">欄位</span><span class="sxs-lookup"><span data-stu-id="5e248-110">Field</span></span> | <span data-ttu-id="5e248-111">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="5e248-111">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="5e248-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5e248-112">\[1\]</span></span> | <span data-ttu-id="5e248-113">GUID，代表已公告功能的元件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e248-113">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="5e248-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="5e248-114">\[2\]</span></span> | <span data-ttu-id="5e248-115">元件識別碼的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="5e248-115">Qualifier of the component ID.</span></span>                               |



 

