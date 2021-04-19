---
title: WCS 登錄機碼
description: WCS 使用登錄機碼來表示已發生特定色彩設定檔事件。 應用程式應該查詢這些登錄機碼，以取得更新的系統色彩設定檔狀態。
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS) ，登錄機碼
- WCS (Windows 色彩系統) ，登錄機碼
- 影像色彩管理、登錄機碼
- 色彩管理，登錄機碼
- 色彩、登錄機碼
- WCS 參考，登錄機碼
- WCS 的參考，登錄機碼
- Windows Color System (WCS) ，登錄
- WCS (Windows Color System) ，registry
- 影像色彩管理，登錄
- 色彩管理，登錄
- 色彩，登錄
- WCS 參考，登錄
- WCS、registry 的參考
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106991381"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="f192a-118">WCS 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="f192a-118">WCS Registry Keys</span></span>

<span data-ttu-id="f192a-119">WCS 使用登錄機碼來表示已發生特定色彩設定檔事件。</span><span class="sxs-lookup"><span data-stu-id="f192a-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="f192a-120">應用程式應該查詢這些登錄機碼，以取得更新的系統色彩設定檔狀態。</span><span class="sxs-lookup"><span data-stu-id="f192a-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="f192a-121">現用色彩設定檔已變更</span><span class="sxs-lookup"><span data-stu-id="f192a-121">Active color profile changed</span></span>

<span data-ttu-id="f192a-122">應用程式可能會想要回應監視裝置的色彩設定檔變更事件;這可確保即使使用者或其他應用程式已變更裝置的使用中設定檔，它們的目標一律會有正確的色彩資訊。</span><span class="sxs-lookup"><span data-stu-id="f192a-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="f192a-123">傳統型應用程式</span><span class="sxs-lookup"><span data-stu-id="f192a-123">Desktop applications</span></span>

<span data-ttu-id="f192a-124">桌面應用程式應該接聽登錄的變更，以判斷色彩設定檔關聯何時使用 [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue)變更。</span><span class="sxs-lookup"><span data-stu-id="f192a-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="f192a-125">應用程式應該針對每個使用者設定檔的關聯變更，以及進行全系統的變更註冊。</span><span class="sxs-lookup"><span data-stu-id="f192a-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="f192a-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) 應該使用 [**REGOPENKEYEX**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)提供的 HKEY 來初始化。</span><span class="sxs-lookup"><span data-stu-id="f192a-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="f192a-127">**RegOpenKeyEx** 應使用下列登錄樹狀目錄位置進行初始化：</span><span class="sxs-lookup"><span data-stu-id="f192a-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f192a-128">每個使用者設定檔關聯</span><span class="sxs-lookup"><span data-stu-id="f192a-128">Per-user profile associations</span></span>    | <span data-ttu-id="f192a-129">**HKEY \_ 目前的 \_ 使用者軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="f192a-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="f192a-130">全系統設定檔關聯</span><span class="sxs-lookup"><span data-stu-id="f192a-130">System-wide profile associations</span></span> | <span data-ttu-id="f192a-131">**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Class \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="f192a-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="f192a-132">當應用程式收到登錄機碼變更的通知時，它應該會先使用呼叫 [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)來查詢是否正在使用每個使用者或整個系統的關聯。</span><span class="sxs-lookup"><span data-stu-id="f192a-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="f192a-133">接著，它應該使用正確的 [**WCS \_ 設定檔 \_ 管理 \_ 範圍**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)值來呼叫 [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) ，以取得監視器的新現用色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="f192a-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="f192a-134">請注意，並非所有登錄機碼變更都會對應到目前作用中色彩設定檔中的實際變更;應用程式必須會檢查 **WcsGetDefaultColorProfile** 所傳回的設定檔是否確實變更。</span><span class="sxs-lookup"><span data-stu-id="f192a-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="f192a-135">通用 Windows (UWP) 應用程式</span><span class="sxs-lookup"><span data-stu-id="f192a-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="f192a-136">通用 Windows 應用程式沒有上述登錄機碼的存取權。</span><span class="sxs-lookup"><span data-stu-id="f192a-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="f192a-137">相反地，它們應該註冊 [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) 事件的處理常式。</span><span class="sxs-lookup"><span data-stu-id="f192a-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="f192a-138">每當應用程式執行所在之監視的現用色彩設定檔變更時，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="f192a-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="f192a-139">ColorProfileChanged 會考慮每個使用者或整個系統設定檔關聯是否正在使用中;這項資訊是從 UWP 應用程式抽象化。</span><span class="sxs-lookup"><span data-stu-id="f192a-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="f192a-140">回應 ColorProfileChanged 事件時，應用程式應該使用 DisplayInformation 來查詢目前作用中的設定檔 [**。**](/uwp/api/Windows.Graphics.Display.DisplayInformation)</span><span class="sxs-lookup"><span data-stu-id="f192a-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 