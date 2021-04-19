---
description: RegisterClassInfo 動作會管理 COM 類別資訊與系統的註冊。 它會使用 AppId 資料表。
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: RegisterClassInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988777"
---
# <a name="registerclassinfo-action"></a><span data-ttu-id="73956-104">RegisterClassInfo 動作</span><span class="sxs-lookup"><span data-stu-id="73956-104">RegisterClassInfo Action</span></span>

<span data-ttu-id="73956-105">RegisterClassInfo 動作會管理 COM 類別資訊與系統的註冊。</span><span class="sxs-lookup"><span data-stu-id="73956-105">The RegisterClassInfo action manages the registration of COM class information with the system.</span></span> <span data-ttu-id="73956-106">它會使用 [AppId 資料表](appid-table.md)。</span><span class="sxs-lookup"><span data-stu-id="73956-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="73956-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="73956-107">Sequence Restrictions</span></span>

<span data-ttu-id="73956-108">RegisterClassInfo 動作必須位於 [InstallFiles](installfiles-action.md) 動作和 [UnregisterClassInfo](unregisterclassinfo-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="73956-108">The RegisterClassInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterClassInfo](unregisterclassinfo-action.md) action.</span></span>

<span data-ttu-id="73956-109">下列群組中的動作順序會受到限制。</span><span class="sxs-lookup"><span data-stu-id="73956-109">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="73956-110">如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="73956-110">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="73956-111">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="73956-111">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="73956-112">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="73956-112">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="73956-113">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="73956-113">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="73956-114">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="73956-114">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   <span data-ttu-id="73956-115">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="73956-115">RegisterClassInfo</span></span>
-   [<span data-ttu-id="73956-116">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="73956-116">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="73956-117">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="73956-117">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="73956-118">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="73956-118">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="73956-119">例如，RegisterClassInfo 必須在 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 的順序資料表中。</span><span class="sxs-lookup"><span data-stu-id="73956-119">For example, RegisterClassInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="73956-120">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="73956-120">ActionData Messages</span></span>



| <span data-ttu-id="73956-121">欄位</span><span class="sxs-lookup"><span data-stu-id="73956-121">Field</span></span> | <span data-ttu-id="73956-122">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="73956-122">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="73956-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="73956-123">\[1\]</span></span> | <span data-ttu-id="73956-124">已註冊 COM 伺服器的 GUID 類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="73956-124">GUID class identifier of the registered COM server.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="73956-125">備註</span><span class="sxs-lookup"><span data-stu-id="73956-125">Remarks</span></span>

<span data-ttu-id="73956-126">如果系統支援 OLE 伺服器的隨選安裝，RegisterClassInfo 會在與選取要安裝或通告之功能相關聯的 [類別資料表](class-table.md) 中註冊所有 COM 類別。</span><span class="sxs-lookup"><span data-stu-id="73956-126">If the system supports install-on-demand for OLE servers, RegisterClassInfo registers all COM classes in the [Class table](class-table.md) associated with a feature selected to be installed or advertised.</span></span> <span data-ttu-id="73956-127">否則，此動作只會註冊與選取要安裝之功能相關聯的 COM 類別。</span><span class="sxs-lookup"><span data-stu-id="73956-127">Otherwise this action only registers the COM classes associated with a feature selected for installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73956-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="73956-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73956-129">**OLEAdvtSupport 屬性**</span><span class="sxs-lookup"><span data-stu-id="73956-129">**OLEAdvtSupport property**</span></span>](oleadvtsupport.md)
</dt> </dl>

 

 



