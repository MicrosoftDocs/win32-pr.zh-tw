---
title: SRPTrustLevel
description: 將軟體限制原則設定 (SRP) 信任層級的應用程式。
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- SRPTrustLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372027"
---
# <a name="srptrustlevel"></a><span data-ttu-id="160d0-104">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="160d0-104">SRPTrustLevel</span></span>

<span data-ttu-id="160d0-105">將軟體限制原則設定 (SRP) 信任層級的應用程式。</span><span class="sxs-lookup"><span data-stu-id="160d0-105">Sets the software restriction policy (SRP) trust level for applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="160d0-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="160d0-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a><span data-ttu-id="160d0-107">備註</span><span class="sxs-lookup"><span data-stu-id="160d0-107">Remarks</span></span>

<span data-ttu-id="160d0-108">這是從 Windows XP 開始提供的 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="160d0-108">This is a **REG\_DWORD** value that is available starting with Windows XP.</span></span>



| <span data-ttu-id="160d0-109">值</span><span class="sxs-lookup"><span data-stu-id="160d0-109">Value</span></span>                                 | <span data-ttu-id="160d0-110">描述</span><span class="sxs-lookup"><span data-stu-id="160d0-110">Description</span></span>                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="160d0-111">0x0 (更安全的 \_ LEVELID 不 \_ 允許) </span><span class="sxs-lookup"><span data-stu-id="160d0-111">0x0 (SAFER\_LEVELID\_DISALLOWED)</span></span>      | <span data-ttu-id="160d0-112">不允許應用程式存取和安全性敏感的使用者權限。</span><span class="sxs-lookup"><span data-stu-id="160d0-112">The application is disallowed from accessing and security-sensitive user privileges.</span></span> |
| <span data-ttu-id="160d0-113">0x40000 (SAFE \_ LEVELID \_ FULLYTRUSTED) </span><span class="sxs-lookup"><span data-stu-id="160d0-113">0x40000 (SAFE\_LEVELID\_FULLYTRUSTED)</span></span> | <span data-ttu-id="160d0-114">應用程式可不受限制地存取使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="160d0-114">The application has unrestricted access to the user's privileges.</span></span>                    |



 

<span data-ttu-id="160d0-115">如果 **SRPTrustLevel** 值不存在， \_ \_ 就會使用 [不允許的安全 LEVELID] 的預設值。</span><span class="sxs-lookup"><span data-stu-id="160d0-115">If the **SRPTrustLevel** value does not exist, the default value of SAFER\_LEVELID\_DISALLOWED is used.</span></span> <span data-ttu-id="160d0-116">如果 **SRPTrustLevel** 的類型錯誤或超出範圍，COM 會傳回錯誤 COMADMIN \_ E \_ SAFERINVALID。</span><span class="sxs-lookup"><span data-stu-id="160d0-116">If **SRPTrustLevel** is of the wrong type or out of range, COM returns the error COMADMIN\_E\_SAFERINVALID.</span></span> <span data-ttu-id="160d0-117">如果任何排序的啟用因為 SRP 信任檢查而失敗，COM 會傳回錯誤共同的 \_ E \_ ACTI加值稅IONFAILED。</span><span class="sxs-lookup"><span data-stu-id="160d0-117">If an activation of any sort fails because of SRP trust checks, COM returns the error CO\_E\_ACTIVATIONFAILED.</span></span>

## <a name="related-topics"></a><span data-ttu-id="160d0-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="160d0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="160d0-119">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="160d0-119">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="160d0-120">**SRPActivateAsActivatorChecks**</span><span class="sxs-lookup"><span data-stu-id="160d0-120">**SRPActivateAsActivatorChecks**</span></span>](srpactivateasactivatorchecks.md)
</dt> <dt>

[<span data-ttu-id="160d0-121">**SRPRunningObjectChecks**</span><span class="sxs-lookup"><span data-stu-id="160d0-121">**SRPRunningObjectChecks**</span></span>](srprunningobjectchecks.md)
</dt> </dl>

 

 




