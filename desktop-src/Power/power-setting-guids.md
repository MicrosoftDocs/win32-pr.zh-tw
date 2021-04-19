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
# <a name="power-setting-guids"></a>電源設定 Guid

電源設定 **GUID** s 識別電源變更事件。 本主題列出最適合應用程式之通知的電源設定 **GUID** s。 應用程式應該針對可能影響其行為的每個電源變更事件註冊。 每次設定變更時就會傳送通知。

電源設定 **GUID** s 定義于 WinNT. h 中。

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID \_ ACDC \_ 電源 \_ 來源**
</dt> <dd> <dl> <dt>

5D3E9A59-E9D5-4B00-A6BD-FF34FF516548
</dt> <dt>



系統電源來源已變更。 **資料** 成員是具有 [**系統 \_ 電源 \_ 條件**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition)列舉值的 **DWORD** ，指出目前的電源來源。

<dl> <dt>

**PoAc** (0) -電腦是由 AC 電源來源 (或類似的電源，例如由12v 汽車介面卡) 所提供的膝上型電腦。
</dt> <dt>

**PoDc** (1) -電腦是使用上架電池電源來源所提供的電源。
</dt> <dt>

**PoHot** (2) -電腦是由短期電源來源（例如 UPS 裝置）所驅動。
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID \_ 剩餘的電池 \_ 百分比 \_**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-EECBB468A9E1
</dt> <dt>



剩餘的電池容量已變更。 資料細微性會因系統而異，但最精細的資料細微性是1%。 **資料** 成員是一個 **DWORD** ，表示目前的電池容量，以從0到100的百分比表示。


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID \_ 主控台 \_ 顯示 \_ 狀態**
</dt> <dd> <dl> <dt>

6FE69556-704A-47A0-8F24-C28D936FDA47
</dt> <dt>



目前監視器的顯示狀態已變更。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 從 Windows 8 和 Windows Server 2012 開始，可以取得這項通知。

**資料** 成員是具有下列其中一個值的 **DWORD** 。

<dl> <dt>

0x0-顯示為關閉。
</dt> <dt>

0x1-顯示為開啟。
</dt> <dt>

0x2-顯示呈現灰色。
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID \_ 全域 \_ 使用者 \_ 狀態**
</dt> <dd> <dl> <dt>

786E8A1D-B427-4344-9207-09E70BDCBEA9
</dt> <dt>



與任何會話相關聯的使用者狀態已變更。 這代表系統上所有本機和遠端會話的使用者狀態合併狀態。

此通知只會傳送服務以及在會話0中執行的其他程式。 使用者模式應用程式應該改為註冊 **GUID \_ 會話使用者的 \_ \_ 狀態** 。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 從 Windows 8 和 Windows Server 2012 開始，可以取得這項通知。

**資料** 成員是具有下列其中一個值的 **DWORD** 。

<dl> <dt>

**PowerUserPresent** (0) -使用者存在於系統上的任何本機或遠端會話中。
</dt> <dt>

**PowerUserInactive** (2) -使用者不存在於系統上的任何本機或遠端會話中。
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID \_ 閒置 \_ 背景 \_ 工作**
</dt> <dd> <dl> <dt>

515C31D8-F734-163D-A0FD-11A08C91E8F1
</dt> <dt>



系統忙碌中。 這表示系統將不會在不久的將來進入閒置狀態，而且目前的時間是元件執行背景或閒置工作的好時機，否則會導致電腦無法進入閒置狀態。

當系統無法進入閒置狀態時，就不會有任何通知。 閒置背景工作通知不會指出使用者是否存在於電腦上。 **資料** 成員沒有任何資訊，而且可以忽略。


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID \_ 監視器 \_ 電源 \_ 開啟**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99E6-E5A17EBD1AEA
</dt> <dt>



主要系統監視器已開啟或關閉電源。 這項通知適用于主動將內容轉譯至顯示裝置的元件，例如媒體視覺效果。 這些應用程式應該註冊此通知，並在監視器關閉時停止轉譯圖形內容，以減少系統電源耗用量。 **資料** 成員是一個 **DWORD** ，表示目前的監視器狀態。

<dl> <dt>

0x0-監視器已關閉。
</dt> <dt>

0x1-監視器已開啟。
</dt> </dl>

**Windows 8 和 Windows Server 2012：** 新的應用程式應該使用 **GUID \_ 主控台 \_ 顯示 \_ 狀態** ，而不是這項通知。

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID \_ 省 \_ 電 \_ 狀態**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



節電程式已關閉或開啟，以回應變更電源的情況。 此通知適用于參與能源節約的元件。 這些應用程式應該註冊這項通知，並在省電模式開啟時省下電源。

**資料** 成員是指出省電模式狀態的 **DWORD** 。

<dl> <dt>

0x0-節電功能已關閉。
</dt> <dt>

0x1-節電開啟。 盡可能省下能源。
</dt> </dl>

如需有關省電模式的一般資訊，請參閱 [硬體元件指導方針中的省電模式 () ](/windows-hardware/design/component-guidelines/battery-saver)。

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID \_ POWERSCHEME \_ 個人化**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-b025-13A784F679B7
</dt> <dt>



使用中的電源配置個人化已變更。 所有電源配置都對應到其中一個特質。 **資料** 成員是指出新的主動式電源配置特性的 **GUID** 。

<dl> <dt>



**GUID \_\_ \_ 省電的最小** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C) 

高效能-此配置旨在提供最高的效能，同時節省耗電量。


</dt> <dt>



**GUID \_\_ \_ 省電** (A1841308-3541-4FAB-BC81-F71556F20B4A) 的最大耗電量

省電-此配置的設計目的是要提供最大的耗電量節省，代價是系統效能和回應性。


</dt> <dt>



**GUID \_一般 \_ \_ 省電** (381B4222-F694-41F0-9685-FF5BB260DF2E) 

自動-此配置的設計目的是要自動平衡效能和耗電量節省量。


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID \_ 會話 \_ 顯示 \_ 狀態**
</dt> <dd> <dl> <dt>

2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5
</dt> <dt>



與應用程式會話相關聯的顯示器已開啟或關閉。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 從 Windows 8 和 Windows Server 2012 開始，可以取得這項通知。

此通知只會傳送至使用者模式應用程式。 在會話0中執行的服務和其他程式不會收到此通知。 **資料** 成員是具有下列其中一個值的 **DWORD** 。

<dl> <dt>

0x0-顯示為關閉。
</dt> <dt>

0x1-顯示為開啟。
</dt> <dt>

0x2-顯示呈現灰色。
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID \_ 會話 \_ 使用者 \_ 狀態**
</dt> <dd> <dl> <dt>

3C0F4548-C03F-4c4d-B9F2-237EDE686376
</dt> <dt>



與應用程式會話相關聯的使用者狀態已變更。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 從 Windows 8 和 Windows Server 2012 開始，可以取得這項通知。

此通知只會傳送到在互動式會話中執行的使用者模式應用程式。 在會話0中執行的服務和其他程式應該註冊 **GUID \_ 全域使用者的 \_ \_ 狀態**。 **資料** 成員是具有下列其中一個值的 **DWORD** 。

<dl> <dt>

**PowerUserPresent** (0) -使用者正在提供會話的輸入。
</dt> <dt>

**PowerUserInactive** (2) -使用者活動等待時間已過，因此沒有使用者的互動。
</dt> </dl>

> [!Note]  
> 在互動式使用者模式會話中執行的所有應用程式都應該使用此設定。 當核心模式應用程式註冊監視狀態時，應該改為使用 **GUID \_ 主控台 \_ 顯示 \_ 狀態** 。

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID \_ 系統 \_ 離開模式**
</dt> <dd> <dl> <dt>

98A7F580-01F7-48AA-9C0F-44352C29E5C0
</dt> <dt>



系統進入或離開模式。 **資料** 成員是一個 **DWORD** ，表示目前的離開模式狀態。

<dl> <dt>

0x0-電腦即將離開模式。
</dt> <dt>

0x1-電腦進入離開模式。
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>WinNT。h</dt> </dl> |



 

