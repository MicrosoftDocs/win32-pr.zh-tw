---
title: 使用 DCOMCNFG 設定 Process-Wide 安全性
description: 如果應用程式的安全性需求與電腦上其他應用程式所需的安全性需求不同，您可能會想要啟用特定應用程式的安全性。
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03174dd66e83a88724ff5d421d7b0dcb0c17699e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311613"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a><span data-ttu-id="aae74-103">使用 DCOMCNFG 設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="aae74-103">Setting Process-Wide Security Using DCOMCNFG</span></span>

<span data-ttu-id="aae74-104">如果應用程式的安全性需求與電腦上其他應用程式所需的安全性需求不同，您可能會想要啟用特定應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="aae74-104">You might want to enable security for a particular application if an application has security needs that are different from those required by other applications on the computer.</span></span> <span data-ttu-id="aae74-105">比方說，您可能會決定針對需要低層級安全性的應用程式使用全系統設定，同時為特定應用程式設定更高層級的安全性。</span><span class="sxs-lookup"><span data-stu-id="aae74-105">For instance, you might decide to use system-wide settings for your applications that require a low level of security while setting a higher level of security for a particular application.</span></span>

<span data-ttu-id="aae74-106">不過，有時不會使用登錄中套用至特定應用程式的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="aae74-106">However, security settings in the registry that apply to a particular application are sometimes not used.</span></span> <span data-ttu-id="aae74-107">例如，如果用戶端呼叫 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) 來設定特定介面 proxy 的安全性，則會覆寫您在登錄中使用 Dcomcnfg.exe 設定的整個進程設定。</span><span class="sxs-lookup"><span data-stu-id="aae74-107">For example, the process-wide settings that you set in the registry using Dcomcnfg.exe will be overridden if a client calls [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) to set security for a particular interface proxy.</span></span> <span data-ttu-id="aae74-108">同樣地，如果用戶端或伺服器 (或兩個) 呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定處理常式的安全性，則會忽略登錄中的設定，而會改用指定給 **CoInitializeSecurity** 的參數。</span><span class="sxs-lookup"><span data-stu-id="aae74-108">Similarly, if a client or server (or both) call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to set security for a process, the settings in the registry will be ignored and the parameters specified to **CoInitializeSecurity** will be used instead.</span></span>

<span data-ttu-id="aae74-109">啟用應用程式的安全性時，可能需要修改數個設定。</span><span class="sxs-lookup"><span data-stu-id="aae74-109">When enabling security for an application, several settings may need to be modified.</span></span> <span data-ttu-id="aae74-110">這些包括驗證層級、位置、啟動許可權、存取權限和身分識別。</span><span class="sxs-lookup"><span data-stu-id="aae74-110">These include authentication level, location, launch permissions, access permissions, and identity.</span></span> <span data-ttu-id="aae74-111">如需逐步程式，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="aae74-111">For step-by-step procedures, see the following:</span></span>

-   [<span data-ttu-id="aae74-112">設定應用程式的驗證層級</span><span class="sxs-lookup"><span data-stu-id="aae74-112">Setting the Authentication Level for an Application</span></span>](#setting-the-authentication-level-for-an-application)
-   [<span data-ttu-id="aae74-113">設定應用程式的位置</span><span class="sxs-lookup"><span data-stu-id="aae74-113">Setting the Location for an Application</span></span>](#setting-the-location-for-an-application)
-   [<span data-ttu-id="aae74-114">設定應用程式的啟動許可權</span><span class="sxs-lookup"><span data-stu-id="aae74-114">Setting Launch Permissions for an Application</span></span>](#setting-launch-permissions-for-an-application)
-   [<span data-ttu-id="aae74-115">設定應用程式的存取權限</span><span class="sxs-lookup"><span data-stu-id="aae74-115">Setting Access Permissions for an Application</span></span>](#setting-access-permissions-for-an-application)
-   [<span data-ttu-id="aae74-116">設定應用程式的身分識別</span><span class="sxs-lookup"><span data-stu-id="aae74-116">Setting the Identity for an Application</span></span>](#setting-the-identity-for-an-application)
-   [<span data-ttu-id="aae74-117">流覽使用者資料庫</span><span class="sxs-lookup"><span data-stu-id="aae74-117">Browsing the User Database</span></span>](#browsing-the-user-database)
-   [<span data-ttu-id="aae74-118">Dcomcnfg.exe 和64位應用程式</span><span class="sxs-lookup"><span data-stu-id="aae74-118">Dcomcnfg.exe and 64-bit Applications</span></span>](#dcomcnfgexe-and-64-bit-applications)
-   [<span data-ttu-id="aae74-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="aae74-119">Related topics</span></span>](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a><span data-ttu-id="aae74-120">設定應用程式的驗證層級</span><span class="sxs-lookup"><span data-stu-id="aae74-120">Setting the Authentication Level for an Application</span></span>

<span data-ttu-id="aae74-121">若要啟用應用程式的安全性，您必須設定 [無] 以外的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="aae74-121">To enable security for an application, you must set an authentication level other than None.</span></span> <span data-ttu-id="aae74-122">驗證層級會告知 COM 需要多少驗證保護，而且其範圍從驗證用戶端的第一個方法呼叫，到完全加密參數狀態。</span><span class="sxs-lookup"><span data-stu-id="aae74-122">The authentication level tells COM how much authentication protection is required, and it can range from authenticating the client at the first method call to encrypting parameter states fully.</span></span>

<span data-ttu-id="aae74-123">**若要設定應用程式的驗證層級**</span><span class="sxs-lookup"><span data-stu-id="aae74-123">**To set an application's authentication level**</span></span>

1.  <span data-ttu-id="aae74-124">在 Dcomcnfg.exe 的 [ **應用程式** ] 屬性頁上，選取應用程式，然後按一下 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="aae74-124">On the **Applications** property page in Dcomcnfg.exe, select the application and click the **Properties** button (or double-click the selected application).</span></span>

2.  <span data-ttu-id="aae74-125">在 [**一般**] 頁面上，從 [**驗證等級**] 清單方塊中選取 [**無 ()** 以外的驗證等級。</span><span class="sxs-lookup"><span data-stu-id="aae74-125">On the **General** page, select an authentication level other than **(None)** from the **Authentication Level** list box.</span></span>

3.  <span data-ttu-id="aae74-126">如果您將設定此應用程式的其他屬性，請選擇 [套用 **] 按鈕以** 套用新的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="aae74-126">If you will be setting other properties for this application, choose the **Apply** button to apply the new authentication level.</span></span> <span data-ttu-id="aae74-127">如果您已完成設定此應用程式的屬性，而且您想要套用變更，請按一下 **[確定]** 。</span><span class="sxs-lookup"><span data-stu-id="aae74-127">Click **OK** if you are finished setting properties for this application and you wish to apply the changes.</span></span>

## <a name="setting-the-location-for-an-application"></a><span data-ttu-id="aae74-128">設定應用程式的位置</span><span class="sxs-lookup"><span data-stu-id="aae74-128">Setting the Location for an Application</span></span>

<span data-ttu-id="aae74-129">您為應用程式設定的位置會決定應用程式將執行的電腦。</span><span class="sxs-lookup"><span data-stu-id="aae74-129">The location you set for your application determines the computer on which the application will run.</span></span> <span data-ttu-id="aae74-130">您可以選擇在資料所在的電腦、用來設定位置的電腦，或指定的電腦上執行您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="aae74-130">You can choose to run your application on the computer where the data is located, on the computer you use to set the location, or on a specified computer.</span></span>

<span data-ttu-id="aae74-131">**若要設定應用程式的位置**</span><span class="sxs-lookup"><span data-stu-id="aae74-131">**To set an application's location**</span></span>

1.  <span data-ttu-id="aae74-132">當 Dcomcnfg.exe 執行時，請從 [ **應用程式** ] 頁面中選取應用程式，並選擇 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="aae74-132">With Dcomcnfg.exe running, select the application from the **Applications** page and choose the **Properties** button (or double-click the selected application).</span></span>

2.  <span data-ttu-id="aae74-133">在 [ **位置** ] 頁面上，選取一或多個對應至您要執行應用程式之位置的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="aae74-133">On the **Location** page, select one or more check boxes that correspond to locations where you want the application to run.</span></span> <span data-ttu-id="aae74-134">如果您選取一個以上的核取方塊，COM 會使用第一個套用的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="aae74-134">If you select more than one check box, COM uses the first one that applies.</span></span> <span data-ttu-id="aae74-135">如果 Dcomcnfg.exe 在伺服器電腦上執行，請一律選取 [ **在這部電腦上執行應用程式**]。</span><span class="sxs-lookup"><span data-stu-id="aae74-135">If Dcomcnfg.exe is being run on the server computer, always select **Run Application On This Computer**.</span></span>

3.  <span data-ttu-id="aae74-136">如果您將設定此應用程式的其他屬性，請選擇 [套用 **] 按鈕以** 套用新的位置。</span><span class="sxs-lookup"><span data-stu-id="aae74-136">If you will be setting other properties for this application, choose the **Apply** button to apply the new location.</span></span> <span data-ttu-id="aae74-137">如果您已完成設定此應用程式的屬性，而且您想要套用變更，請選擇 **[確定]** 。</span><span class="sxs-lookup"><span data-stu-id="aae74-137">Choose **OK** if you are finished setting properties for this application and you wish to apply the changes.</span></span>

## <a name="setting-launch-permissions-for-an-application"></a><span data-ttu-id="aae74-138">設定應用程式的啟動許可權</span><span class="sxs-lookup"><span data-stu-id="aae74-138">Setting Launch Permissions for an Application</span></span>

<span data-ttu-id="aae74-139">您可以使用 Dcomcnfg.exe 設定啟動許可權，以控制被授與或拒絕啟動特定伺服器之許可權的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="aae74-139">With Dcomcnfg.exe, you can set launch permissions to control the list of users who are granted or denied permission to launch a particular server.</span></span> <span data-ttu-id="aae74-140">您可以將使用者或群組新增至清單，以指定是否要授與或拒絕存取權限。</span><span class="sxs-lookup"><span data-stu-id="aae74-140">You can add users or groups to the list, specifying whether access permission is being granted or denied.</span></span> <span data-ttu-id="aae74-141">您也可以從清單中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="aae74-141">You can also remove users from the list.</span></span>

<span data-ttu-id="aae74-142">**若要設定應用程式的啟動許可權**</span><span class="sxs-lookup"><span data-stu-id="aae74-142">**To set launch permissions for an application**</span></span>

1.  <span data-ttu-id="aae74-143">當 Dcomcnfg.exe 執行時，請從 [ **應用程式** ] 頁面中選取應用程式，並選擇 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="aae74-143">With Dcomcnfg.exe running, select the application from the **Applications** page and choose the **Properties** button (or double-click the selected application).</span></span>

2.  <span data-ttu-id="aae74-144">在 [ **安全性** ] 屬性頁上，選取 [ **使用自訂啟動許可權** ] 選項按鈕，然後選擇相同區域中的 [ **編輯** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-144">On the **Security** property page, select the **Use custom launch permissions** option button and choose the **Edit** button in the same area.</span></span>

3.  <span data-ttu-id="aae74-145">若要移除使用者或群組，請選取您要移除的使用者或群組，然後選擇 [ **移除** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-145">To remove users or groups, select the user or group you want to remove and choose the **Remove** button.</span></span> <span data-ttu-id="aae74-146">選取的使用者或群組將不會再出現在清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="aae74-146">The selected user or group will no longer appear in the list box.</span></span> <span data-ttu-id="aae74-147">當您完成移除使用者和群組時，請選擇 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="aae74-147">When you have finished removing user and groups, choose **OK**.</span></span>

4.  <span data-ttu-id="aae74-148">如果您想要新增使用者或群組，請選擇 [ **加入** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-148">If you want to add users or groups, choose the **Add** button.</span></span>

5.  <span data-ttu-id="aae74-149">如果您知道想要新增的完整使用者名稱，請在 [ **加入名稱** ] 文字方塊中輸入。</span><span class="sxs-lookup"><span data-stu-id="aae74-149">If you know the fully qualified user name you want to add, type it in the **Add Names** text box.</span></span> <span data-ttu-id="aae74-150">如果您不知道使用者名稱，您可以流覽使用者資料庫來尋找它 (請參閱下方的流覽使用者資料庫) 。</span><span class="sxs-lookup"><span data-stu-id="aae74-150">If you do not know the user name, you can browse the user database to find it (see Browsing the User Database below).</span></span> <span data-ttu-id="aae74-151">當您找到使用者名稱時，請從 [ **名稱** ] 清單方塊中選取使用者或群組，然後選擇 [ **加入** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-151">When you have located the user name, select the user or group from the **Names** list box and choose the **Add** button.</span></span>

6.  <span data-ttu-id="aae74-152">在 [ **存取類型** ] 清單方塊中，選取 [ **允許啟動** 或 **拒絕啟動**)  (的存取類型。</span><span class="sxs-lookup"><span data-stu-id="aae74-152">From the **Type of Access** list box, select the access type (either **Allow Launch** or **Deny Launch**).</span></span> <span data-ttu-id="aae74-153">若要加入將擁有所選存取類型的其他使用者，請重複步驟5。</span><span class="sxs-lookup"><span data-stu-id="aae74-153">To add other users that will have the selected type of access, repeat step 5.</span></span> <span data-ttu-id="aae74-154">當您完成新增所選存取類型的使用者時，請選擇 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-154">When you have finished adding users for the selected access type, choose the **OK** button.</span></span>

7.  <span data-ttu-id="aae74-155">若要加入將擁有不同類型存取權的使用者，請重複步驟5和6。</span><span class="sxs-lookup"><span data-stu-id="aae74-155">To add users that will have a different type of access, repeat steps 5 and 6.</span></span> <span data-ttu-id="aae74-156">否則，請選擇 **[確定]** 以套用變更。</span><span class="sxs-lookup"><span data-stu-id="aae74-156">Otherwise, choose **OK** to apply the changes.</span></span>

## <a name="setting-access-permissions-for-an-application"></a><span data-ttu-id="aae74-157">設定應用程式的存取權限</span><span class="sxs-lookup"><span data-stu-id="aae74-157">Setting Access Permissions for an Application</span></span>

<span data-ttu-id="aae74-158">使用 Dcomcnfg.exe，您可以藉由設定存取權限，來管理被授與或拒絕存取特定伺服器之方法的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="aae74-158">With Dcomcnfg.exe, you can manage the list of users who are granted or denied access to the methods of a particular server by setting access permissions.</span></span> <span data-ttu-id="aae74-159">您可以將使用者或群組新增至清單，以指定是否要授與或拒絕存取權限。</span><span class="sxs-lookup"><span data-stu-id="aae74-159">You can add users or groups to the list, specifying whether access permission is being granted or denied.</span></span> <span data-ttu-id="aae74-160">您也可以從清單中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="aae74-160">You can also remove users from the list.</span></span>

<span data-ttu-id="aae74-161">設定存取權限時，您必須確定系統已包含在被授與存取權的使用者清單中。</span><span class="sxs-lookup"><span data-stu-id="aae74-161">When setting access permissions, you must ensure that SYSTEM is included in the list of users that are granted access.</span></span> <span data-ttu-id="aae74-162">如果您已將存取權限授與所有人，系統會隱含地包含。</span><span class="sxs-lookup"><span data-stu-id="aae74-162">If you have granted access permissions to Everyone, SYSTEM is included implicitly.</span></span>

<span data-ttu-id="aae74-163">設定應用程式存取權限的程式與設定啟動許可權類似。</span><span class="sxs-lookup"><span data-stu-id="aae74-163">The process of setting access permissions for an application is similar to setting launch permissions.</span></span> <span data-ttu-id="aae74-164">步驟如下所示。</span><span class="sxs-lookup"><span data-stu-id="aae74-164">The steps are as follows.</span></span>

<span data-ttu-id="aae74-165">**若要設定應用程式的存取權限**</span><span class="sxs-lookup"><span data-stu-id="aae74-165">**To set access permissions for an application**</span></span>

1.  <span data-ttu-id="aae74-166">當 Dcomcnfg.exe 執行時，請從 [ **應用程式** ] 頁面中選取應用程式，並選擇 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="aae74-166">With Dcomcnfg.exe running, select the application from the **Applications** page and choose the **Properties** button (or double-click the selected application).</span></span>

2.  <span data-ttu-id="aae74-167">在 [ **安全性** ] 屬性頁上，選取 [ **使用自訂存取權限** ] 選項按鈕，然後選擇相同區域中的 [ **編輯** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-167">On the **Security** property page, select the **Use custom access permissions** option button and choose the **Edit** button in the same area.</span></span>

3.  <span data-ttu-id="aae74-168">若要移除使用者或群組，請選取您要移除的使用者或群組，然後選擇 [ **移除** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-168">To remove users or groups, select the user or group you want to remove and choose the **Remove** button.</span></span> <span data-ttu-id="aae74-169">選取的使用者或群組將不會再出現在清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="aae74-169">The selected user or group will no longer appear in the list box.</span></span> <span data-ttu-id="aae74-170">當您完成移除使用者和群組時，請選擇 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="aae74-170">When you have finished removing user and groups, choose **OK**.</span></span>

4.  <span data-ttu-id="aae74-171">如果您想要新增使用者或群組，請選擇 [ **加入** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-171">If you want to add a user or a group, choose the **Add** button.</span></span>

5.  <span data-ttu-id="aae74-172">如果您知道想要新增的完整使用者名稱，請在 [ **加入名稱** ] 文字方塊中輸入。</span><span class="sxs-lookup"><span data-stu-id="aae74-172">If you know the fully qualified user name you want to add, type it in the **Add Names** text box.</span></span> <span data-ttu-id="aae74-173">如果您不知道使用者名稱，您可以流覽使用者資料庫來尋找它。</span><span class="sxs-lookup"><span data-stu-id="aae74-173">If you do not know the user name, you can browse the user database to find it.</span></span> <span data-ttu-id="aae74-174">當您找到使用者名稱時，請從 [ **名稱** ] 清單方塊中選取使用者或群組，然後選擇 [ **加入** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-174">When you have located the user name, select the user or group from the **Names** list box and choose the **Add** button.</span></span>

6.  <span data-ttu-id="aae74-175">在 [ **存取類型** ] 清單方塊中，選取 [ **允許存取** ] 或 [ **拒絕存取** ])  (存取類型。</span><span class="sxs-lookup"><span data-stu-id="aae74-175">From the **Type of Access** list box, select the access type (either **Allow Access** or **Deny Access**).</span></span> <span data-ttu-id="aae74-176">若要加入將擁有所選存取類型的其他使用者，請重複步驟5。</span><span class="sxs-lookup"><span data-stu-id="aae74-176">To add other users that will have the selected type of access, repeat step 5.</span></span> <span data-ttu-id="aae74-177">當您完成新增所選存取類型的使用者時，請選擇 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-177">When you have finished adding users for the selected access type, choose the **OK** button.</span></span>

7.  <span data-ttu-id="aae74-178">若要加入將擁有不同類型存取權的使用者，請重複步驟5和6。</span><span class="sxs-lookup"><span data-stu-id="aae74-178">To add users that will have a different type of access, repeat steps 5 and 6.</span></span> <span data-ttu-id="aae74-179">否則，請選擇 **[確定]** 以套用變更。</span><span class="sxs-lookup"><span data-stu-id="aae74-179">Otherwise, choose **OK** to apply the changes.</span></span>

## <a name="setting-the-identity-for-an-application"></a><span data-ttu-id="aae74-180">設定應用程式的身分識別</span><span class="sxs-lookup"><span data-stu-id="aae74-180">Setting the Identity for an Application</span></span>

<span data-ttu-id="aae74-181">應用程式的身分識別是用來執行應用程式的帳戶。</span><span class="sxs-lookup"><span data-stu-id="aae74-181">An application's identity is the account that is used to run the application.</span></span> <span data-ttu-id="aae74-182">身分識別可以是目前登入 (互動式使用者) 的使用者、啟動伺服器之用戶端進程的使用者帳戶、指定的使用者或服務。</span><span class="sxs-lookup"><span data-stu-id="aae74-182">The identity can be that of the user that is currently logged on (the interactive user), the user account of the client process that launched the server, a specified user, or a service.</span></span> <span data-ttu-id="aae74-183">您可以使用 Dcomcnfg.exe 來選擇應用程式的其中一個身分識別。</span><span class="sxs-lookup"><span data-stu-id="aae74-183">You can use Dcomcnfg.exe to choose one of these identities for the application.</span></span> <span data-ttu-id="aae74-184">如需決定要為應用程式設定之身分識別的說明，請參閱 [應用程式識別](application-identity.md)。</span><span class="sxs-lookup"><span data-stu-id="aae74-184">For help with deciding which identity to set for your application, see [Application Identity](application-identity.md).</span></span>

<span data-ttu-id="aae74-185">**設定應用程式的身分識別**</span><span class="sxs-lookup"><span data-stu-id="aae74-185">**To set identity for an application**</span></span>

1.  <span data-ttu-id="aae74-186">當 Dcomcnfg.exe 執行時，請從 [ **應用程式** ] 頁面中選取應用程式，並選擇 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="aae74-186">With Dcomcnfg.exe running, select the application from the **Applications** page and choose the **Properties** button (or double-click the selected application).</span></span>

2.  <span data-ttu-id="aae74-187">在 [身分 **識別** ] 屬性頁上，選取您要的身分識別的選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-187">On the **Identity** property page, select the option button for the identity you want.</span></span> <span data-ttu-id="aae74-188">如果您選擇 **此使用者**，您必須輸入使用者名稱、密碼和確認的密碼。</span><span class="sxs-lookup"><span data-stu-id="aae74-188">If you choose **This User**, you must type in the user name, the password, and the confirmed password.</span></span>

3.  <span data-ttu-id="aae74-189">如果您將設定此應用程式的其他屬性，請選擇 [套用 **] 按鈕以** 套用新的身分識別。</span><span class="sxs-lookup"><span data-stu-id="aae74-189">If you will be setting other properties for this application, choose the **Apply** button to apply the new identity.</span></span> <span data-ttu-id="aae74-190">如果您已完成設定此應用程式的屬性，而且您想要套用變更，請選擇 **[確定]** 。</span><span class="sxs-lookup"><span data-stu-id="aae74-190">Choose **OK** if you are finished setting properties for this application and you wish to apply the changes.</span></span>

## <a name="browsing-the-user-database"></a><span data-ttu-id="aae74-191">流覽使用者資料庫</span><span class="sxs-lookup"><span data-stu-id="aae74-191">Browsing the User Database</span></span>

<span data-ttu-id="aae74-192">當您需要尋找特定使用者的完整使用者名稱時，請流覽 Dcomcnfg.exe 中的使用者資料庫。</span><span class="sxs-lookup"><span data-stu-id="aae74-192">You would browse the user database in Dcomcnfg.exe when you need to find the fully qualified user name for a particular user.</span></span> <span data-ttu-id="aae74-193">例如，您可以流覽使用者資料庫，找出您想要新增以取得存取權或啟動許可權的使用者。</span><span class="sxs-lookup"><span data-stu-id="aae74-193">For instance, you can browse the user database to locate a user that you want to add for access or launch permissions.</span></span>

<span data-ttu-id="aae74-194">**流覽使用者資料庫**</span><span class="sxs-lookup"><span data-stu-id="aae74-194">**To browse the user database**</span></span>

1.  <span data-ttu-id="aae74-195">在 [ **清單名稱來源** ] 清單方塊中，選取包含您要新增之使用者或群組的網域。</span><span class="sxs-lookup"><span data-stu-id="aae74-195">In the **List Names From** list box, select the domain containing the user or group you want to add.</span></span>

2.  <span data-ttu-id="aae74-196">若要查看屬於所選網域的使用者，請選擇 [ **顯示使用者** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-196">To see the users that belong to the selected domain, choose the **Show Users** button.</span></span>

3.  <span data-ttu-id="aae74-197">若要查看特定群組的成員，請在 [ **名稱** ] 清單方塊中選取群組，然後選擇 [ **顯示成員** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-197">To see the members of a particular group, select the group in the **Names** list box and choose the **Show Members** button.</span></span>

4.  <span data-ttu-id="aae74-198">如果您找不到想要新增的使用者或群組，請選擇 [ **搜尋** ] 按鈕，這會顯示 [ **尋找帳戶** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aae74-198">If you cannot locate the user or group you want to add, choose the **Search** button, which brings up the **Find Account** dialog box.</span></span> <span data-ttu-id="aae74-199">選取您要搜尋的網域 (或選取 [ **搜尋所有**) ]，輸入您想要尋找的使用者名稱，然後選擇 [ **搜尋** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="aae74-199">Select the domain you want to search (or select **Search All**), type the user name you want to look for, and choose the **Search** button.</span></span>

## <a name="dcomcnfgexe-and-64-bit-applications"></a><span data-ttu-id="aae74-200">Dcomcnfg.exe 和64位應用程式</span><span class="sxs-lookup"><span data-stu-id="aae74-200">Dcomcnfg.exe and 64-bit Applications</span></span>

<span data-ttu-id="aae74-201">在 x64 作業系統上，從 Windows XP 到 Windows Server 2008，64位版本的 DCOMCNFG.EXE 不會正確設定32位的 DCOM 應用程式以進行遠端啟用。</span><span class="sxs-lookup"><span data-stu-id="aae74-201">On x64 operating systems from Windows XP to Windows Server 2008, the 64-bit version of DCOMCNFG.EXE does not correctly configure 32-bit DCOM applications for remote activation.</span></span> <span data-ttu-id="aae74-202">這種行為會導致以遠端方式啟動的元件，而不是在本機啟用。</span><span class="sxs-lookup"><span data-stu-id="aae74-202">This behavior causes components that are meant to be activated remotely instead being activated locally.</span></span> <span data-ttu-id="aae74-203">在 Windows 7 和 Windows Server 2008 R2 和更新版本中不會發生此行為。</span><span class="sxs-lookup"><span data-stu-id="aae74-203">This behavior does not occur in Windows 7 and Windows Server 2008 R2 and higher versions.</span></span>

<span data-ttu-id="aae74-204">解決方法是使用32位版本的 DCOMCNFG。</span><span class="sxs-lookup"><span data-stu-id="aae74-204">The workaround is to use the 32-bit version of DCOMCNFG.</span></span> <span data-ttu-id="aae74-205">執行 mmc.exe 的32位版本，並使用下列命令列載入32位版本的元件服務嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="aae74-205">Run the 32-bit version of mmc.exe and load the 32-bit version of the Component Services snap-in by using the following command line.</span></span>

<span data-ttu-id="aae74-206">C： \\ WINDOWS \\ SysWOW64>**mmc comexp.msc services.msc/32**</span><span class="sxs-lookup"><span data-stu-id="aae74-206">C:\\WINDOWS\\SysWOW64>**mmc comexp.msc /32**</span></span>

<span data-ttu-id="aae74-207">32位版本的元件服務會正確地註冊32位的 DCOM 應用程式以進行遠端啟用。</span><span class="sxs-lookup"><span data-stu-id="aae74-207">The 32-bit version of Component Services correctly registers 32-bit DCOM applications for remote activation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aae74-208">相關主題</span><span class="sxs-lookup"><span data-stu-id="aae74-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aae74-209">設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="aae74-209">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




