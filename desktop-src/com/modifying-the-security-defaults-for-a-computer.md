---
title: 修改電腦的安全性預設值
description: 修改電腦的安全性預設值
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371831"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a><span data-ttu-id="a8dea-103">修改電腦的安全性預設值</span><span class="sxs-lookup"><span data-stu-id="a8dea-103">Modifying the Security Defaults for a Computer</span></span>

<span data-ttu-id="a8dea-104">不建議您變更整個系統的安全性設定，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="a8dea-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="a8dea-105">如果您要變更全系統安全性設定，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。</span><span class="sxs-lookup"><span data-stu-id="a8dea-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="a8dea-106">如需設定整個進程安全性的詳細資訊，請參閱 [設定 Process-Wide 安全性](setting-processwide-security.md)。</span><span class="sxs-lookup"><span data-stu-id="a8dea-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="a8dea-107">登錄中的某些值會決定未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)之應用程式的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="a8dea-107">Certain values in the registry determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="a8dea-108">您可以使用 Dcomcnfg.exe 來修改這些設定。</span><span class="sxs-lookup"><span data-stu-id="a8dea-108">You can modify these settings using Dcomcnfg.exe.</span></span>

<span data-ttu-id="a8dea-109">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="a8dea-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a8dea-110">System-Wide 安全性的登錄值</span><span class="sxs-lookup"><span data-stu-id="a8dea-110">Registry Values for System-Wide Security</span></span>](registry-values-for-machine-wide-security.md)
-   [<span data-ttu-id="a8dea-111">使用 DCOMCNFG 設定 System-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="a8dea-111">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="a8dea-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8dea-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8dea-113">設定整個進程的安全性</span><span class="sxs-lookup"><span data-stu-id="a8dea-113">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> <dt>

[<span data-ttu-id="a8dea-114">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="a8dea-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




