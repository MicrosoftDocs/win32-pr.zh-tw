---
title: 進入被動狀態
description: 進入被動狀態
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840664"
---
# <a name="entering-the-passive-state"></a><span data-ttu-id="28846-103">進入被動狀態</span><span class="sxs-lookup"><span data-stu-id="28846-103">Entering the Passive State</span></span>

<span data-ttu-id="28846-104">物件關閉會強制內嵌或連結化物件進入被動狀態。</span><span class="sxs-lookup"><span data-stu-id="28846-104">Object closure forces an embedded or linked object into the passive state.</span></span> <span data-ttu-id="28846-105">它通常是從 OLE 伺服器應用程式的使用者介面起始，例如當使用者選取 [關閉] 命令時。</span><span class="sxs-lookup"><span data-stu-id="28846-105">It is typically initiated from the OLE server application's user interface, such as when the user selects the File Close command.</span></span> <span data-ttu-id="28846-106">在此情況下，OLE 伺服器應用程式會通知容器，它會釋放物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="28846-106">In this case, the OLE server application notifies the container, which releases its reference count on the object.</span></span> <span data-ttu-id="28846-107">當物件的所有參考都已釋放時，就可以釋出物件。</span><span class="sxs-lookup"><span data-stu-id="28846-107">When all references to the object have been released, the object can be freed.</span></span> <span data-ttu-id="28846-108">釋放所有物件時，可以安全地終止 OLE 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="28846-108">When all objects have been freed, the OLE server application can safely terminate.</span></span>

<span data-ttu-id="28846-109">容器應用程式也可以起始物件關閉。</span><span class="sxs-lookup"><span data-stu-id="28846-109">A container application can also initiate object closure.</span></span> <span data-ttu-id="28846-110">若要關閉物件，容器會在完成選擇性儲存作業之後釋放其參考計數。</span><span class="sxs-lookup"><span data-stu-id="28846-110">To close an object, the container releases its reference count after completing an optional save operation.</span></span> <span data-ttu-id="28846-111">您可以將容器設計成在就地啟用會話之後停用物件時釋出物件，讓使用者可以在物件外部按一下，而不會遺失使用中的編輯會話。</span><span class="sxs-lookup"><span data-stu-id="28846-111">You can design containers to release objects when they are deactivating after an in-place activation session, allowing the user to click outside the object without losing the active editing session.</span></span>

 

 




