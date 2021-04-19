---
description: 在元件層級啟用存取檢查
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: 在元件層級啟用存取檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991630"
---
# <a name="enabling-access-checks-at-the-component-level"></a><span data-ttu-id="8c433-103">在元件層級啟用存取檢查</span><span class="sxs-lookup"><span data-stu-id="8c433-103">Enabling Access Checks at the Component Level</span></span>

<span data-ttu-id="8c433-104">如果您的應用程式包含不需要安全性檢查的元件，您可能會決定停用該元件的角色檢查以改善效能。</span><span class="sxs-lookup"><span data-stu-id="8c433-104">If your application includes a component that does not need security checks, you might decide to disable role checks for that component to improve performance.</span></span> <span data-ttu-id="8c433-105">或者，在進行調試時，停用安全性可能會很有説明，讓您可以專注于程式功能的其他層面。</span><span class="sxs-lookup"><span data-stu-id="8c433-105">Or when debugging, it might be helpful to disable security so that you can concentrate on other aspects of program functionality.</span></span>

<span data-ttu-id="8c433-106">依預設，當您安裝元件時，會啟用元件層級的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="8c433-106">By default, when you install a component, component-level access checks are enabled.</span></span> <span data-ttu-id="8c433-107">不過，只有在啟用 [應用層級的存取檢查](enabling-access-checks-for-an-application.md) ，以及當 [安全性層級](setting-a-security-level-for-access-checks.md) 設定為 **在進程和元件層級執行存取檢查** 時，才會生效。</span><span class="sxs-lookup"><span data-stu-id="8c433-107">However, this takes effect only when [application-level access checks](enabling-access-checks-for-an-application.md) are enabled and when the [security level](setting-a-security-level-for-access-checks.md) is set to **Perform access checks at the process and component level**.</span></span>

<span data-ttu-id="8c433-108">**若要啟用或停用元件層級的存取檢查**</span><span class="sxs-lookup"><span data-stu-id="8c433-108">**To enable or disable access checks at the component level**</span></span>

1.  <span data-ttu-id="8c433-109">在 [元件服務] 系統管理工具的主控台樹中，找出包含您要停用 (或啟用) 角色檢查之元件的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c433-109">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the component for which you want to disable (or enable) role checks.</span></span> <span data-ttu-id="8c433-110">展開樹狀結構中的 [view]，以查看 [ **元件** ] 資料夾中的元件。</span><span class="sxs-lookup"><span data-stu-id="8c433-110">Expand the view in the tree to view the components in the **Components** folder.</span></span>

2.  <span data-ttu-id="8c433-111">以滑鼠右鍵按一下您要啟用角色檢查的元件，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="8c433-111">Right-click the component for which you want to enable role checks, and then click **Properties**.</span></span>

3.  <span data-ttu-id="8c433-112">在 [元件屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="8c433-112">In the component properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="8c433-113">選取 [ **強制執行元件層級存取檢查** ] 以強制執行元件層級的檢查。</span><span class="sxs-lookup"><span data-stu-id="8c433-113">Select **Enforce component level access checks** to enforce component-level checks.</span></span>

5.  <span data-ttu-id="8c433-114">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="8c433-114">Click **OK**.</span></span>

<span data-ttu-id="8c433-115">新設定將會在應用程式下次啟動時生效。</span><span class="sxs-lookup"><span data-stu-id="8c433-115">The new setting will take effect the next time the application is started.</span></span>

> [!Note]  
> <span data-ttu-id="8c433-116">從 Windows Server 2003，建立 COM + 應用程式時，預設會停用元件層級的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="8c433-116">As of Windows Server 2003, component-level access checks are disabled by default when creating a COM+ application.</span></span> <span data-ttu-id="8c433-117">預設會在應用層級啟用存取檢查，並且在元件層級預設為停用。</span><span class="sxs-lookup"><span data-stu-id="8c433-117">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="8c433-118">先前，在應用層級依預設會停用存取檢查，而且在元件層級預設為啟用。</span><span class="sxs-lookup"><span data-stu-id="8c433-118">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8c433-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c433-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c433-120">將角色指派給元件、介面或方法</span><span class="sxs-lookup"><span data-stu-id="8c433-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="8c433-121">設定 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="8c433-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="8c433-122">定義應用程式的角色</span><span class="sxs-lookup"><span data-stu-id="8c433-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="8c433-123">啟用應用程式的存取檢查</span><span class="sxs-lookup"><span data-stu-id="8c433-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="8c433-124">設定存取檢查的安全性等級</span><span class="sxs-lookup"><span data-stu-id="8c433-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



