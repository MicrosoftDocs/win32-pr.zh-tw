---
description: 概述 Windows 8 所引進之 Windows 家長監護的變更。
ms.assetid: 7EB33215-8F8B-4EA4-87E6-A98F0D014548
title: Windows 8 系列安全性的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2123ec7f0d9c3af66528c6c203a3e8ea64bd0384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849118"
---
# <a name="whats-new-in-windows-8-family-safety"></a><span data-ttu-id="ae759-103">Windows 8 系列安全性的新功能</span><span class="sxs-lookup"><span data-stu-id="ae759-103">What's New in Windows 8 Family Safety</span></span>

## <a name="overview-of-parental-controls-changes-for-windows-8"></a><span data-ttu-id="ae759-104">Windows 8 的家長監護變更總覽</span><span class="sxs-lookup"><span data-stu-id="ae759-104">Overview of Parental Controls Changes for Windows 8</span></span>

<span data-ttu-id="ae759-105">本檔的目的是概述 Windows 8 中 Windows 家長監護的變更，並讓協力廠商家長監護解決方案提供者能夠利用這些變更。</span><span class="sxs-lookup"><span data-stu-id="ae759-105">The purpose of this document is to give an overview of the changes to the Windows Parental Controls in Windows 8 and to enable third-party parental control solution providers to take advantage of these changes.</span></span> <span data-ttu-id="ae759-106">本檔假設讀者對 Windows 7 和 Windows Vista 的家長監護有熟悉，而且只會在與協力廠商家長監護開發相關的 Windows 8 中反映對這項功能的變更。</span><span class="sxs-lookup"><span data-stu-id="ae759-106">This document assumes readers' familiarity with Parental Controls for Windows 7 and Windows Vista and will only reflect changes made to this functionality in Windows 8 that are relevant for third-party parental control solutions development.</span></span>

## <a name="key-design-decisions-for-windows-8-parental-controlfamily-safety-changes"></a><span data-ttu-id="ae759-107">Windows 8 家長監護/系列安全性變更的關鍵設計決策</span><span class="sxs-lookup"><span data-stu-id="ae759-107">Key Design Decisions for Windows 8 Parental Control/Family Safety Changes</span></span>

<span data-ttu-id="ae759-108">Windows 8 中所引進之家長監護的變更會繼續提升功能增強功能的主要目標，同時促進協力廠商家長監護解決方案與隨用隨的功能共存。</span><span class="sxs-lookup"><span data-stu-id="ae759-108">Changes to Parental Controls introduced in Windows 8 continue the overarching goal of introducing feature enhancements and at the same time promoting third-party parental control solutions' coexistence with the in-box functionality.</span></span> <span data-ttu-id="ae759-109">變更為：</span><span class="sxs-lookup"><span data-stu-id="ae759-109">The changes are:</span></span>

-   <span data-ttu-id="ae759-110">使用 Microsoft 家長監護服務來提供遠端系統管理和遠端活動監視。</span><span class="sxs-lookup"><span data-stu-id="ae759-110">Use of Microsoft Family Safety to provide remote management and remote activity monitoring.</span></span>
-   <span data-ttu-id="ae759-111">將 web 篩選整合為內建 Microsoft 限制的一部分，以及在 Windows 8 電腦上查看活動報告的功能。</span><span class="sxs-lookup"><span data-stu-id="ae759-111">Integration of web filtering as part of in-box Microsoft restrictions and ability to view activity reports on a Windows 8 computer.</span></span>
-   <span data-ttu-id="ae759-112">主控台中的「家長監護」功能已重新命名為「家庭安全」，在本檔中也稱為。</span><span class="sxs-lookup"><span data-stu-id="ae759-112">The Parental Controls feature in the Control Panel was renamed to Family Safety and will be referred to as such throughout this document.</span></span>
-   <span data-ttu-id="ae759-113">內建的時間限制是藉由提供控制每日電腦總時間量的能力來增強 (時間額度) 除了能夠控制使用電腦 (的時間之外，還能讓您在舊版的 Windows 中使用 ) Curfew。</span><span class="sxs-lookup"><span data-stu-id="ae759-113">The in-box time restrictions were enhanced by providing ability to control total amount of time per day computer can be used (time allowance) in addition to ability to control times when computer can be used (curfew.) Curfew was available in previous versions of Windows.</span></span>
-   <span data-ttu-id="ae759-114">在標準帳戶建立流程期間可以開啟 Windows 8 系列安全功能。</span><span class="sxs-lookup"><span data-stu-id="ae759-114">Windows 8 Family Safety functionality can be turned on during standard account creation flow.</span></span>
-   <span data-ttu-id="ae759-115">Windows Vista 和 Windows 7 家長監護的擴充功能，Windows 8 系列的安全，包括由協力廠商解決方案取代 web 內容篩選器，或是取代內建的設定 UI，同時仍依賴內建的時間、應用程式、遊戲限制和網路內容篩選器等功能。</span><span class="sxs-lookup"><span data-stu-id="ae759-115">Windows Vista and Windows 7 Parental Controls extensibility features are continued to be supported by Windows 8 Family Safety including ability by third-party solutions to replace web content filter or to replace in-box configuration UI while still relying on in-box implementation of Time, Application, Game Restrictions and Web Content Filter.</span></span>
-   <span data-ttu-id="ae759-116">協力廠商提供者啟用會透過家庭安全網站，關閉 Windows 8 系列安全控制項的遠端系統管理和報告。</span><span class="sxs-lookup"><span data-stu-id="ae759-116">Third-party provider activation turns off remote management and reporting of Windows 8 Family Safety controls through Family Safety website.</span></span>
-   <span data-ttu-id="ae759-117">協力廠商的系列安全擴充功能僅支援 Windows 8 桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="ae759-117">The third-party extensibility for Family Safety is supported for Windows 8 desktop applications only.</span></span>

## <a name="family-safety-and-standard-account-creation-in-windows-8"></a><span data-ttu-id="ae759-118">Windows 8 中的家庭安全和標準帳戶建立</span><span class="sxs-lookup"><span data-stu-id="ae759-118">Family Safety and standard account creation in Windows 8</span></span>

<span data-ttu-id="ae759-119">在 Windows 8 中建立標準帳戶的過程中，系統管理員可以依家庭安全開啟帳戶的監視功能。</span><span class="sxs-lookup"><span data-stu-id="ae759-119">As part of standard account creation in Windows 8, an administrator has ability to turn on monitoring of the account by Family Safety.</span></span> <span data-ttu-id="ae759-120">以下是可控制的功能和協力廠商提供者的功能清單：</span><span class="sxs-lookup"><span data-stu-id="ae759-120">The following is a list of the functionality and third-party provider ability to control it:</span></span>

-   <span data-ttu-id="ae759-121">在 Windows 8 標準帳戶建立流程的最後一個畫面上，系統管理員會看到一個核取方塊，以開啟新建立之帳戶的家庭安全。</span><span class="sxs-lookup"><span data-stu-id="ae759-121">On the last screen of Windows 8 standard account creation flow, an administrator is presented with a checkbox to turn on Family Safety for the newly created account.</span></span>
-   <span data-ttu-id="ae759-122">如果選取此核取方塊，則會針對具有下列設定的帳戶開啟家庭安全：</span><span class="sxs-lookup"><span data-stu-id="ae759-122">If this checkbox is checked, Family Safety is turned on for the account with the following settings:</span></span>
    -   <span data-ttu-id="ae759-123">活動報告開啟</span><span class="sxs-lookup"><span data-stu-id="ae759-123">Activity Reporting on</span></span>
    -   <span data-ttu-id="ae759-124">所有限制都已關閉</span><span class="sxs-lookup"><span data-stu-id="ae759-124">All restrictions are off</span></span>
-   <span data-ttu-id="ae759-125">如果系統管理員使用 Microsoft 帳戶登入 Windows，則會將 Windows 8 電腦設定為從遠端系統管理家庭安全設定和電子郵件活動報告。</span><span class="sxs-lookup"><span data-stu-id="ae759-125">If the administrator used a Microsoft account to logon to Windows, the Windows 8 computer will be configured for remote management of family safety settings and email activity reports.</span></span> <span data-ttu-id="ae759-126">然後可以使用家庭安全網站，從遠端系統管理這類電腦。</span><span class="sxs-lookup"><span data-stu-id="ae759-126">The Family Safety website can be then used to manage such a computer remotely.</span></span>
-   <span data-ttu-id="ae759-127">如果協力廠商提供者希望該核取方塊出現在標準帳戶建立流程中，則提供者的註冊值應該會有下列值。</span><span class="sxs-lookup"><span data-stu-id="ae759-127">If the third-party provider wishes for the checkbox to be present in a standard account creation flow the following value should be present among the provider s registration values.</span></span> <span data-ttu-id="ae759-128">如需提供者註冊詳細資料的詳細資訊，請參閱「Windows 7 家長監護的新功能」主題的「 [提供者註冊](what-s-new-in-windows-7-parental-controls.md) 」一節。</span><span class="sxs-lookup"><span data-stu-id="ae759-128">For more information on provider registration details, see the [Provider Registration](what-s-new-in-windows-7-parental-controls.md) section on the What's New in Windows 7 Parental Controls topic.</span></span>

    

    | <span data-ttu-id="ae759-129">詞彙</span><span class="sxs-lookup"><span data-stu-id="ae759-129">Term</span></span>                                                                                                                         | <span data-ttu-id="ae759-130">描述</span><span class="sxs-lookup"><span data-stu-id="ae759-130">Description</span></span>                                                                                                                                                                                                                                                                                  |
    |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ae759-131"><span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>AddUserVisible</span><span class="sxs-lookup"><span data-stu-id="ae759-131"><span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>AddUserVisible</span></span><br/> | <span data-ttu-id="ae759-132">選擇性的 **DWORD** 非零值，指定在將提供者選取為目前的家庭安全提供者之後，Windows 8 中的標準帳戶建立期間，為新建立的帳戶開啟家庭安全監視器的核取方塊選項應該是可見的。</span><span class="sxs-lookup"><span data-stu-id="ae759-132">An optional **DWORD** nonzero value that specifies that the checkbox option to turn on Family Safety monitoring for a newly created account should be visible during standard account creation in Windows 8 after the provider is selected as the current Family Safety provider.</span></span><br/> |

    

     

-   <span data-ttu-id="ae759-133">由於協力廠商提供者的設計是為了取代家庭安全控制項的內建設定 UI，因此根據預設，協力廠商提供者的安裝和啟用將會導致在建立標準帳戶期間開啟家庭安全的核取方塊選項，而不會顯示。</span><span class="sxs-lookup"><span data-stu-id="ae759-133">Since third-party providers are designed to replace in-box configuration UI for Family Safety controls, by default, installation and activation of a third-party provider will result in the checkbox option to turn on Family Safety during standard account creation not to be shown.</span></span>

## <a name="family-safety-top-level-user-interface-changes-in-windows-8"></a><span data-ttu-id="ae759-134">Windows 8 中的系列安全性最上層消費者介面變更</span><span class="sxs-lookup"><span data-stu-id="ae759-134">Family Safety Top-level User Interface Changes in Windows 8</span></span>

<span data-ttu-id="ae759-135">Windows 8 將下列對家長監護的變更，主控台最上層使用者介面：</span><span class="sxs-lookup"><span data-stu-id="ae759-135">Windows 8 brings the following changes to the Parental Controls Control Panel top-level user interface:</span></span>

-   <span data-ttu-id="ae759-136">當 Windows 8 電腦上至少一個標準帳戶的內建系列安全控制項開啟時，系統會顯示 [管理家庭安全網站命令] 連結的設定，讓系統管理員能夠透過家庭安全網站，建立 Windows 8 電腦系列安全性設定的遠端系統管理。</span><span class="sxs-lookup"><span data-stu-id="ae759-136">When in-box Family Safety controls are turned on for at least one standard account on a Windows 8 computer,  Manage settings on Family Safety website  command link is shown that allows an admin to establish remote management of Windows 8 computer Family Safety settings through Family Safety website.</span></span>
-   <span data-ttu-id="ae759-137">當 Windows 8 電腦設定為透過家庭安全網站進行遠端系統管理時，更多的資訊控制項可讓系統管理員透過家庭安全網站停用 Windows 8 電腦的遠端系統管理。</span><span class="sxs-lookup"><span data-stu-id="ae759-137">When a Windows 8 computer is configured for remote management through Family Safety website, the More Information control allows an admin to disable remote management of a Windows 8 computer through the Family Safety website.</span></span>
-   <span data-ttu-id="ae759-138">只有當至少有一個協力廠商提供者向家庭安全註冊時，才會顯示 [控制項] 區段。</span><span class="sxs-lookup"><span data-stu-id="ae759-138">The Controls section is visible only when at least one third-party provider is registered with Family Safety.</span></span> <span data-ttu-id="ae759-139">此區段的 UI 和功能與 Windows 7 家長監護中的 [其他控制項] 區段相同。</span><span class="sxs-lookup"><span data-stu-id="ae759-139">The UI and functionality of this section is identical to the Additional Controls section in Windows 7 Parental Controls.</span></span> <span data-ttu-id="ae759-140">如需詳細資訊，請參閱 [Windows 7 家長](what-s-new-in-windows-7-parental-controls.md) 監護主題的「家長監護使用者介面變更」一節。</span><span class="sxs-lookup"><span data-stu-id="ae759-140">For more information, see the Parental Controls top-level User interface changes section of the [Windows 7 Parental Controls](what-s-new-in-windows-7-parental-controls.md) topic.</span></span>
-   <span data-ttu-id="ae759-141">當協力廠商提供者已安裝並選取為目前的提供者時，會停用透過家庭安全網站的 Windows 8 電腦系列安全設定遠端系統管理。</span><span class="sxs-lookup"><span data-stu-id="ae759-141">When a third-party provider is installed and selected as the current provider, remote management of Windows 8 computer Family Safety settings through the Family Safety website is disabled.</span></span>

## <a name="family-safety-in-box-restrictions-changes-in-windows-8"></a><span data-ttu-id="ae759-142">Windows 8 中的系列安全 In-Box 限制變更</span><span class="sxs-lookup"><span data-stu-id="ae759-142">Family Safety In-Box Restrictions Changes in Windows 8</span></span>

<span data-ttu-id="ae759-143">Windows 8 將下列變更提供給家庭安全的內建限制：</span><span class="sxs-lookup"><span data-stu-id="ae759-143">Windows 8 brings the following changes to the Family Safety in-box restrictions:</span></span>

<span data-ttu-id="ae759-144">Web 限制</span><span class="sxs-lookup"><span data-stu-id="ae759-144">Web Restrictions</span></span>

-   <span data-ttu-id="ae759-145">執行已從多層式服務提供者變更 (LSP) 篩選至 Windows 篩選平台 (WFP) 驅動程式與在使用者會話中執行的家庭安全監視程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="ae759-145">Implementation has changed from a Layered Service Provider (LSP) filter to a Windows Filtering Platform (WFP) driver communicating with the Family Safety monitoring process running in the users  sessions.</span></span>

<span data-ttu-id="ae759-146">時間限制</span><span class="sxs-lookup"><span data-stu-id="ae759-146">Time Limits</span></span>

-   <span data-ttu-id="ae759-147">內建的時間限制已增強，可讓您控制電腦可用的總時間量 (時間額度) 除了能夠控制電腦可用的時間之外，還可以在舊版 Windows 中使用 (curfew) 。</span><span class="sxs-lookup"><span data-stu-id="ae759-147">The in-box time restrictions were enhanced by providing ability to control total amount of time per day computer can be used (time allowance) in addition to ability to control times when computer can be used (curfew) which was available in previous versions of Windows.</span></span>
-   <span data-ttu-id="ae759-148">適用于 curfew 的 UI 可讓您在一周的每一天進行獨立控制，並提供半小時的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="ae759-148">UI for curfew allows independent control for each day of the week with half-hour granularity.</span></span>
-   <span data-ttu-id="ae759-149">時間額度的 UI 可讓您以15分鐘的資料細微性，在一周中的每一天對工作日/週末或獨立控制進行控制。</span><span class="sxs-lookup"><span data-stu-id="ae759-149">UI for time allowance allows controls for weekdays / weekends or independent control for each day of the week with 15 minute granularity.</span></span>
-   <span data-ttu-id="ae759-150">在封鎖的時間週期內，快速使用者切換 (FUS) 機制不再用來強制鎖定或封鎖受控制使用者的登入。</span><span class="sxs-lookup"><span data-stu-id="ae759-150">Fast User Switch (FUS) mechanism is no longer used to forcibly lock out or block login of the controlled user when in blocked time period.</span></span> <span data-ttu-id="ae759-151">切換至不同的桌面會用於這些用途。</span><span class="sxs-lookup"><span data-stu-id="ae759-151">A switch to a separate desktop is used for these purposes.</span></span>
-   <span data-ttu-id="ae759-152">中斷連接警告事件不再適用于應用程式訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae759-152">Disconnect warning events are no longer available for applications to subscribe to.</span></span>

## <a name="family-safety-api-changes-in-windows-8"></a><span data-ttu-id="ae759-153">Windows 8 中的家庭安全 API 變更</span><span class="sxs-lookup"><span data-stu-id="ae759-153">Family Safety API Changes in Windows 8</span></span>

<span data-ttu-id="ae759-154">用於家庭安全的 Api 會公開原則和內建限制設定，以及記錄功能。</span><span class="sxs-lookup"><span data-stu-id="ae759-154">APIs used for Family Safety expose the policy and in-box restrictions settings, and logging functionality.</span></span>

<span data-ttu-id="ae759-155">記錄</span><span class="sxs-lookup"><span data-stu-id="ae759-155">Logging</span></span>

-   <span data-ttu-id="ae759-156">[系列安全性活動報告檢視器] 不再支援自訂事件。</span><span class="sxs-lookup"><span data-stu-id="ae759-156">Custom events are no longer supported in the Family Safety activity reports viewer.</span></span>

<span data-ttu-id="ae759-157">WMI API 設定寫入/讀取</span><span class="sxs-lookup"><span data-stu-id="ae759-157">WMI API Settings Write/Read</span></span>

-   <span data-ttu-id="ae759-158">WpcUserSettings-之前的計時器限制支援1小時的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="ae759-158">WpcUserSettings - Previously, timer restrictions supported 1 hour granularity.</span></span> <span data-ttu-id="ae759-159">在 Windows 8 現有的屬性工作表示每小時的前半小時。</span><span class="sxs-lookup"><span data-stu-id="ae759-159">In Windows 8 the existing property represents the first half-hour for each hour.</span></span> <span data-ttu-id="ae759-160">已加入新的半小時屬性來代表每個小時的後半部。</span><span class="sxs-lookup"><span data-stu-id="ae759-160">A new half-hour property has been added to represent the second half of each hour.</span></span> <span data-ttu-id="ae759-161">引進了其他新的屬性來表示每日額度額度。</span><span class="sxs-lookup"><span data-stu-id="ae759-161">Additional new property was introduced to represent daily time allowance.</span></span>

<span data-ttu-id="ae759-162">Web 內容篩選允許/封鎖清單匯出/匯入格式</span><span class="sxs-lookup"><span data-stu-id="ae759-162">Web Content Filter Allow/Block List Export/Import A Format</span></span>

-   <span data-ttu-id="ae759-163">不再支援 Web 內容篩選允許/封鎖清單匯出功能。</span><span class="sxs-lookup"><span data-stu-id="ae759-163">Web content filter Allow/Block list Export functionality is no longer supported.</span></span>

<span data-ttu-id="ae759-164">系列設定 WMI 提供者架構</span><span class="sxs-lookup"><span data-stu-id="ae759-164">Family Settings WMI Provider Schema</span></span>

-   <span data-ttu-id="ae759-165">已對 WpcUserSettings 類別進行下列新增，以反映時間限制的增強功能：</span><span class="sxs-lookup"><span data-stu-id="ae759-165">The following additions were made to the WpcUserSettings class to reflect time restrictions enhancements:</span></span>
    -   `[write: ToInstance ToSubClass, Description("Logon Half-Hours (30 minute offset) mask for this user"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 LogonHalfHours[7];`
    -   `[write: ToInstance ToSubClass, Description("Daily minute allowance"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 AllowanceMinutes[7];`

> [!Note]  
> <span data-ttu-id="ae759-166">Windows 8 使用新的登錄機碼，表示已為指定的使用者啟用家庭安全 API。</span><span class="sxs-lookup"><span data-stu-id="ae759-166">Windows 8 uses a new registry key to indicate that the Family Safety API is enabled for a given user.</span></span>
>
> <span data-ttu-id="ae759-167">**HKLM** \\**Microsoft** \\**軟體** \\**Windows** \\**CurrentVersion** \\**家長監護** \\**使用者** \\ **{UserSid}** \\**Web** \\**篩選準則**</span><span class="sxs-lookup"><span data-stu-id="ae759-167">**HKLM**\\**Microsoft**\\**Software**\\**Windows**\\**CurrentVersion**\\**Parental Controls**\\**Users**\\ **{UserSid}**\\**Web**\\**Filter On**</span></span>

 

<span data-ttu-id="ae759-168">下列登錄機碼僅支援 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="ae759-168">The following registry key is supported for Windows 7 only.</span></span>

<span data-ttu-id="ae759-169">**HKLM** \\**Microsoft** \\**軟體** \\**Windows** \\**CurrentVersion** \\**家長監護** \\**使用者** \\ **{UserSid}** \\**家長** 監護</span><span class="sxs-lookup"><span data-stu-id="ae759-169">**HKLM**\\**Microsoft**\\**Software**\\**Windows**\\**CurrentVersion**\\**Parental Controls**\\**Users**\\ **{UserSid}**\\**Parental Controls On**</span></span>

<span data-ttu-id="ae759-170">針對這兩個索引鍵，"0x00" (**DWORD**) 表示已停用目前使用者的功能，值為 "0x01" (**DWORD**) 表示已為目前使用者啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="ae759-170">For both keys, a value of "0x00" (**DWORD**) indicates the feature is disabled for the current user and a value of "0x01" (**DWORD**) indicates the feature is enabled for the current user.</span></span> <span data-ttu-id="ae759-171">嘗試讀取這些索引鍵的值時，請將 "{UserSid}" 權杖取代為使用者的系統識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae759-171">When attempting to read the values of these keys, replace the "{UserSid}" token with the user's system ID.</span></span>

 

 




