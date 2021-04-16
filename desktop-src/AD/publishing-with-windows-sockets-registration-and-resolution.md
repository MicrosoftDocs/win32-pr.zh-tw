---
title: 使用 Windows 通訊端註冊發佈 & 解析
description: Windows 通訊端服務可以使用註冊和解析 (RnR) Api 來發佈服務，以及查閱以 RnR 發佈的服務。
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows 通訊端註冊和解析 AD，發行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/04/2019
ms.locfileid: "104462632"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a><span data-ttu-id="9a258-104">使用 Windows 通訊端註冊發佈 & 解析</span><span class="sxs-lookup"><span data-stu-id="9a258-104">Publishing with Windows Sockets Registration & Resolution</span></span>

<span data-ttu-id="9a258-105">Windows 通訊端服務可以使用註冊和解析 (RnR) Api 來發佈服務，以及查閱以 RnR 發佈的服務。</span><span class="sxs-lookup"><span data-stu-id="9a258-105">Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services and look up services published with RnR.</span></span> <span data-ttu-id="9a258-106">RnR 發行會以兩個步驟進行。</span><span class="sxs-lookup"><span data-stu-id="9a258-106">RnR publication occurs in two steps.</span></span> <span data-ttu-id="9a258-107">第一個步驟會安裝服務類別，以將 GUID 與服務的名稱產生關聯。</span><span class="sxs-lookup"><span data-stu-id="9a258-107">The first step installs a service class that associates a GUID with a name for the service.</span></span> <span data-ttu-id="9a258-108">服務類別可保存服務特定的設定資料。</span><span class="sxs-lookup"><span data-stu-id="9a258-108">The service class can hold service-specific configuration data.</span></span> <span data-ttu-id="9a258-109">接著，服務會將自己發佈為服務類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9a258-109">Services can then publish themselves as instances of the service class.</span></span> <span data-ttu-id="9a258-110">發佈時，用戶端可以使用 RnR Api 來查詢指定類別之實例的目錄服務，並選取要系結的實例。</span><span class="sxs-lookup"><span data-stu-id="9a258-110">When published, clients can query the directory service for instances of a given class using the RnR APIs and select an instance to bind to.</span></span> <span data-ttu-id="9a258-111">當不再需要類別時，就可以將它移除。</span><span class="sxs-lookup"><span data-stu-id="9a258-111">When a class is no longer required, it can be removed.</span></span>

 

 




