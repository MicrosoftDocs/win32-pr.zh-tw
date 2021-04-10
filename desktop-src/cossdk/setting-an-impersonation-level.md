---
description: 當您為應用程式設定模擬層級時，您會決定應用程式在呼叫這些應用程式時，要授與其他應用程式使用其身分識別的許可權等級。
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: 設定模擬等級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110897"
---
# <a name="setting-an-impersonation-level"></a><span data-ttu-id="cd1b7-103">設定模擬等級</span><span class="sxs-lookup"><span data-stu-id="cd1b7-103">Setting an Impersonation Level</span></span>

<span data-ttu-id="cd1b7-104">當您為應用程式設定模擬層級時，您會決定應用程式在呼叫這些應用程式時，要授與其他應用程式使用其身分識別的許可權等級。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-104">When you set an impersonation level for an application, you determine what degree of authority the application grants other applications to use its identity when it calls them.</span></span> <span data-ttu-id="cd1b7-105">您只能針對 COM + 伺服器應用程式進行這項作業：程式庫應用程式是在裝載進程的身分識別下執行，並使用其指定的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-105">You can set this only for COM+ server applications—library applications run under the identity of the hosting process and use the impersonation level that it specifies.</span></span> <span data-ttu-id="cd1b7-106">如需詳細資訊，請參閱模擬 [層級](/windows/desktop/com/impersonation-levels)。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-106">For more detail, see [Impersonation Levels](/windows/desktop/com/impersonation-levels).</span></span>

<span data-ttu-id="cd1b7-107">**選取模擬等級**</span><span class="sxs-lookup"><span data-stu-id="cd1b7-107">**To select an impersonation level**</span></span>

1.  <span data-ttu-id="cd1b7-108">以滑鼠右鍵按一下您要設定模擬的 COM + 應用程式，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-108">Right-click the COM+ application for which you are setting impersonation, and then click **Properties**.</span></span>

2.  <span data-ttu-id="cd1b7-109">在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="cd1b7-110">在 [模擬 **等級** ] 方塊中，選取適當的層級。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-110">In the **Impersonation level** box, select the appropriate level.</span></span> <span data-ttu-id="cd1b7-111">層級如下所示，從授與的最小授權單位：</span><span class="sxs-lookup"><span data-stu-id="cd1b7-111">The levels are as follows, ordered from granting least to greatest authority:</span></span>

    -   <span data-ttu-id="cd1b7-112">**匿名**。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-112">**Anonymous**.</span></span> <span data-ttu-id="cd1b7-113">用戶端對伺服器而言是匿名。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-113">The client is anonymous to the server.</span></span> <span data-ttu-id="cd1b7-114">伺服器可以模擬用戶端，但是模擬權杖 (本機認證) 不包含用戶端的任何相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-114">The server can impersonate the client, but the impersonation token (a local credential) does not contain any information about the client.</span></span>
    -   <span data-ttu-id="cd1b7-115">**識別**。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-115">**Identify**.</span></span> <span data-ttu-id="cd1b7-116">伺服器可以取得用戶端的身分識別，並可模擬用戶端來進行 ACL 檢查。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-116">The server can obtain the client's identity and can impersonate the client to do ACL checks.</span></span>
    -   <span data-ttu-id="cd1b7-117">模擬。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-117">**Impersonate**.</span></span> <span data-ttu-id="cd1b7-118">伺服器可以模擬用戶端，並代表它執行動作 (但仍會有部份限制)。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-118">The server can impersonate the client while acting on its behalf, although with restrictions.</span></span> <span data-ttu-id="cd1b7-119">伺服器可以存取與用戶端所在之同一部電腦上的資源。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-119">The server can access resources on the same computer as the client.</span></span> <span data-ttu-id="cd1b7-120">如果伺服器與用戶端位於同一部電腦上，則可以做為用戶端來存取網路資源。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-120">If the server is on the same computer as the client, it can access network resources as the client.</span></span> <span data-ttu-id="cd1b7-121">如果伺服器位於與用戶端不同的電腦上，則只能存取與伺服器位於同一部電腦上的資源。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-121">If the server is on a computer different from the client, it can access only resources that are on the same computer as the server.</span></span> <span data-ttu-id="cd1b7-122">這是 COM+ 伺服器應用程式的預設值。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-122">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="cd1b7-123">**委派**。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-123">**Delegate**.</span></span> <span data-ttu-id="cd1b7-124">伺服器可以模擬用戶端，而不是在與用戶端相同的電腦上代表它。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-124">The server can impersonate the client while acting on its behalf, whether on the same computer as the client.</span></span> <span data-ttu-id="cd1b7-125">在模擬期間，用戶端的認證 (具有本機的憑證，以及具有網路有效) 的憑證可傳遞至任意數目的電腦。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-125">During impersonation, the client's credentials (both those with local and those with network validity) can be passed to any number of machines.</span></span>

4.  <span data-ttu-id="cd1b7-126">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="cd1b7-126">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd1b7-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd1b7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd1b7-128">設定 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="cd1b7-128">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="cd1b7-129">設定軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="cd1b7-129">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="cd1b7-130">啟用程式庫應用程式的驗證</span><span class="sxs-lookup"><span data-stu-id="cd1b7-130">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="cd1b7-131">設定伺服器應用程式的驗證層級</span><span class="sxs-lookup"><span data-stu-id="cd1b7-131">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
