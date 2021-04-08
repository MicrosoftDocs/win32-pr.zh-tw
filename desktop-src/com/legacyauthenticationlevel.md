---
title: LegacyAuthenticationLevel
description: 針對未呼叫 CoInitializeSecurity 的應用程式設定預設驗證層級。
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- LegacyAuthenticationLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022098"
---
# <a name="legacyauthenticationlevel"></a><span data-ttu-id="7cd3d-104">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="7cd3d-104">LegacyAuthenticationLevel</span></span>

<span data-ttu-id="7cd3d-105">針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式設定預設驗證層級。</span><span class="sxs-lookup"><span data-stu-id="7cd3d-105">Sets the default authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="7cd3d-106">不建議您變更這個值，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7cd3d-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="7cd3d-107">如果您要變更此值，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。</span><span class="sxs-lookup"><span data-stu-id="7cd3d-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="7cd3d-108">如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。</span><span class="sxs-lookup"><span data-stu-id="7cd3d-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="7cd3d-109">登錄項目</span><span class="sxs-lookup"><span data-stu-id="7cd3d-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="7cd3d-110">備註</span><span class="sxs-lookup"><span data-stu-id="7cd3d-110">Remarks</span></span>

<span data-ttu-id="7cd3d-111">這是 **REG \_ 單字** 值，相當於 RPC \_ C \_ 驗證 \_ 層級常數。</span><span class="sxs-lookup"><span data-stu-id="7cd3d-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="7cd3d-112">值</span><span class="sxs-lookup"><span data-stu-id="7cd3d-112">Value</span></span> | <span data-ttu-id="7cd3d-113">常數</span><span class="sxs-lookup"><span data-stu-id="7cd3d-113">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="7cd3d-114">1</span><span class="sxs-lookup"><span data-stu-id="7cd3d-114">1</span></span>     | <span data-ttu-id="7cd3d-115">RPC \_ C \_ 驗證 \_ 層級 \_ 無</span><span class="sxs-lookup"><span data-stu-id="7cd3d-115">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="7cd3d-116">2</span><span class="sxs-lookup"><span data-stu-id="7cd3d-116">2</span></span>     | <span data-ttu-id="7cd3d-117">RPC \_ C \_ 驗證 \_ LEVEL \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="7cd3d-117">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="7cd3d-118">3</span><span class="sxs-lookup"><span data-stu-id="7cd3d-118">3</span></span>     | <span data-ttu-id="7cd3d-119">RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫</span><span class="sxs-lookup"><span data-stu-id="7cd3d-119">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="7cd3d-120">4</span><span class="sxs-lookup"><span data-stu-id="7cd3d-120">4</span></span>     | <span data-ttu-id="7cd3d-121">RPC \_ C \_ 驗證 \_ 層級 \_ PKT</span><span class="sxs-lookup"><span data-stu-id="7cd3d-121">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="7cd3d-122">5</span><span class="sxs-lookup"><span data-stu-id="7cd3d-122">5</span></span>     | <span data-ttu-id="7cd3d-123">RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 完整性</span><span class="sxs-lookup"><span data-stu-id="7cd3d-123">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="7cd3d-124">6</span><span class="sxs-lookup"><span data-stu-id="7cd3d-124">6</span></span>     | <span data-ttu-id="7cd3d-125">RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權</span><span class="sxs-lookup"><span data-stu-id="7cd3d-125">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="7cd3d-126">如果此登錄值不存在，系統建立的預設驗證層級為 2 (RPC \_ C \_ 驗證 \_ CONNECT) 。</span><span class="sxs-lookup"><span data-stu-id="7cd3d-126">If this registry value is not present, the default authentication level established by the system is 2 (RPC\_C\_AUTHN\_CONNECT).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cd3d-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="7cd3d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cd3d-128">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="7cd3d-128">**AuthenticationLevel**</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="7cd3d-129">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="7cd3d-129">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="7cd3d-130">設定整個進程的安全性</span><span class="sxs-lookup"><span data-stu-id="7cd3d-130">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




