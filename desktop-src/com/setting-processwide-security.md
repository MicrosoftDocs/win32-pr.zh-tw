---
title: 設定 Process-Wide 安全性
description: 有幾種方式可以設定整個進程的安全性。
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969678"
---
# <a name="setting-process-wide-security"></a><span data-ttu-id="de7b0-103">設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="de7b0-103">Setting Process-Wide Security</span></span>

<span data-ttu-id="de7b0-104">有幾種方式可以設定整個進程的安全性。</span><span class="sxs-lookup"><span data-stu-id="de7b0-104">There are several ways to set process-wide security.</span></span> <span data-ttu-id="de7b0-105">使用 Dcomcnfg.exe 工具的第一種方式是最簡單的，因為它不需要任何程式設計。</span><span class="sxs-lookup"><span data-stu-id="de7b0-105">The first way, using the Dcomcnfg.exe tool, is easiest because it requires no programming.</span></span> <span data-ttu-id="de7b0-106">第二項技巧提供程式設計人員更多的控制，且需要呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)。</span><span class="sxs-lookup"><span data-stu-id="de7b0-106">The second technique offers the programmer more control, and it requires a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="de7b0-107">另一種方法是使用 [AppID](appid-key.md) 金鑰，在登錄中設定整個進程的安全性。</span><span class="sxs-lookup"><span data-stu-id="de7b0-107">Another technique is to set process-wide security in the registry by using the [AppID](appid-key.md) key.</span></span>

<span data-ttu-id="de7b0-108">如需這些技術的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="de7b0-108">For more information about these techniques, see the following topics:</span></span>

-   [<span data-ttu-id="de7b0-109">使用 DCOMCNFG 設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="de7b0-109">Setting Process-Wide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="de7b0-110">使用 CoInitializeSecurity 設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="de7b0-110">Setting Process-Wide Security with CoInitializeSecurity</span></span>](setting-processwide-security-with-coinitializesecurity.md)
-   [<span data-ttu-id="de7b0-111">透過登錄設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="de7b0-111">Setting Process-Wide Security Through the Registry</span></span>](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a><span data-ttu-id="de7b0-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="de7b0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de7b0-113">在介面 Proxy 層級設定安全性</span><span class="sxs-lookup"><span data-stu-id="de7b0-113">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[<span data-ttu-id="de7b0-114">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="de7b0-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




