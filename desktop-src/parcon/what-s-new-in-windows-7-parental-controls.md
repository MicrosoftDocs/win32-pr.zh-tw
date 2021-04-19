---
description: 概述 Windows 7 中引進的 Windows 家長監護的變更。
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Windows 7 家長監護有哪些新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8282021c81ee8611fb7206d75f7e6aab48ebf2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981008"
---
# <a name="whats-new-in-windows-7-parental-controls"></a><span data-ttu-id="8f2c3-103">Windows 7 父母控制項的新功能</span><span class="sxs-lookup"><span data-stu-id="8f2c3-103">What's New in Windows 7 Parental Controls</span></span>

## <a name="overview-of-parental-controls-changes-for-windows-7"></a><span data-ttu-id="8f2c3-104">Windows 7 的家長監護變更總覽</span><span class="sxs-lookup"><span data-stu-id="8f2c3-104">Overview of Parental Controls Changes for Windows 7</span></span>

<span data-ttu-id="8f2c3-105">本檔的目的是概述 Windows 7 中所引進之 Windows 家長監護的變更，並讓協力廠商家長監護解決方案提供者能夠利用這些變更。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-105">The purpose of this document is to give an overview of the changes to the Windows Parental Controls introduced in Windows 7 and to enable third-party parental control solution providers to take advantage of these changes.</span></span> <span data-ttu-id="8f2c3-106">本檔假設讀者對 Windows Vista 的家長監護有更熟悉的程度，而且只會反映對 Windows 7 的這項功能所做的變更，這些變更與協力廠商家長監護解決方案開發有關。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-106">This document assumes readers' familiarity with Parental Controls for Windows Vista and will only reflect changes made to this functionality in Windows 7 that are relevant for third-party parental control solutions development.</span></span> <span data-ttu-id="8f2c3-107">MSDN Windows 家長監護檔的完整更新將在稍後的日期之後進行。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-107">A full update of MSDN Windows Parental Control documentation will follow at a later date.</span></span>

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a><span data-ttu-id="8f2c3-108">Windows 7 家長監護控制項變更的重要設計決策</span><span class="sxs-lookup"><span data-stu-id="8f2c3-108">Key Design Decisions for Windows 7 Parental Control Changes</span></span>

<span data-ttu-id="8f2c3-109">在 Windows 7 中引進之家長監護的變更，可繼續提升協力廠商家長監護解決方案與隨用隨功能共存的主要目標。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-109">Changes to Parental Controls introduced in Windows 7 continue the overarching goal of promoting third-party parental control solutions' coexistence with the in-box functionality.</span></span> <span data-ttu-id="8f2c3-110">變更為：</span><span class="sxs-lookup"><span data-stu-id="8f2c3-110">The changes are:</span></span>

-   <span data-ttu-id="8f2c3-111">從內建家長監護功能移除 web 篩選和活動報告。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-111">Removal of web filtering and activity reporting from the in-box parental controls functionality.</span></span> <span data-ttu-id="8f2c3-112">內建的家長監護提供核心離線 Microsoft 實行的限制，例如時間限制、應用程式限制和遊戲限制。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-112">The in-box parental controls provide core offline Microsoft-implemented restrictions such as time limits, application restrictions, and game restrictions.</span></span> <span data-ttu-id="8f2c3-113">Microsoft 或協力廠商家長監護解決方案可以提供 web 篩選、活動報告和其他功能。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-113">The web filtering, activity reporting, and other functionality can be provided by Microsoft or third-party parental control solutions.</span></span> <span data-ttu-id="8f2c3-114">例如，Windows Live Family 安全性解決方案提供網路篩選、遠端系統管理和活動監控，以及所有 Windows Live 應用程式的連絡人管理。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-114">For example, Windows Live Family Safety solution provides web filtering, remote management, and activity monitoring, as well as contact management for all Windows Live applications.</span></span>
-   <span data-ttu-id="8f2c3-115">啟用協力廠商解決方案來取代內建提供者的設定使用者介面，同時仍依賴內建的時間、應用程式和遊戲限制的執行。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-115">Enabling third-party solutions to replace the in-box provider's configuration user interface while still relying on the in-box implementation of time, application, and game restrictions.</span></span>
-   <span data-ttu-id="8f2c3-116"> (系統管理員帳戶) ，啟用在電腦上探索和啟用的協力廠商解決方案。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-116">Enabling third-party solutions to be discovered and enabled on the computer by a parent or guardian (administrator account).</span></span>

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a><span data-ttu-id="8f2c3-117">家長監護 Windows 7 中最上層的消費者介面變更</span><span class="sxs-lookup"><span data-stu-id="8f2c3-117">Parental Controls Top-level User Interface Changes in Windows 7</span></span>

<span data-ttu-id="8f2c3-118">Windows 7 會將下列變更變更為最上層使用者介面主控台的家長監護：</span><span class="sxs-lookup"><span data-stu-id="8f2c3-118">Windows 7 brings the following changes to the Parental Controls Control Panel top-level user interface:</span></span>

-   <span data-ttu-id="8f2c3-119">另外也引進了可從下拉式清單方塊中選取提供其他功能的控制項（例如，web 篩選、活動報告等等）的控制項區段。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-119">The Additional controls section is introduced where controls that provide additional functionality such as web filtering, activity reporting, and so on, can be selected from a drop down list box.</span></span> <span data-ttu-id="8f2c3-120">Microsoft 或協力廠商提供者必須向 Windows 7 家長監護註冊他們的解決方案，才能從 [其他控制項] 下拉式清單方塊中選取這些控制項。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-120">Microsoft or third-party providers need to register their solutions with Windows 7 Parental Controls for them to be selectable from the Additional controls drop down list box.</span></span> <span data-ttu-id="8f2c3-121">如需註冊解決方案的詳細資訊，請參閱本主題稍後的「提供者註冊」) 。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-121">For information about registering a solution, see Provider Registration, later in this topic).</span></span>
-   <span data-ttu-id="8f2c3-122">目前所選提供者的標誌影像會顯示在頁面的右上角。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-122">The logo image of the currently selected provider is displayed in the upper-right corner of the page.</span></span>
-   <span data-ttu-id="8f2c3-123">受管理的使用者磚可顯示目前所選取提供者所提供之家長設定的摘要。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-123">The managed user tiles can display a summary of the parental settings provided by the currently selected provider.</span></span>

<span data-ttu-id="8f2c3-124">目前選取的提供者可能會選擇針對受管理使用者的使用者控制項畫面使用自己的使用者介面，也可能會選擇依賴此畫面的內建 WPC 執行。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-124">The currently selected provider might choose to use its own user interface for User Control screens for the managed users, or it might select to rely on the in-box WPC implementation of this screen.</span></span> <span data-ttu-id="8f2c3-125">內建的實作為其元素的下列變更：</span><span class="sxs-lookup"><span data-stu-id="8f2c3-125">In-box implementation has the following changes made to its elements:</span></span>

-   <span data-ttu-id="8f2c3-126">已移除活動報告區段。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-126">The activity reporting section is removed.</span></span>
-   <span data-ttu-id="8f2c3-127">已移除用來查看活動報告的連結。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-127">The link to view activity reports is removed.</span></span>

## <a name="parental-controls-api-overview-windows-7-changes"></a><span data-ttu-id="8f2c3-128">家長監護 API 總覽： Windows 7 變更</span><span class="sxs-lookup"><span data-stu-id="8f2c3-128">Parental Controls API Overview: Windows 7 Changes</span></span>

<span data-ttu-id="8f2c3-129">協力廠商解決方案提供者的整合機制已擴充為允許：</span><span class="sxs-lookup"><span data-stu-id="8f2c3-129">The integration mechanism for third-party solution providers was expanded to allow:</span></span>

-   <span data-ttu-id="8f2c3-130">提供者註冊。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-130">Provider registration.</span></span> <span data-ttu-id="8f2c3-131">註冊時，提供者會在 [家長監護] 主控台畫面上的 [其他控制項] 下拉式清單方塊中變成可選取。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-131">Upon registration, a provider becomes selectable in the Additional controls drop-down list box on the Parental Controls Control Panel screen.</span></span>
-   <span data-ttu-id="8f2c3-132">正在查詢目前選取的提供者。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-132">Querying for the currently selected provider.</span></span> <span data-ttu-id="8f2c3-133">公開的 COM 介面可以用來啟用這項功能。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-133">A public COM interface is exposed to enable this functionality.</span></span>
-   <span data-ttu-id="8f2c3-134">此外，新的是要由提供者所執行的一組 COM 介面，以允許：</span><span class="sxs-lookup"><span data-stu-id="8f2c3-134">Also new is the set of COM interfaces to be implemented by the providers to allow:</span></span>
    -   <span data-ttu-id="8f2c3-135">藉由在使用者選取其他控制項時 WPC 來啟用或停用提供者。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-135">Enabling or disabling of the provider by WPC upon user selection of additional controls.</span></span>
    -   <span data-ttu-id="8f2c3-136">WPC 將控制權傳遞給提供者，以設定受管理使用者的家長監護設定。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-136">WPC to pass control to the provider to configure managed user's parental control settings.</span></span>
    -   <span data-ttu-id="8f2c3-137">WPC，查詢提供者以取得受管理使用者之家長監護設定的摘要。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-137">WPC to query the provider for the summary of managed user's parental control settings.</span></span>

## <a name="third-party-provider-integration"></a><span data-ttu-id="8f2c3-138">協力廠商提供者整合</span><span class="sxs-lookup"><span data-stu-id="8f2c3-138">Third-party Provider Integration</span></span>

### <a name="provider-registration"></a><span data-ttu-id="8f2c3-139">提供者註冊</span><span class="sxs-lookup"><span data-stu-id="8f2c3-139">Provider Registration</span></span>

<span data-ttu-id="8f2c3-140">若要向家長監護註冊新的提供者，必須將登錄值寫入 Windows 家長監護的提供者金鑰。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-140">To register a new provider with Parental Controls, a registry value must be written to the Providers key of Windows Parental Controls.</span></span> <span data-ttu-id="8f2c3-141">值名稱是用來識別提供者的唯一 GUID。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-141">The value name is a unique GUID that is used to identify the provider.</span></span> <span data-ttu-id="8f2c3-142">值資料會是 **HKEY \_ 本機 \_ 電腦** 中包含提供者資訊的登錄機碼路徑。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-142">The value data will be a path to a registry key in **HKEY\_LOCAL\_MACHINE** that contains provider information.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Parental Controls
                  Providers
                     {45D63315-0824-4df4-B8A4-EF137D8810D1} = SOFTWARE\Microsoft\Family Safety\WPC\
```

<span data-ttu-id="8f2c3-143">在指定的登錄機碼位置，預期會有下列值。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-143">At the registry key location specified, the following values are expected.</span></span>



| <span data-ttu-id="8f2c3-144">詞彙</span><span class="sxs-lookup"><span data-stu-id="8f2c3-144">Term</span></span>                                                                                                                 | <span data-ttu-id="8f2c3-145">描述</span><span class="sxs-lookup"><span data-stu-id="8f2c3-145">Description</span></span>                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2c3-146"><span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**</span><span class="sxs-lookup"><span data-stu-id="8f2c3-146"><span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**</span></span><br/>         | <span data-ttu-id="8f2c3-147">具有提供者標誌影像負資源識別碼之資源二進位檔的完整路徑 (儲存為 **影像 \_ 點陣圖**) 。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-147">A fully qualified path to a resource binary with a negative resource ID for the provider logo image (stored as an **IMAGE\_BITMAP**).</span></span><br/>                                                        |
| <span data-ttu-id="8f2c3-148"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="8f2c3-148"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span><br/> | <span data-ttu-id="8f2c3-149">資源二進位檔的完整路徑，具有提供者名稱的負資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-149">A fully qualified path to a resource binary with a negative resource ID for the provider name.</span></span> <span data-ttu-id="8f2c3-150">**DisplayName** 長度不應超過50個字元。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-150">**DisplayName** length should not exceed 50 characters.</span></span><br/>                                       |
| <span data-ttu-id="8f2c3-151"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="8f2c3-151"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span><br/> | <span data-ttu-id="8f2c3-152">資源二進位檔的完整路徑，具有提供者描述的負資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-152">A fully qualified path to a resource binary with a negative resource ID for the provider description.</span></span> <span data-ttu-id="8f2c3-153">描述長度不應超過200個字元。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-153">The description length should not exceed 200 characters.</span></span><br/>                               |
| <span data-ttu-id="8f2c3-154"><span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**</span><span class="sxs-lookup"><span data-stu-id="8f2c3-154"><span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**</span></span><br/>     | <span data-ttu-id="8f2c3-155">實 IWPCProviderState 之提供者類別的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-155">The class ID of the provider's class which implements IWPCProviderState.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="8f2c3-156"><span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**</span><span class="sxs-lookup"><span data-stu-id="8f2c3-156"><span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**</span></span><br/> | <span data-ttu-id="8f2c3-157">提供者類別的類別識別碼，它會執行 IWPCProviderConfig。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-157">The class ID of the provider's class, which implements IWPCProviderConfig.</span></span> <span data-ttu-id="8f2c3-158">**StateCLSID** 和 **ConfigCLSID** 可以相同。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-158">**StateCLSID** and **ConfigCLSID** can be the same.</span></span><br/>                                                               |
| <span data-ttu-id="8f2c3-159"><span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**</span><span class="sxs-lookup"><span data-stu-id="8f2c3-159"><span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**</span></span><br/>     | <span data-ttu-id="8f2c3-160">選擇性的 **DWORD** 非零值，指定在選取提供者作為新的目前提供者之後，Windows 家長監護會顯示遊戲評等系統畫面的連結。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-160">An optional **DWORD** nonzero value that specifies that Windows Parental Controls displays a link to the Game Rating System screen after a provider is selected as the new current provider.</span></span><br/> |



 

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Family Safety
            WPC
               LogoImage = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40001
               DisplayName = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40002
               Description = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40003
               StateCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               ConfigCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               GRSVisible = 0x00000001 (1)
```

<span data-ttu-id="8f2c3-161">當選取該提供者時，家長監護主控台會使用 **LogoImage**、 **DisplayName** 和 **Description** 來變更家長監護主控台的主頁面。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-161">The Parental Controls Control Panel uses the **LogoImage**, **DisplayName**, and **Description** to change the main page of the Parental Controls Control Panel when that provider is selected.</span></span> <span data-ttu-id="8f2c3-162">啟用或停用提供者時，會使用 **StateCLSID** 值。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-162">The **StateCLSID** value is used when the provider is enabled or disabled.</span></span> <span data-ttu-id="8f2c3-163">當使用者介面取得每位使用者的動態資訊時，會使用 **ConfigCLSID** 值 (這只是) 提供者目前已選取的情況。</span><span class="sxs-lookup"><span data-stu-id="8f2c3-163">The **ConfigCLSID** value is used when the user interface gets dynamic information about each user (this is only the case if the provider is currently selected).</span></span>

 

 




