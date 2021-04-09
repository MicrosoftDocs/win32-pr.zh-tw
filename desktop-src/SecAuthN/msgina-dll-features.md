---
description: 如果您要撰寫 GINA 來取代 Microsoft standard GINA DLL (MSGina.dll) ，您可能會想要提供部分或所有標準 GINA 功能。
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: MSGina.dll 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51833ab92e47dad01c13df004797e3ab3552b09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851139"
---
# <a name="msginadll-features"></a><span data-ttu-id="02e65-103">MSGina.dll 功能</span><span class="sxs-lookup"><span data-stu-id="02e65-103">MSGina.dll Features</span></span>

<span data-ttu-id="02e65-104">如果您要撰寫 [*GINA*](../secgloss/g-gly.md) 來取代 MICROSOFT STANDARD GINA DLL (MSGina.dll) ，您可能會想要提供部分或所有標準 GINA 功能。</span><span class="sxs-lookup"><span data-stu-id="02e65-104">If you are writing a [*GINA*](../secgloss/g-gly.md) to replace the Microsoft standard GINA DLL (MSGina.dll), you may want to provide some or all of the standard GINA functionality.</span></span> <span data-ttu-id="02e65-105">以下是標準功能的清單，以及如何控制這些功能的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="02e65-105">Following is a list of standard features and a brief description of how they are controlled.</span></span>

> [!Note]  
> <span data-ttu-id="02e65-106">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="02e65-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="02e65-107">登錄機碼值控制許多這些標準 GINA 功能的可用性或行為。</span><span class="sxs-lookup"><span data-stu-id="02e65-107">Registry key values control the availability or behavior of many of these standard GINA features.</span></span> <span data-ttu-id="02e65-108">除非另有說明，否則這些金鑰值屬於 Winlogon 登錄機碼，而且具有數值型別的 \[ REG \_ SZ \] 。</span><span class="sxs-lookup"><span data-stu-id="02e65-108">Unless otherwise noted, these key values belong to the Winlogon registry key and have a value type of \[REG\_SZ\].</span></span> <span data-ttu-id="02e65-109">[*Winlogon*](../secgloss/w-gly.md)金鑰的實際路徑是：</span><span class="sxs-lookup"><span data-stu-id="02e65-109">The actual path of the [*Winlogon*](../secgloss/w-gly.md) key is:</span></span>

<span data-ttu-id="02e65-110">**\\HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon**</span><span class="sxs-lookup"><span data-stu-id="02e65-110">**\\HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon**</span></span>

-   <span data-ttu-id="02e65-111">**法律聲明對話方塊**</span><span class="sxs-lookup"><span data-stu-id="02e65-111">**Legal Notification Dialog Box**</span></span>

    <span data-ttu-id="02e65-112">在某些地方，有權存取工作站以登入並開始工作的任何人都是合法的，除非有通知指出系統僅供授權使用者使用。</span><span class="sxs-lookup"><span data-stu-id="02e65-112">In some places, it is legal for anyone who has access to a workstation to log on and begin working unless there is a notice that indicates that the system is for authorized users only.</span></span> <span data-ttu-id="02e65-113">此外，許多使用者都想要在一般登入之前顯示公司特定的訊息。</span><span class="sxs-lookup"><span data-stu-id="02e65-113">Also, many users want company-specific messages displayed before normal logon.</span></span> <span data-ttu-id="02e65-114">標準 GINA 會使用兩個 Winlogon 登錄機碼值，讓系統在登入之前顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="02e65-114">The standard GINA uses two Winlogon registry key values to allow a system to display information before logon.</span></span> <span data-ttu-id="02e65-115">如果有任一個索引鍵值存在且包含非 null 字串，則會在一般歡迎畫面之前顯示法律聲明對話方塊。</span><span class="sxs-lookup"><span data-stu-id="02e65-115">If either key value is present and contains a non-null string, then a Legal Notice dialog box is displayed before the usual Welcome screen.</span></span> <span data-ttu-id="02e65-116">下表顯示這些機碼值的名稱。</span><span class="sxs-lookup"><span data-stu-id="02e65-116">These key value names are shown in the following table.</span></span>

    

    | <span data-ttu-id="02e65-117">機碼值名稱</span><span class="sxs-lookup"><span data-stu-id="02e65-117">Key value name</span></span>         | <span data-ttu-id="02e65-118">目錄</span><span class="sxs-lookup"><span data-stu-id="02e65-118">Contents</span></span>                                                            |
    |------------------------|---------------------------------------------------------------------|
    | <span data-ttu-id="02e65-119">**LegalNoticeCaption**</span><span class="sxs-lookup"><span data-stu-id="02e65-119">**LegalNoticeCaption**</span></span> | <span data-ttu-id="02e65-120">要顯示為 [法律聲明] 對話方塊標題的字串</span><span class="sxs-lookup"><span data-stu-id="02e65-120">The string to display as the caption of the legal notice dialog box</span></span> |
    | <span data-ttu-id="02e65-121">**LegalNoticeText**</span><span class="sxs-lookup"><span data-stu-id="02e65-121">**LegalNoticeText**</span></span>    | <span data-ttu-id="02e65-122">要顯示為 [法律聲明] 對話方塊訊息的字串</span><span class="sxs-lookup"><span data-stu-id="02e65-122">The string to display as the message of the legal notice dialog box</span></span> |

    

     

-   <span data-ttu-id="02e65-123">**顯示最後的使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="02e65-123">**Display Last User Name**</span></span>

    <span data-ttu-id="02e65-124">根據預設，登入畫面會顯示最後一個使用者的名稱，以成功登入工作站。</span><span class="sxs-lookup"><span data-stu-id="02e65-124">By default, the logon screen displays the name of the last user to successfully log on to the workstation.</span></span> <span data-ttu-id="02e65-125">這項功能是由 **DontDisplayLastUserName** 登錄機碼值所控制。</span><span class="sxs-lookup"><span data-stu-id="02e65-125">This feature is controlled by the **DontDisplayLastUserName** registry key value.</span></span> <span data-ttu-id="02e65-126">當此機碼值設定為1時，使用者名稱不會顯示在 [登入] 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="02e65-126">When this key value is set to one, the user name is not displayed in the logon dialog box.</span></span>

-   <span data-ttu-id="02e65-127">**自動登入**</span><span class="sxs-lookup"><span data-stu-id="02e65-127">**Automatic Logon**</span></span>

    <span data-ttu-id="02e65-128">這項功能可讓系統在每次系統啟動時，自動登入使用者，方法是使用預設資訊，並停用 CTRL + ALT + DEL 登入方塊。</span><span class="sxs-lookup"><span data-stu-id="02e65-128">This feature allows a system to log on a user automatically every time the system starts by using default information and disabling the CTRL+ALT+DEL logon box.</span></span>

    <span data-ttu-id="02e65-129">這項功能會使用 Winlogon 金鑰的下列值。</span><span class="sxs-lookup"><span data-stu-id="02e65-129">This feature uses the following values of the Winlogon key.</span></span>

    

    | <span data-ttu-id="02e65-130">值</span><span class="sxs-lookup"><span data-stu-id="02e65-130">Value</span></span>                 | <span data-ttu-id="02e65-131">目錄</span><span class="sxs-lookup"><span data-stu-id="02e65-131">Contents</span></span>                                           |
    |-----------------------|----------------------------------------------------|
    | <span data-ttu-id="02e65-132">**AutoAdminLogon**</span><span class="sxs-lookup"><span data-stu-id="02e65-132">**AutoAdminLogon**</span></span>    | <span data-ttu-id="02e65-133">1</span><span class="sxs-lookup"><span data-stu-id="02e65-133">1</span></span>                                                  |
    | <span data-ttu-id="02e65-134">**AutoLogonCount**</span><span class="sxs-lookup"><span data-stu-id="02e65-134">**AutoLogonCount**</span></span>    | <span data-ttu-id="02e65-135">要自動登入的次數</span><span class="sxs-lookup"><span data-stu-id="02e65-135">The number of times to do an automatic logon</span></span>       |
    | <span data-ttu-id="02e65-136">**DefaultUserName**</span><span class="sxs-lookup"><span data-stu-id="02e65-136">**DefaultUserName**</span></span>   | <span data-ttu-id="02e65-137">使用者帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="02e65-137">The name of the user account</span></span>                       |
    | <span data-ttu-id="02e65-138">**DefaultDomainName**</span><span class="sxs-lookup"><span data-stu-id="02e65-138">**DefaultDomainName**</span></span> | <span data-ttu-id="02e65-139">使用者帳戶所在網域的名稱</span><span class="sxs-lookup"><span data-stu-id="02e65-139">The name of the domain that the user account is in</span></span> |

    

     

    <span data-ttu-id="02e65-140">如果 **AutoAdminLogon** 索引鍵值存在且包含一個，而且 **AutoLogonCount** 索引鍵值不存在，則每次目前使用者登出或系統重新開機時，就會發生自動登入。</span><span class="sxs-lookup"><span data-stu-id="02e65-140">If the **AutoAdminLogon** key value is present and contains a one, and the **AutoLogonCount** key value is not present, an automatic logon will occur every time the current user logs off or the system is restarted.</span></span> <span data-ttu-id="02e65-141">要登入的帳戶是使用 **DefaultUserName** 和 **DefaultDomainName** 索引鍵值指定的。</span><span class="sxs-lookup"><span data-stu-id="02e65-141">The account being logged onto is specified using the **DefaultUserName** and **DefaultDomainName** key values.</span></span> <span data-ttu-id="02e65-142">您可以用兩種方式之一來指定帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="02e65-142">The password for the account can be specified in one of two ways.</span></span> <span data-ttu-id="02e65-143">若為執行其中一個 Windows Server 2003 或 Windows XP 作業系統的電腦，則應使用 [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) 函式將密碼儲存為秘密。</span><span class="sxs-lookup"><span data-stu-id="02e65-143">For computers running one of the Windows Server 2003 or Windows XP operating systems, the password should be stored as a secret using the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span> <span data-ttu-id="02e65-144">如需詳細資訊，請參閱 [保護自動登入密碼](protecting-the-automatic-logon-password.md)。</span><span class="sxs-lookup"><span data-stu-id="02e65-144">For details, see [Protecting the Automatic Logon Password](protecting-the-automatic-logon-password.md).</span></span> <span data-ttu-id="02e65-145">另一種儲存密碼的方式，是以純文字形式儲存在 Winlogon 金鑰的 **DefaultPassword** 專案中;基於安全性考慮，應避免使用此技術。</span><span class="sxs-lookup"><span data-stu-id="02e65-145">The other way to store the password is in plaintext in the **DefaultPassword** entry of the Winlogon key; for security purposes, this technique should be avoided.</span></span> <span data-ttu-id="02e65-146">如果您使用 **LsaStorePrivateData** 函式來儲存密碼，則請勿在 Winlogon 金鑰中提供 **DefaultPassword** 專案。</span><span class="sxs-lookup"><span data-stu-id="02e65-146">If you store the password using the **LsaStorePrivateData** function, then do not provide a **DefaultPassword** entry in the Winlogon key.</span></span>

    <span data-ttu-id="02e65-147">如果 **AutoAdminLogon** 索引鍵值存在且包含一個值，而且如果 **AutoLogonCount** 索引鍵值存在且不是零，則 **AutoLogonCount** 將會決定所發生的自動登入次數。</span><span class="sxs-lookup"><span data-stu-id="02e65-147">If the **AutoAdminLogon** key value is present and contains a one, and if the **AutoLogonCount** key value is present and is not zero, **AutoLogonCount** will determine the number of automatic logons that occur.</span></span> <span data-ttu-id="02e65-148">每次重新開機系統時， **AutoLogonCount** 的值就會遞減1，直到達到零為止。</span><span class="sxs-lookup"><span data-stu-id="02e65-148">Each time the system is restarted, the value of **AutoLogonCount** will be decremented by one, until it reaches zero.</span></span> <span data-ttu-id="02e65-149">當 **AutoLogonCount** 到達零時，系統將不會自動登入任何帳戶， **AutoLogonCount** 索引鍵值和 **DefaultPassword** 索引鍵值（如果有使用的話）將會從登錄中刪除，而且 **AutoAdminLogon** 會設定為零。</span><span class="sxs-lookup"><span data-stu-id="02e65-149">When **AutoLogonCount** reaches zero, no account will be logged on automatically, the **AutoLogonCount** key value and **DefaultPassword** key value, if used, will be deleted from the registry, and **AutoAdminLogon** will be set to zero.</span></span>

    <span data-ttu-id="02e65-150">使用 **AutoAdminLogon** 有另外一點要注意：根據預設，MSGina.dll 會在 **AutoAdminLogon** 為1時檢查 SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="02e65-150">There is one additional caveat to using **AutoAdminLogon**: By default, MSGina.dll checks the state of the SHIFT key when **AutoAdminLogon** is one.</span></span> <span data-ttu-id="02e65-151">如果在開機過程中保留 SHIFT 鍵，MSGina.dll 將會忽略 **AutoAdminLogon** 金鑰值，並以互動方式提示使用者提供識別和驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="02e65-151">If the SHIFT key is held down during the boot process, MSGina.dll will ignore the **AutoAdminLogon** key value and prompt the user for identification and authentication information interactively.</span></span> <span data-ttu-id="02e65-152">當您要對專用應用程式進行偵錯工具時，這是很有用的功能。</span><span class="sxs-lookup"><span data-stu-id="02e65-152">This is a useful feature when you are debugging a dedicated application.</span></span> <span data-ttu-id="02e65-153">若要停用 SHIFT 鍵的意義，請將 **IgnoreShiftOverride** 索引鍵值設定為一個。</span><span class="sxs-lookup"><span data-stu-id="02e65-153">To disable the meaning of the SHIFT key, set the **IgnoreShiftOverride** key value to one.</span></span>

-   <span data-ttu-id="02e65-154">**允許未經驗證的關機**</span><span class="sxs-lookup"><span data-stu-id="02e65-154">**Allow Unauthenticated Shutdown**</span></span>

    <span data-ttu-id="02e65-155">您可以在 [登入] 對話方塊中，將預設 [*GINA*](../secgloss/g-gly.md) 設定為包含 [ **關閉** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="02e65-155">You can configure the default [*GINA*](../secgloss/g-gly.md) to include a **Shutdown** button in the logon dialog box.</span></span> <span data-ttu-id="02e65-156">這可讓使用者在不先登入的情況下關閉系統。</span><span class="sxs-lookup"><span data-stu-id="02e65-156">This lets users shut down the system without first logging on.</span></span> <span data-ttu-id="02e65-157">下列索引鍵值控制是否包含此按鈕。</span><span class="sxs-lookup"><span data-stu-id="02e65-157">The following key value controls whether this button is included.</span></span>

    

    | <span data-ttu-id="02e65-158">值</span><span class="sxs-lookup"><span data-stu-id="02e65-158">Value</span></span>                    | <span data-ttu-id="02e65-159">描述</span><span class="sxs-lookup"><span data-stu-id="02e65-159">Description</span></span>                                           |
    |--------------------------|-------------------------------------------------------|
    | <span data-ttu-id="02e65-160">**ShutdownWithoutLogon**</span><span class="sxs-lookup"><span data-stu-id="02e65-160">**ShutdownWithoutLogon**</span></span> | <span data-ttu-id="02e65-161">其中一個包含按鈕;零以排除按鈕</span><span class="sxs-lookup"><span data-stu-id="02e65-161">One to include the button; zero to exclude the button</span></span> |

    

     

-   <span data-ttu-id="02e65-162">**Userinit.exe 啟用**</span><span class="sxs-lookup"><span data-stu-id="02e65-162">**Userinit.exe Activation**</span></span>

    <span data-ttu-id="02e65-163">Userinit.exe 是由使用者登入 MSGina.dll 所執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="02e65-163">Userinit.exe is an application that is executed by MSGina.dll when the user has logged on.</span></span> <span data-ttu-id="02e65-164">它會在新登入的使用者 [*內容*](../secgloss/c-gly.md) 和應用程式桌面上執行。</span><span class="sxs-lookup"><span data-stu-id="02e65-164">It runs in the newly logged-on user's [*context*](../secgloss/c-gly.md) and on the application desktop.</span></span> <span data-ttu-id="02e65-165">其目的是要設定使用者的環境，包括還原網路使用、建立字型和螢幕色彩等設定檔設定，以及執行登入腳本。</span><span class="sxs-lookup"><span data-stu-id="02e65-165">Its purpose is to set up the user's environment, including restoring network uses, establishing profile settings such as fonts and screen colors, and running logon scripts.</span></span> <span data-ttu-id="02e65-166">完成這些工作之後，Userinit.exe 會執行使用者 shell 程式。</span><span class="sxs-lookup"><span data-stu-id="02e65-166">After completing those tasks, Userinit.exe executes the user shell programs.</span></span> <span data-ttu-id="02e65-167">Shell 程式會繼承 Userinit.exe 設定的環境。</span><span class="sxs-lookup"><span data-stu-id="02e65-167">The shell programs inherit the environment that Userinit.exe sets up.</span></span> <span data-ttu-id="02e65-168">Userinit.exe 執行的特定 shell 程式會儲存在 Winlogon 登錄機碼下的 **shell** 索引鍵值中。</span><span class="sxs-lookup"><span data-stu-id="02e65-168">The specific shell programs that Userinit.exe executes are stored in the **Shell** key value under the Winlogon registry key.</span></span>

    <span data-ttu-id="02e65-169">**Shell** 金鑰值可以包含要執行的程式清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="02e65-169">The **Shell** key value can contain a comma-separated list of programs to be executed.</span></span> <span data-ttu-id="02e65-170">Windows 檔案總管是預設的 shell 程式，且如果 **shell** 索引鍵值為 null 或不存在，就會執行此程式。</span><span class="sxs-lookup"><span data-stu-id="02e65-170">Windows Explorer is the default shell program and will be executed if the **Shell** key value is null or not present.</span></span> <span data-ttu-id="02e65-171">預設會列出 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="02e65-171">By default, Windows Explorer is listed.</span></span>

-   <span data-ttu-id="02e65-172">**登入的安全性選項**</span><span class="sxs-lookup"><span data-stu-id="02e65-172">**Logged-On Security Options**</span></span>

    <span data-ttu-id="02e65-173">登入時，如果使用者輸入 (SAS) 的 [*安全注意順序*](../secgloss/s-gly.md) ，使用者會看到 [安全性選項] 畫面。</span><span class="sxs-lookup"><span data-stu-id="02e65-173">When logged on, if a user enters a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), the user is presented with a security options screen.</span></span> <span data-ttu-id="02e65-174">其中所列的選項包括：</span><span class="sxs-lookup"><span data-stu-id="02e65-174">Among the options listed are:</span></span>

    -   <span data-ttu-id="02e65-175">關閉系統。</span><span class="sxs-lookup"><span data-stu-id="02e65-175">Shut down the system.</span></span>
    -   <span data-ttu-id="02e65-176">登出。</span><span class="sxs-lookup"><span data-stu-id="02e65-176">Log off.</span></span>
    -   <span data-ttu-id="02e65-177">變更密碼。</span><span class="sxs-lookup"><span data-stu-id="02e65-177">Change the password.</span></span>
    -   <span data-ttu-id="02e65-178">移至 [工作] 清單。</span><span class="sxs-lookup"><span data-stu-id="02e65-178">Go to the task list.</span></span>
    -   <span data-ttu-id="02e65-179">鎖定工作站。</span><span class="sxs-lookup"><span data-stu-id="02e65-179">Lock the workstation.</span></span>

    <span data-ttu-id="02e65-180">當使用者登入時收到 SAS 事件時，取代 GINA 可以提供類似的選項。</span><span class="sxs-lookup"><span data-stu-id="02e65-180">A replacement GINA can provide similar options when a SAS event is received while a user is logged on.</span></span>

 

 
