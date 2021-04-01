---
description: Windows XP 和 Windows Vista 中的 [開始] 功能表包含預設網際網路 (瀏覽器) 的保留位置，以及電子郵件 (mail) 用戶端，通常稱為「開始功能表網際網路應用程式」。
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: 如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195794"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a><span data-ttu-id="ca267-103">如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式</span><span class="sxs-lookup"><span data-stu-id="ca267-103">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>

> [!Note]  
> <span data-ttu-id="ca267-104">本主題適用于 Windows XP、Windows Vista 和 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="ca267-104">This topic applies to Windows XP, Windows Vista, and Windows 7.</span></span>

 

<span data-ttu-id="ca267-105">Windows XP 和 Windows Vista 中的 [開始] 功能表包含預設 **網際網路** (瀏覽器) 的保留位置，以及 **電子郵件** (mail) 用戶端，通常稱為 *「開始功能表網際網路應用程式」*。</span><span class="sxs-lookup"><span data-stu-id="ca267-105">The Start menu in Windows XP and Windows Vista contains reserved slots for the default **Internet** (browser) and **E-mail** (mail) clients, together commonly known as *Start Menu Internet Applications*.</span></span> <span data-ttu-id="ca267-106">以 [開始] 功能表的形式註冊的應用程式，會在整個系統 (每部電腦) 。</span><span class="sxs-lookup"><span data-stu-id="ca267-106">Applications which register as Start Menu Internet Applications do so across the entire system (per-machine).</span></span> <span data-ttu-id="ca267-107">在 Windows Vista 中，使用者可以使用 [ **預設程式** ] 功能來設定每個使用者的預設值。</span><span class="sxs-lookup"><span data-stu-id="ca267-107">In Windows Vista, the user may use the **Default Programs** feature to set a per-user default.</span></span>

<span data-ttu-id="ca267-108">當應用程式註冊為開始功能表網際網路應用程式時，Windows XP 和 Windows Vista 會在 [開始] 功能表上建立 **網際網路** 和 **電子郵件** 圖示。</span><span class="sxs-lookup"><span data-stu-id="ca267-108">When applications register as Start Menu Internet Applications, Windows XP and Windows Vista create **Internet** and **E-mail** icons on the Start menu.</span></span> <span data-ttu-id="ca267-109">按一下這些圖示會導致 [開始] 功能表檢查每位使用者的登錄子樹， (**HKEY \_ 目前的 \_ 使用者**) 。</span><span class="sxs-lookup"><span data-stu-id="ca267-109">Clicking these icons causes the Start menu to check the per-user registry subtree (**HKEY\_CURRENT\_USER**).</span></span> <span data-ttu-id="ca267-110">如果找不到每個使用者的預設設定，[開始] 功能表會在 [ **HKEY \_ 本機 \_ 電腦** ] 子樹中尋找每部電腦的預設子機碼。</span><span class="sxs-lookup"><span data-stu-id="ca267-110">If no per-user default setting is found, the Start menu looks for the per-machine default subkey in the **HKEY\_LOCAL\_MACHINE** subtree.</span></span>

> [!Note]  
> <span data-ttu-id="ca267-111">Windows 的預設安裝不會註冊每位使用者的預設網際網路或電子郵件程式，只會註冊整個系統的預設值。</span><span class="sxs-lookup"><span data-stu-id="ca267-111">The default installation of Windows does not register a per-user default Internet or email program, only a system-wide default.</span></span> <span data-ttu-id="ca267-112">這會從舊版作業系統提供順暢的升級路徑，在此版本中， \_ \_ 用戶端註冊只支援 HKEY 本機電腦子樹。</span><span class="sxs-lookup"><span data-stu-id="ca267-112">This provides a smooth upgrade path from previous versions of the operating system, in which only the HKEY\_LOCAL\_MACHINE subtree is supported for client registrations.</span></span>

 

<span data-ttu-id="ca267-113">本主題將討論下列專案：</span><span class="sxs-lookup"><span data-stu-id="ca267-113">This topic discusses the following items:</span></span>

-   <span data-ttu-id="ca267-114">[註冊 [開始] 功能表網際網路連結](#registering-for-the-start-menu-internet-link)</span><span class="sxs-lookup"><span data-stu-id="ca267-114">[Registering for the Start Menu Internet Link](#registering-for-the-start-menu-internet-link)</span></span>
    -   [<span data-ttu-id="ca267-115">如何註冊為預設的網際網路用戶端</span><span class="sxs-lookup"><span data-stu-id="ca267-115">How to Register as the Default Internet Client</span></span>](#how-to-register-as-the-default-internet-client)
-   <span data-ttu-id="ca267-116">[註冊 [開始] 功能表電子郵件連結](#registering-for-the-start-menu-email-link)</span><span class="sxs-lookup"><span data-stu-id="ca267-116">[Registering for the Start Menu Email Link](#registering-for-the-start-menu-email-link)</span></span>
    -   <span data-ttu-id="ca267-117">[[開始] 功能表如何顯示預設電子郵件客戶](#how-the-start-menu-displays-the-default-email-client)</span><span class="sxs-lookup"><span data-stu-id="ca267-117">[How the Start Menu Displays the Default Email Client](#how-the-start-menu-displays-the-default-email-client)</span></span>
    -   [<span data-ttu-id="ca267-118">如何註冊為預設電子郵件客戶</span><span class="sxs-lookup"><span data-stu-id="ca267-118">How to Register as the Default EMail Client</span></span>](#how-to-register-as-the-default-email-client)
-   [<span data-ttu-id="ca267-119">自訂內容功能表</span><span class="sxs-lookup"><span data-stu-id="ca267-119">Customizing the Context Menu</span></span>](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a><span data-ttu-id="ca267-120">註冊 [開始] 功能表網際網路連結</span><span class="sxs-lookup"><span data-stu-id="ca267-120">Registering for the Start Menu Internet Link</span></span>

> [!Note]  
> <span data-ttu-id="ca267-121">此註冊已從 Windows 7 淘汰，不再提供 [開始] 功能表的網際網路連結。</span><span class="sxs-lookup"><span data-stu-id="ca267-121">This registration is deprecated as of Windows 7, which no longer provides a Start menu Internet link.</span></span> <span data-ttu-id="ca267-122">在 Windows 7 和更新版本中會忽略現有的註冊。</span><span class="sxs-lookup"><span data-stu-id="ca267-122">Existing registrations are ignored in Windows 7 and later.</span></span> <span data-ttu-id="ca267-123">註冊為預設的 [開始] 功能表網際網路應用程式與註冊為預設網頁瀏覽器並不相同。</span><span class="sxs-lookup"><span data-stu-id="ca267-123">Being registered as the default Start menu Internet application is not the same as being registered as the default web browser.</span></span> <span data-ttu-id="ca267-124">預設的網頁瀏覽器可用來從系統中的任何位置啟動任意 Url。</span><span class="sxs-lookup"><span data-stu-id="ca267-124">The default web browser is used for launching arbitrary URLs from anywhere in the system.</span></span> <span data-ttu-id="ca267-125">[開始] 功能表的網際網路應用程式只會控制當使用者按一下 [開始] 功能表上的網際網路圖示時所啟動的程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-125">The Start menu Internet application merely controls the program that is started when the user clicks the Internet icon on the Start menu.</span></span>

 

<span data-ttu-id="ca267-126">任何網頁瀏覽器應用程式都可以註冊，以 [開始] 功能表上的網際網路用戶端顯示。</span><span class="sxs-lookup"><span data-stu-id="ca267-126">Any web browser application can register to appear as an Internet client on the Start menu.</span></span> <span data-ttu-id="ca267-127">此可見度會結合[適當的應用程式檔案和](fa-intro.md)[通訊協定](/previous-versions//aa767743(v=vs.85))類型註冊，並提供應用程式預設瀏覽器狀態。</span><span class="sxs-lookup"><span data-stu-id="ca267-127">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default browser status.</span></span>

<span data-ttu-id="ca267-128">在 [ **HKEY \_ 目前 \_ 使用者** ] 子樹中進行的註冊，其優先順序會高於在 **HKEY \_ 本機 \_ 電腦** 中所做的相對應註冊的主控台使用者。</span><span class="sxs-lookup"><span data-stu-id="ca267-128">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="ca267-129">針對系統上的新使用者，會使用儲存在 **HKEY \_ 本機 \_ 電腦** 中的設定。</span><span class="sxs-lookup"><span data-stu-id="ca267-129">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="ca267-130">從 Windows XP，[開始] 功能表的網際網路設定會保留在兩個登錄位置的預設專案中：</span><span class="sxs-lookup"><span data-stu-id="ca267-130">As of Windows XP, Start menu Internet settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="ca267-131">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **用戶端** \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="ca267-131">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>
-   <span data-ttu-id="ca267-132">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="ca267-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>

<span data-ttu-id="ca267-133">子機碼 **HKEY \_ 目前的 \_ 使用者** \\ **軟體** \\ **用戶端** \\ **StartMenuInternet** 描述當使用者按一下 [開始] 功能表上的 **網際網路** 圖示時，所啟動的網際網路瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="ca267-133">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** describes the Internet browser that is started when the user clicks the **Internet** icon on the Start menu.</span></span> <span data-ttu-id="ca267-134">如果該子機碼為空白或遺失，則 [開始] 功能表上的 **網際網路** 圖示會設定為儲存在第二個位置的系統預設值 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **StartMenuInternet** ，其中描述系統上安裝的所有網際網路瀏覽器應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-134">If that subkey is blank or missing, then the **Internet** icon on the Start menu is set to the system default stored in the second location at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** , which describes all Internet browser applications that are installed on the system.</span></span>

<span data-ttu-id="ca267-135">當新的使用者登入系統時，[開始] 功能表會在 [ **\_ 本機 \_ 電腦** 軟體用戶端] StartMenuInternet 的子機碼中使用預設值， \\  \\  \\ 以顯示預設的網際網路用戶端，並在按一下該圖示時啟動已註冊的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-135">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** to display the default Internet client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-internet-client"></a><span data-ttu-id="ca267-136">如何註冊為預設的網際網路用戶端</span><span class="sxs-lookup"><span data-stu-id="ca267-136">How to Register as the Default Internet Client</span></span>

<span data-ttu-id="ca267-137">在 [ **\_ 本機 \_ 電腦** 軟體用戶端 HKEY] 子機碼底下 \\  \\  \\ **StartMenuInternet** 可以有零個或多個子機碼，每個已註冊的網際網路瀏覽器應用程式一個</span><span class="sxs-lookup"><span data-stu-id="ca267-137">Below the subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** there can be zero or more subkeys, one for each registered Internet browser application.</span></span> <span data-ttu-id="ca267-138">例如，假設系統可能會有這種安排：</span><span class="sxs-lookup"><span data-stu-id="ca267-138">For example, a hypothetical system might have this arrangement:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

<span data-ttu-id="ca267-139">我們將會從虛構公司（稱為 Litware Inc.）示範具有假設瀏覽器的登錄專案。假設亮 View 的可執行檔名稱是 Litview.exe。</span><span class="sxs-lookup"><span data-stu-id="ca267-139">We will demonstrate registry entries with a hypothetical browser called "Lit View" from a fictional company called Litware Inc. Suppose that the executable name for Lit View is Litview.exe.</span></span> <span data-ttu-id="ca267-140">此時會出現 [亮視圖] 的註冊，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ca267-140">The registration of Lit View occurs as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="ca267-141">>localizedstring 資料是 REG \_ SZ 類型， \_ \_ 如果使用路徑變數（例如），則 reg EXPAND sz `%programfiles%` 。</span><span class="sxs-lookup"><span data-stu-id="ca267-141">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="ca267-142">>localizedstring 會提供可執行檔 ( .exe) 或程式庫 ( .dll) 檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="ca267-142">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="ca267-143">請注意，路徑字串的開頭為 "at" 符號 ( @ ) 而且路徑周圍不需要任何引號，不論其內是否有空格。</span><span class="sxs-lookup"><span data-stu-id="ca267-143">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="ca267-144">十進位整數是字串資源的識別碼，包含在指定的 DLL 內，其值會顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="ca267-144">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="ca267-145">這可讓相同的註冊用於多個語言。</span><span class="sxs-lookup"><span data-stu-id="ca267-145">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="ca267-146">每種語言都提供不同的 ResourceDLL.dll。</span><span class="sxs-lookup"><span data-stu-id="ca267-146">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="ca267-147">這可讓系統根據目前選取的語言顯示正確的字串。</span><span class="sxs-lookup"><span data-stu-id="ca267-147">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="ca267-148">下列 REG \_ sz 或 REG \_ EXPAND \_ sz 值會通知 [開始] 功能表當使用者選取 [亮視圖] 作為 [開始] 功能表的網際網路瀏覽器時，所要顯示的預設圖示。</span><span class="sxs-lookup"><span data-stu-id="ca267-148">The following REG\_SZ or REG\_EXPAND\_SZ value informs the Start menu of the default icon to display when the user selects Lit View as the Start menu Internet browser.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

<span data-ttu-id="ca267-149">下列登錄子機碼會指定當使用者按一下 [開始] 功能表上的 [網際網路] 功能表命令時要執行的命令列，並假設 [亮視圖] 是選取的 [開始] 功能表網際網路瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="ca267-149">The following registry subkey specifies a command line to run when the user clicks the Internet menu command on the Start menu, assuming that Lit View is the selected Start menu Internet browser.</span></span> <span data-ttu-id="ca267-150">例如，此命令可能會使用使用者的首頁來開啟瀏覽器，或命令可能會啟動獨立軟體廠商 (ISV) 所覺得的入門使用者介面。</span><span class="sxs-lookup"><span data-stu-id="ca267-150">For example, the command might open the browser with the user's home page or the command could launch an introductory user interface that the independent software vendor (ISV) feels is appropriate.</span></span> <span data-ttu-id="ca267-151">資料的類型是 REG \_ sz 或 reg \_ EXPAND \_ sz，但請注意，因為命令列路徑中有一個空格，可執行檔路徑會以引號括住。</span><span class="sxs-lookup"><span data-stu-id="ca267-151">The data is of type REG\_SZ or REG\_EXPAND\_SZ, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

<span data-ttu-id="ca267-152">當使用者透過 [ [設定程式存取] 和 [電腦預設值 ](cpl-setprogramaccess.md) ] 來指定時 (SPAD) 應該使用亮 View 作為電腦層級的預設網頁瀏覽器，應用程式應該設定下列 REG \_ SZ 專案。</span><span class="sxs-lookup"><span data-stu-id="ca267-152">When the user specifies through [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) that Lit View should be used as the computer-level default web browser, the application should set the following REG\_SZ entry.</span></span> <span data-ttu-id="ca267-153">請注意，由於 SPAD 是以系統管理員許可權執行，因此允許存取此子機碼。</span><span class="sxs-lookup"><span data-stu-id="ca267-153">Note that because SPAD runs with Administrator privileges, access to this subkey is allowed.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> <span data-ttu-id="ca267-154">在 Windows Vista 中，使用者層級的預設網頁瀏覽器應該使用 [ **預設程式** ] 工具來設定，而不是 [ [SPAD](cpl-setprogramaccess.md)]。</span><span class="sxs-lookup"><span data-stu-id="ca267-154">In Windows Vista, the user-level default web browser should be set using the **Default Programs** tool, not [SPAD](cpl-setprogramaccess.md).</span></span>
> 
> <span data-ttu-id="ca267-155">**下列資訊僅適用于 Windows XP。**</span><span class="sxs-lookup"><span data-stu-id="ca267-155">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="ca267-156">如果在 HKEY 本機電腦下註冊電腦層級的預設網頁瀏覽器 \_ \_ （如上所示），則應用程式應該刪除下列子機碼底下的預設專案：</span><span class="sxs-lookup"><span data-stu-id="ca267-156">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> <span data-ttu-id="ca267-157">如果在 HKEY 本機電腦下註冊電腦層級的預設網頁瀏覽器 \_ \_ 失敗，應用程式應該 \_ 為「亮視圖」應用程式設定如下列範例所示的 REG SZ 資料：</span><span class="sxs-lookup"><span data-stu-id="ca267-157">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE fails, the application should set the REG\_SZ data as shown in this example for the Lit View application:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

<span data-ttu-id="ca267-158">更新適當的子機碼之後，應用程式會廣播 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) 訊息，並將其 *wParam* 參數設定為0，並將其 *lParam* 參數指向以 null 終止的字串 `"Software\Clients\StartMenuInternet"` 。</span><span class="sxs-lookup"><span data-stu-id="ca267-158">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\StartMenuInternet"`.</span></span> <span data-ttu-id="ca267-159">這會通知作業系統預設用戶端已變更。</span><span class="sxs-lookup"><span data-stu-id="ca267-159">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="ca267-160">針對預設的 [開始] 功能表網際網路瀏覽器設定這些子機碼，必須保持與舊版網頁瀏覽器的回溯相容性，而這些網頁瀏覽器不支援每一使用者的註冊。</span><span class="sxs-lookup"><span data-stu-id="ca267-160">Setting these subkeys for the default Start menu Internet browser is necessary to preserve backward compatibility with old web browsers that do not support per-user registrations.</span></span>

## <a name="registering-for-the-start-menu-email-link"></a><span data-ttu-id="ca267-161">註冊 [開始] 功能表電子郵件連結</span><span class="sxs-lookup"><span data-stu-id="ca267-161">Registering for the Start Menu Email Link</span></span>

> [!Note]  
> <span data-ttu-id="ca267-162">從 Windows 7 起，已移除 [開始] 功能表電子郵件] 連結。</span><span class="sxs-lookup"><span data-stu-id="ca267-162">The Start menu Email link has been removed as of Windows 7.</span></span> <span data-ttu-id="ca267-163">不過，本章節中討論的這項註冊仍應針對其對指派預設 MAPI 用戶端的影響執行。</span><span class="sxs-lookup"><span data-stu-id="ca267-163">However, this registration discussed in this section should still be performed for its effect in assigning the default MAPI client.</span></span>

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a><span data-ttu-id="ca267-164">[開始] 功能表如何顯示預設電子郵件客戶</span><span class="sxs-lookup"><span data-stu-id="ca267-164">How the Start Menu Displays the Default Email Client</span></span>

<span data-ttu-id="ca267-165">任何電子郵件應用程式都可以註冊，以在 [開始] 功能表上顯示為電子郵件客戶程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-165">Any email application can register to appear as an email client on the Start menu.</span></span> <span data-ttu-id="ca267-166">此可見度與適當的應用程式[檔案和](fa-intro.md)[通訊協定](/previous-versions//aa767743(v=vs.85))類型註冊結合，可提供應用程式預設的郵件狀態。</span><span class="sxs-lookup"><span data-stu-id="ca267-166">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default mail status.</span></span>

<span data-ttu-id="ca267-167">在 [ **HKEY \_ 目前 \_ 使用者** ] 子樹中進行的註冊，其優先順序會高於在 **HKEY \_ 本機 \_ 電腦** 中所做的相對應註冊的主控台使用者。</span><span class="sxs-lookup"><span data-stu-id="ca267-167">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="ca267-168">針對系統上的新使用者，會使用儲存在 **HKEY \_ 本機 \_ 電腦** 中的設定。</span><span class="sxs-lookup"><span data-stu-id="ca267-168">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="ca267-169">從 Windows XP，[開始] 功能表的電子郵件設定會保留在兩個登錄位置的預設專案中：</span><span class="sxs-lookup"><span data-stu-id="ca267-169">As of Windows XP, Start menu Email settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="ca267-170">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **用戶端** \\ **郵件**</span><span class="sxs-lookup"><span data-stu-id="ca267-170">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>
-   <span data-ttu-id="ca267-171">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件**</span><span class="sxs-lookup"><span data-stu-id="ca267-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>

<span data-ttu-id="ca267-172">子機碼 **HKEY \_ CURRENT \_ user** \\ **SOFTWARE** \\ **Clients** \\ **Mail** 描述當使用者按一下 [開始] 功能表上的 **電子郵件** 圖示時，所啟動的電子郵件客戶程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-172">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email client that is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="ca267-173">子 **機碼 HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件** 會描述安裝在系統上的電子郵件應用程式，以及預設的電子郵件應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-173">The subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email applications that are installed on the system, as well as the default email application.</span></span>

<span data-ttu-id="ca267-174">如果 **HKEY \_ CURRENT \_ USER** \\ **software** \\ **用戶端** \\ **郵件** 為空白或遺失，則會使用 [ **HKEY \_ 本機 \_ 電腦** 軟體用戶端郵件] 中定義的預設值 \\  \\  \\ 來選取出現在 [開始] 功能表上的電子郵件應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-174">If the **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** is blank or missing, the default value defined in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** is used to select the email application that appears on the Start menu.</span></span>

<span data-ttu-id="ca267-175">當新的使用者登入系統時，[開始] 功能表會使用子機碼中 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件** 的預設值來顯示預設電子郵件客戶程式，並在按一下該圖示時啟動已註冊的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-175">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** to display the default email client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-email-client"></a><span data-ttu-id="ca267-176">如何註冊為預設電子郵件客戶</span><span class="sxs-lookup"><span data-stu-id="ca267-176">How to Register as the Default EMail Client</span></span>

<span data-ttu-id="ca267-177">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件** 可以包含零或多個子機碼，每個已註冊的電子郵件應用程式都有一個。</span><span class="sxs-lookup"><span data-stu-id="ca267-177">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** can contain zero or more subkeys, one for each registered email application.</span></span> <span data-ttu-id="ca267-178">例如，假設系統可能會定義下列子機碼：</span><span class="sxs-lookup"><span data-stu-id="ca267-178">For example, a hypothetical system might define the following subkeys:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

<span data-ttu-id="ca267-179">我們將示範名為 Litware Inc. Litware Inc. 之虛構公司的假設電子郵件客戶的登錄專案，其名為 "LitMail" 的虛構公司的電子郵件用戶端。</span><span class="sxs-lookup"><span data-stu-id="ca267-179">We will demonstrate registry entries with a hypothetical email client called "Lit Mail" from the fictional company called Litware Inc. Litware Inc. decides to register this email client under the internal name "LitMail".</span></span> <span data-ttu-id="ca267-180">如同瀏覽器，內部名稱是用來做為子機碼名稱的唯一字串，但永遠不會向使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="ca267-180">As with a browser, the internal name is a unique string used as the subkey name, but it is never shown to the user.</span></span>

<span data-ttu-id="ca267-181">若要安裝 Lit Mail 電子郵件用戶端作為預設值，則會使用下列子機碼和其專案：</span><span class="sxs-lookup"><span data-stu-id="ca267-181">To install the Lit Mail email client as the default, they use the following subkey and its entries:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

<span data-ttu-id="ca267-182">>localizedstring 資料是 REG \_ SZ 類型， \_ \_ 如果使用路徑變數（例如），則 reg EXPAND sz `%programfiles%` 。</span><span class="sxs-lookup"><span data-stu-id="ca267-182">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="ca267-183">>localizedstring 會提供可執行檔 ( .exe) 或程式庫 ( .dll) 檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="ca267-183">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="ca267-184">請注意，路徑字串的開頭為 "at" 符號 ( @ ) 而且路徑周圍不需要任何引號，不論其內是否有空格。</span><span class="sxs-lookup"><span data-stu-id="ca267-184">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="ca267-185">十進位整數是字串資源的識別碼，包含在指定的 DLL 內，其值會顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="ca267-185">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="ca267-186">這可讓相同的註冊用於多個語言。</span><span class="sxs-lookup"><span data-stu-id="ca267-186">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="ca267-187">每種語言都提供不同的 ResourceDLL.dll。</span><span class="sxs-lookup"><span data-stu-id="ca267-187">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="ca267-188">這可讓系統根據目前選取的語言顯示正確的字串。</span><span class="sxs-lookup"><span data-stu-id="ca267-188">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="ca267-189">更新適當的子機碼之後，應用程式會廣播 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) 訊息，並將其 *wParam* 參數設定為0，並將其 *lParam* 參數指向以 null 終止的字串 `"Software\Clients\Mail"` 。</span><span class="sxs-lookup"><span data-stu-id="ca267-189">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\Mail"`.</span></span> <span data-ttu-id="ca267-190">這會通知作業系統預設用戶端已變更。</span><span class="sxs-lookup"><span data-stu-id="ca267-190">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="ca267-191">為了與不支援當地語系化字串的應用程式回溯相容，已安裝語言中的應用程式名稱也應該設定為子機碼的預設值。</span><span class="sxs-lookup"><span data-stu-id="ca267-191">For backward compatibility with applications that do not support localized strings, the name of the application in the installed language should also be set as the default value for the subkey.</span></span>

<span data-ttu-id="ca267-192">下列 **reg \_ Sz** 或 **REG \_ EXPAND \_ Sz** 值會在使用者選取 Lit mail 做為 [開始] 功能表 mail 程式時，通知顯示預設圖示的 [開始] 功能表：</span><span class="sxs-lookup"><span data-stu-id="ca267-192">The following **REG\_SZ** or **REG\_EXPAND\_SZ** value informs the Start menu of the default icon to display when the user selects Lit Mail as the Start menu mail program:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

<span data-ttu-id="ca267-193">下列專案會指定當使用者按一下 [開始] 功能表上的 [ **電子郵件** ] 功能表項目時要執行的命令列，並假設 [Lit mail] 是選取的 [開始] 功能表電子郵件程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-193">The following entry specifies a command line to run when the user clicks the **E-mail** menu item on the Start menu, assuming that Lit Mail is the selected Start menu email program.</span></span> <span data-ttu-id="ca267-194">如果使用者從 Windows Internet Explorer [**工具**] 功能表選取 [**讀取電子郵件**]，也會執行此命令列。</span><span class="sxs-lookup"><span data-stu-id="ca267-194">This command line is also run if the user selects **Read email** from the Windows Internet Explorer **Tools** menu.</span></span> <span data-ttu-id="ca267-195">資料的類型是 **REG \_ Sz** 或 **reg \_ EXPAND \_ sz**，但請注意，因為命令列路徑中有一個空格，可執行檔路徑會以引號括住。</span><span class="sxs-lookup"><span data-stu-id="ca267-195">The data is of type **REG\_SZ** or **REG\_EXPAND\_SZ**, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

<span data-ttu-id="ca267-196">如果 (，而且只有在) *使用者* 將 [lit mail] 指定為預設 [開始] 功能表電子郵件應用程式時，則 lit mail 應用程式可能會將其內部名稱寫入至下列 **REG \_ SZ** 值：</span><span class="sxs-lookup"><span data-stu-id="ca267-196">If (and only if) *the user* specifies Lit Mail to be the default Start menu email application, the Lit Mail application may write its internal name to the following **REG\_SZ** value:</span></span>

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="ca267-197">如果 (，而且只有在) *使用者* 將 Lit mail 指定為全系統的預設電子郵件應用程式時，lit mail 應用程式可能會將其內部名稱寫入至下列指定的 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="ca267-197">If (and only if) *the user* specifies Lit Mail to be the system-wide default email application, the Lit Mail application may write its internal name to the **REG\_SZ** value specified below.</span></span> <span data-ttu-id="ca267-198">請注意，這個子機碼的存取權可能會受到限制。</span><span class="sxs-lookup"><span data-stu-id="ca267-198">Note that access to this subkey might be restricted.</span></span> <span data-ttu-id="ca267-199">應用程式不應假設所有使用者都有變更全系統預設電子郵件應用程式的許可權。</span><span class="sxs-lookup"><span data-stu-id="ca267-199">Applications should not assume that all users have permission to change the system-wide default email application.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="ca267-200">註冊為預設的 [開始] 功能表電子郵件應用程式，並不等同于註冊為系統預設電子郵件客戶程式或註冊的 *mailto* 處理常式。</span><span class="sxs-lookup"><span data-stu-id="ca267-200">Registration as the default Start menu email application is not equivalent to registration as the system default email client or the registered *mailto* handler.</span></span>

-   <span data-ttu-id="ca267-201">當使用者按一下 Internet Explorer [**工具**] 功能表中的 [**讀取電子郵件**] 時，就會啟動系統預設電子郵件客戶程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-201">The system default email client is started when the user clicks **Read email** from the Internet Explorer **Tools** menu.</span></span>
-   <span data-ttu-id="ca267-202">當使用者按一下表單的 URL 時，即會啟動註冊的 *mailto* 處理常式 `mailto:someone@example.com` 。</span><span class="sxs-lookup"><span data-stu-id="ca267-202">The registered *mailto* handler is started when the user clicks a URL of the form `mailto:someone@example.com`.</span></span>
-   <span data-ttu-id="ca267-203">當使用者按一下 [開始] 功能表上的 [ **電子郵件** ] 圖示時，就會啟動 [開始] 功能表電子郵件應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-203">The Start menu email application is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="ca267-204">如果未指定預設的 [開始] 功能表電子郵件應用程式，[開始] 功能表的電子郵件圖示就會啟動系統預設的電子郵件客戶程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-204">If no default Start menu email application is specified, the Email icon on the Start menu launches the system default email client.</span></span>

<span data-ttu-id="ca267-205">本主題並未涵蓋將應用程式註冊為預設 *mailto* 通訊協定處理常式的程式。</span><span class="sxs-lookup"><span data-stu-id="ca267-205">This topic does not cover registration of the application as the default *mailto* protocol handler.</span></span> <span data-ttu-id="ca267-206">想要以這種方式註冊的應用程式應該繼續遵循本主題的現有規格。</span><span class="sxs-lookup"><span data-stu-id="ca267-206">Applications that want to register in such a manner should continue to follow existing specifications on this subject.</span></span>

## <a name="customizing-the-context-menu"></a><span data-ttu-id="ca267-207">自訂內容功能表</span><span class="sxs-lookup"><span data-stu-id="ca267-207">Customizing the Context Menu</span></span>

<span data-ttu-id="ca267-208">應用程式可以自訂使用者從 **電子郵件** 中選取 **屬性** 時所顯示的屬性頁 (或 **網際網路**) 圖示的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="ca267-208">An application can customize the property pages that are displayed when the user selects **Properties** from the **E-mail** (or **Internet**) icon's shortcut menu.</span></span> <span data-ttu-id="ca267-209">例如，Litware 電子郵件應用程式會新增下列 **REG \_ Sz** 或 **REG \_ EXPAND \_ sz** 資料，以顯示 **電子郵件** 圖示的自訂屬性工作表，而不是其預設屬性表。</span><span class="sxs-lookup"><span data-stu-id="ca267-209">For example, the Litware email application adds the following **REG\_SZ** or **REG\_EXPAND\_SZ** data to display a custom property sheet for the **E-mail** icon rather than its default property sheet.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

<span data-ttu-id="ca267-210">MUIVerb 資料項目是以 "at" 正負號 ( @ ) 開始，後面接著資源 DLL 的完整路徑、逗號、減號 ( ) ，然後是要顯示的十進位字串資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca267-210">The MUIVerb data item is constructed beginning with an "at" sign (@), followed by the full path to the resource DLL, a comma, a minus sign (-), and then the decimal string resource identifier to display.</span></span> <span data-ttu-id="ca267-211">請注意，LitMail.exe 程式的路徑包含空格，因此路徑字串會放置在引號內。</span><span class="sxs-lookup"><span data-stu-id="ca267-211">Note that the path to the LitMail.exe program contains spaces, so the path string is placed inside quotation marks.</span></span>

<span data-ttu-id="ca267-212">應用程式也可以在內容功能表中新增其他命令。</span><span class="sxs-lookup"><span data-stu-id="ca267-212">An application can also add additional commands to the context menu.</span></span> <span data-ttu-id="ca267-213">例如，Litware 電子郵件應用程式會新增具有下列 **REG \_ SZ** 資料的 **find** 命令：</span><span class="sxs-lookup"><span data-stu-id="ca267-213">For example, the Litware email application adds a **find** command with the following **REG\_SZ** data:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

<span data-ttu-id="ca267-214">**Shell** 下的子機碼名稱 (在此案例中，"find" ) 是任意的未當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="ca267-214">The subkey name below **shell** (in this case, "find") is an arbitrary, nonlocalized name.</span></span> <span data-ttu-id="ca267-215">同樣地，MUIVerb 的資料也會包含 "at" 符號 ( @ ) 作為第一個元素，後面接著資源 DLL 的路徑、逗號分隔字元，然後是小數點字串資源識別碼前面的減號。</span><span class="sxs-lookup"><span data-stu-id="ca267-215">Once again the MUIVerb data contains an "at" sign (@) as the first element, followed by the path to a resource DLL, a comma separator, and then a minus sign preceding the decimal string resource identifier.</span></span> <span data-ttu-id="ca267-216">例如，該字串資源可能是「開啟通訊錄」。</span><span class="sxs-lookup"><span data-stu-id="ca267-216">For example, that string resource might be "Open Address Book".</span></span> <span data-ttu-id="ca267-217">最後，請注意，命令列字串包含空格，因此會以引號括住。</span><span class="sxs-lookup"><span data-stu-id="ca267-217">Finally, note that the command-line string contains spaces, so it is enclosed in quotation marks.</span></span>

 

 
