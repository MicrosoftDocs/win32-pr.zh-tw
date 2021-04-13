---
title: 持續性物件狀態
description: 持續性物件狀態
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300368"
---
# <a name="persistent-object-state"></a><span data-ttu-id="43892-103">持續性物件狀態</span><span class="sxs-lookup"><span data-stu-id="43892-103">Persistent Object State</span></span>

<span data-ttu-id="43892-104">某些 COM 物件可能會在用戶端要求您這麼做時，儲存其內部狀態。</span><span class="sxs-lookup"><span data-stu-id="43892-104">Some COM objects can save their internal state when asked to do so by a client.</span></span>

<span data-ttu-id="43892-105">COM 會定義標準，讓用戶端可以要求將物件初始化、載入及儲存至資料存放區， (例如一般檔案、結構化儲存體或記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="43892-105">COM defines standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="43892-106">用戶端負責管理物件的持續性資料的儲存位置，而非資料的格式。</span><span class="sxs-lookup"><span data-stu-id="43892-106">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span> <span data-ttu-id="43892-107">遵守這些標準的 COM 物件稱為持續性 *物件*。</span><span class="sxs-lookup"><span data-stu-id="43892-107">COM objects that adhere to these standards are called *persistent objects*.</span></span>

<span data-ttu-id="43892-108">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="43892-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="43892-109">持續性物件介面</span><span class="sxs-lookup"><span data-stu-id="43892-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
-   [<span data-ttu-id="43892-110">初始化持續性物件</span><span class="sxs-lookup"><span data-stu-id="43892-110">Initializing Persistent Objects</span></span>](initializing-persistent-objects.md)

## <a name="related-topics"></a><span data-ttu-id="43892-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="43892-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43892-112">COM 用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="43892-112">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




