---
description: UnregisterComPlus 動作會從登錄中移除 COM + 應用程式。
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: UnregisterComPlus 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945414"
---
# <a name="unregistercomplus-action"></a><span data-ttu-id="89377-103">UnregisterComPlus 動作</span><span class="sxs-lookup"><span data-stu-id="89377-103">UnregisterComPlus Action</span></span>

<span data-ttu-id="89377-104">UnregisterComPlus 動作會從登錄中移除 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="89377-104">The UnregisterComPlus action removes COM+ applications from the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="89377-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="89377-105">Sequence Restrictions</span></span>

<span data-ttu-id="89377-106">[RegisterComPlus 動作](registercomplus-action.md)必須遵循[InstallFiles 動作](installfiles-action.md)和 UnregisterComPlus 動作。</span><span class="sxs-lookup"><span data-stu-id="89377-106">The [RegisterComPlus action](registercomplus-action.md) must follow the [InstallFiles action](installfiles-action.md) and the UnregisterComPlus action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="89377-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="89377-107">ActionData Messages</span></span>



| <span data-ttu-id="89377-108">欄位</span><span class="sxs-lookup"><span data-stu-id="89377-108">Field</span></span> | <span data-ttu-id="89377-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="89377-109">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="89377-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="89377-110">\[1\]</span></span> | <span data-ttu-id="89377-111">要移除之 COM + 應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="89377-111">Application identifier of the COM+ application being removed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="89377-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="89377-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89377-113">RegisterComPlus 動作</span><span class="sxs-lookup"><span data-stu-id="89377-113">RegisterComPlus action</span></span>](registercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="89377-114">Complus 資料表</span><span class="sxs-lookup"><span data-stu-id="89377-114">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="89377-115">安裝具有 Windows Installer 的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="89377-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



