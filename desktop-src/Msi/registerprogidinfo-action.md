---
description: RegisterProgIdInfo 動作會管理與系統之間的 OLE ProgId 資訊註冊。
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: RegisterProgIdInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001365"
---
# <a name="registerprogidinfo-action"></a><span data-ttu-id="2b800-103">RegisterProgIdInfo 動作</span><span class="sxs-lookup"><span data-stu-id="2b800-103">RegisterProgIdInfo Action</span></span>

<span data-ttu-id="2b800-104">RegisterProgIdInfo 動作會管理與系統之間的 OLE ProgId 資訊註冊。</span><span class="sxs-lookup"><span data-stu-id="2b800-104">The RegisterProgIdInfo action manages the registration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2b800-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="2b800-105">Sequence Restrictions</span></span>

<span data-ttu-id="2b800-106">RegisterProgIdInfo 動作必須位於 [InstallFiles](installfiles-action.md) 動作、 [UnregisterProgIdInfo](unregisterprogidinfo-action.md) 動作、 [RegisterClassInfo](registerclassinfo-action.md) 動作和 [RegisterExtensionInfo](registerextensioninfo-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="2b800-106">The RegisterProgIdInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterProgIdInfo](unregisterprogidinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="2b800-107">下列群組中的動作順序會受到限制。</span><span class="sxs-lookup"><span data-stu-id="2b800-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="2b800-108">如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2b800-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="2b800-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="2b800-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="2b800-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="2b800-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="2b800-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="2b800-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="2b800-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="2b800-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="2b800-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="2b800-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="2b800-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="2b800-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   <span data-ttu-id="2b800-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="2b800-115">RegisterProgIdInfo</span></span>
-   [<span data-ttu-id="2b800-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="2b800-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="2b800-117">例如，RegisterProgIdInfo 必須在 [RegisterExtensionInfo](registerextensioninfo-action.md) 的順序資料表中。</span><span class="sxs-lookup"><span data-stu-id="2b800-117">For example, RegisterProgIdInfo must come after [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2b800-118">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="2b800-118">ActionData Messages</span></span>



| <span data-ttu-id="2b800-119">欄位</span><span class="sxs-lookup"><span data-stu-id="2b800-119">Field</span></span> | <span data-ttu-id="2b800-120">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="2b800-120">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="2b800-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2b800-121">\[1\]</span></span> | <span data-ttu-id="2b800-122">已註冊程式的程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b800-122">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2b800-123">備註</span><span class="sxs-lookup"><span data-stu-id="2b800-123">Remarks</span></span>

<span data-ttu-id="2b800-124">RegisterProgIdInfo 動作會註冊 [progid 資料表](progid-table.md) 中指定之伺服器的所有 progid 資訊，以及已選取要安裝的對應類別伺服器或延伸模組伺服器。</span><span class="sxs-lookup"><span data-stu-id="2b800-124">The RegisterProgIdInfo action registers all ProgId information for servers that are specified in the [ProgId table](progid-table.md) and for which the corresponding class server or extension server has been selected to be installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b800-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b800-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b800-126">類別資料表</span><span class="sxs-lookup"><span data-stu-id="2b800-126">Class table</span></span>](class-table.md)
</dt> <dt>

[<span data-ttu-id="2b800-127">延伸模組資料表</span><span class="sxs-lookup"><span data-stu-id="2b800-127">Extension table</span></span>](extension-table.md)
</dt> </dl>

 

 



