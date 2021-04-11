---
description: UnregisterMIMEInfo 動作會從系統中取消註冊 MIME 相關的登錄資訊。 動作會從 MIME 資料表中取消註冊伺服器的 MIME 資訊，而這項功能目前已選取要卸載的對應功能。
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: UnregisterMIMEInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195417"
---
# <a name="unregistermimeinfo-action"></a><span data-ttu-id="78a39-104">UnregisterMIMEInfo 動作</span><span class="sxs-lookup"><span data-stu-id="78a39-104">UnregisterMIMEInfo Action</span></span>

<span data-ttu-id="78a39-105">UnregisterMIMEInfo 動作會從系統中取消註冊 MIME 相關的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="78a39-105">The UnregisterMIMEInfo action unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="78a39-106">動作會從 [mime 資料表](mime-table.md) 中取消註冊伺服器的 mime 資訊，而這項功能目前已選取要卸載的對應功能。</span><span class="sxs-lookup"><span data-stu-id="78a39-106">The action unregisters MIME information for servers from the [MIME table](mime-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="78a39-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="78a39-107">Sequence Restrictions</span></span>

<span data-ttu-id="78a39-108">UnregisterMIMEInfo 動作必須位於 [InstallInitialize](installinitialize-action.md) 動作、 [UnregisterClassInfo](unregisterclassinfo-action.md) 動作、 [UnregisterExtensionInfo](unregisterextensioninfo-action.md) 動作和 [RegisterMIMEInfo](registermimeinfo-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="78a39-108">The UnregisterMIMEInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action, and before the [RegisterMIMEInfo](registermimeinfo-action.md) action.</span></span>

<span data-ttu-id="78a39-109">[RemoveRegistryValues](removeregistryvalues-action.md) 必須在順序中 UnregisterMIMEInfo 之前。</span><span class="sxs-lookup"><span data-stu-id="78a39-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterMIMEInfo in the sequence.</span></span>

<span data-ttu-id="78a39-110">下列群組中的動作順序會受到限制。</span><span class="sxs-lookup"><span data-stu-id="78a39-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="78a39-111">如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="78a39-111">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="78a39-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="78a39-112">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="78a39-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="78a39-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="78a39-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="78a39-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   <span data-ttu-id="78a39-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="78a39-115">UnregisterMIMEInfo</span></span>
-   [<span data-ttu-id="78a39-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="78a39-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="78a39-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="78a39-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="78a39-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="78a39-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="78a39-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="78a39-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="78a39-120">例如，UnregisterMIMEInfo 必須在順序資料表的 [RegisterExtensionInfo](registerextensioninfo-action.md) 之前。</span><span class="sxs-lookup"><span data-stu-id="78a39-120">For example, UnregisterMIMEInfo must come before [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="78a39-121">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="78a39-121">ActionData Messages</span></span>



| <span data-ttu-id="78a39-122">欄位</span><span class="sxs-lookup"><span data-stu-id="78a39-122">Field</span></span> | <span data-ttu-id="78a39-123">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="78a39-123">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="78a39-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="78a39-124">\[1\]</span></span> | <span data-ttu-id="78a39-125">未註冊 MIME 內容類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="78a39-125">Identifier of unregistered MIME content type.</span></span> |
| <span data-ttu-id="78a39-126">\[2\]</span><span class="sxs-lookup"><span data-stu-id="78a39-126">\[2\]</span></span> | <span data-ttu-id="78a39-127">與 MIME 內容類型相關聯的副檔名。</span><span class="sxs-lookup"><span data-stu-id="78a39-127">Extension associated with MIME content type.</span></span>  |



 

 

 



