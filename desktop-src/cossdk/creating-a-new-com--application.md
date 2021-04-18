---
description: 建立新的 COM + 應用程式
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: 建立新的 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971330"
---
# <a name="creating-a-new-com-application"></a><span data-ttu-id="88f76-103">建立新的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="88f76-103">Creating a New COM+ Application</span></span>

<span data-ttu-id="88f76-104">建立新的 COM + 應用程式需要兩個基本步驟，如下所示：</span><span class="sxs-lookup"><span data-stu-id="88f76-104">Creating a new COM+ application requires two basic steps, as follows:</span></span>

-   <span data-ttu-id="88f76-105">建立空的 COM + 應用程式 (如下) 所述。</span><span class="sxs-lookup"><span data-stu-id="88f76-105">Creating an empty COM+ application (described below).</span></span>
-   <span data-ttu-id="88f76-106">將元件新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="88f76-106">Adding components to the application.</span></span> <span data-ttu-id="88f76-107"> (參閱 [安裝新元件](installing-new-components.md) 和匯 [入元件](importing-components.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="88f76-107">(See [Installing New Components](installing-new-components.md) and [Importing Components](importing-components.md).)</span></span>

<span data-ttu-id="88f76-108">**若要建立空白的 COM + 應用程式**</span><span class="sxs-lookup"><span data-stu-id="88f76-108">**To create an empty COM+ application**</span></span>

1.  <span data-ttu-id="88f76-109">在 [元件服務] 系統管理工具的主控台樹中，選取您要建立應用程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="88f76-109">In the console tree of the Component Services administrative tool, select the computer on which you want to create an application.</span></span>

2.  <span data-ttu-id="88f76-110">選取該電腦的 [ **Com + 應用程式** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="88f76-110">Select the **COM+ Applications** folder for that computer.</span></span>

3.  <span data-ttu-id="88f76-111">在 [ **動作** ] 功能表上，指向 [ **新增**]，然後按一下 [ **應用程式**]。</span><span class="sxs-lookup"><span data-stu-id="88f76-111">On the **Action** menu, point to **New**, and then click **Application**.</span></span> <span data-ttu-id="88f76-112">您也可以在 [ **Com + 應用程式** ] 資料夾上按一下滑鼠右鍵，指向 [ **新增**]，然後按一下 [ **應用程式**]。</span><span class="sxs-lookup"><span data-stu-id="88f76-112">You can also right-click the **COM+ Applications** folder, point to **New**, and then click **Application**.</span></span>

4.  <span data-ttu-id="88f76-113">在 [COM + 應用程式安裝精靈] 的 [ **歡迎使用** ] 頁面上，按 [ **下一步**]，然後在 [ **安裝或建立新應用程式** ] 對話方塊中，按一下 [ **建立空的應用程式**]。</span><span class="sxs-lookup"><span data-stu-id="88f76-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Install or Create a New Application** dialog box, click **Create an empty application**.</span></span>

5.  <span data-ttu-id="88f76-114">在提供的方塊中，輸入新應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="88f76-114">In the box provided, type a name for the new application.</span></span> <span data-ttu-id="88f76-115"> (請注意，下列特殊字元不能用在應用程式名稱中： \\ 、/、~、！、@、 \# 、%、^、&、 \* 、 (、) 、 \| 、}、{、、、、、、 \] \[ >、<、、？、：和;。) [ **啟用類型**] 下，按一下 [連結 **庫應用程式** 或 **伺服器應用程式**]。</span><span class="sxs-lookup"><span data-stu-id="88f76-115">(Note that the following special characters cannot be used in an application name: \\, /, ~, !, @, \#, %, ^, &, \*, (, ), \|, }, {, \], \[, ', ", >, <, ., ?, :, and ;.) Under **Activation type**, click **Library application** or **Server application**.</span></span> <span data-ttu-id="88f76-116">按一下 [下一步] 。</span><span class="sxs-lookup"><span data-stu-id="88f76-116">Click **Next**.</span></span>

    > [!Note]  
    > <span data-ttu-id="88f76-117">伺服器應用程式會在自己的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="88f76-117">A server application runs in its own process.</span></span> <span data-ttu-id="88f76-118">伺服器應用程式可支援所有 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="88f76-118">Server applications can support all COM+ services.</span></span> <span data-ttu-id="88f76-119">程式庫應用程式會在建立它的用戶端的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="88f76-119">A library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="88f76-120">程式庫應用程式可以使用以角色為基礎的安全性，但不支援遠端存取或已排入佇列的元件。</span><span class="sxs-lookup"><span data-stu-id="88f76-120">Library applications can use role-based security but do not support remote access or queued components.</span></span>

     

6.  <span data-ttu-id="88f76-121">在 [ **設定應用程式識別碼** ] 對話方塊中，選擇將執行應用程式的身分識別。</span><span class="sxs-lookup"><span data-stu-id="88f76-121">In the **Set Application Identity** dialog box, choose an identity under which the application will run.</span></span> <span data-ttu-id="88f76-122">如果您選取 [ **此使用者**]，請輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="88f76-122">If you select **This user**, type the user name and password.</span></span> <span data-ttu-id="88f76-123">您也必須在 [ **確認密碼** ] 方塊中重新輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="88f76-123">You must also retype the password in the **Confirm password** box.</span></span> <span data-ttu-id="88f76-124">按一下 [下一步] 。</span><span class="sxs-lookup"><span data-stu-id="88f76-124">Click **Next**.</span></span> <span data-ttu-id="88f76-125"> ([應用程式識別] 的預設選項為 [ **互動式使用者**]。</span><span class="sxs-lookup"><span data-stu-id="88f76-125">(The default selection for application identity is **Interactive User**.</span></span> <span data-ttu-id="88f76-126">互動式使用者在任何指定時間都是登入伺服器電腦的使用者。</span><span class="sxs-lookup"><span data-stu-id="88f76-126">The interactive user is the user logged on to the server computer at any given time.</span></span> <span data-ttu-id="88f76-127">您可以選取 [使用者]，然後輸入特定的使用者或 **群組，以** 選取不同的使用者。 ) </span><span class="sxs-lookup"><span data-stu-id="88f76-127">You can select a different user by selecting **This user** and entering a specific user or group.)</span></span>

    > [!Note]  
    > <span data-ttu-id="88f76-128">只有當您在 [COM 應用程式安裝精靈] 的先前對話方塊中，為新應用程式的啟用類型選取 [**伺服器應用程式**] 時，才會顯示 [**設定應用程式識別**] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="88f76-128">The **Set Application Identity** dialog box appears only if you selected **Server application** for the new application's activation type in the COM Application Install Wizard's preceding dialog box.</span></span> <span data-ttu-id="88f76-129">識別屬性不會用於程式庫應用程式。</span><span class="sxs-lookup"><span data-stu-id="88f76-129">The identity property is not used for library applications.</span></span>

     

7.  <span data-ttu-id="88f76-130">在 [ **新增應用程式角色** ] 對話方塊中，新增您想要與應用程式建立關聯的任何角色。</span><span class="sxs-lookup"><span data-stu-id="88f76-130">In the **Add Application Roles** dialog box, add any roles you want to associate with the application.</span></span> <span data-ttu-id="88f76-131">依預設，只會定義 **CreatorOwner** 角色。</span><span class="sxs-lookup"><span data-stu-id="88f76-131">By default, only the **CreatorOwner** role is defined.</span></span> <span data-ttu-id="88f76-132">如需角色的詳細資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="88f76-132">For information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

8.  <span data-ttu-id="88f76-133">在 [ **將使用者新增至角色** ] 對話方塊中，將您在上一個步驟中建立的每個角色填入至您要授與該角色相關聯之許可權的使用者、群組或內建安全性主體。</span><span class="sxs-lookup"><span data-stu-id="88f76-133">In the **Add Users to Roles** dialog box, populate each role you created in the last step with the users, groups, or built-in security principals to which you want to grant the privileges associated with that role.</span></span> <span data-ttu-id="88f76-134">根據預設，互動式使用者會置於 **CreatorOwner** 角色中。</span><span class="sxs-lookup"><span data-stu-id="88f76-134">By default, the interactive user is placed in the **CreatorOwner** role.</span></span>

9.  <span data-ttu-id="88f76-135">按一下 [完成] 。</span><span class="sxs-lookup"><span data-stu-id="88f76-135">Click **Finish**.</span></span>

<span data-ttu-id="88f76-136">新的應用程式現在會顯示在 [元件服務] 系統管理工具的主控台樹的 [ **Com + 應用程式** ] 資料夾底下。</span><span class="sxs-lookup"><span data-stu-id="88f76-136">The new application will now be displayed under the **COM+ Applications** folder in the console tree of the Component Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="88f76-137">從 Windows Server 2003，建立 COM + 應用程式時，預設會啟用存取檢查。</span><span class="sxs-lookup"><span data-stu-id="88f76-137">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="88f76-138">在先前的版本中，在應用層級依預設會停用存取檢查。</span><span class="sxs-lookup"><span data-stu-id="88f76-138">In previous versions, access checks were disabled by default at the application level.</span></span> <span data-ttu-id="88f76-139">結果是，根據預設，只有在與應用程式相關聯之角色中的使用者，才能夠存取 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="88f76-139">The result is that by default, access to a COM+ application is allowed only to users that are in the roles associated with the application.</span></span> <span data-ttu-id="88f76-140"> (查看以 [角色為基礎的安全性管理](role-based-security-administration.md)。 ) 或者，您也可以停用 com + 應用程式的存取檢查，以允許存取所有使用者。</span><span class="sxs-lookup"><span data-stu-id="88f76-140">(See [Role-Based Security Administration](role-based-security-administration.md).) Alternatively, you can allow access to all users by disabling access checks on a COM+ application.</span></span> <span data-ttu-id="88f76-141"> (參閱 [啟用應用程式的存取檢查](enabling-access-checks-for-an-application.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="88f76-141">(See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md).)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="88f76-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="88f76-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f76-143">複製元件</span><span class="sxs-lookup"><span data-stu-id="88f76-143">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="88f76-144">刪除 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="88f76-144">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="88f76-145">匯入元件</span><span class="sxs-lookup"><span data-stu-id="88f76-145">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="88f76-146">安裝新元件</span><span class="sxs-lookup"><span data-stu-id="88f76-146">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="88f76-147">移動元件</span><span class="sxs-lookup"><span data-stu-id="88f76-147">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="88f76-148">從 COM + 應用程式移除元件</span><span class="sxs-lookup"><span data-stu-id="88f76-148">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



