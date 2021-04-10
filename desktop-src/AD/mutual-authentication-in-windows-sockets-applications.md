---
title: Windows 通訊端應用程式中的相互驗證
description: Microsoft Windows 通訊端服務可以使用註冊和解析 (RnR) Api 來發佈服務，或者可以使用服務連接點。
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Windows 通訊端應用程式中的相互驗證
- Windows sockets 應用程式中的 Active Directory、使用雙向驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183003"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a><span data-ttu-id="674b7-105">Windows 通訊端應用程式中的相互驗證</span><span class="sxs-lookup"><span data-stu-id="674b7-105">Mutual Authentication in Windows Sockets Applications</span></span>

<span data-ttu-id="674b7-106">Microsoft Windows 通訊端服務可以使用註冊和解析 (RnR) Api 來發佈服務，或者可以使用服務連接點。</span><span class="sxs-lookup"><span data-stu-id="674b7-106">Microsoft Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services, or they can use service connection points.</span></span>

<span data-ttu-id="674b7-107">如需詳細資訊和示範如何針對使用服務連接點發行的 Windows 通訊端服務執行相互驗證的程式碼範例，請參閱 [具有 SCP 的 Windows 通訊端服務中的相互驗證](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md)。</span><span class="sxs-lookup"><span data-stu-id="674b7-107">For more information and a code example that shows how to perform mutual authentication for a Windows Sockets service that publishes using a service connection point, see [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span></span> <span data-ttu-id="674b7-108">這個程式碼範例會使用 SSPI 安全性封裝來管理用戶端和 WinSock 服務之間的驗證協商。</span><span class="sxs-lookup"><span data-stu-id="674b7-108">This code example uses an SSPI security package to manage the authentication negotiations between a client and the WinSock service.</span></span>

<span data-ttu-id="674b7-109">WinSock RnR 服務可以使用類似的程式碼，以使用 SSPI 封裝執行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="674b7-109">A WinSock RnR service can use similar code to perform mutual authentication using an SSPI package.</span></span> <span data-ttu-id="674b7-110">在此情況下，服務會使用目錄的 WinsockServices 容器中服務專案的分辨名稱來撰寫其 Spn。</span><span class="sxs-lookup"><span data-stu-id="674b7-110">In this case, the service would compose its SPNs using the distinguished name of the service's entry in the WinsockServices container in the directory.</span></span>

<span data-ttu-id="674b7-111">例如，如果服務使用名稱 "WinSockRnRSampleService" 註冊本身，您會從下列辨別名稱撰寫服務的 SPN：</span><span class="sxs-lookup"><span data-stu-id="674b7-111">For example, if the service registers itself with the name "WinSockRnRSampleService", you would compose the service's SPN from the following distinguished name:</span></span>


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




