---
description: DeleteServices 動作會停止服務，並從系統中移除其註冊。 此動作會查詢 ServiceControl 資料表。
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: DeleteServices 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319515"
---
# <a name="deleteservices-action"></a><span data-ttu-id="b6456-104">DeleteServices 動作</span><span class="sxs-lookup"><span data-stu-id="b6456-104">DeleteServices Action</span></span>

<span data-ttu-id="b6456-105">DeleteServices 動作會停止服務，並從系統中移除其註冊。</span><span class="sxs-lookup"><span data-stu-id="b6456-105">The DeleteServices action stops a service and removes its registration from the system.</span></span> <span data-ttu-id="b6456-106">此動作會查詢 [ServiceControl 資料表](servicecontrol-table.md)。</span><span class="sxs-lookup"><span data-stu-id="b6456-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b6456-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="b6456-107">Sequence Restrictions</span></span>

<span data-ttu-id="b6456-108">服務動作必須以下列順序使用：</span><span class="sxs-lookup"><span data-stu-id="b6456-108">The services actions must be used in the following sequence:</span></span>

1.  [<span data-ttu-id="b6456-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="b6456-109">StopServices</span></span>](stopservices-action.md)
2.  <span data-ttu-id="b6456-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="b6456-110">DeleteServices</span></span>
3.  <span data-ttu-id="b6456-111">下列任何一個動作： [InstallFiles](installfiles-action.md)、 [RemoveFiles](removefiles-action.md)、 [DuplicateFiles](duplicatefiles-action.md)、 [MoveFiles](movefiles-action.md)、 [PatchFiles](patchfiles-action.md)和 [RemoveDuplicateFiles](removeduplicatefiles-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="b6456-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>
4.  [<span data-ttu-id="b6456-112">InstallServices 動作</span><span class="sxs-lookup"><span data-stu-id="b6456-112">InstallServices action</span></span>](installservices-action.md)
5.  [<span data-ttu-id="b6456-113">StartServices</span><span class="sxs-lookup"><span data-stu-id="b6456-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="b6456-114">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="b6456-114">ActionData Messages</span></span>



| <span data-ttu-id="b6456-115">欄位</span><span class="sxs-lookup"><span data-stu-id="b6456-115">Field</span></span> | <span data-ttu-id="b6456-116">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="b6456-116">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="b6456-117">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b6456-117">\[1\]</span></span> | <span data-ttu-id="b6456-118">服務顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b6456-118">Service display name.</span></span>      |
| <span data-ttu-id="b6456-119">\[2\]</span><span class="sxs-lookup"><span data-stu-id="b6456-119">\[2\]</span></span> | <span data-ttu-id="b6456-120">服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b6456-120">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="b6456-121">備註</span><span class="sxs-lookup"><span data-stu-id="b6456-121">Remarks</span></span>

<span data-ttu-id="b6456-122">這項動作需要使用者是系統管理員，或具有可刪除服務或應用程式屬於受管理安裝之許可權的更高許可權。</span><span class="sxs-lookup"><span data-stu-id="b6456-122">This action requires the user be an administrator or have elevated privileges with permission to delete services or that the application be part of a managed installation.</span></span>

 

 



