---
title: 設定 COM 應用程式的安全性
description: 設定 COM 應用程式的安全性
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840903"
---
# <a name="setting-security-for-com-applications"></a><span data-ttu-id="60e4d-103">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="60e4d-103">Setting Security for COM Applications</span></span>

<span data-ttu-id="60e4d-104">有數種方式可協助您控制應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="60e4d-104">There are several ways you can help control security for your applications.</span></span> <span data-ttu-id="60e4d-105">您可以變更電腦的預設安全性設定，而電腦上的所有應用程式都會使用這些設定來提供自己的安全性值。</span><span class="sxs-lookup"><span data-stu-id="60e4d-105">You can change a computer's default security settings, which are used by all applications on the computer that do not supply their own security values.</span></span> <span data-ttu-id="60e4d-106">您可以使用 Dcomcnfg.exe 或藉由呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)來設定特定進程的安全性。</span><span class="sxs-lookup"><span data-stu-id="60e4d-106">You can set security for a particular process, either by using Dcomcnfg.exe or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="60e4d-107">您也可以透過程式設計的方式控制介面 proxy 層級的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="60e4d-107">You can also programmatically control security settings at the interface proxy level.</span></span>

<span data-ttu-id="60e4d-108">下列主題提供說明如何設定安全性的程式：</span><span class="sxs-lookup"><span data-stu-id="60e4d-108">The following topics provide procedures that explain how to set security:</span></span>

-   [<span data-ttu-id="60e4d-109">修改電腦的安全性預設值</span><span class="sxs-lookup"><span data-stu-id="60e4d-109">Modifying the Security Defaults for a Computer</span></span>](modifying-the-security-defaults-for-a-computer.md)
-   [<span data-ttu-id="60e4d-110">設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="60e4d-110">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
-   [<span data-ttu-id="60e4d-111">在介面 Proxy 層級設定安全性</span><span class="sxs-lookup"><span data-stu-id="60e4d-111">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a><span data-ttu-id="60e4d-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="60e4d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60e4d-113">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="60e4d-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




