---
description: RegisterComPlus 動作會註冊 COM + 應用程式。
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: RegisterComPlus 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115501"
---
# <a name="registercomplus-action"></a><span data-ttu-id="4879f-103">RegisterComPlus 動作</span><span class="sxs-lookup"><span data-stu-id="4879f-103">RegisterComPlus Action</span></span>

<span data-ttu-id="4879f-104">RegisterComPlus 動作會註冊 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="4879f-104">The RegisterComPlus action registers COM+ applications.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4879f-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="4879f-105">Sequence Restrictions</span></span>

<span data-ttu-id="4879f-106">RegisterComPlus 動作必須遵循 [InstallFiles 動作](installfiles-action.md) 和 [UnregisterComPlus 動作](unregistercomplus-action.md)。</span><span class="sxs-lookup"><span data-stu-id="4879f-106">The RegisterComPlus action must follow the [InstallFiles action](installfiles-action.md) and the [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4879f-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="4879f-107">ActionData Messages</span></span>



| <span data-ttu-id="4879f-108">欄位</span><span class="sxs-lookup"><span data-stu-id="4879f-108">Field</span></span> | <span data-ttu-id="4879f-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="4879f-109">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="4879f-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4879f-110">\[1\]</span></span> | <span data-ttu-id="4879f-111">COM + 應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="4879f-111">Application ID of the COM+ application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4879f-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="4879f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4879f-113">Complus 資料表</span><span class="sxs-lookup"><span data-stu-id="4879f-113">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="4879f-114">UnregisterComPlus 動作</span><span class="sxs-lookup"><span data-stu-id="4879f-114">UnregisterComPlus action</span></span>](unregistercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="4879f-115">安裝具有 Windows Installer 的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="4879f-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



