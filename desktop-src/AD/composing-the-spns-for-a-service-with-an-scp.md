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
ms.openlocfilehash: 9e48175bc5fa3d686aab104f8e025d66d7900162235292ed5b853c3284285cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022218"
---
# <a name="composing-the-spns-for-a-service-with-an-scp"></a>使用 SCP 撰寫服務的 Spn

下列程式碼範例撰寫使用服務連接點 (SCP) 之服務的 SPN。 傳回的 SPN 具有下列格式。


```C++
<service class>/<host>/<service name>
```



「 &lt; 服務類別」 &gt; 和「 &lt; 服務名稱」會 &gt; 對應至 *pszDNofSCP* 和 *pszServiceClass* 參數。 「 &lt; 主機」 &gt; 預設為本機電腦的 DNS 名稱。


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



 

 




