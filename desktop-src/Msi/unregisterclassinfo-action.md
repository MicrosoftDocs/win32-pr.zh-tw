---
description: UnregisterClassInfo 動作會管理從系統登錄移除 COM 類別資訊。 它會使用 AppId 資料表。
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: UnregisterClassInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001454"
---
# <a name="unregisterclassinfo-action"></a><span data-ttu-id="8f718-104">UnregisterClassInfo 動作</span><span class="sxs-lookup"><span data-stu-id="8f718-104">UnregisterClassInfo Action</span></span>

<span data-ttu-id="8f718-105">UnregisterClassInfo 動作會管理從系統登錄移除 COM 類別資訊。</span><span class="sxs-lookup"><span data-stu-id="8f718-105">The UnregisterClassInfo action manages the removal of COM class information from the system registry.</span></span> <span data-ttu-id="8f718-106">它會使用 [AppId 資料表](appid-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8f718-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8f718-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="8f718-107">Sequence Restrictions</span></span>

<span data-ttu-id="8f718-108">UnregisterClassInfo 動作必須在 [InstallInitialize](installinitialize-action.md) 動作之後，以及在 [RegisterClassInfo](registerclassinfo-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="8f718-108">The UnregisterClassInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterClassInfo](registerclassinfo-action.md) action.</span></span>

<span data-ttu-id="8f718-109">[RemoveRegistryValues](removeregistryvalues-action.md) 必須在順序中 UnregisterClassInfo 之前。</span><span class="sxs-lookup"><span data-stu-id="8f718-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterClassInfo in the sequence.</span></span>

<span data-ttu-id="8f718-110">下列群組中的動作順序會受到限制。</span><span class="sxs-lookup"><span data-stu-id="8f718-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="8f718-111">如果這些動作的任何子集在順序資料表中一起發生，它們必須以與下表所示相同的相對順序發生：</span><span class="sxs-lookup"><span data-stu-id="8f718-111">If any subset of these actions occur together in a sequence table, they must occur in the same relative sequence as shown in the following table:</span></span>

-   <span data-ttu-id="8f718-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="8f718-112">UnregisterClassInfo</span></span>
-   [<span data-ttu-id="8f718-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="8f718-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="8f718-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="8f718-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="8f718-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="8f718-115">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="8f718-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="8f718-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="8f718-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="8f718-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="8f718-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="8f718-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="8f718-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="8f718-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="8f718-120">例如， [RegisterExtensionInfo](registerextensioninfo-action.md) 必須在順序資料表的 UnregisterClassInfo 之前。</span><span class="sxs-lookup"><span data-stu-id="8f718-120">For example, [RegisterExtensionInfo](registerextensioninfo-action.md) must come before UnregisterClassInfo in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8f718-121">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="8f718-121">ActionData Messages</span></span>



| <span data-ttu-id="8f718-122">欄位</span><span class="sxs-lookup"><span data-stu-id="8f718-122">Field</span></span> | <span data-ttu-id="8f718-123">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="8f718-123">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="8f718-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8f718-124">\[1\]</span></span> | <span data-ttu-id="8f718-125">未註冊 COM 類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8f718-125">GUID of unregistered COM class.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8f718-126">備註</span><span class="sxs-lookup"><span data-stu-id="8f718-126">Remarks</span></span>

<span data-ttu-id="8f718-127">當目前使用者的系統已升級為搭配透過 COM 的隨選安裝時，安裝程式會將 [**OLEAdvtSupport**](oleadvtsupport.md) 屬性設定為 true。</span><span class="sxs-lookup"><span data-stu-id="8f718-127">The installer sets the [**OLEAdvtSupport**](oleadvtsupport.md) property to true when the current user's system has been upgraded to work with install-on-demand through COM.</span></span> <span data-ttu-id="8f718-128">如果系統不支援透過 COM 進行隨選安裝，UnregisterClassInfo 會將與已卸載的功能或安裝的功能相關聯之 [類別資料表](class-table.md) 中所列的所有 COM 類別，從系統登錄中移除。</span><span class="sxs-lookup"><span data-stu-id="8f718-128">If the system does not support install-on-demand through COM, UnregisterClassInfo removes all COM classes listed in the [Class table](class-table.md) associated with either uninstalled features or features installed as advertised from the system registry.</span></span> <span data-ttu-id="8f718-129">否則，此動作只會移除與選取要從系統登錄卸載之功能相關聯的 COM 類別。</span><span class="sxs-lookup"><span data-stu-id="8f718-129">Otherwise, this action removes only the COM classes associated with features selected to be uninstalled from the system registry.</span></span>

 

 



