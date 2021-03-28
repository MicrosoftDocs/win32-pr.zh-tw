---
description: 當有數個元件希望在端對端追蹤案例中建立其事件的關聯時，請使用 EventWriteTransfer 函數。
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: 在以資訊清單為基礎的提供者中撰寫相關的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512181"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a><span data-ttu-id="90f28-103">在以資訊清單為基礎的提供者中撰寫相關的事件</span><span class="sxs-lookup"><span data-stu-id="90f28-103">Writing Related Events in a Manifest-based Provider</span></span>

<span data-ttu-id="90f28-104">當有數個元件希望在端對端追蹤案例中建立其事件的關聯時，請使用 [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) 函數。</span><span class="sxs-lookup"><span data-stu-id="90f28-104">Use the [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) function when several components want to relate their events in an end-to-end tracing scenario.</span></span> <span data-ttu-id="90f28-105">例如，元件 A、B 和 C 會針對相關活動執行工作，而且想要連結與該活動相關的所有事件。</span><span class="sxs-lookup"><span data-stu-id="90f28-105">For example, components A, B and C perform work on a related activity and want to link all the events related to that activity.</span></span>

<span data-ttu-id="90f28-106">ETW 使用執行緒區域儲存區，將上一個元件的活動識別碼提供給下一個元件。</span><span class="sxs-lookup"><span data-stu-id="90f28-106">ETW uses thread local storage to make the previous component's activity identifier available to the next component.</span></span> <span data-ttu-id="90f28-107">元件會從本機儲存體取出先前元件的識別碼，並將相關的活動識別碼設定為它。</span><span class="sxs-lookup"><span data-stu-id="90f28-107">The component retrieves the previous component's identifier from the local storage and sets the related activity identifier to it.</span></span> <span data-ttu-id="90f28-108">然後，取用者可以使用相關的活動識別碼，將來自某個元件的事件鏈引導至下一個元件。</span><span class="sxs-lookup"><span data-stu-id="90f28-108">The consumer can then use the related activity identifier to walk the chain of the events from one component to the next.</span></span>

 

 



