---
description: StartServices 動作會啟動系統服務。 此動作會查詢 ServiceControl 資料表。
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: StartServices 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974625"
---
# <a name="startservices-action"></a><span data-ttu-id="04d0f-104">StartServices 動作</span><span class="sxs-lookup"><span data-stu-id="04d0f-104">StartServices Action</span></span>

<span data-ttu-id="04d0f-105">StartServices 動作會啟動系統服務。</span><span class="sxs-lookup"><span data-stu-id="04d0f-105">The StartServices action starts system services.</span></span> <span data-ttu-id="04d0f-106">此動作會查詢 [ServiceControl 資料表](servicecontrol-table.md)。</span><span class="sxs-lookup"><span data-stu-id="04d0f-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="04d0f-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="04d0f-107">Sequence Restrictions</span></span>

<span data-ttu-id="04d0f-108">服務動作必須以下列順序使用：</span><span class="sxs-lookup"><span data-stu-id="04d0f-108">The services actions must be used in the following sequence:</span></span>

-   [<span data-ttu-id="04d0f-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="04d0f-109">StopServices</span></span>](stopservices-action.md)
-   [<span data-ttu-id="04d0f-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="04d0f-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="04d0f-111">下列任一動作：</span><span class="sxs-lookup"><span data-stu-id="04d0f-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="04d0f-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="04d0f-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="04d0f-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="04d0f-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="04d0f-114">DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="04d0f-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="04d0f-115">MoveFiles</span><span class="sxs-lookup"><span data-stu-id="04d0f-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="04d0f-116">PatchFiles</span><span class="sxs-lookup"><span data-stu-id="04d0f-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="04d0f-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="04d0f-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="04d0f-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="04d0f-118">InstallServices</span></span>](installservices-action.md)
-   <span data-ttu-id="04d0f-119">StartServices</span><span class="sxs-lookup"><span data-stu-id="04d0f-119">StartServices</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="04d0f-120">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="04d0f-120">ActionData Messages</span></span>



| <span data-ttu-id="04d0f-121">欄位</span><span class="sxs-lookup"><span data-stu-id="04d0f-121">Field</span></span> | <span data-ttu-id="04d0f-122">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="04d0f-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="04d0f-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="04d0f-123">\[1\]</span></span> | <span data-ttu-id="04d0f-124">服務顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="04d0f-124">Service display name.</span></span>      |
| <span data-ttu-id="04d0f-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="04d0f-125">\[2\]</span></span> | <span data-ttu-id="04d0f-126">服務名稱。</span><span class="sxs-lookup"><span data-stu-id="04d0f-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="04d0f-127">備註</span><span class="sxs-lookup"><span data-stu-id="04d0f-127">Remarks</span></span>

<span data-ttu-id="04d0f-128">此動作會要求使用者必須是系統管理員或具有控制服務之許可權的較高許可權，或應用程式屬於受管理安裝的一部分。</span><span class="sxs-lookup"><span data-stu-id="04d0f-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



