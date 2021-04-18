---
title: LegacyImpersonationLevel
description: 針對未呼叫 CoInitializeSecurity 的應用程式設定預設的模擬層級。
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- LegacyImpersonationLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968641"
---
# <a name="legacyimpersonationlevel"></a><span data-ttu-id="7adad-104">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="7adad-104">LegacyImpersonationLevel</span></span>

<span data-ttu-id="7adad-105">針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式設定預設的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="7adad-105">Sets the default level of impersonation for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="7adad-106">不建議您變更這個值，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7adad-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="7adad-107">如果您要變更此值，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。</span><span class="sxs-lookup"><span data-stu-id="7adad-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="7adad-108">如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。</span><span class="sxs-lookup"><span data-stu-id="7adad-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="7adad-109">登錄項目</span><span class="sxs-lookup"><span data-stu-id="7adad-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="7adad-110">備註</span><span class="sxs-lookup"><span data-stu-id="7adad-110">Remarks</span></span>

<span data-ttu-id="7adad-111">這是 **REG \_ 單字** 值，相當於 RPC \_ C \_ IMP \_ 層級常數。</span><span class="sxs-lookup"><span data-stu-id="7adad-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_IMP\_LEVEL constants.</span></span>



| <span data-ttu-id="7adad-112">值</span><span class="sxs-lookup"><span data-stu-id="7adad-112">Value</span></span> | <span data-ttu-id="7adad-113">常數</span><span class="sxs-lookup"><span data-stu-id="7adad-113">Constant</span></span>                        |
|-------|---------------------------------|
| <span data-ttu-id="7adad-114">1</span><span class="sxs-lookup"><span data-stu-id="7adad-114">1</span></span>     | <span data-ttu-id="7adad-115">RPC \_ C \_ IMP \_ 層級 \_ 匿名</span><span class="sxs-lookup"><span data-stu-id="7adad-115">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   |
| <span data-ttu-id="7adad-116">2</span><span class="sxs-lookup"><span data-stu-id="7adad-116">2</span></span>     | <span data-ttu-id="7adad-117">RPC \_ C \_ IMP \_ 層級 \_ 識別</span><span class="sxs-lookup"><span data-stu-id="7adad-117">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    |
| <span data-ttu-id="7adad-118">3</span><span class="sxs-lookup"><span data-stu-id="7adad-118">3</span></span>     | <span data-ttu-id="7adad-119">RPC \_ C \_ IMP \_ 層級模擬 \_</span><span class="sxs-lookup"><span data-stu-id="7adad-119">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> |
| <span data-ttu-id="7adad-120">4</span><span class="sxs-lookup"><span data-stu-id="7adad-120">4</span></span>     | <span data-ttu-id="7adad-121">RPC \_ C \_ IMP \_ 層級 \_ 委派</span><span class="sxs-lookup"><span data-stu-id="7adad-121">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    |



 

<span data-ttu-id="7adad-122">如果此登錄值不存在，系統建立的預設模擬等級為 2 (RPC \_ C \_ IMP \_ 層級 \_ 識別) 。</span><span class="sxs-lookup"><span data-stu-id="7adad-122">If this registry value is not present, the default impersonation level established by the system is 2 (RPC\_C\_IMP\_LEVEL\_IDENTIFY).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7adad-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="7adad-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7adad-124">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="7adad-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="7adad-125">設定整個進程的安全性</span><span class="sxs-lookup"><span data-stu-id="7adad-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




