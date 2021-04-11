---
description: 設定軟體限制原則
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: 設定軟體限制原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025993"
---
# <a name="configuring-the-software-restriction-policy"></a><span data-ttu-id="88f4a-103">設定軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="88f4a-103">Configuring the Software Restriction Policy</span></span>

<span data-ttu-id="88f4a-104">當您明確設定 COM + 應用程式的軟體限制原則信任層級時，會覆寫預設的全系統設定。</span><span class="sxs-lookup"><span data-stu-id="88f4a-104">When you explicitly set the software restriction policy trust levels of a COM+ application, you are overriding the default systemwide settings.</span></span> <span data-ttu-id="88f4a-105">這通常是 COM + 伺服器應用程式的必要項，因為所有伺服器應用程式都有相同的全系統信任層級設定， (因為它們都是在相同的檔案中執行，dllhost.exe) 。</span><span class="sxs-lookup"><span data-stu-id="88f4a-105">This is often necessary for COM+ server applications because the systemwide trust level is set the same for all server applications (because they all run in the same file, dllhost.exe).</span></span> <span data-ttu-id="88f4a-106">但是，當您設定 COM + 程式庫應用程式的軟體限制原則信任層級時，會影響該應用程式的全系統設定。</span><span class="sxs-lookup"><span data-stu-id="88f4a-106">However, when you set the software restriction policy trust level of a COM+ library application, you are affecting the systemwide configuration for that application.</span></span> <span data-ttu-id="88f4a-107">如需如何在 COM + 中使用軟體限制原則的討論，請參閱 [在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)。</span><span class="sxs-lookup"><span data-stu-id="88f4a-107">For a discussion of how to use the software restriction policy in COM+, see [Using the Software Restriction Policy in COM+](using-the-software-restriction-policy-in-com-.md).</span></span>

<span data-ttu-id="88f4a-108">**設定軟體限制原則**</span><span class="sxs-lookup"><span data-stu-id="88f4a-108">**To set the software restriction policy**</span></span>

1.  <span data-ttu-id="88f4a-109">在您要設定軟體限制原則的 COM + 應用程式 **上按一下滑鼠** 右鍵，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="88f4a-109">Right-click the COM+ application for which you are setting the software restriction policy, and then click **Properties**.</span></span>

2.  <span data-ttu-id="88f4a-110">在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="88f4a-110">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="88f4a-111">在 [ **軟體限制原則**] 底下，選取 [套用 **軟體限制原則** ] 核取方塊。這可讓您設定信任層級。</span><span class="sxs-lookup"><span data-stu-id="88f4a-111">Under **Software Restriction Policy**, select the **Apply software restriction policy** check box; this enables you to set the trust level.</span></span> <span data-ttu-id="88f4a-112">清除此核取方塊會導致 COM + 針對應用程式使用軟體限制原則的全系統設定。</span><span class="sxs-lookup"><span data-stu-id="88f4a-112">Clearing the check box will cause COM+ to use the systemwide configuration of the software restriction policy for the application.</span></span> <span data-ttu-id="88f4a-113">這個核取方塊會對應到 [**應用程式**](applications.md) 集合的 SRPEnabled 屬性。</span><span class="sxs-lookup"><span data-stu-id="88f4a-113">This check box corresponds to the SRPEnabled property of the [**Applications**](applications.md) collection.</span></span>

4.  <span data-ttu-id="88f4a-114">在 [ **限制等級** ] 方塊中，選取適當的層級。</span><span class="sxs-lookup"><span data-stu-id="88f4a-114">In the **Restriction Level** box, select the appropriate level.</span></span> <span data-ttu-id="88f4a-115">這個下拉式清單方塊對應至 [**應用程式**](applications.md) 集合的 SRPTrustLevel 屬性。</span><span class="sxs-lookup"><span data-stu-id="88f4a-115">This drop-down box corresponds to the SRPTrustLevel property of the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="88f4a-116">層級如下所示，從最高到最受信任的順序：</span><span class="sxs-lookup"><span data-stu-id="88f4a-116">The levels are as follows, ordered from least to most trusted:</span></span>

    -   <span data-ttu-id="88f4a-117">不 **允許**。</span><span class="sxs-lookup"><span data-stu-id="88f4a-117">**Disallowed**.</span></span> <span data-ttu-id="88f4a-118">不允許應用程式使用使用者的完整許可權。</span><span class="sxs-lookup"><span data-stu-id="88f4a-118">The application is disallowed from using the full privileges of the user.</span></span> <span data-ttu-id="88f4a-119">具有任何信任層級的元件可以載入到其中。</span><span class="sxs-lookup"><span data-stu-id="88f4a-119">Components with any trust level can be loaded into it.</span></span>
    -   <span data-ttu-id="88f4a-120">不 **受限制**。</span><span class="sxs-lookup"><span data-stu-id="88f4a-120">**Unrestricted**.</span></span> <span data-ttu-id="88f4a-121">應用程式可不受限制地存取使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="88f4a-121">The application has unrestricted access to the user's privileges.</span></span> <span data-ttu-id="88f4a-122">只有具有不受限制之信任層級的元件可以載入到其中。</span><span class="sxs-lookup"><span data-stu-id="88f4a-122">Only components with an Unrestricted trust level can be loaded into it.</span></span>

5.  <span data-ttu-id="88f4a-123">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="88f4a-123">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88f4a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="88f4a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f4a-125">設定 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="88f4a-125">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="88f4a-126">啟用程式庫應用程式的驗證</span><span class="sxs-lookup"><span data-stu-id="88f4a-126">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="88f4a-127">設定伺服器應用程式的驗證層級</span><span class="sxs-lookup"><span data-stu-id="88f4a-127">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[<span data-ttu-id="88f4a-128">設定模擬等級</span><span class="sxs-lookup"><span data-stu-id="88f4a-128">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



