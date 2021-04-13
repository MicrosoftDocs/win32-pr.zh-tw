---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300888"
---
# <a name="iagent"></a><span data-ttu-id="bbc87-103">IAgent</span><span class="sxs-lookup"><span data-stu-id="bbc87-103">IAgent</span></span>

<span data-ttu-id="bbc87-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bbc87-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bbc87-105">**IAgent** 定義了一個介面，可讓應用程式載入字元、接收事件，以及檢查 Microsoft 代理程式伺服器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="bbc87-105">**IAgent** defines an interface that allows applications to load characters, receive events, and check the current state of the Microsoft Agent Server.</span></span> <span data-ttu-id="bbc87-106">這些函數也可從 [**IAgentEx**](iagentex.md)取得。</span><span class="sxs-lookup"><span data-stu-id="bbc87-106">These functions are also available from [**IAgentEx**](iagentex.md).</span></span>

<span data-ttu-id="bbc87-107">舊版中包含的 GetSuspended 方法已淘汰，而且會傳回 **False** 以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="bbc87-107">The GetSuspended method included in previous versions is obsolete and returns **False** for backward compatibility.</span></span>

<span data-ttu-id="bbc87-108">**依照 Vtable 順序的方法**</span><span class="sxs-lookup"><span data-stu-id="bbc87-108">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="bbc87-109">IAgent 方法</span><span class="sxs-lookup"><span data-stu-id="bbc87-109">IAgent Methods</span></span>                               | <span data-ttu-id="bbc87-110">Description</span><span class="sxs-lookup"><span data-stu-id="bbc87-110">Description</span></span>                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="bbc87-111">**載入**</span><span class="sxs-lookup"><span data-stu-id="bbc87-111">**Load**</span></span>](load-method.md)                  | <span data-ttu-id="bbc87-112">載入字元的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="bbc87-112">Loads a character's data file.</span></span>                                |
| [<span data-ttu-id="bbc87-113">**卸載**</span><span class="sxs-lookup"><span data-stu-id="bbc87-113">**Unload**</span></span>](unload-method.md)              | <span data-ttu-id="bbc87-114">卸載字元的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="bbc87-114">Unloads a character's data file.</span></span>                              |
| [<span data-ttu-id="bbc87-115">**註冊**</span><span class="sxs-lookup"><span data-stu-id="bbc87-115">**Register**</span></span>](iagent--register.md)         | <span data-ttu-id="bbc87-116">註冊用戶端的通知接收。</span><span class="sxs-lookup"><span data-stu-id="bbc87-116">Registers a notification sink for the client.</span></span>                 |
| [<span data-ttu-id="bbc87-117">**Unegister**</span><span class="sxs-lookup"><span data-stu-id="bbc87-117">**Unegister**</span></span>](iagent--unregister.md)      | <span data-ttu-id="bbc87-118">取消註冊用戶端的通知接收。</span><span class="sxs-lookup"><span data-stu-id="bbc87-118">Unregisters a client's notification sink.</span></span>                     |
| [<span data-ttu-id="bbc87-119">**GetCharacter**</span><span class="sxs-lookup"><span data-stu-id="bbc87-119">**GetCharacter**</span></span>](iagent--getcharacter.md) | <span data-ttu-id="bbc87-120">傳回已載入字元的 IAgentCharacter 介面。</span><span class="sxs-lookup"><span data-stu-id="bbc87-120">Returns the IAgentCharacter interface for a loaded character.</span></span> |



 

 

 




