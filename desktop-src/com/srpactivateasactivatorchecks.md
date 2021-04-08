---
title: SRPActivateAsActivatorChecks
description: 判斷 ActivateAsActivator 啟用期間是否使用軟體限制原則 (SRP) 信任層級。
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- SRPActivateAsActivatorChecks 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672488"
---
# <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="f088b-104">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="f088b-104">SRPActivateAsActivatorChecks</span></span>

<span data-ttu-id="f088b-105">判斷 ActivateAsActivator 啟用期間是否使用軟體限制原則 (SRP) 信任層級。</span><span class="sxs-lookup"><span data-stu-id="f088b-105">Determines whether software restriction policy (SRP) trust levels are used during ActivateAsActivator activations.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f088b-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="f088b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a><span data-ttu-id="f088b-107">備註</span><span class="sxs-lookup"><span data-stu-id="f088b-107">Remarks</span></span>

<span data-ttu-id="f088b-108">這是 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="f088b-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="f088b-109">字串值 {N，N，NO，No，no} 表示伺服器物件會以用戶端物件的 SRP 信任層級執行，而不論其設定所在的 SRP 信任層級為何。</span><span class="sxs-lookup"><span data-stu-id="f088b-109">String values of {N, n, NO, No, no} indicate that the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which it was configured.</span></span> <span data-ttu-id="f088b-110">如果此登錄值設定為任何其他值或不存在，則為伺服器物件設定的 SRP 信任層級會與用戶端物件的 SRP 信任層級進行比較，並使用更嚴格的信任層級來執行伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="f088b-110">If this registry value is set to any other value or does not exist, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and that the more stringent trust level is used to run the server object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f088b-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="f088b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f088b-112">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="f088b-112">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




