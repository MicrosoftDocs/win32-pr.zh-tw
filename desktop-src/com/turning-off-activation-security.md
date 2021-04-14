---
title: 關閉啟用安全性
description: 關閉啟用安全性
ms.assetid: 3474f8ad-f041-4886-ad39-ff0603c5c69e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da3ebd7cc03d79fc38fbafe3bc652efc3499437
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382950"
---
# <a name="turning-off-activation-security"></a><span data-ttu-id="fd223-103">關閉啟用安全性</span><span class="sxs-lookup"><span data-stu-id="fd223-103">Turning Off Activation Security</span></span>

<span data-ttu-id="fd223-104">一般來說，啟用會使用預設安全性設定。</span><span class="sxs-lookup"><span data-stu-id="fd223-104">Normally, activation uses default security settings.</span></span> <span data-ttu-id="fd223-105">不過，您可以藉由指定 [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 結構來控制啟用安全性，這是傳遞給啟用函式的 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構成員。</span><span class="sxs-lookup"><span data-stu-id="fd223-105">However, you can control activation security by specifying a [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure, which is a member of the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure that is passed to the activation functions.</span></span> <span data-ttu-id="fd223-106">如果用戶端 \_ \_ 在 COAUTHINFO 結構中指定 RPC C 驗證 \_ 層級無驗證等級 \_ ，則不會嘗試驗證。 </span><span class="sxs-lookup"><span data-stu-id="fd223-106">If the client specifies an authentication level of RPC\_C\_AUTHN\_LEVEL\_NONE in the **COAUTHINFO** structure, authentication is not attempted.</span></span> <span data-ttu-id="fd223-107">否則，將會嘗試安全啟用，如果驗證失敗，則啟用會失敗。</span><span class="sxs-lookup"><span data-stu-id="fd223-107">Otherwise, secure activation is attempted, and if authentication fails, activation fails.</span></span>

<span data-ttu-id="fd223-108">如果用戶端未指定明確的 [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 結構，而改為將指標設定為 **Null**，COM 將會嘗試驗證用戶端。</span><span class="sxs-lookup"><span data-stu-id="fd223-108">If the client does not specify an explicit [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure and instead sets the pointer to **NULL**, COM will attempt to authenticate the client.</span></span> <span data-ttu-id="fd223-109">如果無法驗證用戶端，COM 會檢查啟動許可權安全描述項，以查看是否有 **Null** DACL 或允許存取所有人的 ACL。</span><span class="sxs-lookup"><span data-stu-id="fd223-109">If it cannot authenticate the client, COM checks the launch permission security descriptor to see whether there is a **NULL** DACL or an ACL that allows access to Everyone.</span></span> <span data-ttu-id="fd223-110">如果此檢查成功，則會啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="fd223-110">If this check succeeds, the server is launched.</span></span> <span data-ttu-id="fd223-111">因此，即使用戶端未指定 **COAUTHINFO** 結構，在伺服器允許不安全的啟用時也可能會發生。</span><span class="sxs-lookup"><span data-stu-id="fd223-111">Therefore, even if the client does not specify a **COAUTHINFO** structure, unsecure activation may take place when the server allows it.</span></span>

> [!Note]  
> <span data-ttu-id="fd223-112">若要允許未驗證的網路使用者執行 COM 應用程式，應用程式角色必須包含匿名使用者。</span><span class="sxs-lookup"><span data-stu-id="fd223-112">To allow unauthenticated network users to run a COM application, the application roles must include the Anonymous user.</span></span> <span data-ttu-id="fd223-113">從 Windows Server 2003 開始，根據預設，匿名使用者不會包含在 Everyone 群組中。</span><span class="sxs-lookup"><span data-stu-id="fd223-113">Starting with Windows Server 2003, by default, the Anonymous user is not included in the Everyone group.</span></span>

 

<span data-ttu-id="fd223-114">為什麼用戶端會想要明確關閉啟用安全性，即使伺服器允許不安全的啟用也會發生？</span><span class="sxs-lookup"><span data-stu-id="fd223-114">Why would a client want to turn off activation security explicitly even though unsecure activation will eventually take place if the server allows it?</span></span> <span data-ttu-id="fd223-115">因為當用戶端不想要或不需要安全性檢查時，明確關閉啟用安全性可提高效能。</span><span class="sxs-lookup"><span data-stu-id="fd223-115">Because explicitly turning off activation security increases performance when the client does not want or need security checks.</span></span>

<span data-ttu-id="fd223-116">您必須執行下列動作，以明確關閉啟用安全性：</span><span class="sxs-lookup"><span data-stu-id="fd223-116">The following things must be done to explicitly turn off activation security:</span></span>

-   <span data-ttu-id="fd223-117">用戶端必須 \_ 在 COAUTHINFO 結構中指定 RPC C 驗證層級 NONE 的驗證層級，該 \_ \_ \_ 結構是提供給啟用函式之 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)結構的成員。 [](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo)</span><span class="sxs-lookup"><span data-stu-id="fd223-117">The client must specify an authentication level of RPC\_C\_AUTHN\_LEVEL\_NONE in the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure that is a member of the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure supplied to the activation function.</span></span>
-   <span data-ttu-id="fd223-118">用戶端必須在 COAUTHINFO 結構中指定模擬的 RPC C IMP 層級模擬層級，該 \_ \_ \_ \_ 結構是提供給啟用函式之 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)結構的成員。 [](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo)</span><span class="sxs-lookup"><span data-stu-id="fd223-118">The client must specify an impersonation level of RPC\_C\_IMP\_LEVEL\_IMPERSONATE in the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure that is a member of the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure supplied to the activation function.</span></span> <span data-ttu-id="fd223-119">如果未傳遞此值，您將無法取得 RPC \_ S \_ 伺服器 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fd223-119">If this value is not passed, you will get RPC\_S\_SERVER\_UNAVAILABLE.</span></span>
-   <span data-ttu-id="fd223-120">伺服器必須指定 **預設啟動許可權** 的 **所有人**。</span><span class="sxs-lookup"><span data-stu-id="fd223-120">The server must specify **Everyone** for **Default Launch Permissions**.</span></span> <span data-ttu-id="fd223-121">執行這項工作的建議方式是使用 Dcomcnfg.exe，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fd223-121">The recommended way to perform this task is to use Dcomcnfg.exe as follows:</span></span>
    1.  <span data-ttu-id="fd223-122">執行 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="fd223-122">Run Dcomcnfg.exe.</span></span>
    2.  <span data-ttu-id="fd223-123">在 [ **應用程式** ] 頁面上，選取代表伺服器的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fd223-123">On the **Applications** page, select the application that represents the server.</span></span> <span data-ttu-id="fd223-124">按一下 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="fd223-124">Click the **Properties** button (or double-click the selected application).</span></span>
    3.  <span data-ttu-id="fd223-125">在 [ **安全性** ] 屬性頁上，按一下 [ **使用自訂啟動許可權** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fd223-125">On the **Security** property page, click the **Use Custom Launch Permissions** button.</span></span>
    4.  <span data-ttu-id="fd223-126">按一下 [**啟動許可權**] 區域中的 [**編輯**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fd223-126">Click the **Edit** button in the **Launch Permissions** area.</span></span>
    5.  <span data-ttu-id="fd223-127">在 [登錄 **值許可權** ] 對話方塊中，按一下 [ **新增** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fd223-127">In the **Registry Value Permissions** dialog box, click the **Add** button.</span></span>
    6.  <span data-ttu-id="fd223-128">在清單方塊中選取 [ **所有人** ] 的專案。</span><span class="sxs-lookup"><span data-stu-id="fd223-128">Select the entry for **Everyone** in the list box.</span></span>
    7.  <span data-ttu-id="fd223-129">在 [ **存取類型** ] 清單方塊中，選擇 [ **允許啟動**]。</span><span class="sxs-lookup"><span data-stu-id="fd223-129">In the **Type of Access** list box, choose **Allow Launch**.</span></span>
    8.  <span data-ttu-id="fd223-130">按一下 [確定] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fd223-130">Click the **OK** button.</span></span>

> [!Note]  
> <span data-ttu-id="fd223-131">在 Windows Server 2003 中，COM + 系統應用程式的驗證功能包含 EOAC \_ DISABLE AAA 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fd223-131">In Windows Server 2003, the authentication capability for the COM+ system application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="fd223-132">此值會在啟動系統應用程式時，在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 呼叫中使用停用的 (AAA) 啟用。</span><span class="sxs-lookup"><span data-stu-id="fd223-132">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the system application.</span></span> <span data-ttu-id="fd223-133">將驗證功能設定為 EOAC \_ DISABLE \_ AAA，可讓在特殊許可權帳戶下執行的應用程式 (例如 LocalSystem) ，以協助防止其身分識別用來啟動未受信任的元件。</span><span class="sxs-lookup"><span data-stu-id="fd223-133">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fd223-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd223-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd223-135">關閉通話安全性</span><span class="sxs-lookup"><span data-stu-id="fd223-135">Turning Off Call Security</span></span>](turning-off-call-security.md)
</dt> </dl>

 

 