---
description: WriteRegistryValues 動作會設定應用程式的登錄資訊。
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: WriteRegistryValues 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975754"
---
# <a name="writeregistryvalues-action"></a><span data-ttu-id="7d0e6-103">WriteRegistryValues 動作</span><span class="sxs-lookup"><span data-stu-id="7d0e6-103">WriteRegistryValues Action</span></span>

<span data-ttu-id="7d0e6-104">WriteRegistryValues 動作會設定應用程式的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-104">The WriteRegistryValues action sets up an application's registry information.</span></span> <span data-ttu-id="7d0e6-105">登錄資訊會由 [元件表格](component-table.md)進行閘道。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-105">The registry information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="7d0e6-106">如果對應的元件已設定為要安裝在本機或從來源執行，則會將登錄值寫入登錄。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-106">A registry value is written to the registry if the corresponding component has been set to be installed either locally or as run from source.</span></span> <span data-ttu-id="7d0e6-107">如需詳細資訊，請參閱登錄 [表](registry-table.md)。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-107">For more information, see [Registry table](registry-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7d0e6-108">順序限制</span><span class="sxs-lookup"><span data-stu-id="7d0e6-108">Sequence Restrictions</span></span>

<span data-ttu-id="7d0e6-109">[InstallValidate 動作](installvalidate-action.md)必須位於 WriteRegistryValues 動作之前。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-109">The [InstallValidate action](installvalidate-action.md) must come before the WriteRegistryValues action.</span></span> <span data-ttu-id="7d0e6-110">如果有 [RemoveRegistryValues 動作](removeregistryvalues-action.md)，它必須在 WriteRegistryValues 動作之前。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-110">If there is a [RemoveRegistryValues action](removeregistryvalues-action.md), then it must come before the WriteRegistryValues action.</span></span>

<span data-ttu-id="7d0e6-111">自訂動作可在安裝、卸載或修復交易期間，用來將資料列新增至登錄 [資料表](registry-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="7d0e6-112">這些資料列不會保存在登錄資料表中，而且只有在目前的交易期間，才可使用此資訊。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="7d0e6-113">因此，自訂動作必須在需要這些額外資料列資訊的每個安裝、卸載或修復交易中執行。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="7d0e6-114">自訂動作必須位於動作順序中的 [RemoveRegistryValues](removeregistryvalues-action.md) 和 WriteRegistryValues 動作之前。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-114">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and WriteRegistryValues actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7d0e6-115">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="7d0e6-115">ActionData Messages</span></span>



| <span data-ttu-id="7d0e6-116">欄位</span><span class="sxs-lookup"><span data-stu-id="7d0e6-116">Field</span></span> | <span data-ttu-id="7d0e6-117">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="7d0e6-117">Description of action data</span></span>                               |
|-------|----------------------------------------------------------|
| <span data-ttu-id="7d0e6-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7d0e6-118">\[1\]</span></span> | <span data-ttu-id="7d0e6-119">寫入登錄之值的登錄機碼路徑。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-119">Path to registry key of value written to registry.</span></span>       |
| <span data-ttu-id="7d0e6-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="7d0e6-120">\[2\]</span></span> | <span data-ttu-id="7d0e6-121">寫入登錄之值的格式化文字字串名稱。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-121">Formatted text string name of value written to registry.</span></span> |
| <span data-ttu-id="7d0e6-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="7d0e6-122">\[3\]</span></span> | <span data-ttu-id="7d0e6-123">寫入登錄之值的格式化文字字串。</span><span class="sxs-lookup"><span data-stu-id="7d0e6-123">Formatted text string of value written to registry.</span></span>      |



 

 

 



