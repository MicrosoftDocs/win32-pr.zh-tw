---
title: AuthenticationLevel
description: 針對未呼叫 CoInitializeSecurity 的應用程式，或針對呼叫 CoInitializeSecurity 並指定 AppID 的應用程式，設定驗證等級。
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- AuthenticationLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311505"
---
# <a name="authenticationlevel"></a><span data-ttu-id="687ef-104">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="687ef-104">AuthenticationLevel</span></span>

<span data-ttu-id="687ef-105">針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 的應用程式，或針對呼叫 **CoInitializeSecurity** 並指定 AppID 的應用程式，設定驗證等級。</span><span class="sxs-lookup"><span data-stu-id="687ef-105">Sets the authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or for applications that call **CoInitializeSecurity** and specify an AppID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="687ef-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="687ef-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="687ef-107">備註</span><span class="sxs-lookup"><span data-stu-id="687ef-107">Remarks</span></span>

<span data-ttu-id="687ef-108">這是 **REG \_ DWORD** 值，相當於 RPC \_ C \_ 驗證 \_ 層級常數。</span><span class="sxs-lookup"><span data-stu-id="687ef-108">This is a **REG\_DWORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="687ef-109">值</span><span class="sxs-lookup"><span data-stu-id="687ef-109">Value</span></span> | <span data-ttu-id="687ef-110">常數</span><span class="sxs-lookup"><span data-stu-id="687ef-110">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="687ef-111">1</span><span class="sxs-lookup"><span data-stu-id="687ef-111">1</span></span>     | <span data-ttu-id="687ef-112">RPC \_ C \_ 驗證 \_ 層級 \_ 無</span><span class="sxs-lookup"><span data-stu-id="687ef-112">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="687ef-113">2</span><span class="sxs-lookup"><span data-stu-id="687ef-113">2</span></span>     | <span data-ttu-id="687ef-114">RPC \_ C \_ 驗證 \_ LEVEL \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="687ef-114">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="687ef-115">3</span><span class="sxs-lookup"><span data-stu-id="687ef-115">3</span></span>     | <span data-ttu-id="687ef-116">RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫</span><span class="sxs-lookup"><span data-stu-id="687ef-116">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="687ef-117">4</span><span class="sxs-lookup"><span data-stu-id="687ef-117">4</span></span>     | <span data-ttu-id="687ef-118">RPC \_ C \_ 驗證 \_ 層級 \_ PKT</span><span class="sxs-lookup"><span data-stu-id="687ef-118">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="687ef-119">5</span><span class="sxs-lookup"><span data-stu-id="687ef-119">5</span></span>     | <span data-ttu-id="687ef-120">RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 完整性</span><span class="sxs-lookup"><span data-stu-id="687ef-120">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="687ef-121">6</span><span class="sxs-lookup"><span data-stu-id="687ef-121">6</span></span>     | <span data-ttu-id="687ef-122">RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權</span><span class="sxs-lookup"><span data-stu-id="687ef-122">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="687ef-123">**AuthenticationLevel** 值類似于 [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)值。</span><span class="sxs-lookup"><span data-stu-id="687ef-123">The **AuthenticationLevel** value is similar to the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) value.</span></span> <span data-ttu-id="687ef-124">如果有 **AuthenticationLevel** 值，就會使用它，而不是該 AppID 的 **LegacyAuthenticationLevel** 值。</span><span class="sxs-lookup"><span data-stu-id="687ef-124">If the **AuthenticationLevel** value is present, it is used instead of the **LegacyAuthenticationLevel** value for that AppID.</span></span>

<span data-ttu-id="687ef-125">如果 **AuthenticationLevel** 值的類型錯誤或超出範圍，則 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 會失敗，而導致介面封送處理失敗。</span><span class="sxs-lookup"><span data-stu-id="687ef-125">If the **AuthenticationLevel** value is of the wrong type or out of range, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fails, causing interface marshaling to fail.</span></span> <span data-ttu-id="687ef-126">這可防止應用程式在所有 (跨單元、跨執行緒、跨進程或跨電腦) 進行任何呼叫。</span><span class="sxs-lookup"><span data-stu-id="687ef-126">This prevents the application from making any calls at all (cross-apartment, cross-thread, cross-process, or cross-computer).</span></span>

<span data-ttu-id="687ef-127">**AuthenticationLevel** 和 [**AccessPermission**](accesspermission.md)值是獨立的。</span><span class="sxs-lookup"><span data-stu-id="687ef-127">The **AuthenticationLevel** and [**AccessPermission**](accesspermission.md) values are independent.</span></span> <span data-ttu-id="687ef-128">如果不存在，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="687ef-128">If one is not present, the default is used.</span></span> <span data-ttu-id="687ef-129">下列規則會列出 **AuthenticationLevel** 值與 **AccessPermission** 值之間的互動：</span><span class="sxs-lookup"><span data-stu-id="687ef-129">The following rules list the interaction between the **AuthenticationLevel** value and the **AccessPermission** value:</span></span>

-   <span data-ttu-id="687ef-130">如果 **AuthenticationLevel** 為 NONE，則) 的應用程式 (會忽略 [**AccessPermission**](accesspermission.md) 和 [**DefaultAccessPermission**](defaultaccesspermission.md) 值。</span><span class="sxs-lookup"><span data-stu-id="687ef-130">If the **AuthenticationLevel** is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>
-   <span data-ttu-id="687ef-131">如果 **AuthenticationLevel** 不存在，而且 [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) 為 NONE，則會忽略該應用程式)  (的 [**AccessPermission**](accesspermission.md) 和 [**DefaultAccessPermission**](defaultaccesspermission.md) 值。</span><span class="sxs-lookup"><span data-stu-id="687ef-131">If the **AuthenticationLevel** is not present and the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>

## <a name="related-topics"></a><span data-ttu-id="687ef-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="687ef-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="687ef-133">驗證層級常數</span><span class="sxs-lookup"><span data-stu-id="687ef-133">Authentication Level Constants</span></span>](com-authentication-level-constants.md)
</dt> <dt>

[<span data-ttu-id="687ef-134">**LegacyAuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="687ef-134">**LegacyAuthenticationLevel**</span></span>](legacyauthenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="687ef-135">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="687ef-135">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="687ef-136">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="687ef-136">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




