---
title: 在電腦物件下發布
description: 一般而言，主機型服務會在主機電腦的電腦物件底下建立 Scp。 以主機為基礎的服務是與單一主機電腦緊密系結的服務。
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842039"
---
# <a name="publishing-under-a-computer-object"></a><span data-ttu-id="cd1cf-104">在電腦物件下發布</span><span class="sxs-lookup"><span data-stu-id="cd1cf-104">Publishing Under a Computer Object</span></span>

<span data-ttu-id="cd1cf-105">一般而言，主機型服務會在主機電腦的電腦物件底下建立 Scp。</span><span class="sxs-lookup"><span data-stu-id="cd1cf-105">Typically, host-based services create SCPs under the computer object for the host computer.</span></span> <span data-ttu-id="cd1cf-106">以主機為基礎的服務是與單一主機電腦緊密系結的服務。</span><span class="sxs-lookup"><span data-stu-id="cd1cf-106">Host-based services are services closely tied to a single host computer.</span></span>

<span data-ttu-id="cd1cf-107">**若要在電腦物件下建立 Scp**</span><span class="sxs-lookup"><span data-stu-id="cd1cf-107">**To create SCPs under a computer object**</span></span>

1.  <span data-ttu-id="cd1cf-108">呼叫 [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) 函式，以取得本機電腦之電腦物件目錄中 (DN) 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="cd1cf-108">Call the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the distinguished name (DN) in the directory of the computer object for the local computer.</span></span>
2.  <span data-ttu-id="cd1cf-109">使用該 DN 系結至電腦物件，並建立 SCP。</span><span class="sxs-lookup"><span data-stu-id="cd1cf-109">Use that DN to bind to the computer object and create the SCP.</span></span>

<span data-ttu-id="cd1cf-110">如需詳細資訊和程式碼範例，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="cd1cf-110">For more information and a code example, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="cd1cf-111">請注意，只有網域成員電腦在目錄中具有有效的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="cd1cf-111">Be aware that only domain-member computers have valid computer objects in the directory.</span></span>

<span data-ttu-id="cd1cf-112">若要取得本機電腦的 DNS 或 NetBIOS 名稱，請呼叫 [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="cd1cf-112">To get the DNS or NetBIOS name of the local computer, call the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function.</span></span>

 

 