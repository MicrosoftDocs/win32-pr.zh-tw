---
description: RegisterExtensionInfo 動作會管理與系統相關的擴充功能相關資訊的註冊。
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: RegisterExtensionInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982407"
---
# <a name="registerextensioninfo-action"></a><span data-ttu-id="4c840-103">RegisterExtensionInfo 動作</span><span class="sxs-lookup"><span data-stu-id="4c840-103">RegisterExtensionInfo Action</span></span>

<span data-ttu-id="4c840-104">RegisterExtensionInfo 動作會管理與系統相關的擴充功能相關資訊的註冊。</span><span class="sxs-lookup"><span data-stu-id="4c840-104">The RegisterExtensionInfo action manages the registration of extension related information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4c840-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="4c840-105">Sequence Restrictions</span></span>

<span data-ttu-id="4c840-106">RegisterExtensionInfo 動作必須位於 [InstallFiles](installfiles-action.md) 動作和 [UnregisterExtensionInfo](unregisterextensioninfo-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="4c840-106">The RegisterExtensionInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action.</span></span>

<span data-ttu-id="4c840-107">下列群組中的動作順序會受到限制。</span><span class="sxs-lookup"><span data-stu-id="4c840-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="4c840-108">如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4c840-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="4c840-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="4c840-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="4c840-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="4c840-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="4c840-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="4c840-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="4c840-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="4c840-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="4c840-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="4c840-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   <span data-ttu-id="4c840-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="4c840-114">RegisterExtensionInfo</span></span>
-   [<span data-ttu-id="4c840-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="4c840-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="4c840-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="4c840-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="4c840-117">例如，RegisterExtensionInfo 必須在 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 的順序資料表中。</span><span class="sxs-lookup"><span data-stu-id="4c840-117">For example, RegisterExtensionInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4c840-118">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="4c840-118">ActionData Messages</span></span>



| <span data-ttu-id="4c840-119">欄位</span><span class="sxs-lookup"><span data-stu-id="4c840-119">Field</span></span> | <span data-ttu-id="4c840-120">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="4c840-120">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="4c840-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4c840-121">\[1\]</span></span> | <span data-ttu-id="4c840-122">註冊的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4c840-122">Registered extension.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="4c840-123">備註</span><span class="sxs-lookup"><span data-stu-id="4c840-123">Remarks</span></span>

<span data-ttu-id="4c840-124">如果系統支援擴充功能伺服器的隨選安裝，RegisterExtensionInfo 會在與安裝或公告設定的功能相關聯的 [延伸模組表格](extension-table.md) 中註冊所有延伸模組伺服器。</span><span class="sxs-lookup"><span data-stu-id="4c840-124">If the system supports installation-on-demand for extension servers, RegisterExtensionInfo registers all extension servers in the [Extension table](extension-table.md) associated with features set for installation or advertisement.</span></span> <span data-ttu-id="4c840-125">否則，此動作只會註冊與設定為安裝的功能相關聯的延伸模組伺服器。</span><span class="sxs-lookup"><span data-stu-id="4c840-125">Otherwise this action only registers extension servers associated with features set to installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c840-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c840-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c840-127">**ShellAdvtSupport 屬性**</span><span class="sxs-lookup"><span data-stu-id="4c840-127">**ShellAdvtSupport property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



