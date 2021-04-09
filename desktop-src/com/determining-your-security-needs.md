---
title: 判斷您的安全性需求
description: 您如何設定應用程式的 COM 安全性，取決於您的應用程式所需的安全性類型。 有幾種常見的情況會決定您應該做什麼。
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675823"
---
# <a name="determining-your-security-needs"></a><span data-ttu-id="21ba3-104">判斷您的安全性需求</span><span class="sxs-lookup"><span data-stu-id="21ba3-104">Determining Your Security Needs</span></span>

<span data-ttu-id="21ba3-105">您如何設定應用程式的 COM 安全性，取決於您的應用程式所需的安全性類型。</span><span class="sxs-lookup"><span data-stu-id="21ba3-105">How you set up COM security for your application depends on what kind of security your application needs.</span></span> <span data-ttu-id="21ba3-106">有幾種常見的情況會決定您應該做什麼。</span><span class="sxs-lookup"><span data-stu-id="21ba3-106">There are several common situations that determine what you should do.</span></span>

<span data-ttu-id="21ba3-107">如果您決定使用 COM 安全性預設值，就不需要執行 anythingâ€」 COM 全部處理。</span><span class="sxs-lookup"><span data-stu-id="21ba3-107">If you decide to use the COM security defaults, you do not have to do anythingâ€”COM handles it all.</span></span> <span data-ttu-id="21ba3-108">如需這些預設設定的詳細資訊，請參閱 [COM 安全性預設值](com-security-defaults.md)。</span><span class="sxs-lookup"><span data-stu-id="21ba3-108">For information on what these default settings are, see [COM Security Defaults](com-security-defaults.md).</span></span>

<span data-ttu-id="21ba3-109">您也可以停用遠端電腦) 之間的所有遠端電腦 (COM，以防止任何遠端呼叫您的電腦。</span><span class="sxs-lookup"><span data-stu-id="21ba3-109">You can also prevent any remote calls into your machine by disabling DCOM altogether (COM between remote computers).</span></span> <span data-ttu-id="21ba3-110">如需詳細資訊，請參閱 [使用 DCOMCNFG 設定 System-Wide 安全性](setting-machine-wide-security-using-dcomcnfg.md)。</span><span class="sxs-lookup"><span data-stu-id="21ba3-110">For more information, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="21ba3-111">針對舊版或新的應用程式，您可以在登錄中設定整個進程的安全性。</span><span class="sxs-lookup"><span data-stu-id="21ba3-111">For legacy or new applications, you can set process-wide security in the registry.</span></span> <span data-ttu-id="21ba3-112">如需詳細資訊，請參閱 [透過登錄設定 Processwide 安全性](setting-processwide-security-through-the-registry.md)。</span><span class="sxs-lookup"><span data-stu-id="21ba3-112">For more information, see [Setting Processwide Security Through the Registry](setting-processwide-security-through-the-registry.md).</span></span>

<span data-ttu-id="21ba3-113">您也可以覆寫進程中特定介面呼叫的預設安全性設定，同時設定其餘進程 (的預設安全性，以允許 COM 處理一般案例) 。</span><span class="sxs-lookup"><span data-stu-id="21ba3-113">You can also override default security settings for calls to certain interfaces in the process while setting default security for the remainder of the process (to allow COM to handle the general cases).</span></span> <span data-ttu-id="21ba3-114">如需詳細資訊，請參閱在 [介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)。</span><span class="sxs-lookup"><span data-stu-id="21ba3-114">For more information, see [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="21ba3-115">針對複雜的安全性需求，您可以透過程式設計方式來處理所有安全性，而不是讓 COM 為您處理。</span><span class="sxs-lookup"><span data-stu-id="21ba3-115">For complex security requirements, you can handle all security programmatically rather than allowing COM to handle it for you.</span></span> <span data-ttu-id="21ba3-116">若要這樣做，請呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來停用自動驗證，然後藉由設定每個介面的安全性來控制所有安全性設定。</span><span class="sxs-lookup"><span data-stu-id="21ba3-116">To do this, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to disable automatic authentication, and then control all the security settings by setting security on a per-interface proxy basis.</span></span> <span data-ttu-id="21ba3-117">如需詳細資訊，請參閱 [使用 CoInitializeSecurity 設定 Processwide 安全性](setting-processwide-security-with-coinitializesecurity.md) 和 [在介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)。</span><span class="sxs-lookup"><span data-stu-id="21ba3-117">For more information, see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) and [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="21ba3-118">在某些情況下，您可能會想要完全關閉安全性。</span><span class="sxs-lookup"><span data-stu-id="21ba3-118">In some scenarios, you might want to turn off security completely.</span></span> <span data-ttu-id="21ba3-119">您可能會決定您的應用程式不需要任何安全性，或者您可能想要在開發期間停用安全性，讓您可以個別啟用安全性功能。</span><span class="sxs-lookup"><span data-stu-id="21ba3-119">You might decide that your application does not need any security, or you might want to disable security during development time so that you can enable security features individually.</span></span> <span data-ttu-id="21ba3-120">若要瞭解如何停用 COM 安全性，請參閱 [關閉安全性](turning-off-security.md)。</span><span class="sxs-lookup"><span data-stu-id="21ba3-120">To learn how to disable COM security, see [Turning Off Security](turning-off-security.md).</span></span>

<span data-ttu-id="21ba3-121">COM 中的安全性依賴安全性封裝所管理的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="21ba3-121">Security in COM relies on authentication services administered by security packages.</span></span> <span data-ttu-id="21ba3-122">NTLMSSP 適用于許多應用程式，但不提供其他封裝所提供的更健全安全性。</span><span class="sxs-lookup"><span data-stu-id="21ba3-122">NTLMSSP works well for many applications but does not provide the more robust security offered by other packages.</span></span> <span data-ttu-id="21ba3-123">因此，COM 支援 Schannel 安全性封裝和 Kerberos v5 安全性通訊協定。</span><span class="sxs-lookup"><span data-stu-id="21ba3-123">Therefore, COM supports the Schannel security package and the Kerberos v5 security protocol.</span></span> <span data-ttu-id="21ba3-124">如需使用這些安全性封裝的詳細資訊，請參閱 [COM 和安全性封裝](com-and-security-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="21ba3-124">For more details on using these security packages, see [COM and Security Packages](com-and-security-packages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21ba3-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="21ba3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21ba3-126">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="21ba3-126">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




