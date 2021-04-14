---
title: 關閉通話安全性
description: 呼叫安全性可判斷用戶端是否有權呼叫伺服器的方法。 有兩種方式可以停用呼叫安全性，其中一個方法是使用 Dcomcnfg.exe 修改登錄，而另一個則需要呼叫 CoInitializeSecurity。
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371963"
---
# <a name="turning-off-call-security"></a><span data-ttu-id="f497e-104">關閉通話安全性</span><span class="sxs-lookup"><span data-stu-id="f497e-104">Turning Off Call Security</span></span>

<span data-ttu-id="f497e-105">呼叫安全性可判斷用戶端是否有權呼叫伺服器的方法。</span><span class="sxs-lookup"><span data-stu-id="f497e-105">Call security determines whether a client has permission to call a server's methods.</span></span> <span data-ttu-id="f497e-106">有兩種方式可以停用呼叫安全性：其中一個會牽涉到使用 Dcomcnfg.exe 修改登錄，而另一個則需要呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)。</span><span class="sxs-lookup"><span data-stu-id="f497e-106">There are two ways to disable call security: One involves using Dcomcnfg.exe to modify the registry, and the other requires calls to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

-   [<span data-ttu-id="f497e-107">使用 DCOMCNFG 關閉通話安全性</span><span class="sxs-lookup"><span data-stu-id="f497e-107">Turning Off Call Security Using DCOMCNFG</span></span>](#turning-off-call-security-using-dcomcnfg)
-   [<span data-ttu-id="f497e-108">以程式設計方式關閉通話安全性</span><span class="sxs-lookup"><span data-stu-id="f497e-108">Turning Off Call Security Programmatically</span></span>](#turning-off-call-security-programmatically)
-   [<span data-ttu-id="f497e-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="f497e-109">Related topics</span></span>](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a><span data-ttu-id="f497e-110">使用 DCOMCNFG 關閉通話安全性</span><span class="sxs-lookup"><span data-stu-id="f497e-110">Turning Off Call Security Using DCOMCNFG</span></span>

<span data-ttu-id="f497e-111">使用 Dcomcnfg.exe 修改登錄，可最輕鬆地關閉呼叫安全性。</span><span class="sxs-lookup"><span data-stu-id="f497e-111">Call security can most easily be turned off by using Dcomcnfg.exe to modify the registry.</span></span> <span data-ttu-id="f497e-112">但是，如果用戶端和伺服器都沒有呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)，使用 Dcomcnfg.exe 關閉安全性將會運作。</span><span class="sxs-lookup"><span data-stu-id="f497e-112">However, using Dcomcnfg.exe to turn security off will work only if both the client and the server do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="f497e-113">這是因為當呼叫 **CoInitializeSecurity** 時，DCOM 會忽略登錄設定，並改用提供給 **CoInitializeSecurity** 的值。</span><span class="sxs-lookup"><span data-stu-id="f497e-113">This is because when **CoInitializeSecurity** is called, DCOM ignores the registry settings and uses the values supplied to **CoInitializeSecurity** instead.</span></span>

<span data-ttu-id="f497e-114">若要關閉 Dcomcnfg.exe 的安全性，用戶端和伺服器都必須將其驗證層級設定為 [無]。</span><span class="sxs-lookup"><span data-stu-id="f497e-114">To turn off security with Dcomcnfg.exe, both the client and the server must set their Authentication Levels to None.</span></span> <span data-ttu-id="f497e-115">必須完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f497e-115">The following steps must be completed:</span></span>

1.  <span data-ttu-id="f497e-116">執行 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="f497e-116">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="f497e-117">在 [ **應用程式** ] 頁面上，選取代表伺服器的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f497e-117">On the **Applications** page, select the application that represents the server.</span></span> <span data-ttu-id="f497e-118">按一下 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="f497e-118">Click the **Properties** button (or double-click the selected application).</span></span>
3.  <span data-ttu-id="f497e-119">按一下 [General] \(一般\) 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="f497e-119">Click the **General** tab.</span></span>
4.  <span data-ttu-id="f497e-120">從 [ **預設驗證等級** ] 清單方塊中，選取 [ **無] ()**。</span><span class="sxs-lookup"><span data-stu-id="f497e-120">From the **Default Authentication Level** list box, select **(None)**.</span></span>
5.  <span data-ttu-id="f497e-121">按一下 [ **套用** ] 按鈕以套用變更;不過，變更不會套用至任何執行中的應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="f497e-121">Click the **Apply** button to apply changes; however, changes are not applied to any running instances of the application.</span></span>
6.  <span data-ttu-id="f497e-122">如果用戶端出現在 [ *應用程式* ] 頁面上的清單中，請重複步驟2到5，選擇用戶端，而不是步驟2的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f497e-122">If the client appears on the list on the *Applications* page, repeat steps 2 through 5, choosing the client instead of the server for step 2.</span></span> <span data-ttu-id="f497e-123">然後按一下 **[確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f497e-123">Then click the **OK** button.</span></span> <span data-ttu-id="f497e-124">如果用戶端不在清單中，您可以執行下列三項作業的其中一項：</span><span class="sxs-lookup"><span data-stu-id="f497e-124">If the client is not on the list, you can do one of the following three things:</span></span>
    -   <span data-ttu-id="f497e-125">您可以使用 Dcomcnfg.exe，在整個電腦上將用戶端的驗證層級設定為 [無]。</span><span class="sxs-lookup"><span data-stu-id="f497e-125">You can set the client's Authentication Level to None on a computer-wide basis by using Dcomcnfg.exe.</span></span> <span data-ttu-id="f497e-126"> (查看警告和下列程式。 ) </span><span class="sxs-lookup"><span data-stu-id="f497e-126">(See the warning and the procedure below.)</span></span>
    -   <span data-ttu-id="f497e-127">您可以用程式設計的方式將用戶端的驗證層級設定為 [無]。</span><span class="sxs-lookup"><span data-stu-id="f497e-127">You can set the client's authentication level to None programmatically.</span></span>
    -   <span data-ttu-id="f497e-128">您可以為用戶端建立 [AppID](appid-key.md) 金鑰，以指出驗證層級為 [無]。</span><span class="sxs-lookup"><span data-stu-id="f497e-128">You can create an [AppID](appid-key.md) key for the client to indicate an authentication level of None.</span></span> <span data-ttu-id="f497e-129"> (參閱 [透過登錄設定 Process-Wide 安全性](setting-processwide-security-through-the-registry.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="f497e-129">(See [Setting Process-Wide Security Through the Registry](setting-processwide-security-through-the-registry.md).)</span></span>

<span data-ttu-id="f497e-130">若要在整個電腦上將驗證等級設定為 [無]：</span><span class="sxs-lookup"><span data-stu-id="f497e-130">To set the Authentication Level to None on a computer-wide basis:</span></span>

> [!Note]  
> <span data-ttu-id="f497e-131">將全電腦的驗證層級設定為 [無] 非常不安全。</span><span class="sxs-lookup"><span data-stu-id="f497e-131">Setting the computer-wide Authentication Level to None is extremely unsecure.</span></span>

 

1.  <span data-ttu-id="f497e-132">執行 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="f497e-132">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="f497e-133">選擇 [ **預設** 內容] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="f497e-133">Choose the **Default Properties** tab.</span></span>
3.  <span data-ttu-id="f497e-134">從 [ **預設驗證等級** ] 清單方塊中，選擇 [ **無] ()**。</span><span class="sxs-lookup"><span data-stu-id="f497e-134">From the **Default Authentication Level** list box, choose **(None)**.</span></span>
4.  <span data-ttu-id="f497e-135">按一下 [確定] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f497e-135">Click the **OK** button.</span></span>

## <a name="turning-off-call-security-programmatically"></a><span data-ttu-id="f497e-136">以程式設計方式關閉通話安全性</span><span class="sxs-lookup"><span data-stu-id="f497e-136">Turning Off Call Security Programmatically</span></span>

<span data-ttu-id="f497e-137">若要以程式設計方式關閉呼叫安全性，用戶端和伺服器都必須呼叫 **CoInitializeSecurity**，將 *dwAuthnLevel* 參數中的驗證層級設定為「RPC \_ C \_ 驗證 \_ 層級 \_ 無」。</span><span class="sxs-lookup"><span data-stu-id="f497e-137">To turn call security off programmatically, both the client and the server must call **CoInitializeSecurity**, setting the authentication level in the *dwAuthnLevel* parameter to RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f497e-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="f497e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f497e-139">關閉啟用安全性</span><span class="sxs-lookup"><span data-stu-id="f497e-139">Turning Off Activation Security</span></span>](turning-off-activation-security.md)
</dt> </dl>

 

 




