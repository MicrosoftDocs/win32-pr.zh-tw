---
description: RemoveShortcuts 動作會管理移除已選取要卸載其功能的已公告快捷方式，或已選取要卸載其元件之 nonadvertised 快速鍵的移除。 如需詳細資訊，請參閱快速鍵對應表。
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: RemoveShortcuts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975139"
---
# <a name="removeshortcuts-action"></a><span data-ttu-id="8cfd9-104">RemoveShortcuts 動作</span><span class="sxs-lookup"><span data-stu-id="8cfd9-104">RemoveShortcuts Action</span></span>

<span data-ttu-id="8cfd9-105">RemoveShortcuts 動作會管理移除已選取要卸載其功能的已公告快捷方式，或已選取要卸載其元件之 nonadvertised 快速鍵的移除。</span><span class="sxs-lookup"><span data-stu-id="8cfd9-105">The RemoveShortcuts action manages the removal of an advertised shortcut whose feature is selected for uninstallation or a nonadvertised shortcut whose component is selected for uninstallation.</span></span> <span data-ttu-id="8cfd9-106">如需詳細資訊，請參閱 [快速鍵對應表](shortcut-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8cfd9-106">For more information, see the [Shortcut Table](shortcut-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8cfd9-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="8cfd9-107">Sequence Restrictions</span></span>

<span data-ttu-id="8cfd9-108">RemoveShortcuts 動作必須位於 [CreateShortcuts](createshortcuts-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="8cfd9-108">The RemoveShortcuts action must come before the [CreateShortcuts](createshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8cfd9-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="8cfd9-109">ActionData Messages</span></span>



| <span data-ttu-id="8cfd9-110">欄位</span><span class="sxs-lookup"><span data-stu-id="8cfd9-110">Field</span></span> | <span data-ttu-id="8cfd9-111">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="8cfd9-111">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="8cfd9-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8cfd9-112">\[1\]</span></span> | <span data-ttu-id="8cfd9-113">已移除快捷方式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8cfd9-113">Identifier of removed shortcut.</span></span> |



 

 

 



