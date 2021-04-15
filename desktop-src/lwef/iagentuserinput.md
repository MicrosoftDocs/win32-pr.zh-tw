---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375156"
---
# <a name="iagentuserinput"></a><span data-ttu-id="472c3-103">IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="472c3-103">IAgentUserInput</span></span>

<span data-ttu-id="472c3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="472c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="472c3-105">當伺服器使用 [**IAgentNotifySink：：命令**](iagentnotifysink--command.md)通知輸入-主動用戶端時，它會透過 [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) 物件傳回信息。</span><span class="sxs-lookup"><span data-stu-id="472c3-105">When the server notifies the input-active client with [**IAgentNotifySink::Command**](iagentnotifysink--command.md), it returns information through the [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="472c3-106">**IAgentUserInput** 會定義可讓應用程式查詢這些值的介面。</span><span class="sxs-lookup"><span data-stu-id="472c3-106">**IAgentUserInput** defines an interface that allows applications to query these values.</span></span>

<span data-ttu-id="472c3-107">**依照 Vtable 順序的方法**</span><span class="sxs-lookup"><span data-stu-id="472c3-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="472c3-108">IAgentUserInput 方法</span><span class="sxs-lookup"><span data-stu-id="472c3-108">IAgentUserInput Methods</span></span>                                         | <span data-ttu-id="472c3-109">Description</span><span class="sxs-lookup"><span data-stu-id="472c3-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="472c3-110">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="472c3-110">**GetCount**</span></span>](iagentuserinput--getcount.md)                   | <span data-ttu-id="472c3-111">傳回 [**命令**](command-event.md) 事件中傳回的命令替代專案數目。</span><span class="sxs-lookup"><span data-stu-id="472c3-111">Returns the number of command alternatives returned in a [**Command**](command-event.md) event.</span></span>                                         |
| [<span data-ttu-id="472c3-112">**GetItemID**</span><span class="sxs-lookup"><span data-stu-id="472c3-112">**GetItemID**</span></span>](iagentuserinput--getitemid.md)                 | <span data-ttu-id="472c3-113">傳回特定 [**命令**](command-event.md) 替代的識別碼。</span><span class="sxs-lookup"><span data-stu-id="472c3-113">Returns the ID for a specific [**Command**](command-event.md) alternative.</span></span>                                                              |
| [<span data-ttu-id="472c3-114">**GetItemConfidence**</span><span class="sxs-lookup"><span data-stu-id="472c3-114">**GetItemConfidence**</span></span>](iagentuserinput--getitemconfidence.md) | <span data-ttu-id="472c3-115">傳回特定 [**命令**](command-event.md)替代的 [**信賴**](confidence-property.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="472c3-115">Returns the value of the [**Confidence**](confidence-property.md) property for a specific [**Command**](command-event.md) alternative.</span></span> |
| [<span data-ttu-id="472c3-116">**GetItemText**</span><span class="sxs-lookup"><span data-stu-id="472c3-116">**GetItemText**</span></span>](iagentuserinput--getitemtext.md)             | <span data-ttu-id="472c3-117">傳回特定 [**命令**](command-event.md)替代的 [**語音**](voice-property.md)文字值。</span><span class="sxs-lookup"><span data-stu-id="472c3-117">Returns the value of [**Voice**](voice-property.md) text for a specific [**Command**](command-event.md) alternative.</span></span>                   |
| [<span data-ttu-id="472c3-118">**GetAllItemData**</span><span class="sxs-lookup"><span data-stu-id="472c3-118">**GetAllItemData**</span></span>](iagentuserinput--getallitemdata.md)       | <span data-ttu-id="472c3-119">傳回所有 [**命令**](command-event.md) 替代專案的資料。</span><span class="sxs-lookup"><span data-stu-id="472c3-119">Returns the data for all [**Command**](command-event.md) alternatives.</span></span>                                                                  |



 

 

 