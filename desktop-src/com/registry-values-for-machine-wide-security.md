---
title: System-Wide 安全性的登錄值
description: System-Wide 安全性的登錄值
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932075"
---
# <a name="registry-values-for-system-wide-security"></a><span data-ttu-id="6b1f8-103">System-Wide 安全性的登錄值</span><span class="sxs-lookup"><span data-stu-id="6b1f8-103">Registry Values for System-Wide Security</span></span>

<span data-ttu-id="6b1f8-104">不建議您變更整個系統的安全性設定，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="6b1f8-105">如果您要變更全系統安全性設定，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="6b1f8-106">如需設定整個進程安全性的詳細資訊，請參閱 [設定 Process-Wide 安全性](setting-processwide-security.md)。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="6b1f8-107">登錄中的某些值是用來判斷未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)之應用程式的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-107">Certain values in the registry are used to determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="6b1f8-108">您可以使用 Dcomcnfg.exe 來修改電腦的這些預設安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-108">You can use Dcomcnfg.exe to modify these default security settings for a computer.</span></span> <span data-ttu-id="6b1f8-109">如需說明如何將 Dcomcnfg.exe 用於此用途的逐步程式，請參閱 [使用 DCOMCNFG 設定 System-Wide 安全性](setting-machine-wide-security-using-dcomcnfg.md)。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-109">For step-by-step procedures that describe how to use Dcomcnfg.exe for this purpose, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="6b1f8-110">變更預設全系統設定的另一種方式是直接操作登錄值。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-110">Another way to change default system-wide settings is to manipulate registry values directly.</span></span> <span data-ttu-id="6b1f8-111">不過，只有系統管理員和系統具有登錄部分的完整存取權，其中包含預設的全系統呼叫安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-111">However, only administrators and the system have full access to the portion of the registry that contains the default system-wide call-security settings.</span></span> <span data-ttu-id="6b1f8-112">所有其他使用者都只能讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="6b1f8-112">All other users have read-access only.</span></span>

<span data-ttu-id="6b1f8-113">會影響全系統安全性預設值的命名值如下：</span><span class="sxs-lookup"><span data-stu-id="6b1f8-113">The named values that affect system-wide security defaults are as follows:</span></span>

-   [<span data-ttu-id="6b1f8-114">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="6b1f8-114">DefaultLaunchPermission</span></span>](defaultlaunchpermission.md)
-   [<span data-ttu-id="6b1f8-115">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="6b1f8-115">DefaultAccessPermission</span></span>](defaultaccesspermission.md)
-   [<span data-ttu-id="6b1f8-116">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="6b1f8-116">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
-   [<span data-ttu-id="6b1f8-117">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="6b1f8-117">LegacyImpersonationLevel</span></span>](legacyimpersonationlevel.md)
-   [<span data-ttu-id="6b1f8-118">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="6b1f8-118">LegacySecureReferences</span></span>](legacysecurereferences.md)
-   [<span data-ttu-id="6b1f8-119">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="6b1f8-119">SRPRunningObjectChecks</span></span>](srprunningobjectchecks.md)
-   [<span data-ttu-id="6b1f8-120">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="6b1f8-120">SRPActivateAsActivatorChecks</span></span>](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a><span data-ttu-id="6b1f8-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b1f8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b1f8-122">設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="6b1f8-122">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




