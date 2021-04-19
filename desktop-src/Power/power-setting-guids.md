---
description: 電源設定 Guid 可識別電源變更事件。
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: '電源設定 Guid (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983198"
---
# <a name="power-setting-guids"></a><span data-ttu-id="16008-103">電源設定 Guid</span><span class="sxs-lookup"><span data-stu-id="16008-103">Power Setting GUIDs</span></span>

<span data-ttu-id="16008-104">電源設定 **GUID** s 識別電源變更事件。</span><span class="sxs-lookup"><span data-stu-id="16008-104">Power setting **GUID** s identify power change events.</span></span> <span data-ttu-id="16008-105">本主題列出最適合應用程式之通知的電源設定 **GUID** s。</span><span class="sxs-lookup"><span data-stu-id="16008-105">This topic lists power setting **GUID** s for notifications that are most useful to applications.</span></span> <span data-ttu-id="16008-106">應用程式應該針對可能影響其行為的每個電源變更事件註冊。</span><span class="sxs-lookup"><span data-stu-id="16008-106">An application should register for each power change event that might impact its behavior.</span></span> <span data-ttu-id="16008-107">每次設定變更時就會傳送通知。</span><span class="sxs-lookup"><span data-stu-id="16008-107">Notification is sent each time a setting changes.</span></span>

<span data-ttu-id="16008-108">電源設定 **GUID** s 定義于 WinNT. h 中。</span><span class="sxs-lookup"><span data-stu-id="16008-108">Power setting **GUID** s are defined in WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="16008-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID \_ ACDC \_ 電源 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="16008-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID\_ACDC\_POWER\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span><span class="sxs-lookup"><span data-stu-id="16008-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span></span>
</dt> <dt>



<span data-ttu-id="16008-111">系統電源來源已變更。</span><span class="sxs-lookup"><span data-stu-id="16008-111">The system power source has changed.</span></span> <span data-ttu-id="16008-112">**資料** 成員是具有 [**系統 \_ 電源 \_ 條件**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition)列舉值的 **DWORD** ，指出目前的電源來源。</span><span class="sxs-lookup"><span data-stu-id="16008-112">The **Data** member is a **DWORD** with values from the [**SYSTEM\_POWER\_CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) enumeration that indicates the current power source.</span></span>

<dl> <dt>

<span data-ttu-id="16008-113">**PoAc** (0) -電腦是由 AC 電源來源 (或類似的電源，例如由12v 汽車介面卡) 所提供的膝上型電腦。</span><span class="sxs-lookup"><span data-stu-id="16008-113">**PoAc** (0) - The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive adapter).</span></span>
</dt> <dt>

<span data-ttu-id="16008-114">**PoDc** (1) -電腦是使用上架電池電源來源所提供的電源。</span><span class="sxs-lookup"><span data-stu-id="16008-114">**PoDc** (1) - The computer is powered by an onboard battery power source.</span></span>
</dt> <dt>

<span data-ttu-id="16008-115">**PoHot** (2) -電腦是由短期電源來源（例如 UPS 裝置）所驅動。</span><span class="sxs-lookup"><span data-stu-id="16008-115">**PoHot** (2) - The computer is powered by a short-term power source such as a UPS device.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="16008-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID \_ 剩餘的電池 \_ 百分比 \_**</span><span class="sxs-lookup"><span data-stu-id="16008-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID\_BATTERY\_PERCENTAGE\_REMAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span><span class="sxs-lookup"><span data-stu-id="16008-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span></span>
</dt> <dt>



<span data-ttu-id="16008-118">剩餘的電池容量已變更。</span><span class="sxs-lookup"><span data-stu-id="16008-118">The remaining battery capacity has changed.</span></span> <span data-ttu-id="16008-119">資料細微性會因系統而異，但最精細的資料細微性是1%。</span><span class="sxs-lookup"><span data-stu-id="16008-119">The granularity varies from system to system but the finest granularity is 1 percent.</span></span> <span data-ttu-id="16008-120">**資料** 成員是一個 **DWORD** ，表示目前的電池容量，以從0到100的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="16008-120">The **Data** member is a **DWORD** that indicates the current battery capacity remaining as a percentage from 0 through 100.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16008-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID \_ 主控台 \_ 顯示 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="16008-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID\_CONSOLE\_DISPLAY\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span><span class="sxs-lookup"><span data-stu-id="16008-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span></span>
</dt> <dt>



<span data-ttu-id="16008-123">目前監視器的顯示狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="16008-123">The current monitor's display state has changed.</span></span>

<span data-ttu-id="16008-124">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 從 Windows 8 和 Windows Server 2012 開始，可以取得這項通知。</span><span class="sxs-lookup"><span data-stu-id="16008-124">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="16008-125">**資料** 成員是具有下列其中一個值的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="16008-125">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="16008-126">0x0-顯示為關閉。</span><span class="sxs-lookup"><span data-stu-id="16008-126">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="16008-127">0x1-顯示為開啟。</span><span class="sxs-lookup"><span data-stu-id="16008-127">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="16008-128">0x2-顯示呈現灰色。</span><span class="sxs-lookup"><span data-stu-id="16008-128">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="16008-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID \_ 全域 \_ 使用者 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="16008-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID\_GLOBAL\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span><span class="sxs-lookup"><span data-stu-id="16008-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span></span>
</dt> <dt>



<span data-ttu-id="16008-131">與任何會話相關聯的使用者狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="16008-131">The user status associated with any session has changed.</span></span> <span data-ttu-id="16008-132">這代表系統上所有本機和遠端會話的使用者狀態合併狀態。</span><span class="sxs-lookup"><span data-stu-id="16008-132">This represents the combined status of user presence across all local and remote sessions on the system.</span></span>

<span data-ttu-id="16008-133">此通知只會傳送服務以及在會話0中執行的其他程式。</span><span class="sxs-lookup"><span data-stu-id="16008-133">This notification is sent only services and other programs running in session 0.</span></span> <span data-ttu-id="16008-134">使用者模式應用程式應該改為註冊 **GUID \_ 會話使用者的 \_ \_ 狀態** 。</span><span class="sxs-lookup"><span data-stu-id="16008-134">User-mode applications should register for **GUID\_SESSION\_USER\_PRESENCE** instead.</span></span>

<span data-ttu-id="16008-135">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 從 Windows 8 和 Windows Server 2012 開始，可以取得這項通知。</span><span class="sxs-lookup"><span data-stu-id="16008-135">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="16008-136">**資料** 成員是具有下列其中一個值的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="16008-136">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="16008-137">**PowerUserPresent** (0) -使用者存在於系統上的任何本機或遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="16008-137">**PowerUserPresent** (0) - The user is present in any local or remote session on the system.</span></span>
</dt> <dt>

<span data-ttu-id="16008-138">**PowerUserInactive** (2) -使用者不存在於系統上的任何本機或遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="16008-138">**PowerUserInactive** (2) - The user is not present in any local or remote session on the system.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="16008-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID \_ 閒置 \_ 背景 \_ 工作**</span><span class="sxs-lookup"><span data-stu-id="16008-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID\_IDLE\_BACKGROUND\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span><span class="sxs-lookup"><span data-stu-id="16008-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span></span>
</dt> <dt>



<span data-ttu-id="16008-141">系統忙碌中。</span><span class="sxs-lookup"><span data-stu-id="16008-141">The system is busy.</span></span> <span data-ttu-id="16008-142">這表示系統將不會在不久的將來進入閒置狀態，而且目前的時間是元件執行背景或閒置工作的好時機，否則會導致電腦無法進入閒置狀態。</span><span class="sxs-lookup"><span data-stu-id="16008-142">This indicates that the system will not be moving into an idle state in the near future and that the current time is a good time for components to perform background or idle tasks that would otherwise prevent the computer from entering an idle state.</span></span>

<span data-ttu-id="16008-143">當系統無法進入閒置狀態時，就不會有任何通知。</span><span class="sxs-lookup"><span data-stu-id="16008-143">There is no notification when the system is able to move into an idle state.</span></span> <span data-ttu-id="16008-144">閒置背景工作通知不會指出使用者是否存在於電腦上。</span><span class="sxs-lookup"><span data-stu-id="16008-144">The idle background task notification does not indicate whether a user is present at the computer.</span></span> <span data-ttu-id="16008-145">**資料** 成員沒有任何資訊，而且可以忽略。</span><span class="sxs-lookup"><span data-stu-id="16008-145">The **Data** member has no information and can be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16008-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID \_ 監視器 \_ 電源 \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="16008-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID\_MONITOR\_POWER\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span><span class="sxs-lookup"><span data-stu-id="16008-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span></span>
</dt> <dt>



<span data-ttu-id="16008-148">主要系統監視器已開啟或關閉電源。</span><span class="sxs-lookup"><span data-stu-id="16008-148">The primary system monitor has been powered on or off.</span></span> <span data-ttu-id="16008-149">這項通知適用于主動將內容轉譯至顯示裝置的元件，例如媒體視覺效果。</span><span class="sxs-lookup"><span data-stu-id="16008-149">This notification is useful for components that actively render content to the display device, such as media visualization.</span></span> <span data-ttu-id="16008-150">這些應用程式應該註冊此通知，並在監視器關閉時停止轉譯圖形內容，以減少系統電源耗用量。</span><span class="sxs-lookup"><span data-stu-id="16008-150">These applications should register for this notification and stop rendering graphics content when the monitor is off to reduce system power consumption.</span></span> <span data-ttu-id="16008-151">**資料** 成員是一個 **DWORD** ，表示目前的監視器狀態。</span><span class="sxs-lookup"><span data-stu-id="16008-151">The **Data** member is a **DWORD** that indicates the current monitor state.</span></span>

<dl> <dt>

<span data-ttu-id="16008-152">0x0-監視器已關閉。</span><span class="sxs-lookup"><span data-stu-id="16008-152">0x0 - The monitor is off.</span></span>
</dt> <dt>

<span data-ttu-id="16008-153">0x1-監視器已開啟。</span><span class="sxs-lookup"><span data-stu-id="16008-153">0x1 - The monitor is on.</span></span>
</dt> </dl>

<span data-ttu-id="16008-154">**Windows 8 和 Windows Server 2012：** 新的應用程式應該使用 **GUID \_ 主控台 \_ 顯示 \_ 狀態** ，而不是這項通知。</span><span class="sxs-lookup"><span data-stu-id="16008-154">**Windows 8 and Windows Server 2012:** New applications should use **GUID\_CONSOLE\_DISPLAY\_STATE** instead of this notification.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="16008-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID \_ 省 \_ 電 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="16008-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID\_POWER\_SAVING\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span><span class="sxs-lookup"><span data-stu-id="16008-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span></span>
</dt> <dt>



<span data-ttu-id="16008-157">節電程式已關閉或開啟，以回應變更電源的情況。</span><span class="sxs-lookup"><span data-stu-id="16008-157">Battery saver has been turned off or on in response to changing power conditions.</span></span> <span data-ttu-id="16008-158">此通知適用于參與能源節約的元件。</span><span class="sxs-lookup"><span data-stu-id="16008-158">This notification is useful for components that participate in energy conservation.</span></span> <span data-ttu-id="16008-159">這些應用程式應該註冊這項通知，並在省電模式開啟時省下電源。</span><span class="sxs-lookup"><span data-stu-id="16008-159">These applications should register for this notification and save power when battery saver is on.</span></span>

<span data-ttu-id="16008-160">**資料** 成員是指出省電模式狀態的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="16008-160">The **Data** member is a **DWORD** that indicates battery saver state.</span></span>

<dl> <dt>

<span data-ttu-id="16008-161">0x0-節電功能已關閉。</span><span class="sxs-lookup"><span data-stu-id="16008-161">0x0 - Battery saver is off.</span></span>
</dt> <dt>

<span data-ttu-id="16008-162">0x1-節電開啟。</span><span class="sxs-lookup"><span data-stu-id="16008-162">0x1 - Battery saver is on.</span></span> <span data-ttu-id="16008-163">盡可能省下能源。</span><span class="sxs-lookup"><span data-stu-id="16008-163">Save energy where possible.</span></span>
</dt> </dl>

<span data-ttu-id="16008-164">如需有關省電模式的一般資訊，請參閱 [硬體元件指導方針中的省電模式 () ](/windows-hardware/design/component-guidelines/battery-saver)。</span><span class="sxs-lookup"><span data-stu-id="16008-164">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

</dl> </dd> <dt>

<span data-ttu-id="16008-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID \_ POWERSCHEME \_ 個人化**</span><span class="sxs-lookup"><span data-stu-id="16008-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID\_POWERSCHEME\_PERSONALITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-166">245d8541-3943-4422-b025-13A784F679B7</span><span class="sxs-lookup"><span data-stu-id="16008-166">245d8541-3943-4422-b025-13A784F679B7</span></span>
</dt> <dt>



<span data-ttu-id="16008-167">使用中的電源配置個人化已變更。</span><span class="sxs-lookup"><span data-stu-id="16008-167">The active power scheme personality has changed.</span></span> <span data-ttu-id="16008-168">所有電源配置都對應到其中一個特質。</span><span class="sxs-lookup"><span data-stu-id="16008-168">All power schemes map to one of these personalities.</span></span> <span data-ttu-id="16008-169">**資料** 成員是指出新的主動式電源配置特性的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="16008-169">The **Data** member is a **GUID** that indicates the new active power scheme personality.</span></span>

<dl> <dt>



<span data-ttu-id="16008-170">**GUID \_\_ \_ 省電的最小** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C) </span><span class="sxs-lookup"><span data-stu-id="16008-170">**GUID\_MIN\_POWER\_SAVINGS** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span></span>

<span data-ttu-id="16008-171">高效能-此配置旨在提供最高的效能，同時節省耗電量。</span><span class="sxs-lookup"><span data-stu-id="16008-171">High Performance - The scheme is designed to deliver maximum performance at the expense of power consumption savings.</span></span>


</dt> <dt>



<span data-ttu-id="16008-172">**GUID \_\_ \_ 省電** (A1841308-3541-4FAB-BC81-F71556F20B4A) 的最大耗電量</span><span class="sxs-lookup"><span data-stu-id="16008-172">**GUID\_MAX\_POWER\_SAVINGS** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span></span>

<span data-ttu-id="16008-173">省電-此配置的設計目的是要提供最大的耗電量節省，代價是系統效能和回應性。</span><span class="sxs-lookup"><span data-stu-id="16008-173">Power Saver - The scheme is designed to deliver maximum power consumption savings at the expense of system performance and responsiveness.</span></span>


</dt> <dt>



<span data-ttu-id="16008-174">**GUID \_一般 \_ \_ 省電** (381B4222-F694-41F0-9685-FF5BB260DF2E) </span><span class="sxs-lookup"><span data-stu-id="16008-174">**GUID\_TYPICAL\_POWER\_SAVINGS** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span></span>

<span data-ttu-id="16008-175">自動-此配置的設計目的是要自動平衡效能和耗電量節省量。</span><span class="sxs-lookup"><span data-stu-id="16008-175">Automatic - The scheme is designed to automatically balance performance and power consumption savings.</span></span>


</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="16008-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID \_ 會話 \_ 顯示 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="16008-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID\_SESSION\_DISPLAY\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span><span class="sxs-lookup"><span data-stu-id="16008-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span></span>
</dt> <dt>



<span data-ttu-id="16008-178">與應用程式會話相關聯的顯示器已開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="16008-178">The display associated with the application's session has been powered on or off.</span></span>

<span data-ttu-id="16008-179">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 從 Windows 8 和 Windows Server 2012 開始，可以取得這項通知。</span><span class="sxs-lookup"><span data-stu-id="16008-179">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="16008-180">此通知只會傳送至使用者模式應用程式。</span><span class="sxs-lookup"><span data-stu-id="16008-180">This notification is sent only to user-mode applications.</span></span> <span data-ttu-id="16008-181">在會話0中執行的服務和其他程式不會收到此通知。</span><span class="sxs-lookup"><span data-stu-id="16008-181">Services and other programs running in session 0 do not receive this notification.</span></span> <span data-ttu-id="16008-182">**資料** 成員是具有下列其中一個值的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="16008-182">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="16008-183">0x0-顯示為關閉。</span><span class="sxs-lookup"><span data-stu-id="16008-183">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="16008-184">0x1-顯示為開啟。</span><span class="sxs-lookup"><span data-stu-id="16008-184">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="16008-185">0x2-顯示呈現灰色。</span><span class="sxs-lookup"><span data-stu-id="16008-185">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="16008-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID \_ 會話 \_ 使用者 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="16008-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID\_SESSION\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span><span class="sxs-lookup"><span data-stu-id="16008-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span></span>
</dt> <dt>



<span data-ttu-id="16008-188">與應用程式會話相關聯的使用者狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="16008-188">The user status associated with the application's session has changed.</span></span>

<span data-ttu-id="16008-189">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 從 Windows 8 和 Windows Server 2012 開始，可以取得這項通知。</span><span class="sxs-lookup"><span data-stu-id="16008-189">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="16008-190">此通知只會傳送到在互動式會話中執行的使用者模式應用程式。</span><span class="sxs-lookup"><span data-stu-id="16008-190">This notification is sent only to user-mode applications running in an interactive session.</span></span> <span data-ttu-id="16008-191">在會話0中執行的服務和其他程式應該註冊 **GUID \_ 全域使用者的 \_ \_ 狀態**。</span><span class="sxs-lookup"><span data-stu-id="16008-191">Services and other programs running in session 0 should register for **GUID\_GLOBAL\_USER\_PRESENCE**.</span></span> <span data-ttu-id="16008-192">**資料** 成員是具有下列其中一個值的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="16008-192">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="16008-193">**PowerUserPresent** (0) -使用者正在提供會話的輸入。</span><span class="sxs-lookup"><span data-stu-id="16008-193">**PowerUserPresent** (0) - The user is providing input to the session.</span></span>
</dt> <dt>

<span data-ttu-id="16008-194">**PowerUserInactive** (2) -使用者活動等待時間已過，因此沒有使用者的互動。</span><span class="sxs-lookup"><span data-stu-id="16008-194">**PowerUserInactive** (2) - The user activity timeout has elapsed with no interaction from the user.</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="16008-195">在互動式使用者模式會話中執行的所有應用程式都應該使用此設定。</span><span class="sxs-lookup"><span data-stu-id="16008-195">All applications that run in an interactive user-mode session should use this setting.</span></span> <span data-ttu-id="16008-196">當核心模式應用程式註冊監視狀態時，應該改為使用 **GUID \_ 主控台 \_ 顯示 \_ 狀態** 。</span><span class="sxs-lookup"><span data-stu-id="16008-196">When kernel mode applications register for monitor status they should use **GUID\_CONSOLE\_DISPLAY\_STATUS** instead.</span></span>

 

</dl> </dd> <dt>

<span data-ttu-id="16008-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID \_ 系統 \_ 離開模式**</span><span class="sxs-lookup"><span data-stu-id="16008-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID\_SYSTEM\_AWAYMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16008-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span><span class="sxs-lookup"><span data-stu-id="16008-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span></span>
</dt> <dt>



<span data-ttu-id="16008-199">系統進入或離開模式。</span><span class="sxs-lookup"><span data-stu-id="16008-199">The system is entering or exiting away mode.</span></span> <span data-ttu-id="16008-200">**資料** 成員是一個 **DWORD** ，表示目前的離開模式狀態。</span><span class="sxs-lookup"><span data-stu-id="16008-200">The **Data** member is a **DWORD** that indicates the current away mode state.</span></span>

<dl> <dt>

<span data-ttu-id="16008-201">0x0-電腦即將離開模式。</span><span class="sxs-lookup"><span data-stu-id="16008-201">0x0 - The computer is exiting away mode.</span></span>
</dt> <dt>

<span data-ttu-id="16008-202">0x1-電腦進入離開模式。</span><span class="sxs-lookup"><span data-stu-id="16008-202">0x1 - The computer is entering away mode.</span></span>
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16008-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="16008-203">Requirements</span></span>



| <span data-ttu-id="16008-204">需求</span><span class="sxs-lookup"><span data-stu-id="16008-204">Requirement</span></span> | <span data-ttu-id="16008-205">值</span><span class="sxs-lookup"><span data-stu-id="16008-205">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16008-206">標頭</span><span class="sxs-lookup"><span data-stu-id="16008-206">Header</span></span><br/> | <dl> <span data-ttu-id="16008-207"><dt>WinNT。h</dt></span><span class="sxs-lookup"><span data-stu-id="16008-207"><dt>WinNT.h</dt></span></span> </dl> |



 

