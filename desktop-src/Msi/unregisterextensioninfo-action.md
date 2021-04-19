---
description: UnregisterExtensionInfo 動作會管理從系統登錄移除擴充功能相關資訊的功能。
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: UnregisterExtensionInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986628"
---
# <a name="unregisterextensioninfo-action"></a><span data-ttu-id="2ee65-103">UnregisterExtensionInfo 動作</span><span class="sxs-lookup"><span data-stu-id="2ee65-103">UnregisterExtensionInfo Action</span></span>

<span data-ttu-id="2ee65-104">UnregisterExtensionInfo 動作會管理從系統登錄移除擴充功能相關資訊的功能。</span><span class="sxs-lookup"><span data-stu-id="2ee65-104">The UnregisterExtensionInfo action manages the removal of extension-related information from the system registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2ee65-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="2ee65-105">Sequence Restrictions</span></span>

<span data-ttu-id="2ee65-106">UnregisterExtensionInfo 動作必須在 [InstallInitialize](installinitialize-action.md) 動作之後，以及在 [RegisterExtensionInfo](registerextensioninfo-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="2ee65-106">The UnregisterExtensionInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="2ee65-107">[RemoveRegistryValues](removeregistryvalues-action.md) 必須在順序中 UnregisterExtensionInfo 之前。</span><span class="sxs-lookup"><span data-stu-id="2ee65-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterExtensionInfo in the sequence.</span></span>

<span data-ttu-id="2ee65-108">下列群組中的動作順序會受到限制。</span><span class="sxs-lookup"><span data-stu-id="2ee65-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="2ee65-109">如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2ee65-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="2ee65-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="2ee65-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   <span data-ttu-id="2ee65-111">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="2ee65-111">UnregisterExtensionInfo</span></span>
-   [<span data-ttu-id="2ee65-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="2ee65-112">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="2ee65-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="2ee65-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="2ee65-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="2ee65-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="2ee65-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="2ee65-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="2ee65-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="2ee65-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="2ee65-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="2ee65-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="2ee65-118">例如，UnregisterExtensionInfo 必須在順序資料表的 [UnregisterProgIdInfo](unregisterprogidinfo-action.md) 之前。</span><span class="sxs-lookup"><span data-stu-id="2ee65-118">For example, UnregisterExtensionInfo must come before [UnregisterProgIdInfo](unregisterprogidinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2ee65-119">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="2ee65-119">ActionData Messages</span></span>



| <span data-ttu-id="2ee65-120">欄位</span><span class="sxs-lookup"><span data-stu-id="2ee65-120">Field</span></span> | <span data-ttu-id="2ee65-121">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="2ee65-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="2ee65-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2ee65-122">\[1\]</span></span> | <span data-ttu-id="2ee65-123">已移除擴充功能。</span><span class="sxs-lookup"><span data-stu-id="2ee65-123">Removed extension.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="2ee65-124">備註</span><span class="sxs-lookup"><span data-stu-id="2ee65-124">Remarks</span></span>

<span data-ttu-id="2ee65-125">如果系統不支援擴充功能伺服器的隨選安裝，UnregisterExtensionInfo 會移除 [延伸模組資料表](extension-table.md) 中與已卸載的功能相關聯的所有擴充功能伺服器，或從登錄中安裝的功能。</span><span class="sxs-lookup"><span data-stu-id="2ee65-125">If the system does not support the install-on-demand of extension servers, UnregisterExtensionInfo removes all extension servers in the [Extension table](extension-table.md) associated with either an uninstalled feature or a feature installed as advertised from the registry.</span></span> <span data-ttu-id="2ee65-126">否則，此動作會移除與已選取要從登錄中移除之功能相關聯的延伸模組伺服器。</span><span class="sxs-lookup"><span data-stu-id="2ee65-126">Otherwise, this action removes the extension servers associated with a feature that is selected to be removed from the registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ee65-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ee65-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ee65-128">**ShellAdvtSupport 屬性**</span><span class="sxs-lookup"><span data-stu-id="2ee65-128">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



