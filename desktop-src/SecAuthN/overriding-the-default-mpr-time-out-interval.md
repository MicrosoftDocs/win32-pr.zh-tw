---
description: 多個提供者路由器 (MPR) 會呼叫 NPGetCaps，以找出網路提供者何時將開始 (nIndex 設定為 WNNC \_ 啟動) 。
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: 覆寫預設 MPR 逾時間隔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944830"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a><span data-ttu-id="357ac-103">覆寫預設 MPR 逾時間隔</span><span class="sxs-lookup"><span data-stu-id="357ac-103">Overriding the Default MPR Time-out Interval</span></span>

<span data-ttu-id="357ac-104">[*多個提供者路由器*](../secgloss/m-gly.md) (MPR) 會呼叫 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) ，以找出網路提供者何時將開始 (*nIndex* 設定為 WNNC \_ 啟動) 。</span><span class="sxs-lookup"><span data-stu-id="357ac-104">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) calls [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) to find out when the network providers will start (*nIndex* is set to WNNC\_START).</span></span> <span data-ttu-id="357ac-105">然後，MPR 會等待所有網路提供者所指定的最長超時時間，再向使用者呈現匯總的網路。</span><span class="sxs-lookup"><span data-stu-id="357ac-105">The MPR then waits for the longest time-out period specified by all network providers before it presents the consolidated network to the user.</span></span> <span data-ttu-id="357ac-106">如果其中一個網路提供者不知道何時會開始，MPR 會使用該提供者的預設超時時間（60秒）。</span><span class="sxs-lookup"><span data-stu-id="357ac-106">If one of the network providers does not know when it will start, MPR uses a default time-out of 60 seconds for that provider.</span></span>

<span data-ttu-id="357ac-107">如果有需要，系統管理員可以藉由建立下列登錄 **\_ DWORD** 登錄超時（其中 *n* 是逾時間隔，以毫秒為單位）來覆寫預設超時時間：</span><span class="sxs-lookup"><span data-stu-id="357ac-107">If necessary, the administrator can override the default time-out by creating the following **REG\_DWORD** registry time-out, where *n* is the time-out interval in milliseconds:</span></span>

<span data-ttu-id="357ac-108">**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **>restoretimeout**  =  *n*</span><span class="sxs-lookup"><span data-stu-id="357ac-108">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**RestoreTimeout** = *n*</span></span>

<span data-ttu-id="357ac-109">下列虛擬程式碼會顯示 MPR 的完成時間處理的完整邏輯流程。</span><span class="sxs-lookup"><span data-stu-id="357ac-109">The following pseudocode shows the complete logic flow for time-out handling by the MPR.</span></span>


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
