---
title: 使用 SCP 撰寫服務的 Spn
description: 下列程式碼範例撰寫使用服務連接點 (SCP) 之服務的 SPN。
ms.assetid: cbaa11ba-d32b-46cf-86a4-9050bb1be3a6
ms.tgt_platform: multiple
keywords:
- 使用 SCP AD 撰寫服務的 Spn
- 服務主體名稱 AD，使用 SCP 撰寫服務的 Spn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a9c44bc603372af35e874acfea4c1e12a2433d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020743"
---
# <a name="composing-the-spns-for-a-service-with-an-scp"></a><span data-ttu-id="4aa5e-105">使用 SCP 撰寫服務的 Spn</span><span class="sxs-lookup"><span data-stu-id="4aa5e-105">Composing the SPNs for a Service with an SCP</span></span>

<span data-ttu-id="4aa5e-106">下列程式碼範例撰寫使用服務連接點 (SCP) 之服務的 SPN。</span><span class="sxs-lookup"><span data-stu-id="4aa5e-106">The following code example composes an SPN for a service that uses a service connection point (SCP).</span></span> <span data-ttu-id="4aa5e-107">傳回的 SPN 具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="4aa5e-107">The returned SPN has the following format.</span></span>


```C++
<service class>/<host>/<service name>
```



<span data-ttu-id="4aa5e-108">「 &lt; 服務類別」 &gt; 和「 &lt; 服務名稱」會 &gt; 對應至 *pszDNofSCP* 和 *pszServiceClass* 參數。</span><span class="sxs-lookup"><span data-stu-id="4aa5e-108">"&lt;service class&gt;" and "&lt;service name&gt;" correspond to the *pszDNofSCP* and *pszServiceClass* parameters.</span></span> <span data-ttu-id="4aa5e-109">「 &lt; 主機」 &gt; 預設為本機電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="4aa5e-109">"&lt;host&gt;" defaults to the DNS name of the local computer.</span></span>


```C++
DWORD
SpnCompose(
    TCHAR ***pspn,          // Output: an array of SPNs
    unsigned long *pulSpn,  // Output: the number of SPNs returned
    TCHAR *pszDNofSCP,      // Input: DN of the service's SCP
    TCHAR* pszServiceClass) // Input: the name of the service class
{
DWORD   dwStatus;    
 
dwStatus = DsGetSpn(
    DS_SPN_SERVICE, // Type of SPN to create (enumerated type)
    pszServiceClass, // Service class - a name in this case
    pszDNofSCP, // Service name - DN of the service SCP
    0, // Default: omit port component of SPN
    0, // Number of entries in hostnames and ports arrays
    NULL, // Array of hostnames. Default is local computer
    NULL, // Array of ports. Default omits port component
    pulSpn, // Receives number of SPNs returned in array
    pspn // Receives array of SPN(s)
    );
 
return dwStatus;
}
```



 

 




