---
description: UnregisterTypeLibraries 動作會從系統中取消註冊類型程式庫。 此動作會套用至在 TypeLib 資料表中所列的每個檔案，該檔案會被觸發為已卸載。
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: UnregisterTypeLibraries 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971650"
---
# <a name="unregistertypelibraries-action"></a><span data-ttu-id="9ea2a-104">UnregisterTypeLibraries 動作</span><span class="sxs-lookup"><span data-stu-id="9ea2a-104">UnregisterTypeLibraries Action</span></span>

<span data-ttu-id="9ea2a-105">UnregisterTypeLibraries 動作會從系統中取消註冊類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="9ea2a-105">The UnregisterTypeLibraries action unregisters type libraries from the system.</span></span> <span data-ttu-id="9ea2a-106">此動作會套用至在 [TypeLib](typelib-table.md) 資料表中所列的每個檔案，該檔案會被觸發為已卸載。</span><span class="sxs-lookup"><span data-stu-id="9ea2a-106">This action is applied to each file listed in the [TypeLib](typelib-table.md) table that is triggered to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9ea2a-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="9ea2a-107">Sequence Restrictions</span></span>

<span data-ttu-id="9ea2a-108">UnregisterTypeLibraries 動作必須位於 [RemoveFiles](removefiles-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="9ea2a-108">The UnregisterTypeLibraries action must come before the [RemoveFiles](removefiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9ea2a-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="9ea2a-109">ActionData Messages</span></span>



| <span data-ttu-id="9ea2a-110">欄位</span><span class="sxs-lookup"><span data-stu-id="9ea2a-110">Field</span></span> | <span data-ttu-id="9ea2a-111">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="9ea2a-111">Description of action data</span></span>                        |
|-------|---------------------------------------------------|
| <span data-ttu-id="9ea2a-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9ea2a-112">\[1\]</span></span> | <span data-ttu-id="9ea2a-113">未註冊之類型程式庫的[GUID](guid.md) 。</span><span class="sxs-lookup"><span data-stu-id="9ea2a-113">[GUID](guid.md) of an unregistered type library.</span></span> |



 

 

 



