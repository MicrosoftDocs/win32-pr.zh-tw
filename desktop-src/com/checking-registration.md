---
title: 正在檢查註冊
description: 正在檢查註冊
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932029"
---
# <a name="checking-registration"></a><span data-ttu-id="c2c25-103">正在檢查註冊</span><span class="sxs-lookup"><span data-stu-id="c2c25-103">Checking Registration</span></span>

<span data-ttu-id="c2c25-104">每次載入應用程式時，它應該會檢查其註冊以判斷下列各項：</span><span class="sxs-lookup"><span data-stu-id="c2c25-104">Each time an application loads, it should check its registration to determine the following:</span></span>

-   <span data-ttu-id="c2c25-105">Clsid 是否存在於登錄中。</span><span class="sxs-lookup"><span data-stu-id="c2c25-105">Whether the CLSIDs are present in the registry.</span></span> <span data-ttu-id="c2c25-106">如果不存在，應用程式應該註冊為原始設定。</span><span class="sxs-lookup"><span data-stu-id="c2c25-106">If they are not present, the application should register as the original setup.</span></span>
-   <span data-ttu-id="c2c25-107">應用程式的 Clsid 是否存在於登錄中，但其中沒有 OLE 2 相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="c2c25-107">Whether the application's CLSIDs are present in the register but have no OLE 2-related information in them.</span></span> <span data-ttu-id="c2c25-108">如果是這種情況，應用程式應該註冊為原始設定。</span><span class="sxs-lookup"><span data-stu-id="c2c25-108">If this is the case, the application should register as the original setup.</span></span>
-   <span data-ttu-id="c2c25-109"> ([LocalServer](localserver.md) 和 [LocalServer32](localserver32.md)、 [InprocServer](inprocserver.md) 和 [InprocServer32](inprocserver32.md)，以及 [DefaultIcon](defaulticon.md)) 包含伺服器專案的路徑，會指向目前安裝應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="c2c25-109">Whether the path containing server entries ([LocalServer](localserver.md) and [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) and [InprocServer32](inprocserver32.md), and [DefaultIcon](defaulticon.md)) points to the location at which the application is currently installed.</span></span> <span data-ttu-id="c2c25-110">如果路徑不存在，請重寫路徑專案以指向目前的位置。</span><span class="sxs-lookup"><span data-stu-id="c2c25-110">If the path does not, rewrite the path entries to point to the current location.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2c25-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2c25-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2c25-112">註冊 COM 應用程式</span><span class="sxs-lookup"><span data-stu-id="c2c25-112">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




