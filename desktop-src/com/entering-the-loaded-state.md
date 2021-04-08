---
title: 進入載入的狀態
description: 進入載入的狀態
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672495"
---
# <a name="entering-the-loaded-state"></a><span data-ttu-id="57348-103">進入載入的狀態</span><span class="sxs-lookup"><span data-stu-id="57348-103">Entering the Loaded State</span></span>

<span data-ttu-id="57348-104">當物件進入載入的狀態時，就會建立代表物件的記憶體內結構，以便在其上叫用作業。</span><span class="sxs-lookup"><span data-stu-id="57348-104">When an object enters the loaded state, the in-memory structures representing the object are created so that operations can be invoked on it.</span></span> <span data-ttu-id="57348-105">載入物件的處理常式或同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="57348-105">The object's handler or in-process server is loaded.</span></span> <span data-ttu-id="57348-106">從持續性儲存體載入物件 (從被動轉換到載入的) 狀態，或第一次建立物件時，會發生這個進程（稱為具現 *化*）。</span><span class="sxs-lookup"><span data-stu-id="57348-106">This process, referred to as *instantiation*, occurs when an object is loaded from persistent storage (a transition from the passive to the loaded state) or when an object is being created for the first time.</span></span>

<span data-ttu-id="57348-107">就內部而言，具現化是兩階段的程式。</span><span class="sxs-lookup"><span data-stu-id="57348-107">Internally, instantiation is a two-phase process.</span></span> <span data-ttu-id="57348-108">系統會建立適當類別的物件，之後呼叫該物件上的方法來執行初始化，並授與物件資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="57348-108">An object of the appropriate class is created, after which a method on that object is called to perform initialization and give access to the object's data.</span></span> <span data-ttu-id="57348-109">初始化方法是在物件的其中一個支援的介面中定義。</span><span class="sxs-lookup"><span data-stu-id="57348-109">The initialization method is defined in one of the object's supported interfaces.</span></span> <span data-ttu-id="57348-110">呼叫的特定初始化方法取決於要具現化物件的內容，以及初始化資料的位置。</span><span class="sxs-lookup"><span data-stu-id="57348-110">The particular initialization method called depends on the context in which the object is being instantiated and the location of the initialization data.</span></span>

 

 




