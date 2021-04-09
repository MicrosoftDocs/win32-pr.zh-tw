---
description: InstallInitialize 動作和 InstallFinalize 動作會標示變更系統的一連串動作的開頭和結尾。
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: InstallInitialize 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690779"
---
# <a name="installinitialize-action"></a><span data-ttu-id="b120a-103">InstallInitialize 動作</span><span class="sxs-lookup"><span data-stu-id="b120a-103">InstallInitialize Action</span></span>

<span data-ttu-id="b120a-104">InstallInitialize 動作和 [InstallFinalize](installfinalize-action.md) 動作會標示變更系統的一連串動作的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="b120a-104">The InstallInitialize action and [InstallFinalize](installfinalize-action.md) action mark the beginning and end of a sequence of actions that change the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b120a-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="b120a-105">Sequence Restrictions</span></span>

<span data-ttu-id="b120a-106">InstallInitialize 動作必須在任何變更系統的動作之前排序，例如 [InstallFiles](installfiles-action.md) 動作、 [WriteRegistryValues](writeregistryvalues-action.md) 動作、 [SelfRegModules](selfregmodules-action.md) 動作和 [ProcessComponents](processcomponents-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="b120a-106">The InstallInitialize action must be sequenced before any actions that change the system, such as the [InstallFiles](installfiles-action.md) action, the [WriteRegistryValues](writeregistryvalues-action.md) action, the [SelfRegModules](selfregmodules-action.md) action, and the [ProcessComponents](processcomponents-action.md) action.</span></span> <span data-ttu-id="b120a-107">因此，InstallInitialize 動作必須在 [InstallFinalize](installfinalize-action.md) 動作和 [InstallExecute](installexecute-action.md) 動作之前進行排序。</span><span class="sxs-lookup"><span data-stu-id="b120a-107">The InstallInitialize action must therefore be sequenced before the [InstallFinalize](installfinalize-action.md) action and the [InstallExecute](installexecute-action.md) action.</span></span>

<span data-ttu-id="b120a-108">修改 Windows Installer 封裝的[自訂動作](custom-actions.md)（例如，將資料列加入至處理可安裝資源的資料表，例如登錄[資料表或](registry-table.md) [DuplicateFile](duplicatefile-table.md)資料表）必須在 InstallInitialize 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="b120a-108">[Custom actions](custom-actions.md) that modify the Windows Installer package, for example by adding rows to a table that handles installable resources, such as the [Registry](registry-table.md) table or [DuplicateFile](duplicatefile-table.md) table, must be sequenced before InstallInitialize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b120a-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="b120a-109">ActionData Messages</span></span>

<span data-ttu-id="b120a-110">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="b120a-110">There are no ActionData messages.</span></span>

 

 



