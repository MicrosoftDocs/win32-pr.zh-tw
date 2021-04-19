---
description: C + + 提供者和用戶端應用程式都必須執行許多相同的作業來維護 WMI 安全性。
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: 保護 c + + 用戶端和提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983553"
---
# <a name="securing-c-clients-and-providers"></a><span data-ttu-id="acb39-103">保護 c + + 用戶端和提供者</span><span class="sxs-lookup"><span data-stu-id="acb39-103">Securing C++ Clients and Providers</span></span>

<span data-ttu-id="acb39-104">C + + 提供者和用戶端應用程式都必須執行許多相同的作業來維護 WMI 安全性。</span><span class="sxs-lookup"><span data-stu-id="acb39-104">Both C++ providers and client applications must perform many of the same operations to maintain WMI security.</span></span>

<span data-ttu-id="acb39-105">用戶端應用程式在連線至 WMI 時，必須正確 [設定 DCOM 模擬](setting-the-default-process-security-level-using-c-.md) 和 [驗證](setting-authentication-in-wmi.md) 層級。</span><span class="sxs-lookup"><span data-stu-id="acb39-105">Client applications must set DCOM [impersonation](setting-the-default-process-security-level-using-c-.md) and [authentication](setting-authentication-in-wmi.md) levels correctly when connecting to WMI.</span></span> <span data-ttu-id="acb39-106">[非同步呼叫](setting-security-on-an-asynchronous-call.md)的回呼有安全性風險，因此用戶端應用程式必須[執行存取檢查](performing-access-checks.md)，以確保回呼來自信任的來源。</span><span class="sxs-lookup"><span data-stu-id="acb39-106">Callbacks from [asynchronous calls](setting-security-on-an-asynchronous-call.md) have security risks, so client applications must [perform access checks](performing-access-checks.md) to ensure the callback is from a trusted source.</span></span> <span data-ttu-id="acb39-107">用戶端需要保護 [暫時性和永久事件取用者](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="acb39-107">Clients need to secure both [temporary and permanent event consumers](securing-wmi-events.md).</span></span>

<span data-ttu-id="acb39-108">提供者可能會 [執行存取檢查](performing-access-checks.md) ，以確保它所建立的資源只能由適當的用戶端存取。</span><span class="sxs-lookup"><span data-stu-id="acb39-108">A provider may [perform access checks](performing-access-checks.md) to ensure that the resources it creates are only accessed by appropriate clients.</span></span>

<span data-ttu-id="acb39-109">提供者和用戶端也可以設定 [特定 proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) 連接的安全性。</span><span class="sxs-lookup"><span data-stu-id="acb39-109">Both providers and clients also can set the security on a [specific proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) connection.</span></span> <span data-ttu-id="acb39-110">兩者也可以啟用 [許可權](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="acb39-110">Both can also enable [privileges](executing-privileged-operations.md).</span></span> <span data-ttu-id="acb39-111">事件提供者必須確保用戶端取用者有權 [接收要求的事件](providing-events-securely.md)。</span><span class="sxs-lookup"><span data-stu-id="acb39-111">An event provider must ensure that the client consumer has privileges to [receive a requested event](providing-events-securely.md).</span></span>

<span data-ttu-id="acb39-112">用戶端或提供者可能需要建立需要不同驗證服務的遠端連線，例如 NTLM 而非 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="acb39-112">Either a client or provider may need to make a remote connection that requires a different authentication service, NTLM instead of Kerberos for example.</span></span>

 

 



