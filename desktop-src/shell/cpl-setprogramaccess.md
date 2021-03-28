---
description: 本主題討論主控台中找到的 (SPAD) 功能設定程式存取和電腦預設值。
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: " (SPAD) 設定程式存取和電腦預設值"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f35d9ed70d382e2db6714082ade2d2d76e6ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191178"
---
# <a name="set-program-access-and-computer-defaults-spad"></a><span data-ttu-id="c4bdc-103"> (SPAD) 設定程式存取和電腦預設值</span><span class="sxs-lookup"><span data-stu-id="c4bdc-103">Set Program Access and Computer Defaults (SPAD)</span></span>

<span data-ttu-id="c4bdc-104">本主題討論主控台中找到的 **(SPAD) 功能設定程式存取和電腦預設值** 。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-104">This topic discusses the **Set Program Access and Computer Defaults (SPAD)** feature found in Control Panel.</span></span> <span data-ttu-id="c4bdc-105">SPAD 位於 Windows Vista 和更新版本的 Windows 中 [預設程式](default-programs.md) 主控台專案。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-105">SPAD is located under the [Default Programs](default-programs.md) Control Panel item in Windows Vista and later versions of Windows.</span></span> <span data-ttu-id="c4bdc-106">在 Windows XP 中，它位於 [ **新增或移除程式** ] 專案中，並且標題為 [ **設定程式存取和預設值**]。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-106">In Windows XP, it is located in the **Add or Remove Programs** item and titled **Set Program Access and Defaults**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4bdc-107">本主題不適用於 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="c4bdc-108">預設檔案關聯在 Windows 10 中的運作方式有所變更。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="c4bdc-109">如需詳細資訊，請參閱 [這篇文章](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)中有關 **Windows 10 如何處理預設應用程式的變更** 一節。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

-   <span data-ttu-id="c4bdc-110">[使用 [設定程式存取和電腦預設值] 工具](#using-the-set-program-access-and-computer-defaults-tool)</span><span class="sxs-lookup"><span data-stu-id="c4bdc-110">[Using the Set Program Access and Computer Defaults Tool](#using-the-set-program-access-and-computer-defaults-tool)</span></span>
    -   [<span data-ttu-id="c4bdc-111">設定程式存取和電腦預設值的總覽</span><span class="sxs-lookup"><span data-stu-id="c4bdc-111">An Overview of Set Program Access and Computer Defaults</span></span>](#an-overview-of-set-program-access-and-computer-defaults)
    -   [<span data-ttu-id="c4bdc-112">LastUserInitiatedDefaultChange 登錄值</span><span class="sxs-lookup"><span data-stu-id="c4bdc-112">The LastUserInitiatedDefaultChange Registry Value</span></span>](#the-lastuserinitiateddefaultchange-registry-value)
-   [<span data-ttu-id="c4bdc-113">篩選新增或移除程式清單</span><span class="sxs-lookup"><span data-stu-id="c4bdc-113">Filtering the Add or Remove Programs List</span></span>](#filtering-the-add-or-remove-programs-list)
-   [<span data-ttu-id="c4bdc-114">其他資源</span><span class="sxs-lookup"><span data-stu-id="c4bdc-114">Additional Resources</span></span>](#filtering-the-add-or-remove-programs-list)
-   [<span data-ttu-id="c4bdc-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4bdc-115">Related topics</span></span>](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a><span data-ttu-id="c4bdc-116">使用 [設定程式存取和電腦預設值] 工具</span><span class="sxs-lookup"><span data-stu-id="c4bdc-116">Using the Set Program Access and Computer Defaults Tool</span></span>

> [!Note]  
> <span data-ttu-id="c4bdc-117">從 Windows 8，SPAD 會針對目前的使用者，以每個使用者為基礎來設定預設值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-117">As of Windows 8, SPAD configures defaults on a per-user basis for the current user.</span></span> <span data-ttu-id="c4bdc-118">在 Windows 8 之前，SPAD 設定每一電腦預設值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-118">Prior to Windows 8, SPAD set per-computer defaults.</span></span> <span data-ttu-id="c4bdc-119">當使用者尚未設定每位使用者的預設值時，系統會提示他們設定每位使用者預設值，而不是回復每部電腦的預設值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-119">When a per-user default has not yet been configured by the user, the system will prompt them to set a per-user default rather than falling back on a per-machine default.</span></span> <span data-ttu-id="c4bdc-120">Windows Vista 和 Windows 7 中的使用者在先前設定每個使用者預設值時，可能永遠不會看到每部電腦的預設值，因為每個使用者預設會覆寫這些作業系統中的每一電腦預設值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-120">It's possible that the per-machine defaults were never seen by users in Windows Vista and Windows 7 if they had previously set per-user defaults, because per-user defaults override per-computer defaults in those operating systems.</span></span>

 

<span data-ttu-id="c4bdc-121">在 Windows XP 中，[ **設定程式存取和預設值** ] 是在主控台的 [ **新增或移除程式** ] 專案中找到選項的工具。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-121">In Windows XP, **Set Program Access and Defaults** is a tool found as an option in Control Panel's **Add or Remove Programs** item.</span></span> <span data-ttu-id="c4bdc-122">在 Windows Vista 和更新版本中，它位於 [ [預設程式](default-programs.md) ] 主控台專案下。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-122">In Windows Vista and later, it is located under the [Default Programs](default-programs.md) Control Panel item.</span></span> <span data-ttu-id="c4bdc-123">針對 [已註冊](reg-middleware-apps.md) 的程式，它會執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="c4bdc-123">For [registered](reg-middleware-apps.md) programs, it performs the following functions:</span></span>

-   <span data-ttu-id="c4bdc-124">可為每個用戶端類型選擇預設程式， (最多隻) Windows 7。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-124">Enables the choice of default programs for each client type (up to Windows 7 only).</span></span>
-   <span data-ttu-id="c4bdc-125">可控制程式圖示、快捷方式和功能表項目的顯示。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-125">Enables control of the display of the program's icons, shortcuts, and menu entries.</span></span>
-   <span data-ttu-id="c4bdc-126">提供一組預設的預設程式選項。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-126">Provides a set of preset default program choices.</span></span> <span data-ttu-id="c4bdc-127"> (Windows XP Service Pack 1 (SP1) 僅) </span><span class="sxs-lookup"><span data-stu-id="c4bdc-127">(Windows XP Service Pack 1 (SP1) only)</span></span>

<span data-ttu-id="c4bdc-128">這項工具會用於下列五種用戶端類型。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-128">This tool is used for the following five client types.</span></span>

-   <span data-ttu-id="c4bdc-129">瀏覽器</span><span class="sxs-lookup"><span data-stu-id="c4bdc-129">Browser</span></span>
-   <span data-ttu-id="c4bdc-130">電子郵件</span><span class="sxs-lookup"><span data-stu-id="c4bdc-130">Email</span></span>
-   <span data-ttu-id="c4bdc-131">立即的傳送程式</span><span class="sxs-lookup"><span data-stu-id="c4bdc-131">Instant messenging program</span></span>
-   <span data-ttu-id="c4bdc-132">媒體播放器</span><span class="sxs-lookup"><span data-stu-id="c4bdc-132">Media player</span></span>
-   <span data-ttu-id="c4bdc-133">適用于 JAVA 的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="c4bdc-133">Virtual machine for Java</span></span>

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a><span data-ttu-id="c4bdc-134">設定程式存取和電腦預設值的總覽</span><span class="sxs-lookup"><span data-stu-id="c4bdc-134">An Overview of Set Program Access and Computer Defaults</span></span>

<span data-ttu-id="c4bdc-135">下列螢幕擷取畫面顯示 Windows 8 **設定程式存取和電腦預設值** ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-135">The Windows 8 **Set Program Access and Computer Defaults** page is shown in the following screen shot.</span></span>

![[設定程式存取和電腦預設值] 專案視圖的螢幕擷取畫面](images/spad-initial.png)

<span data-ttu-id="c4bdc-137">有三個可能的設定選項會顯示給使用者，讓 Oem 有選項顯示名為「電腦製造商」的第四個選項。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-137">Three possible configuration options are presented to the user, with the option for OEMs to present a fourth option titled "Computer Manufacturer".</span></span>

-   [<span data-ttu-id="c4bdc-138">Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="c4bdc-138">Microsoft Windows</span></span>](#microsoft-windows)
-   [<span data-ttu-id="c4bdc-139">非 Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4bdc-139">Non-Microsoft</span></span>](#non-microsoft)
-   [<span data-ttu-id="c4bdc-140">Custom</span><span class="sxs-lookup"><span data-stu-id="c4bdc-140">Custom</span></span>](#custom)
-   [<span data-ttu-id="c4bdc-141">電腦製造商</span><span class="sxs-lookup"><span data-stu-id="c4bdc-141">Computer Manufacturer</span></span>](#computer-manufacturer)

### <a name="microsoft-windows"></a><span data-ttu-id="c4bdc-142">Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="c4bdc-142">Microsoft Windows</span></span>

<span data-ttu-id="c4bdc-143">**Microsoft windows** 設定是由 Windows 提供的一組預設程式所組成，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-143">The **Microsoft Windows** configuration consists of a set of default programs provided with Windows, as shown in the following screen shot.</span></span>

![[設定程式存取和預設 microsoft 選項] 的螢幕擷取畫面](images/mspage.png)

<span data-ttu-id="c4bdc-145">選取 **Microsoft Windows** 設定也可讓您顯示針對五種用戶端類型中任何一種註冊之程式的圖示、快捷方式或功能表項目。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-145">Selecting the **Microsoft Windows** configuration also enables the display of the icons, shortcuts, or menu entries for each program registered for any of the five client types.</span></span> <span data-ttu-id="c4bdc-146">使用者可以在 [ **開始** ] 功能表或開始畫面、桌面上以及新增的所有其他位置，使用這些圖示、快捷方式和功能表項目。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-146">Those icons, shortcuts, and menu entries are available to the user in the **Start** menu or Start screen, on the desktop, and in all other locations to which they were added.</span></span>

### <a name="non-microsoft"></a><span data-ttu-id="c4bdc-147">非 Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4bdc-147">Non-Microsoft</span></span>

<span data-ttu-id="c4bdc-148">下列螢幕擷取畫面中所示的 **非 microsoft** 設定，可用於使用者系統上不是由 Microsoft 所產生的已註冊應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-148">The **Non-Microsoft** configuration, shown in the following screen shot, is used for registered applications on the user's system that are not produced by Microsoft.</span></span> <span data-ttu-id="c4bdc-149">這些應用程式可以預先安裝在使用者的系統上，也可以是使用者已安裝的非 Microsoft 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-149">These applications can be preinstalled on the user's system, or they can be non-Microsoft applications that the user has installed.</span></span>

> [!Note]  
> <span data-ttu-id="c4bdc-150">應用程式必須註冊才能顯示在此頁面上。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-150">Applications must register to appear on this page.</span></span> <span data-ttu-id="c4bdc-151">如需註冊應用程式的指示，請參閱 [使用用戶端類型註冊程式](reg-middleware-apps.md)。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-151">For instructions on registering an application, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

 

![[設定程式存取和預設非 microsoft 選項] 選項的螢幕擷取畫面](images/nonmspage.png)

<span data-ttu-id="c4bdc-153">選取 [ **非 Microsoft** ] 選項，也會移除所有具有 microsoft [Windows](#microsoft-windows) 設定中所列 microsoft 程式的圖示、快捷方式和功能表項目的存取權。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-153">Selecting the **Non-Microsoft** option also removes access to the icons, shortcuts, and menu entries of the Microsoft programs listed in the [Microsoft Windows](#microsoft-windows) configuration for all client types that have them.</span></span> <span data-ttu-id="c4bdc-154">這些 Microsoft 圖示、快捷方式和功能表項目會從 [ **開始** ] 功能表、桌面及新增這些專案的其他位置移除。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-154">These Microsoft icons, shortcuts, and menu entries are removed from the **Start** menu, the desktop, and other locations to which they were added.</span></span>

### <a name="custom"></a><span data-ttu-id="c4bdc-155">自訂</span><span class="sxs-lookup"><span data-stu-id="c4bdc-155">Custom</span></span>

<span data-ttu-id="c4bdc-156">**自訂** 設定（如下列螢幕擷取畫面所示）可讓使用者使用 Microsoft 和非 microsoft 程式的任何組合（註冊為五個用戶端類型的預設可能性）來自訂其系統。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-156">The **Custom** configuration, shown in the following screen shot, enables users to customize their systems with any combination of Microsoft and non-Microsoft programs registered as default possibilities for the five client types.</span></span> <span data-ttu-id="c4bdc-157">這是 Windows 2000 Service Pack 3 (SP3) 唯一提供的四個選項之一。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-157">This is the only one of the four options available in Windows 2000 Service Pack 3 (SP3).</span></span>

![[設定程式存取] 和 [預設自訂] 選項的螢幕擷取畫面](images/custompage.png)

<span data-ttu-id="c4bdc-159">[Microsoft Windows](#microsoft-windows)和 [非 Microsoft](#non-microsoft)設定中提供的所有選項都可供 **自訂** 章節中的使用者使用，以及任何其他不屬於 Windows 的其他已安裝 microsoft 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-159">All options presented in the [Microsoft Windows](#microsoft-windows) and [Non-Microsoft](#non-microsoft) configurations are available to the user in the **Custom** section, as well as any additionally installed Microsoft applications that are not part of Windows.</span></span> <span data-ttu-id="c4bdc-160">[ **使用我目前的網頁瀏覽器** ] 選項按鈕已預先選取，如先前的螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-160">The **Use my current web browser** radio button is preselected, as shown in the preceding screen shot.</span></span> <span data-ttu-id="c4bdc-161">沒有任何方法可以從 UI 判斷目前的預設瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-161">There is no way to determine the current default browser from the UI.</span></span> <span data-ttu-id="c4bdc-162">在 Windows 中叫用網頁連結或檔案，是探索目前預設瀏覽器的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-162">Invoking web links or files in Windows is the only way to discover the current default browser.</span></span>

<span data-ttu-id="c4bdc-163">當使用者選取某個程式的 [ **啟用對這個程式的存取** ] 核取方塊時，該程式的圖示、快捷方式和功能表項目會顯示在 [開始] 功能表或開始畫面、桌面上或已安裝的任何其他位置。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-163">When a user selects the **Enable access to this program** check box for a program, that program's icons, shortcuts, and menu entries are displayed in the Start menu or Start screen, on the desktop, or in any other location where they were installed.</span></span> <span data-ttu-id="c4bdc-164">清除此選項應該會移除這些圖示、快捷方式和功能表項目，不過這些選項的行為方式完全取決於應用程式廠商。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-164">Clearing this option should remove those icons, shortcuts, and menu entries, however, how these options behave is entirely up to the application vendor.</span></span> <span data-ttu-id="c4bdc-165">Windows 不會控制在整個 UI 中啟用或移除存取的方式。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-165">Windows does not control how access is enabled or removed throughout the UI.</span></span> <span data-ttu-id="c4bdc-166">也請務必瞭解，應用程式不需要註冊 **設定程式存取和電腦預設值**。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-166">It is also important to understand that applications are not required to register for **Set Program Access and Computer Defaults**.</span></span>

### <a name="computer-manufacturer"></a><span data-ttu-id="c4bdc-167">電腦製造商</span><span class="sxs-lookup"><span data-stu-id="c4bdc-167">Computer Manufacturer</span></span>

<span data-ttu-id="c4bdc-168">第四個名為「電腦製造商」的類別，可以出現在某些系統的 SPAD 視窗中。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-168">A fourth category titled "Computer Manufacturer" can appear in the SPAD window on some systems.</span></span> <span data-ttu-id="c4bdc-169">電腦製造商可以選擇使用一組自訂的預設值來預先設定電腦，並從 [自訂](#custom) 設定中提供的相同選項中進行選擇。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-169">Computer manufacturers can choose to preconfigure their computers with a custom set of defaults, choosing from the same selections available in the [Custom](#custom) configuration.</span></span> <span data-ttu-id="c4bdc-170"> (為了方便說明，我們會註冊一組稱為 LitWare 的虛構應用程式，以搭配所有用戶端類型使用 ) 。您可以選擇 [電腦製造商] 選項，選擇 [ **電腦製造商** ] 選項，讓使用者隨時都能返回電腦製造商的預設設定，如下列 Windows XP 螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-170">(For illustrative purposes, a fictional set of applications called LitWare is registered for use with all client types.) A user can return to the computer manufacturer's default configuration at any time by choosing the **Computer Manufacturer** option, as shown in the following Windows XP screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="c4bdc-171">此設定不會出現在所有系統上。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-171">This configuration does not appear on all systems.</span></span> <span data-ttu-id="c4bdc-172">如需詳細資訊，請參閱 OEM 預先安裝套件 (OPK) 。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-172">For details, refer to the OEM Preinstallation Kit (OPK).</span></span>

 

![[設定程式存取和預設電腦製造商] 選項的螢幕擷取畫面](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a><span data-ttu-id="c4bdc-174">LastUserInitiatedDefaultChange 登錄值</span><span class="sxs-lookup"><span data-stu-id="c4bdc-174">The LastUserInitiatedDefaultChange Registry Value</span></span>

<span data-ttu-id="c4bdc-175">LastUserInitiatedDefaultChange 值已新增至登錄，以協助應用程式辨識和尊重使用者的預設選項。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-175">The LastUserInitiatedDefaultChange value has been added to the registry to assist applications in recognizing and respecting the user's default choices.</span></span> <span data-ttu-id="c4bdc-176">值 \_ 以 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構的形式來保存 REG 二進位資料，其中包含上次使用者透過 [ **設定程式存取和電腦預設值** ] 工具變更預設值時，國際標準時間 (UTC) ) 的日期和時間 (。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-176">The value holds REG\_BINARY data in the form of a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the date and time (in Coordinated Universal Time (UTC)) of the last time the user changed a default choice through the **Set Program Access and Computer Defaults** tool.</span></span> <span data-ttu-id="c4bdc-177">您可以在下列子機碼底下找到此值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-177">This value is found under the following subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

<span data-ttu-id="c4bdc-178">下列案例會針對監視檔案關聯的應用程式使用此值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-178">The following scenario uses this value for an application that monitors file associations.</span></span>

1.  <span data-ttu-id="c4bdc-179">應用程式會在安裝時記錄最後將時間設定為其用戶端類型預設程式的時間， (在安裝期間或稍後) 。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-179">An application internally records the time when it was last set as the default program for its client type (either at installation or at a later time).</span></span>
2.  <span data-ttu-id="c4bdc-180">應用程式會偵測到其用戶端類型的預設程式已變更為本身以外的程式，或在背景 helper 程式) 的情況下，它所代表的應用程式 (。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-180">The application detects that the default program for its client type has been changed to a program other than itself or the application it represents (in the case of background helper programs).</span></span> <span data-ttu-id="c4bdc-181">Windows 8 不支援。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-181">Not supported in Windows 8.</span></span>
3.  <span data-ttu-id="c4bdc-182">應用程式會讀取 LastUserInitiatedDefaultChange 的值 (上次使用者起始之預設變更) 的時間戳記，並將其與儲存作為預設值的時間戳記值進行比較。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-182">The application reads the value of LastUserInitiatedDefaultChange (the time stamp of the last user-initiated default change) and compares it to the time stamp value it has stored for its own choice as default.</span></span>
4.  <span data-ttu-id="c4bdc-183">如果 LastUserInitiatedDefaultChange 晚于應用程式的儲存值，則該應用程式不應採取任何動作，因為使用者透過 [ **設定程式存取和預設值** ] 工具明確要求變更。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-183">If LastUserInitiatedDefaultChange is later than the application's stored value, then no action should be taken by that application because the change was explicitly requested by the user through the **Set Program Access and Defaults** tool.</span></span>
5.  <span data-ttu-id="c4bdc-184">應用程式在再次選擇為預設值之前，不會再監視該檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-184">The application no longer monitors that file association until it is again chosen as the default.</span></span> <span data-ttu-id="c4bdc-185">Windows 8 不支援。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-185">Not supported in Windows 8.</span></span>

<span data-ttu-id="c4bdc-186">藉由遵守這種配置，將會遵守使用者的期望，並維護其系統的最終擁有權。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-186">By adhering to such a scheme, the user's wishes are respected and their ultimate ownership of their systems is maintained.</span></span>

## <a name="filtering-the-add-or-remove-programs-list"></a><span data-ttu-id="c4bdc-187">篩選新增或移除程式清單</span><span class="sxs-lookup"><span data-stu-id="c4bdc-187">Filtering the Add or Remove Programs List</span></span>

> [!Note]  
> <span data-ttu-id="c4bdc-188">本節適用于 Windows XP Service Pack 2 (SP2) 和更新版本，以及 Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-188">This section applies to Windows XP Service Pack 2 (SP2) and later and Windows Server 2003 and later.</span></span>

 

<span data-ttu-id="c4bdc-189">在 Windows XP 和 Windows Server 2003 中，[**新增或移除程式**] 底下的 [**變更或移除程式**] 索引標籤中所顯示的應用程式清單，可以由使用者篩選以排除應用程式更新的專案。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-189">In Windows XP and Windows Server 2003, the list of applications displayed in the **Change or Remove Programs** tab under **Add or Remove Programs** can be filtered by the user to exclude entries for application updates.</span></span> <span data-ttu-id="c4bdc-190">在這些版本的 Windows 中，這是透過視窗頂端的 [ **顯示更新** ] 核取方塊來完成。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-190">In these versions of Windows, this is accomplished through a **Show updates** check box at the top of the window.</span></span> <span data-ttu-id="c4bdc-191">預設不會選取 [ **顯示更新** ] 選項，因此除非使用者選擇顯示更新，否則 *不* 會顯示更新。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-191">The **Show updates** option is not selected by default, so updates are *not* shown unless the user chooses to show them.</span></span> <span data-ttu-id="c4bdc-192">當 [ **新增或移除程式** ] 關閉時，對核取方塊狀態的變更會保持不變;如果使用者選擇顯示更新，則會繼續顯示，直到使用者清除核取方塊為止。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-192">Changes to the check box state persist when **Add or Remove Programs** is closed; if a user chooses to show the updates, they continue to be shown until the user clears the check box.</span></span>

> [!Note]  
> <span data-ttu-id="c4bdc-193">Windows XP SP2 更新本身是篩選的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-193">The Windows XP SP2 update itself is an exception to the filtering.</span></span> <span data-ttu-id="c4bdc-194">無論核取方塊的狀態為何，一律會顯示它。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-194">It is always displayed regardless of the check box state.</span></span>

 

<span data-ttu-id="c4bdc-195">在 Windows Vista 和更新版本中，應用程式更新會顯示在單獨的頁面上，主控台專用於更新。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-195">In Windows Vista and later, application updates are displayed on a separate page in Control Panel dedicated to updates alone.</span></span> <span data-ttu-id="c4bdc-196">當使用者按一下 [ **已安裝的更新** ] 工作連結時，就會顯示此頁面。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-196">This page is shown when the user clicks the **View installed updates** task link.</span></span> <span data-ttu-id="c4bdc-197">沒有使用者可選取的選項，無法在與已安裝的程式相同的頁面上顯示更新。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-197">There is no user-selectable option to show updates on the same page as installed programs.</span></span> <span data-ttu-id="c4bdc-198">儘管 UI 的變更，註冊為已安裝程式更新的機制仍會與舊版 Windows 中的相同。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-198">Despite the change in UI, the mechanism for registering as an update to an installed program remains the same as in earlier versions of Windows.</span></span>

<span data-ttu-id="c4bdc-199">使用 Windows Installer 的 microsoft 和非 Microsoft 應用程式不需要進一步進行更新，就能被辨識為更新。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-199">Microsoft and non-Microsoft applications that use the Windows Installer do not need to do anything further for their updates to be recognized as updates.</span></span> <span data-ttu-id="c4bdc-200">未使用 Windows Installer 的非 Microsoft 應用程式必須在安裝時宣告登錄中的特定值，才能將其辨識為現有程式的更新。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-200">Non-Microsoft applications that do not use Windows Installer must declare certain values in the registry as part of their installation to be recognized as an update to an existing program.</span></span>

<span data-ttu-id="c4bdc-201">下列範例說明要宣告哪些登錄值，以將安裝識別為現有程式的更新。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-201">The following example illustrates which registry values to declare for an installation to be recognized as an update to an existing program.</span></span>

1.  <span data-ttu-id="c4bdc-202">父應用程式必須將其卸載資訊新增至 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **uninstall** 子機碼底下的子機碼中。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-202">The parent application must add its uninstall information in a subkey under the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall** subkey.</span></span> <span data-ttu-id="c4bdc-203">如需使用 **卸載** 子機碼的詳細資訊，請參閱 [安裝](/previous-versions/ms997548(v=msdn.10))主題。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-203">See the [Installation](/previous-versions/ms997548(v=msdn.10)) topic for more information on using the **Uninstall** subkey.</span></span>
2.  <span data-ttu-id="c4bdc-204">對該父應用程式的每個更新也必須將其資訊新增為 **Uninstall** 子機碼的子機碼。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-204">Each update to that parent application also must add its information as a subkey of the **Uninstall** subkey.</span></span> <span data-ttu-id="c4bdc-205">它應該使用其選擇的特定命名慣例，以避免可能與其他程式發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-205">It should use a particular naming convention of its choice, attempting to avoid potential conflicts with other programs.</span></span> <span data-ttu-id="c4bdc-206">Microsoft 會將下列慣例保留為子機碼名稱，以用於 Windows update。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-206">The following conventions are reserved as subkey names by Microsoft for use with Windows updates.</span></span>
    -   <span data-ttu-id="c4bdc-207">IEUpdate</span><span class="sxs-lookup"><span data-stu-id="c4bdc-207">IEUpdate</span></span>
    -   <span data-ttu-id="c4bdc-208">OEUpdate</span><span class="sxs-lookup"><span data-stu-id="c4bdc-208">OEUpdate</span></span>
    -   <span data-ttu-id="c4bdc-209">"KB" 後面接著六位數，例如 "KB123456"</span><span class="sxs-lookup"><span data-stu-id="c4bdc-209">"KB" followed by six digits, for example "KB123456"</span></span>
    -   <span data-ttu-id="c4bdc-210">"Q" 後面接著六位數，例如 "Q123456"</span><span class="sxs-lookup"><span data-stu-id="c4bdc-210">"Q" followed by six digits, for example "Q123456"</span></span>
    -   <span data-ttu-id="c4bdc-211">六位數，例如 "123456"</span><span class="sxs-lookup"><span data-stu-id="c4bdc-211">Six digits, for example "123456"</span></span>
3.  <span data-ttu-id="c4bdc-212">除了針對父應用程式新增的標準卸載資訊之外，每個更新的子機碼還必須包含下列三個專案的其中兩個。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-212">In addition to the standard uninstall information added for the parent application, the subkeys for each update additionally must include two of the following three entries.</span></span> <span data-ttu-id="c4bdc-213">其值的型別為 REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-213">Their values are of type REG\_SZ.</span></span>
    -   <span data-ttu-id="c4bdc-214">**ParentKeyName**。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-214">**ParentKeyName**.</span></span> <span data-ttu-id="c4bdc-215">這是必要的值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-215">This value is required.</span></span> <span data-ttu-id="c4bdc-216">這是在步驟1中宣告的父系子機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-216">This is the name of the parent's subkey declared in step 1.</span></span> <span data-ttu-id="c4bdc-217">這會將更新與程式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-217">This associates the update with the program.</span></span>
    -   <span data-ttu-id="c4bdc-218">**ParentDisplayName**。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-218">**ParentDisplayName**.</span></span> <span data-ttu-id="c4bdc-219">這是必要的值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-219">This value is required.</span></span> <span data-ttu-id="c4bdc-220">如果沒有子機碼符合在 ParentKeyName 中所指定的子機碼，此值會用來做為要在 [ **新增或移除程式**] 中顯示的預留位置父程式。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-220">If no subkey matches that named in ParentKeyName, this value is used as a placeholder parent program to be displayed in **Add or Remove Programs**.</span></span>
    -   <span data-ttu-id="c4bdc-221">**InstallDate**。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-221">**InstallDate**.</span></span> <span data-ttu-id="c4bdc-222">這是選擇性的值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-222">This value is optional.</span></span> <span data-ttu-id="c4bdc-223">它應該使用表單 `yyyymmdd` 來指定日期。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-223">It should use the form `yyyymmdd` to specify the date.</span></span> <span data-ttu-id="c4bdc-224">此日期可用於顯示在 UI 中更新專案旁的 **已安裝** 資訊。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-224">This date is used for the **Installed On** information displayed next to the update's entry in the UI.</span></span> <span data-ttu-id="c4bdc-225">如果沒有 **InstallDate** 專案，或存在但未指派任何值，則會發生下列情況：</span><span class="sxs-lookup"><span data-stu-id="c4bdc-225">If there is no **InstallDate** entry or if it is present but has no value assigned to it, the following occurs:</span></span>
        -   <span data-ttu-id="c4bdc-226">Windows Vista 和 Windows 7 以外的作業系統版本：未顯示任何 **已安裝的** 資訊。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-226">Operating system versions other than Windows Vista and Windows 7: No **Installed On** information is shown.</span></span>
        -   <span data-ttu-id="c4bdc-227">Windows Vista 和更新版本：使用預設日期。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-227">Windows Vista and later: A default date is used.</span></span> <span data-ttu-id="c4bdc-228">這是該更新子機碼下任何專案的「上次修改日期」。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-228">This is the "last modified" date for any of the entries under that update's subkey.</span></span> <span data-ttu-id="c4bdc-229">這通常是更新新增至登錄的日期。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-229">This is normally the day that the update was added to the registry.</span></span> <span data-ttu-id="c4bdc-230">不過，因為它是「上次修改日期」，所以任何子機碼專案的後續變更都會使 InstallDate 值變更為該變更的日期。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-230">However, because it is a "last modified" date, any subsequent change to any of the subkey's entries causes the InstallDate value to be changed to the date of that change.</span></span>

<span data-ttu-id="c4bdc-231">下列範例顯示 LitWare Deluxe 應用程式更新的相關登錄專案。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-231">The following example shows the pertinent registry entries for an update to the LitWare Deluxe application.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Uninstall
                  LitWare
                     DisplayName = LitWare Deluxe
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\litware.exe" /uninstall
                  LitWare_Update123456
                     DisplayName = LitWare Deluxe Update 123456. Fixes printing problems.
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\Updates\123456.exe" /uninstall
                     ParentKeyName = LitWare
                     ParentDisplayName = LitWare Deluxe
                     InstallDate = 20050513
```

<span data-ttu-id="c4bdc-232">未提供適當登錄資訊的非 Microsoft 應用程式（例如，在此選項可用之前所產生的更新）仍會在已安裝的程式清單中繼續正常顯示，且不會被篩選掉。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-232">Non-Microsoft applications that do not supply the appropriate registry information, such as updates produced before this option was available, continue to be displayed normally in the list of installed programs and are not filtered out.</span></span>

<span data-ttu-id="c4bdc-233">在 Windows Vista 和 Windows 7 以外的作業系統版本中，更新篩選通常是使用者控制的設定，而且應該依照應用程式的方式來遵守。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-233">Update filtering in operating system versions other than Windows Vista and Windows 7 is normally a user-controlled setting and should be respected as such by applications.</span></span> <span data-ttu-id="c4bdc-234">不過，在企業環境中，系統管理員可以控制使用者是否可透過 DontGroupPatches 登錄值篩選更新，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-234">However, in an enterprise environment, administrators can control whether users are given the option to filter updates through the DontGroupPatches registry value, as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               policies
                  Uninstall
                     DontGroupPatches = 0 or 1
```

<span data-ttu-id="c4bdc-235">此值的型別為 REG \_ DWORD，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-235">This value is of type REG\_DWORD and is interpreted as follows.</span></span>



| <span data-ttu-id="c4bdc-236">DontGroupPatches 值</span><span class="sxs-lookup"><span data-stu-id="c4bdc-236">DontGroupPatches value</span></span>             | <span data-ttu-id="c4bdc-237">意義</span><span class="sxs-lookup"><span data-stu-id="c4bdc-237">Meaning</span></span>                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bdc-238">0</span><span class="sxs-lookup"><span data-stu-id="c4bdc-238">0</span></span>                                  | <span data-ttu-id="c4bdc-239">使用者會看到 [ **顯示更新** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-239">The **Show updates** check box is displayed to the user.</span></span> <span data-ttu-id="c4bdc-240">篩選取決於使用者是否已核取此方塊。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-240">Filtering depends on whether the user has checked this box or not.</span></span>                                                                                         |
| <span data-ttu-id="c4bdc-241">1</span><span class="sxs-lookup"><span data-stu-id="c4bdc-241">1</span></span>                                  | <span data-ttu-id="c4bdc-242">[ **顯示更新** ] 核取方塊會從 UI 中移除。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-242">The **Show updates** check box is removed from the UI.</span></span> <span data-ttu-id="c4bdc-243">更新不會從清單中篩選。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-243">Updates are not filtered from the list.</span></span> <span data-ttu-id="c4bdc-244">在引進「 **顯示更新** 」功能之前，此值基本上會還原為 WINDOWS XP SP1 行為。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-244">This value essentially reverts to Windows XP SP1 behavior, before the **Show updates** functionality was introduced.</span></span> |
| <span data-ttu-id="c4bdc-245">DontGroupPatches 專案不存在</span><span class="sxs-lookup"><span data-stu-id="c4bdc-245">DontGroupPatches entry not present</span></span> | <span data-ttu-id="c4bdc-246">這相當於將值設定為0。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-246">This is equivalent to setting the value to 0.</span></span>                                                                                                                                                                       |



 

<span data-ttu-id="c4bdc-247">DontGroupPatches 在 Windows Vista 和 Windows 7 中沒有任何作用，因為 UI 不包含任何核取方塊，且已註冊的更新一律會進行篩選。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-247">DontGroupPatches has no effect in Windows Vista and Windows 7, where the UI contains no check box and registered updates are always filtered.</span></span>

> [!Note]  
> <span data-ttu-id="c4bdc-248">原則只會由系統管理員設定。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-248">Policies are set only by administrators.</span></span> <span data-ttu-id="c4bdc-249">應用程式不應變更此值。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-249">Applications should not alter this value.</span></span> <span data-ttu-id="c4bdc-250">如需有關如何設定以登錄為基礎的群組原則的詳細資訊，請參閱 [群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page) 或 [Windows Server 群組原則](/windows/deployment/deploy-whats-new)。</span><span class="sxs-lookup"><span data-stu-id="c4bdc-250">For more information on how to set a registry-based Group Policy, see [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page) or [Windows Server Group Policy](/windows/deployment/deploy-whats-new).</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="c4bdc-251">其他資源</span><span class="sxs-lookup"><span data-stu-id="c4bdc-251">Additional Resources</span></span>

-   [<span data-ttu-id="c4bdc-252">使用用戶端類型註冊程式</span><span class="sxs-lookup"><span data-stu-id="c4bdc-252">Registering Programs with Client Types</span></span>](reg-middleware-apps.md)
-   <span data-ttu-id="c4bdc-253">[安裝](/previous-versions/ms997548(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c4bdc-253">[Installation](/previous-versions/ms997548(v=msdn.10))</span></span>
-   [<span data-ttu-id="c4bdc-254">使用 Windows Installer 設定新增/移除程式</span><span class="sxs-lookup"><span data-stu-id="c4bdc-254">Configuring Add/Remove Programs with Windows Installer</span></span>](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a><span data-ttu-id="c4bdc-255">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4bdc-255">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4bdc-256">檔案關聯的最佳作法</span><span class="sxs-lookup"><span data-stu-id="c4bdc-256">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="c4bdc-257">檔案關聯範例案例</span><span class="sxs-lookup"><span data-stu-id="c4bdc-257">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="c4bdc-258">在 Windows Vista 和更新版本中管理預設應用程式的指導方針</span><span class="sxs-lookup"><span data-stu-id="c4bdc-258">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="c4bdc-259">預設程式</span><span class="sxs-lookup"><span data-stu-id="c4bdc-259">Default Programs</span></span>](default-programs.md)
</dt> </dl>

 

 
