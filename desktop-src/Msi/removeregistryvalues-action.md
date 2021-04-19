---
description: RemoveRegistryValues 動作只能從已撰寫至登錄資料表或 RemoveRegistry 資料表的系統登錄中移除值。
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: RemoveRegistryValues 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975140"
---
# <a name="removeregistryvalues-action"></a><span data-ttu-id="916ce-103">RemoveRegistryValues 動作</span><span class="sxs-lookup"><span data-stu-id="916ce-103">RemoveRegistryValues Action</span></span>

<span data-ttu-id="916ce-104">RemoveRegistryValues 動作只能從已撰寫至登錄 [資料表](registry-table.md) 或 [RemoveRegistry 資料表](removeregistry-table.md)的系統登錄中移除值。</span><span class="sxs-lookup"><span data-stu-id="916ce-104">The RemoveRegistryValues action can only remove values from the system registry that have been authored into the [Registry table](registry-table.md) or the [RemoveRegistry table](removeregistry-table.md).</span></span> <span data-ttu-id="916ce-105">如果相關聯的元件安裝在本機或從來源執行，而且現在已設定為要卸載，此動作會移除已在登錄表中撰寫的登錄值。</span><span class="sxs-lookup"><span data-stu-id="916ce-105">This action removes a registry value that has been authored into the Registry table if the associated component was installed locally or as run from source and is now set to be uninstalled.</span></span> <span data-ttu-id="916ce-106">如果相關聯的元件設定為在本機安裝或從來源執行，此動作會移除已撰寫至 RemoveRegistry 資料表的登錄值。</span><span class="sxs-lookup"><span data-stu-id="916ce-106">This action removes a registry value that has been authored into the RemoveRegistry table if the associated component is set to be installed locally or as run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="916ce-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="916ce-107">Sequence Restrictions</span></span>

<span data-ttu-id="916ce-108">呼叫 RemoveRegistryValues 之前，必須先呼叫 [InstallValidate](installvalidate-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="916ce-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveRegistryValues.</span></span> <span data-ttu-id="916ce-109">如果使用 [WriteRegistryValues](writeregistryvalues-action.md) 動作，它必須在 RemoveRegistryValues 之後。</span><span class="sxs-lookup"><span data-stu-id="916ce-109">If a [WriteRegistryValues](writeregistryvalues-action.md) action is used, it must come after RemoveRegistryValues.</span></span> <span data-ttu-id="916ce-110">RemoveRegistryValues 必須位於 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 或 [UnregisterProgIDInfo](unregisterprogidinfo-action.md)之前。</span><span class="sxs-lookup"><span data-stu-id="916ce-110">RemoveRegistryValues must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) or [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span></span>

<span data-ttu-id="916ce-111">自訂動作可在安裝、卸載或修復交易期間，用來將資料列新增至登錄 [資料表](registry-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="916ce-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="916ce-112">這些資料列不會保存在登錄資料表中，而且只有在目前的交易期間，才可使用此資訊。</span><span class="sxs-lookup"><span data-stu-id="916ce-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="916ce-113">因此，自訂動作必須在需要這些額外資料列資訊的每個安裝、卸載或修復交易中執行。</span><span class="sxs-lookup"><span data-stu-id="916ce-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="916ce-114">自訂動作必須位於動作順序中的 RemoveRegistryValues 和 [WriteRegistryValues](writeregistryvalues-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="916ce-114">The custom action must come before the RemoveRegistryValues and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="916ce-115">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="916ce-115">ActionData Messages</span></span>



| <span data-ttu-id="916ce-116">欄位</span><span class="sxs-lookup"><span data-stu-id="916ce-116">Field</span></span> | <span data-ttu-id="916ce-117">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="916ce-117">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="916ce-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="916ce-118">\[1\]</span></span> | <span data-ttu-id="916ce-119">已移除登錄值之索引鍵的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="916ce-119">Registry path to key of removed registry value.</span></span>     |
| <span data-ttu-id="916ce-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="916ce-120">\[2\]</span></span> | <span data-ttu-id="916ce-121">已移除之登錄值名稱的格式化字串。</span><span class="sxs-lookup"><span data-stu-id="916ce-121">Formatted string of name of removed registry value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="916ce-122">備註</span><span class="sxs-lookup"><span data-stu-id="916ce-122">Remarks</span></span>

<span data-ttu-id="916ce-123">若要移除登錄值，請將值記錄在登錄資料表的 [值] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="916ce-123">To remove a registry value, record the value in the Value column of the Registry table.</span></span> <span data-ttu-id="916ce-124">如果 WriteRegistryValues 動作已將 REG \_ 多重 \_ SZ 字串附加至登錄 [表](registry-table.md)中的值，則 RemoveRegistryValues 動作只會從登錄值移除這些字串。</span><span class="sxs-lookup"><span data-stu-id="916ce-124">If the WriteRegistryValues action has attached REG\_MULTI\_SZ strings to the value in the [Registry table](registry-table.md), then the RemoveRegistryValues action removes only those strings from the registry value.</span></span>

 

 



