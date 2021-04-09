---
description: UnregisterProgIdInfo 動作會管理將 OLE ProgId 資訊與系統的註冊。
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: UnregisterProgIdInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852920"
---
# <a name="unregisterprogidinfo-action"></a><span data-ttu-id="fca04-103">UnregisterProgIdInfo 動作</span><span class="sxs-lookup"><span data-stu-id="fca04-103">UnregisterProgIdInfo Action</span></span>

<span data-ttu-id="fca04-104">UnregisterProgIdInfo 動作會管理將 OLE ProgId 資訊與系統的註冊。</span><span class="sxs-lookup"><span data-stu-id="fca04-104">The UnregisterProgIdInfo action manages the unregistration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fca04-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="fca04-105">Sequence Restrictions</span></span>

<span data-ttu-id="fca04-106">UnregisterProgIdInfo 動作必須位於 [InstallInitialize](installinitialize-action.md) 動作、 [UnregisterClassInfo](unregisterclassinfo-action.md) 動作、 [UnregisterExtensioninfo](unregisterextensioninfo-action.md) 動作和 [RegisterProgIdInfo](registerprogidinfo-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="fca04-106">The UnregisterProgIdInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action, and before the [RegisterProgIdInfo](registerprogidinfo-action.md) action.</span></span>

<span data-ttu-id="fca04-107">[RemoveRegistryValues](removeregistryvalues-action.md) 必須在順序中 UnregisterProgIdInfo 之前。</span><span class="sxs-lookup"><span data-stu-id="fca04-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterProgIdInfo in the sequence.</span></span>

<span data-ttu-id="fca04-108">下列群組中的動作順序會受到限制。</span><span class="sxs-lookup"><span data-stu-id="fca04-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="fca04-109">如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fca04-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="fca04-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="fca04-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="fca04-111">UnregisterExtensioninfo</span><span class="sxs-lookup"><span data-stu-id="fca04-111">UnregisterExtensioninfo</span></span>](unregisterextensioninfo-action.md)
-   <span data-ttu-id="fca04-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="fca04-112">UnregisterProgIdInfo</span></span>
-   [<span data-ttu-id="fca04-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="fca04-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="fca04-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="fca04-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="fca04-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="fca04-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="fca04-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="fca04-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="fca04-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="fca04-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="fca04-118">例如，UnregisterProgIdInfo 必須在順序資料表的 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 之前。</span><span class="sxs-lookup"><span data-stu-id="fca04-118">For example, UnregisterProgIdInfo must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fca04-119">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="fca04-119">ActionData Messages</span></span>



| <span data-ttu-id="fca04-120">欄位</span><span class="sxs-lookup"><span data-stu-id="fca04-120">Field</span></span> | <span data-ttu-id="fca04-121">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="fca04-121">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="fca04-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fca04-122">\[1\]</span></span> | <span data-ttu-id="fca04-123">已註冊程式的程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="fca04-123">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fca04-124">備註</span><span class="sxs-lookup"><span data-stu-id="fca04-124">Remarks</span></span>

<span data-ttu-id="fca04-125">UnregisterProgIdInfo 動作會從登錄中移除 ProgId 資訊 ([Progid 資料表](progid-table.md)) 針對連接到擴充功能資訊 ([延伸模組資料表](extension-table.md)) 或類別資訊 ([類別表](class-table.md)) 和目前已選取要卸載的功能。</span><span class="sxs-lookup"><span data-stu-id="fca04-125">The UnregisterProgIdInfo action removes ProgId information from the registry ([ProgId Table](progid-table.md)) for features that are connected to the extension information ([Extension table](extension-table.md)) or the Class information ([Class table](class-table.md)) and are currently selected to be uninstalled.</span></span>

 

 



