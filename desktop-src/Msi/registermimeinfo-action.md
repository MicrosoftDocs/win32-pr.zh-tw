---
description: RegisterMIMEInfo 動作會向系統註冊 MIME 相關的登錄資訊。
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: RegisterMIMEInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692952"
---
# <a name="registermimeinfo-action"></a><span data-ttu-id="1c7c9-103">RegisterMIMEInfo 動作</span><span class="sxs-lookup"><span data-stu-id="1c7c9-103">RegisterMIMEInfo Action</span></span>

<span data-ttu-id="1c7c9-104">RegisterMIMEInfo 動作會向系統註冊 MIME 相關的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="1c7c9-104">The RegisterMIMEInfo action registers MIME-related registry information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1c7c9-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="1c7c9-105">Sequence Restrictions</span></span>

<span data-ttu-id="1c7c9-106">RegisterMIMEInfo 動作必須位於 [InstallFiles](installfiles-action.md) 動作、 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 動作、 [RegisterClassInfo](registerclassinfo-action.md) 動作和 [RegisterExtensionInfo](registerextensioninfo-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="1c7c9-106">The RegisterMIMEInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterMIMEInfo](unregistermimeinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="1c7c9-107">下列群組中的動作順序會受到限制。</span><span class="sxs-lookup"><span data-stu-id="1c7c9-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="1c7c9-108">如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1c7c9-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="1c7c9-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="1c7c9-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="1c7c9-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="1c7c9-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="1c7c9-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="1c7c9-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="1c7c9-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="1c7c9-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="1c7c9-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="1c7c9-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="1c7c9-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="1c7c9-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="1c7c9-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="1c7c9-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   <span data-ttu-id="1c7c9-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="1c7c9-116">RegisterMIMEInfo</span></span>

<span data-ttu-id="1c7c9-117">例如，RegisterMIMEInfo 必須在 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 的順序資料表中。</span><span class="sxs-lookup"><span data-stu-id="1c7c9-117">For example, RegisterMIMEInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1c7c9-118">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="1c7c9-118">ActionData Messages</span></span>



| <span data-ttu-id="1c7c9-119">欄位</span><span class="sxs-lookup"><span data-stu-id="1c7c9-119">Field</span></span> | <span data-ttu-id="1c7c9-120">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="1c7c9-120">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="1c7c9-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1c7c9-121">\[1\]</span></span> | <span data-ttu-id="1c7c9-122">已註冊之 MIME 內容類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c7c9-122">Identifier of registered MIME content type.</span></span>  |
| <span data-ttu-id="1c7c9-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="1c7c9-123">\[2\]</span></span> | <span data-ttu-id="1c7c9-124">與 MIME 內容類型相關聯的副檔名。</span><span class="sxs-lookup"><span data-stu-id="1c7c9-124">Extension associated with MIME content type.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1c7c9-125">備註</span><span class="sxs-lookup"><span data-stu-id="1c7c9-125">Remarks</span></span>

<span data-ttu-id="1c7c9-126">RegisterMIMEInfo 動作會註冊 [mime 資料表](mime-table.md) 中，已選取要安裝對應類別伺服器或延伸模組伺服器之伺服器的所有 mime 資訊。</span><span class="sxs-lookup"><span data-stu-id="1c7c9-126">The RegisterMIMEInfo action registers all MIME information for servers from the [MIME table](mime-table.md) for which the corresponding class server or extension server has been selected to be installed.</span></span>

 

 



