---
description: 多個進程可以有相同事件、mutex、信號或計時器物件的控制碼，因此可以使用這些物件來完成進程間的同步處理。
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: 進程進程同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979936"
---
# <a name="interprocess-synchronization"></a><span data-ttu-id="ded9c-103">進程進程同步處理</span><span class="sxs-lookup"><span data-stu-id="ded9c-103">Interprocess Synchronization</span></span>

<span data-ttu-id="ded9c-104">多個進程可以有相同事件、mutex、信號或計時器物件的控制碼，因此可以使用這些物件來完成進程間的同步處理。</span><span class="sxs-lookup"><span data-stu-id="ded9c-104">Multiple processes can have handles to the same event, mutex, semaphore, or timer object, so these objects can be used to accomplish interprocess synchronization.</span></span> <span data-ttu-id="ded9c-105">建立物件的程式可以使用建立函數所傳回的控制碼 ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)、 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)、 [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)或 [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)) 。</span><span class="sxs-lookup"><span data-stu-id="ded9c-105">The process that creates an object can use the handle returned by the creation function ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea), or [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span></span> <span data-ttu-id="ded9c-106">其他處理常式可以使用其名稱或透過繼承或重複來開啟物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ded9c-106">Other processes can open a handle to the object by using its name, or through inheritance or duplication.</span></span> <span data-ttu-id="ded9c-107">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="ded9c-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ded9c-108">物件名稱</span><span class="sxs-lookup"><span data-stu-id="ded9c-108">Object Names</span></span>](object-names.md)
-   [<span data-ttu-id="ded9c-109">物件繼承</span><span class="sxs-lookup"><span data-stu-id="ded9c-109">Object Inheritance</span></span>](object-inheritance.md)
-   [<span data-ttu-id="ded9c-110">物件重複</span><span class="sxs-lookup"><span data-stu-id="ded9c-110">Object Duplication</span></span>](object-duplication.md)

 

 
