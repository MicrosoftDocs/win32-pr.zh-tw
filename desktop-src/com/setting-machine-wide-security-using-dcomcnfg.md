---
title: 使用 DCOMCNFG 設定 System-Wide 安全性
description: 當您想讓一部電腦上的所有應用程式都未提供自己的安全性以共用相同的預設安全性設定時，您會以全系統為基礎來設定安全性。
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7feaaf356263a48c2c93eb9b3b3764b7352cd39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372404"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a><span data-ttu-id="3e04f-103">使用 DCOMCNFG 設定 System-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="3e04f-103">Setting System-Wide Security Using DCOMCNFG</span></span>

<span data-ttu-id="3e04f-104">變更全系統安全性設定會影響所有未設定整個進程安全性的 COM 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="3e04f-104">Changing the system-wide security settings will affect all COM server applications that do not set their own process-wide security.</span></span> <span data-ttu-id="3e04f-105">這可能會導致這類應用程式無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3e04f-105">This may prevent such applications from working properly.</span></span> <span data-ttu-id="3e04f-106">如果您要變更全系統安全性設定，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。</span><span class="sxs-lookup"><span data-stu-id="3e04f-106">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="3e04f-107">如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。</span><span class="sxs-lookup"><span data-stu-id="3e04f-107">For more information about setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="3e04f-108">當您想讓一部電腦上的所有應用程式都未提供自己的安全性以共用相同的預設安全性設定時，您會以全系統為基礎來設定安全性。</span><span class="sxs-lookup"><span data-stu-id="3e04f-108">When you want all of the applications on one computer that do not provide their own security to share the same default security settings, you would set security on a system-wide basis.</span></span> <span data-ttu-id="3e04f-109">使用 Dcomcnfg.exe 可讓您輕鬆地在登錄中設定適用于電腦上所有應用程式的預設值。</span><span class="sxs-lookup"><span data-stu-id="3e04f-109">Using Dcomcnfg.exe makes it easy to set default values in the registry that apply to all applications on a computer.</span></span>

<span data-ttu-id="3e04f-110">請務必瞭解，如果用戶端或伺服器明確呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定整個進程的安全性，則會忽略登錄中的預設設定，而會使用 **CoInitializeSecurity** 的參數，而不是處理常式的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="3e04f-110">It is important to understand that if the client or server explicitly calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to set process-wide security, the default settings in the registry will be ignored and the parameters to **CoInitializeSecurity** will be used instead for the security settings for the process.</span></span> <span data-ttu-id="3e04f-111">此外，如果您使用 Dcomcnfg.exe 指定特定進程的安全性設定，則會由處理常式的設定覆寫預設的電腦設定。</span><span class="sxs-lookup"><span data-stu-id="3e04f-111">Also, if you use Dcomcnfg.exe to specify security settings for a particular process, the default computer settings are overridden by the settings for the process.</span></span>

<span data-ttu-id="3e04f-112">啟用全系統安全性時，您必須將驗證等級設定為 [無] 以外的值，而且您必須設定 [啟動] 和 [存取權限]。</span><span class="sxs-lookup"><span data-stu-id="3e04f-112">When enabling system-wide security, you must set the authentication level to a value other than None and you must set launch and access permissions.</span></span> <span data-ttu-id="3e04f-113">您可以選擇設定預設模擬等級，也可以啟用參考追蹤。</span><span class="sxs-lookup"><span data-stu-id="3e04f-113">You have the option of setting the default impersonation level, and you also can enable reference tracking.</span></span> <span data-ttu-id="3e04f-114">下列主題提供逐步程式：</span><span class="sxs-lookup"><span data-stu-id="3e04f-114">The following topics provide step-by-step procedures:</span></span>

-   [<span data-ttu-id="3e04f-115">設定 System-Wide 預設驗證層級</span><span class="sxs-lookup"><span data-stu-id="3e04f-115">Setting System-Wide Default Authentication Level</span></span>](#setting-system-wide-default-authentication-level)
-   [<span data-ttu-id="3e04f-116">設定 System-Wide 啟動許可權</span><span class="sxs-lookup"><span data-stu-id="3e04f-116">Setting System-Wide Launch Permissions</span></span>](#setting-system-wide-launch-permissions)
-   [<span data-ttu-id="3e04f-117">設定 System-Wide 存取權限</span><span class="sxs-lookup"><span data-stu-id="3e04f-117">Setting System-Wide Access Permissions</span></span>](#setting-system-wide-access-permissions)
-   [<span data-ttu-id="3e04f-118">設定 System-Wide 模擬等級</span><span class="sxs-lookup"><span data-stu-id="3e04f-118">Setting System-Wide Impersonation Level</span></span>](#setting-system-wide-impersonation-level)
-   [<span data-ttu-id="3e04f-119">設定 System-Wide 參考追蹤</span><span class="sxs-lookup"><span data-stu-id="3e04f-119">Setting System-Wide Reference Tracking</span></span>](#setting-system-wide-reference-tracking)
-   [<span data-ttu-id="3e04f-120">啟用和停用 DCOM</span><span class="sxs-lookup"><span data-stu-id="3e04f-120">Enabling and Disabling DCOM</span></span>](#enabling-and-disabling-dcom)
-   [<span data-ttu-id="3e04f-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e04f-121">Related topics</span></span>](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a><span data-ttu-id="3e04f-122">設定 System-Wide 預設驗證層級</span><span class="sxs-lookup"><span data-stu-id="3e04f-122">Setting System-Wide Default Authentication Level</span></span>

<span data-ttu-id="3e04f-123">驗證層級可用來告知 COM 您希望用戶端進行驗證的層級。</span><span class="sxs-lookup"><span data-stu-id="3e04f-123">The authentication level is used to tell COM at what level you want the client to be authenticated.</span></span> <span data-ttu-id="3e04f-124">這些層級提供各種保護層級，而不是完整加密的保護。</span><span class="sxs-lookup"><span data-stu-id="3e04f-124">These levels offer various levels of protection, from no protection to full encryption.</span></span> <span data-ttu-id="3e04f-125">若要啟用電腦的安全性，您必須選擇 [無] 以外的驗證等級。</span><span class="sxs-lookup"><span data-stu-id="3e04f-125">To enable security for a computer, you need to choose an authentication level other than None.</span></span> <span data-ttu-id="3e04f-126">您可以藉由完成下列步驟，使用 Dcomcnfg.exe 來選擇這類設定。</span><span class="sxs-lookup"><span data-stu-id="3e04f-126">You can choose such a setting, using Dcomcnfg.exe, by completing the following steps.</span></span>

<span data-ttu-id="3e04f-127">**若要以全系統為基礎設定驗證層級**</span><span class="sxs-lookup"><span data-stu-id="3e04f-127">**To set the authentication level on a system-wide basis**</span></span>

1.  <span data-ttu-id="3e04f-128">執行 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="3e04f-128">Run Dcomcnfg.exe.</span></span>

2.  <span data-ttu-id="3e04f-129">選擇 [ **預設** 內容] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3e04f-129">Choose the **Default Properties** tab.</span></span>

3.  <span data-ttu-id="3e04f-130">從 [ **DefaultÂ AuthenticationÂ層級** ] 清單方塊中，選擇 [ **無 (])** 以外的值。</span><span class="sxs-lookup"><span data-stu-id="3e04f-130">From the **DefaultÂ AuthenticationÂ Level** list box, choose a value other than **(None)**.</span></span>

4.  <span data-ttu-id="3e04f-131">如果您要為電腦設定更多屬性，請 **按一下 [套用** ] 按鈕以套用新的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="3e04f-131">If you will be setting more properties for the computer, click the **Apply** button to apply the new authentication level.</span></span> <span data-ttu-id="3e04f-132">否則，請按一下 **[確定]** 以套用變更並結束 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="3e04f-132">Otherwise, click **OK** to apply the changes and exit Dcomcnfg.exe.</span></span>

## <a name="setting-system-wide-launch-permissions"></a><span data-ttu-id="3e04f-133">設定 System-Wide 啟動許可權</span><span class="sxs-lookup"><span data-stu-id="3e04f-133">Setting System-Wide Launch Permissions</span></span>

<span data-ttu-id="3e04f-134">您使用 Dcomcnfg.exe 設定的啟動許可權會決定使用者清單，其中每個使用者都被明確授與或拒絕啟動任何未提供其本身啟動許可權設定之伺服器的許可權。</span><span class="sxs-lookup"><span data-stu-id="3e04f-134">The launch permissions you set with Dcomcnfg.exe determine a list of users, each of which is explicitly granted or denied permission to launch any server that does not provide its own launch-permission settings.</span></span> <span data-ttu-id="3e04f-135">設定啟動許可權時，您可以在此清單中新增或移除一或多個使用者或群組。</span><span class="sxs-lookup"><span data-stu-id="3e04f-135">When setting launch permissions, you can add or remove one or more users or groups from this list.</span></span> <span data-ttu-id="3e04f-136">針對您新增的每個使用者，您必須指定是否要授與或拒絕使用者啟動許可權。</span><span class="sxs-lookup"><span data-stu-id="3e04f-136">For each user that you add, you must specify whether the user is being granted or denied launch permission.</span></span>

<span data-ttu-id="3e04f-137">**設定電腦的啟動許可權**</span><span class="sxs-lookup"><span data-stu-id="3e04f-137">**To set launch permissions for a computer**</span></span>

1.  <span data-ttu-id="3e04f-138">在 Dcomcnfg.exe 的 [**預設安全性**] 屬性頁上，選擇 [**預設啟動許可權**] 區域中的 [**編輯預設值**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-138">On the **Default Security** property page in Dcomcnfg.exe, choose the **Edit Default** button in the **Default Launch Permissions** area.</span></span>

2.  <span data-ttu-id="3e04f-139">若要移除使用者或群組，請選取您要移除的使用者或群組，然後選擇 [ **移除** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-139">To remove users or groups, select the user or group you want to remove and choose the **Remove** button.</span></span> <span data-ttu-id="3e04f-140">選取的使用者或群組將不會再出現在清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="3e04f-140">The selected user or group will no longer appear in the list box.</span></span> <span data-ttu-id="3e04f-141">當您完成移除使用者和群組時，請選擇 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="3e04f-141">When you have finished removing users and groups, choose **OK**.</span></span>

3.  <span data-ttu-id="3e04f-142">如果您想要新增使用者或群組，請選擇 [ **加入** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-142">If you want to add a user or group, choose the **Add** button.</span></span>

4.  <span data-ttu-id="3e04f-143">如果您知道想要新增的完整使用者名稱，請在 [ **加入名稱** ] 文字方塊中輸入。</span><span class="sxs-lookup"><span data-stu-id="3e04f-143">If you know the fully qualified user name you want to add, type it in the **Add Names** text box.</span></span> <span data-ttu-id="3e04f-144">如果您不知道使用者名稱，請參閱 **使用 DCOMCNFG 設定 Processwide 安全性** 來尋找它。</span><span class="sxs-lookup"><span data-stu-id="3e04f-144">If you do not know the user name, see **Setting Processwide Security Using DCOMCNFG** to find it.</span></span> <span data-ttu-id="3e04f-145">當您找到使用者名稱時，請從 [ **名稱** ] 清單方塊中選取使用者或群組，然後選擇 [ **加入** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-145">When you have located the user name, select the user or group from the **Names** list box and choose the **Add** button.</span></span>

5.  <span data-ttu-id="3e04f-146">在 [ **存取類型** ] 清單方塊中，選取 [ **允許啟動** 或 **拒絕啟動**)  (的存取類型。</span><span class="sxs-lookup"><span data-stu-id="3e04f-146">From the **Type of Access** list box, select the access type (either **Allow Launch** or **Deny Launch**).</span></span> <span data-ttu-id="3e04f-147">若要新增其他也會有所選存取類型的使用者，請重複步驟4。</span><span class="sxs-lookup"><span data-stu-id="3e04f-147">To add other users that will also have the selected type of access, repeat step 4.</span></span> <span data-ttu-id="3e04f-148">當您完成新增所選存取類型的使用者時，請選擇 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-148">When you have finished adding users for the selected access type, choose the **OK** button.</span></span>

6.  <span data-ttu-id="3e04f-149">若要加入將擁有不同類型存取權的使用者，請重複步驟4和5。</span><span class="sxs-lookup"><span data-stu-id="3e04f-149">To add users that will have a different type of access, repeat steps 4 and 5.</span></span> <span data-ttu-id="3e04f-150">否則，請選擇 **[確定]** 以套用變更。</span><span class="sxs-lookup"><span data-stu-id="3e04f-150">Otherwise, choose **OK** to apply the changes.</span></span>

## <a name="setting-system-wide-access-permissions"></a><span data-ttu-id="3e04f-151">設定 System-Wide 存取權限</span><span class="sxs-lookup"><span data-stu-id="3e04f-151">Setting System-Wide Access Permissions</span></span>

<span data-ttu-id="3e04f-152">Dcomcnfg.exe 可讓您設定存取權限，以控制被授與或拒絕存取這些伺服器之方法的使用者清單，這些伺服器不提供自己的存取權限。</span><span class="sxs-lookup"><span data-stu-id="3e04f-152">Dcomcnfg.exe allows you to set access permissions to control the list of users who are granted or denied access to the methods of those servers that do not provide their own access permissions.</span></span> <span data-ttu-id="3e04f-153">您可以將使用者或群組新增至清單，以指定是否要授與或拒絕存取權限。</span><span class="sxs-lookup"><span data-stu-id="3e04f-153">You can add users or groups to the list, specifying whether access permission is being granted or denied.</span></span> <span data-ttu-id="3e04f-154">您也可以從清單中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="3e04f-154">You can also remove users from the list.</span></span>

<span data-ttu-id="3e04f-155">設定存取權限時，您必須確定系統已包含在被授與存取權的使用者清單中。</span><span class="sxs-lookup"><span data-stu-id="3e04f-155">When setting access permissions, you must ensure that SYSTEM is included in the list of users that are granted access.</span></span> <span data-ttu-id="3e04f-156">如果您已將存取權限授與所有人，系統會隱含地包含。</span><span class="sxs-lookup"><span data-stu-id="3e04f-156">If you have granted access permissions to Everyone, SYSTEM is included implicitly.</span></span>

<span data-ttu-id="3e04f-157">設定電腦存取權限的程式與設定啟動許可權類似。</span><span class="sxs-lookup"><span data-stu-id="3e04f-157">The process of setting access permissions for a computer is similar to setting launch permissions.</span></span> <span data-ttu-id="3e04f-158">應採取下列步驟。</span><span class="sxs-lookup"><span data-stu-id="3e04f-158">The following steps should be taken.</span></span>

<span data-ttu-id="3e04f-159">**設定電腦的存取權限**</span><span class="sxs-lookup"><span data-stu-id="3e04f-159">**To set access permissions for a computer**</span></span>

1.  <span data-ttu-id="3e04f-160">在 Dcomcnfg.exe 的 [**預設安全性**] 屬性頁上，選擇 [**預設存取權限**] 區域中的 [**編輯預設值**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-160">On the **Default Security** property page in Dcomcnfg.exe, choose the **Edit Default** button in the **Default Access Permissions** area.</span></span>

2.  <span data-ttu-id="3e04f-161">若要移除使用者或群組，請選取您要移除的使用者或群組，然後選擇 [ **移除** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-161">To remove users or groups, select the user or group you want to remove and choose the **Remove** button.</span></span> <span data-ttu-id="3e04f-162">選取的使用者或群組將不會再出現在清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="3e04f-162">The selected user or group will no longer appear in the list box.</span></span> <span data-ttu-id="3e04f-163">當您完成移除使用者和群組時，請選擇 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="3e04f-163">When you have finished removing user and groups, choose **OK**.</span></span>

3.  <span data-ttu-id="3e04f-164">如果您想要新增使用者或群組，請選擇 [ **加入** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-164">If you want to add a user or a group, choose the **Add** button.</span></span>

4.  <span data-ttu-id="3e04f-165">如果您知道想要新增的完整使用者名稱，請在 [ **加入名稱** ] 文字方塊中輸入。</span><span class="sxs-lookup"><span data-stu-id="3e04f-165">If you know the fully qualified user name you want to add, type it in the **Add Names** text box.</span></span> <span data-ttu-id="3e04f-166">如果您不知道使用者名稱，請參閱 [使用 DCOMCNFG 設定整個進程的安全性](setting-processwide-security-using-dcomcnfg.md) 來尋找它。</span><span class="sxs-lookup"><span data-stu-id="3e04f-166">If you do not know the user name, see [Setting Process-wide Security Using DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) to find it.</span></span> <span data-ttu-id="3e04f-167">當您找到使用者名稱時，請從 [ **名稱** ] 清單方塊中選取使用者或群組，然後選擇 [ **加入** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-167">When you have located the user name, select the user or group from the **Names** list box and choose the **Add** button.</span></span>

5.  <span data-ttu-id="3e04f-168">在 [ **存取類型** ] 清單方塊中，選取 [ **允許存取** ] 或 [ **拒絕存取** ])  (存取類型。</span><span class="sxs-lookup"><span data-stu-id="3e04f-168">From the **Type of Access** list box, select the access type (either **Allow Access** or **Deny Access**).</span></span> <span data-ttu-id="3e04f-169">若要加入將擁有所選存取類型的其他使用者，請重複步驟4。</span><span class="sxs-lookup"><span data-stu-id="3e04f-169">To add other users that will have the selected type of access, repeat step 4.</span></span> <span data-ttu-id="3e04f-170">當您完成新增所選存取類型的使用者時，請選擇 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e04f-170">When you have finished adding users for the selected access type, choose the **OK** button.</span></span>

6.  <span data-ttu-id="3e04f-171">若要加入將擁有不同類型存取權的使用者，請重複步驟4和5。</span><span class="sxs-lookup"><span data-stu-id="3e04f-171">To add users that will have a different type of access, repeat steps 4 and 5.</span></span> <span data-ttu-id="3e04f-172">否則，請選擇 **[確定]** 以套用變更。</span><span class="sxs-lookup"><span data-stu-id="3e04f-172">Otherwise, choose **OK** to apply the changes.</span></span>

## <a name="setting-system-wide-impersonation-level"></a><span data-ttu-id="3e04f-173">設定 System-Wide 模擬等級</span><span class="sxs-lookup"><span data-stu-id="3e04f-173">Setting System-Wide Impersonation Level</span></span>

<span data-ttu-id="3e04f-174">用戶端所設定的模擬層級會決定授與給伺服器以代表用戶端的授權數量。</span><span class="sxs-lookup"><span data-stu-id="3e04f-174">The impersonation level, set by the client, determines the amount of authority given to the server to act on the client's behalf.</span></span> <span data-ttu-id="3e04f-175">例如，當用戶端將模擬層級設定為委派時，伺服器可以存取本機和遠端資源做為用戶端，而且如果設定了隱匿功能，伺服器可以在多部電腦界限上進行掩蔽。</span><span class="sxs-lookup"><span data-stu-id="3e04f-175">For example, when the client has set its impersonation level to delegate, the server can access local and remote resources as the client, and the server can cloak over multiple computer boundaries if the cloaking capability is set.</span></span> <span data-ttu-id="3e04f-176">若要協助判斷您應該選擇哪一種模擬等級，請參閱模擬 [層](impersonation-levels.md) 級和 [掩蓋](cloaking.md)。</span><span class="sxs-lookup"><span data-stu-id="3e04f-176">To help determine which impersonation level you should choose, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="3e04f-177">設定整部電腦的預設模擬等級，會告知 COM 在電腦上的特定用戶端未使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 或 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)以程式設計方式指定模擬等級時要使用的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="3e04f-177">Setting the default impersonation level for the whole computer tells COM what impersonation level to use when a particular client on the computer does not specify an impersonation level programmatically by using [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="3e04f-178">**設定電腦的模擬等級**</span><span class="sxs-lookup"><span data-stu-id="3e04f-178">**To set the impersonation level for a computer**</span></span>

1.  <span data-ttu-id="3e04f-179">當 Dcomcnfg.exe 執行時，請選擇 [ **預設屬性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3e04f-179">With Dcomcnfg.exe running, choose the **Default Properties** tab.</span></span>

2.  <span data-ttu-id="3e04f-180">從 [ **預設模擬等級** ] 清單方塊中，選擇您想要的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="3e04f-180">From the **Default Impersonation Level** list box, choose the impersonation level you want.</span></span>

3.  <span data-ttu-id="3e04f-181">如果您要為電腦設定更多屬性，請選擇 [套用 **] 按鈕以** 套用新的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="3e04f-181">If you will be setting more properties for the computer, choose the **Apply** button to apply the new impersonation level.</span></span> <span data-ttu-id="3e04f-182">否則，請選擇 **[確定]** 以套用變更並結束 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="3e04f-182">Otherwise, choose **OK** to apply the changes and exit Dcomcnfg.exe.</span></span>

## <a name="setting-system-wide-reference-tracking"></a><span data-ttu-id="3e04f-183">設定 System-Wide 參考追蹤</span><span class="sxs-lookup"><span data-stu-id="3e04f-183">Setting System-Wide Reference Tracking</span></span>

<span data-ttu-id="3e04f-184">當您啟用參考追蹤時，會要求 COM 進行額外的安全性檢查，並追蹤會讓物件不會提早釋放的資訊。</span><span class="sxs-lookup"><span data-stu-id="3e04f-184">When you enable reference tracking, you are asking COM to do additional security checks and to keep track of information that will keep objects from being released too early.</span></span> <span data-ttu-id="3e04f-185">請記住，這些額外的檢查很昂貴。</span><span class="sxs-lookup"><span data-stu-id="3e04f-185">Keep in mind that these additional checks are expensive.</span></span> <span data-ttu-id="3e04f-186">如需參考追蹤的詳細資訊，請參閱 [參考追蹤](reference-tracking.md)。</span><span class="sxs-lookup"><span data-stu-id="3e04f-186">For more information about reference tracking, see [Reference Tracking](reference-tracking.md).</span></span> <span data-ttu-id="3e04f-187">使用下列步驟來啟用或停用參考追蹤。</span><span class="sxs-lookup"><span data-stu-id="3e04f-187">Use the following steps to enable or disable reference tracking.</span></span>

<span data-ttu-id="3e04f-188">**設定電腦的參考追蹤**</span><span class="sxs-lookup"><span data-stu-id="3e04f-188">**To set reference tracking for a computer**</span></span>

1.  <span data-ttu-id="3e04f-189">當 Dcomcnfg.exe 執行時，請選擇 [ **預設屬性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3e04f-189">With Dcomcnfg.exe running, choose the **Default Properties** tab.</span></span>

2.  <span data-ttu-id="3e04f-190">若要啟用 (或停用) 參考追蹤，請選取 [ (] 或 [清除]，) 頁面底部附近的 [為 **參考追蹤提供額外的安全性** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="3e04f-190">To enable (or disable) reference tracking, select (or clear) the **Provide additional security for reference tracking** check box near the bottom of the page.</span></span>

3.  <span data-ttu-id="3e04f-191">如果您要為電腦設定更多屬性，請選擇 [套用 **] 按鈕以** 套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="3e04f-191">If you will be setting more properties for the computer, choose the **Apply** button to apply the new setting.</span></span> <span data-ttu-id="3e04f-192">否則，請選擇 **[確定]** 以套用變更並結束 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="3e04f-192">Otherwise, choose **OK** to apply the changes and exit Dcomcnfg.exe.</span></span>

## <a name="enabling-and-disabling-dcom"></a><span data-ttu-id="3e04f-193">啟用和停用 DCOM</span><span class="sxs-lookup"><span data-stu-id="3e04f-193">Enabling and Disabling DCOM</span></span>

<span data-ttu-id="3e04f-194">當電腦是網路的一部分時，DCOM 有線通訊協定可讓該電腦上的 COM 物件與其他電腦上的 COM 物件進行通訊。</span><span class="sxs-lookup"><span data-stu-id="3e04f-194">When a computer is part of a network, the DCOM wire protocol enables COM objects on that computer to communicate with COM objects on other computers.</span></span> <span data-ttu-id="3e04f-195">您可以停用特定電腦的 DCOM，但是這樣做會停用該電腦上物件與其他電腦上物件之間的所有通訊。</span><span class="sxs-lookup"><span data-stu-id="3e04f-195">You can disable DCOM for a particular computer, but doing so will disable all communication between objects on that computer and objects on other computers.</span></span>

<span data-ttu-id="3e04f-196">停用電腦上的 DCOM 不會影響本機 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="3e04f-196">Disabling DCOM on a computer has no effect on local COM objects.</span></span> <span data-ttu-id="3e04f-197">COM 仍會尋找您已指定的啟動許可權。</span><span class="sxs-lookup"><span data-stu-id="3e04f-197">COM still looks for launch permissions that you have specified.</span></span> <span data-ttu-id="3e04f-198">如果未指定任何啟動許可權，則會使用預設啟動許可權。</span><span class="sxs-lookup"><span data-stu-id="3e04f-198">If no launch permissions have been specified, default launch permissions are used.</span></span> <span data-ttu-id="3e04f-199">即使您停用 DCOM，如果使用者具有電腦的實體存取權，他們就可以在電腦上啟動伺服器，除非您將啟動許可權設定為不允許。</span><span class="sxs-lookup"><span data-stu-id="3e04f-199">Even if you disable DCOM, if a user has physical access to the computer, they could launch a server on the computer unless you set launch permissions not to allow it.</span></span>

> [!Note]  
> <span data-ttu-id="3e04f-200">如果您停用遠端電腦上的 DCOM，則在重新啟用 DCOM 之後，您將無法從遠端存取該電腦。</span><span class="sxs-lookup"><span data-stu-id="3e04f-200">If you disable DCOM on a remote computer, you will not be able to remotely access that computer afterward to re-enable DCOM.</span></span> <span data-ttu-id="3e04f-201">若要重新啟用 DCOM，您將需要該電腦的實體存取權。</span><span class="sxs-lookup"><span data-stu-id="3e04f-201">To re-enable DCOM, you will need physical access to that computer.</span></span>

 

<span data-ttu-id="3e04f-202">**手動啟用 (或停用電腦的) DCOM**</span><span class="sxs-lookup"><span data-stu-id="3e04f-202">**To manually enable (or disable) DCOM for a computer**</span></span>

1.  <span data-ttu-id="3e04f-203">執行 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="3e04f-203">Run Dcomcnfg.exe.</span></span>

2.  <span data-ttu-id="3e04f-204">選擇 [ **DefaultÂ屬性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3e04f-204">Choose the **DefaultÂ Properties** tab.</span></span>

3.  <span data-ttu-id="3e04f-205">選取 (或清除 [ **在這部電腦上啟用分散式 COMÂ** ] 核取方塊) 。</span><span class="sxs-lookup"><span data-stu-id="3e04f-205">Select (or clear) the **Enable Distributed COMÂ on this Computer** check box.</span></span>

4.  <span data-ttu-id="3e04f-206">如果您要為電腦設定更多屬性，請 **按一下 [套用** ] 按鈕來啟用 (或停用) DCOM。</span><span class="sxs-lookup"><span data-stu-id="3e04f-206">If you will be setting more properties for the computer, click the **Apply** button to enable (or disable) DCOM.</span></span> <span data-ttu-id="3e04f-207">否則，請按一下 **[確定]** 以套用變更並結束 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="3e04f-207">Otherwise, click **OK** to apply the changes and exit Dcomcnfg.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e04f-208">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e04f-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e04f-209">設定整個進程的安全性</span><span class="sxs-lookup"><span data-stu-id="3e04f-209">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




