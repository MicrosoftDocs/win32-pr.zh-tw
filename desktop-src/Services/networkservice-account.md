---
description: NetworkService 帳戶是服務控制管理員所使用的預先定義本機帳戶。
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: NetworkService 帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983832"
---
# <a name="networkservice-account"></a><span data-ttu-id="a44e8-103">NetworkService 帳戶</span><span class="sxs-lookup"><span data-stu-id="a44e8-103">NetworkService Account</span></span>

<span data-ttu-id="a44e8-104">NetworkService 帳戶是服務控制管理員所使用的預先定義本機帳戶。</span><span class="sxs-lookup"><span data-stu-id="a44e8-104">The NetworkService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="a44e8-105">安全性子系統無法辨識此帳戶，因此您無法在 [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) 函式的呼叫中指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="a44e8-105">This account is not recognized by the security subsystem, so you cannot specify its name in a call to the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span> <span data-ttu-id="a44e8-106">它在本機電腦上具有最小許可權，而且會作為網路上的電腦。</span><span class="sxs-lookup"><span data-stu-id="a44e8-106">It has minimum privileges on the local computer and acts as the computer on the network.</span></span>

<span data-ttu-id="a44e8-107">您可以在 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 和 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函數的呼叫中指定這個帳戶。</span><span class="sxs-lookup"><span data-stu-id="a44e8-107">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="a44e8-108">請注意，此帳戶沒有密碼，因此會忽略您在此呼叫中提供的任何密碼資訊。</span><span class="sxs-lookup"><span data-stu-id="a44e8-108">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="a44e8-109">雖然安全性子系統會當地語系化此帳戶名稱，但 SCM 不支援當地語系化的名稱。</span><span class="sxs-lookup"><span data-stu-id="a44e8-109">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="a44e8-110">因此，您將會從 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) 函式接收此帳戶的當地語系化名稱，但 \\ 當您呼叫 **CreateService** 或 **ChangeServiceConfig** 時，不論地區設定為何，或可能發生非預期的結果，帳戶的名稱都必須是 NT 授權單位 NetworkService。</span><span class="sxs-lookup"><span data-stu-id="a44e8-110">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\NetworkService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="a44e8-111">在 NetworkService 帳戶內容中執行的服務，會向遠端伺服器顯示電腦的認證。</span><span class="sxs-lookup"><span data-stu-id="a44e8-111">A service that runs in the context of the NetworkService account presents the computer's credentials to remote servers.</span></span> <span data-ttu-id="a44e8-112">根據預設，遠端權杖包含 Everyone 和已驗證使用者群組的 Sid。</span><span class="sxs-lookup"><span data-stu-id="a44e8-112">By default, the remote token contains SIDs for the Everyone and Authenticated Users groups.</span></span> <span data-ttu-id="a44e8-113">使用者 SID 是從 **安全性 \_ 網路 \_ 服務 \_ RID** 值建立的。</span><span class="sxs-lookup"><span data-stu-id="a44e8-113">The user SID is created from the **SECURITY\_NETWORK\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="a44e8-114">NetworkService 帳戶在 **HKEY \_ USERS** 登錄機碼底下有自己的子機碼。</span><span class="sxs-lookup"><span data-stu-id="a44e8-114">The NetworkService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="a44e8-115">因此， **HKEY \_ CURRENT \_ USER** 登錄機碼與 NetworkService 帳戶相關聯。</span><span class="sxs-lookup"><span data-stu-id="a44e8-115">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the NetworkService account.</span></span>

<span data-ttu-id="a44e8-116">NetworkService 帳戶具有下列許可權：</span><span class="sxs-lookup"><span data-stu-id="a44e8-116">The NetworkService account has the following privileges:</span></span>

-   <span data-ttu-id="a44e8-117">**SE \_ASSIGNPRIMARYTOKEN \_ 名稱** (停用) </span><span class="sxs-lookup"><span data-stu-id="a44e8-117">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="a44e8-118">**SE \_ (\_** 停用的審核名稱) </span><span class="sxs-lookup"><span data-stu-id="a44e8-118">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="a44e8-119">**SE \_ (啟用變更 \_ 通知 \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="a44e8-119">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="a44e8-120">**SE \_ (啟用 [建立 \_ 全域 \_ 名稱** ]) </span><span class="sxs-lookup"><span data-stu-id="a44e8-120">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="a44e8-121">**SE \_ (\_** 啟用模擬名稱) </span><span class="sxs-lookup"><span data-stu-id="a44e8-121">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="a44e8-122">**SE \_ (停用) 增加 \_ 配額 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="a44e8-122">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="a44e8-123">**SE \_停用的關機 \_ 名稱** () </span><span class="sxs-lookup"><span data-stu-id="a44e8-123">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="a44e8-124">**SE \_停用移除 \_ 名稱** (停用) </span><span class="sxs-lookup"><span data-stu-id="a44e8-124">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="a44e8-125">指派給使用者和已驗證使用者的任何許可權</span><span class="sxs-lookup"><span data-stu-id="a44e8-125">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="a44e8-126">如需詳細資訊，請參閱 [服務安全性和存取權限](service-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="a44e8-126">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
