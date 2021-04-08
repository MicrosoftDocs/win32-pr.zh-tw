---
title: 安全性方法
description: Microsoft RPC 支援兩種不同的方法，可將安全性新增至您的分散式應用程式。
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021901"
---
# <a name="security-methods"></a><span data-ttu-id="3abe5-103">安全性方法</span><span class="sxs-lookup"><span data-stu-id="3abe5-103">Security Methods</span></span>

<span data-ttu-id="3abe5-104">Microsoft RPC 支援兩種不同的方法，可將安全性新增至您的分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="3abe5-104">Microsoft RPC supports two different methods for adding security to your distributed application.</span></span> <span data-ttu-id="3abe5-105">第一個方法是使用安全性支援提供者介面 (SSPI) ，您可以使用 RPC 函數來存取此介面。</span><span class="sxs-lookup"><span data-stu-id="3abe5-105">The first method is to use the Security Support Provider Interface (SSPI), which can be accessed using the RPC functions.</span></span> <span data-ttu-id="3abe5-106">一般而言，最好是使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="3abe5-106">In general, it is best to use this method.</span></span> <span data-ttu-id="3abe5-107">SSPI 提供最具彈性且與網路無關的驗證功能。</span><span class="sxs-lookup"><span data-stu-id="3abe5-107">The SSPI provides the most flexible and network-independent authentication features.</span></span>

<span data-ttu-id="3abe5-108">第二種方法是使用系統傳輸通訊協定內建的安全性功能。</span><span class="sxs-lookup"><span data-stu-id="3abe5-108">The second method is to use the security features built into the system transport protocols.</span></span> <span data-ttu-id="3abe5-109">傳輸層級安全性方法並非慣用的方法。</span><span class="sxs-lookup"><span data-stu-id="3abe5-109">The transport-level security method is not the preferred method.</span></span> <span data-ttu-id="3abe5-110">建議使用 SSPI，因為它適用于所有跨平臺的傳輸，並提供高層級的安全性，包括隱私權。</span><span class="sxs-lookup"><span data-stu-id="3abe5-110">Using the SSPI is recommended because it works on all transports, across platforms, and provides high levels of security, including privacy.</span></span>

<span data-ttu-id="3abe5-111">本節提供下列主題中 SSPI 和傳輸層級安全性的概述：</span><span class="sxs-lookup"><span data-stu-id="3abe5-111">This section provides overviews of both SSPI and transport-level security in the following topics:</span></span>

-   [<span data-ttu-id="3abe5-112">安全性支援提供者介面 (SSPI)</span><span class="sxs-lookup"><span data-stu-id="3abe5-112">Security Support Provider Interface (SSPI)</span></span>](security-support-provider-interface-sspi-.md)
-   [<span data-ttu-id="3abe5-113">傳輸安全性</span><span class="sxs-lookup"><span data-stu-id="3abe5-113">Transport Security</span></span>](transport-security.md)

 

 




