---
description: LocalService 帳戶是服務控制管理員所使用的預先定義本機帳戶。
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: LocalService 帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513905"
---
# <a name="localservice-account"></a><span data-ttu-id="9063d-103">LocalService 帳戶</span><span class="sxs-lookup"><span data-stu-id="9063d-103">LocalService Account</span></span>

<span data-ttu-id="9063d-104">LocalService 帳戶是服務控制管理員所使用的預先定義本機帳戶。</span><span class="sxs-lookup"><span data-stu-id="9063d-104">The LocalService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="9063d-105">它在本機電腦上具有最低許可權，並在網路上呈現匿名認證。</span><span class="sxs-lookup"><span data-stu-id="9063d-105">It has minimum privileges on the local computer and presents anonymous credentials on the network.</span></span>

<span data-ttu-id="9063d-106">您可以在 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 和 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函數的呼叫中指定這個帳戶。</span><span class="sxs-lookup"><span data-stu-id="9063d-106">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="9063d-107">請注意，此帳戶沒有密碼，因此會忽略您在此呼叫中提供的任何密碼資訊。</span><span class="sxs-lookup"><span data-stu-id="9063d-107">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="9063d-108">雖然安全性子系統會當地語系化此帳戶名稱，但 SCM 不支援當地語系化的名稱。</span><span class="sxs-lookup"><span data-stu-id="9063d-108">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="9063d-109">因此，您會從 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) 函式接收此帳戶的當地語系化名稱，但 \\ 當您呼叫 **CreateService** 或 **ChangeServiceConfig** 時，帳戶的名稱必須是 NT 授權單位 LocalService，無論地區設定為何，或可能發生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="9063d-109">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\LocalService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="9063d-110">使用者 SID 是從 **安全性 \_ 本地 \_ 服務 \_ RID** 值建立。</span><span class="sxs-lookup"><span data-stu-id="9063d-110">The user SID is created from the **SECURITY\_LOCAL\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="9063d-111">LocalService 帳戶在 **HKEY \_ USERS** 登錄機碼底下有自己的子機碼。</span><span class="sxs-lookup"><span data-stu-id="9063d-111">The LocalService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="9063d-112">因此， **HKEY \_ CURRENT \_ USER** 登錄機碼與 LocalService 帳戶相關聯。</span><span class="sxs-lookup"><span data-stu-id="9063d-112">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the LocalService account.</span></span>

<span data-ttu-id="9063d-113">LocalService 帳戶具有下列許可權：</span><span class="sxs-lookup"><span data-stu-id="9063d-113">The LocalService account has the following privileges:</span></span>

-   <span data-ttu-id="9063d-114">**SE \_ASSIGNPRIMARYTOKEN \_ 名稱** (停用) </span><span class="sxs-lookup"><span data-stu-id="9063d-114">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9063d-115">**SE \_ (\_** 停用的審核名稱) </span><span class="sxs-lookup"><span data-stu-id="9063d-115">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9063d-116">**SE \_ (啟用變更 \_ 通知 \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="9063d-116">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="9063d-117">**SE \_ (啟用 [建立 \_ 全域 \_ 名稱** ]) </span><span class="sxs-lookup"><span data-stu-id="9063d-117">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="9063d-118">**SE \_ (\_** 啟用模擬名稱) </span><span class="sxs-lookup"><span data-stu-id="9063d-118">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="9063d-119">**SE \_ (停用) 增加 \_ 配額 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="9063d-119">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9063d-120">**SE \_停用的關機 \_ 名稱** () </span><span class="sxs-lookup"><span data-stu-id="9063d-120">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9063d-121">**SE \_停用移除 \_ 名稱** (停用) </span><span class="sxs-lookup"><span data-stu-id="9063d-121">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9063d-122">指派給使用者和已驗證使用者的任何許可權</span><span class="sxs-lookup"><span data-stu-id="9063d-122">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="9063d-123">如需詳細資訊，請參閱 [服務安全性和存取權限](service-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="9063d-123">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
