---
title: 優先權旗標
description: 優先權旗標會以優先權模式開啟儲存物件。
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- 優先權旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022131"
---
# <a name="priority-flags"></a><span data-ttu-id="20815-104">優先權旗標</span><span class="sxs-lookup"><span data-stu-id="20815-104">Priority Flags</span></span>

<span data-ttu-id="20815-105">優先權旗標會以優先權模式開啟儲存物件。</span><span class="sxs-lookup"><span data-stu-id="20815-105">The priority flag opens a storage object in priority mode.</span></span> <span data-ttu-id="20815-106">當它開啟物件時，應用程式通常會從快照集複本運作，因為其他應用程式也可以同時使用該物件。</span><span class="sxs-lookup"><span data-stu-id="20815-106">When it opens an object, an application usually works from a snapshot copy because other applications may also be using the object at the same time.</span></span> <span data-ttu-id="20815-107">不過，在優先順序模式中開啟儲存物件時，應用程式具有將變更認可至物件的獨佔許可權。</span><span class="sxs-lookup"><span data-stu-id="20815-107">When opening a storage object in priority mode, however, the application has exclusive rights to commit changes to the object.</span></span>

<span data-ttu-id="20815-108">優先權模式可讓應用程式在需要系統進行快照集複製的模式中開啟物件之前，先從儲存體讀取一些資料流程。</span><span class="sxs-lookup"><span data-stu-id="20815-108">Priority mode enables an application to read some streams from storage before opening the object in a mode that would require the system to make a snapshot copy.</span></span> <span data-ttu-id="20815-109">由於應用程式具有獨佔存取權，因此不需要製作物件的快照集複本。</span><span class="sxs-lookup"><span data-stu-id="20815-109">Because the application has exclusive access, it does not have to make a snapshot copy of the object.</span></span> <span data-ttu-id="20815-110">當應用程式後續以需要快照集複本的模式開啟物件時，應用程式可以排除已經從快照集讀取的資料流程，進而減少開啟物件的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="20815-110">When the application subsequently opens the object in a mode where a snapshot copy is required, the application can exclude the streams it has already read from the snapshot, thereby reducing the overhead of opening the object.</span></span>

<span data-ttu-id="20815-111">由於其他應用程式在 [優先權] 模式中開啟時，無法認可物件的變更，因此應用程式應該盡可能短時間將物件保留在該模式中。</span><span class="sxs-lookup"><span data-stu-id="20815-111">Because other applications cannot commit changes to an object while it is open in priority mode, applications should keep the object in that mode for as short a time as possible.</span></span>

 

 




