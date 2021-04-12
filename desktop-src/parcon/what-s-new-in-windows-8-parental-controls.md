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
# <a name="whats-new-in-windows-8-family-safety"></a>Windows 8 系列安全性的新功能

## <a name="overview-of-parental-controls-changes-for-windows-8"></a>Windows 8 的家長監護變更總覽

本檔的目的是概述 Windows 8 中 Windows 家長監護的變更，並讓協力廠商家長監護解決方案提供者能夠利用這些變更。 本檔假設讀者對 Windows 7 和 Windows Vista 的家長監護有熟悉，而且只會在與協力廠商家長監護開發相關的 Windows 8 中反映對這項功能的變更。

## <a name="key-design-decisions-for-windows-8-parental-controlfamily-safety-changes"></a>Windows 8 家長監護/系列安全性變更的關鍵設計決策

Windows 8 中所引進之家長監護的變更會繼續提升功能增強功能的主要目標，同時促進協力廠商家長監護解決方案與隨用隨的功能共存。 變更為：

-   使用 Microsoft 家長監護服務來提供遠端系統管理和遠端活動監視。
-   將 web 篩選整合為內建 Microsoft 限制的一部分，以及在 Windows 8 電腦上查看活動報告的功能。
-   主控台中的「家長監護」功能已重新命名為「家庭安全」，在本檔中也稱為。
-   內建的時間限制是藉由提供控制每日電腦總時間量的能力來增強 (時間額度) 除了能夠控制使用電腦 (的時間之外，還能讓您在舊版的 Windows 中使用 ) Curfew。
-   在標準帳戶建立流程期間可以開啟 Windows 8 系列安全功能。
-   Windows Vista 和 Windows 7 家長監護的擴充功能，Windows 8 系列的安全，包括由協力廠商解決方案取代 web 內容篩選器，或是取代內建的設定 UI，同時仍依賴內建的時間、應用程式、遊戲限制和網路內容篩選器等功能。
-   協力廠商提供者啟用會透過家庭安全網站，關閉 Windows 8 系列安全控制項的遠端系統管理和報告。
-   協力廠商的系列安全擴充功能僅支援 Windows 8 桌面應用程式。

## <a name="family-safety-and-standard-account-creation-in-windows-8"></a>Windows 8 中的家庭安全和標準帳戶建立

在 Windows 8 中建立標準帳戶的過程中，系統管理員可以依家庭安全開啟帳戶的監視功能。 以下是可控制的功能和協力廠商提供者的功能清單：

-   在 Windows 8 標準帳戶建立流程的最後一個畫面上，系統管理員會看到一個核取方塊，以開啟新建立之帳戶的家庭安全。
-   如果選取此核取方塊，則會針對具有下列設定的帳戶開啟家庭安全：
    -   活動報告開啟
    -   所有限制都已關閉
-   如果系統管理員使用 Microsoft 帳戶登入 Windows，則會將 Windows 8 電腦設定為從遠端系統管理家庭安全設定和電子郵件活動報告。 然後可以使用家庭安全網站，從遠端系統管理這類電腦。
-   如果協力廠商提供者希望該核取方塊出現在標準帳戶建立流程中，則提供者的註冊值應該會有下列值。 如需提供者註冊詳細資料的詳細資訊，請參閱「Windows 7 家長監護的新功能」主題的「 [提供者註冊](what-s-new-in-windows-7-parental-controls.md) 」一節。

    

    | 詞彙                                                                                                                         | 描述                                                                                                                                                                                                                                                                                  |
    |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>AddUserVisible<br/> | 選擇性的 **DWORD** 非零值，指定在將提供者選取為目前的家庭安全提供者之後，Windows 8 中的標準帳戶建立期間，為新建立的帳戶開啟家庭安全監視器的核取方塊選項應該是可見的。<br/> |

    

     

-   由於協力廠商提供者的設計是為了取代家庭安全控制項的內建設定 UI，因此根據預設，協力廠商提供者的安裝和啟用將會導致在建立標準帳戶期間開啟家庭安全的核取方塊選項，而不會顯示。

## <a name="family-safety-top-level-user-interface-changes-in-windows-8"></a>Windows 8 中的系列安全性最上層消費者介面變更

Windows 8 將下列對家長監護的變更，主控台最上層使用者介面：

-   當 Windows 8 電腦上至少一個標準帳戶的內建系列安全控制項開啟時，系統會顯示 [管理家庭安全網站命令] 連結的設定，讓系統管理員能夠透過家庭安全網站，建立 Windows 8 電腦系列安全性設定的遠端系統管理。
-   當 Windows 8 電腦設定為透過家庭安全網站進行遠端系統管理時，更多的資訊控制項可讓系統管理員透過家庭安全網站停用 Windows 8 電腦的遠端系統管理。
-   只有當至少有一個協力廠商提供者向家庭安全註冊時，才會顯示 [控制項] 區段。 此區段的 UI 和功能與 Windows 7 家長監護中的 [其他控制項] 區段相同。 如需詳細資訊，請參閱 [Windows 7 家長](what-s-new-in-windows-7-parental-controls.md) 監護主題的「家長監護使用者介面變更」一節。
-   當協力廠商提供者已安裝並選取為目前的提供者時，會停用透過家庭安全網站的 Windows 8 電腦系列安全設定遠端系統管理。

## <a name="family-safety-in-box-restrictions-changes-in-windows-8"></a>Windows 8 中的系列安全 In-Box 限制變更

Windows 8 將下列變更提供給家庭安全的內建限制：

Web 限制

-   執行已從多層式服務提供者變更 (LSP) 篩選至 Windows 篩選平台 (WFP) 驅動程式與在使用者會話中執行的家庭安全監視程式進行通訊。

時間限制

-   內建的時間限制已增強，可讓您控制電腦可用的總時間量 (時間額度) 除了能夠控制電腦可用的時間之外，還可以在舊版 Windows 中使用 (curfew) 。
-   適用于 curfew 的 UI 可讓您在一周的每一天進行獨立控制，並提供半小時的資料細微性。
-   時間額度的 UI 可讓您以15分鐘的資料細微性，在一周中的每一天對工作日/週末或獨立控制進行控制。
-   在封鎖的時間週期內，快速使用者切換 (FUS) 機制不再用來強制鎖定或封鎖受控制使用者的登入。 切換至不同的桌面會用於這些用途。
-   中斷連接警告事件不再適用于應用程式訂閱。

## <a name="family-safety-api-changes-in-windows-8"></a>Windows 8 中的家庭安全 API 變更

用於家庭安全的 Api 會公開原則和內建限制設定，以及記錄功能。

記錄

-   [系列安全性活動報告檢視器] 不再支援自訂事件。

WMI API 設定寫入/讀取

-   WpcUserSettings-之前的計時器限制支援1小時的資料細微性。 在 Windows 8 現有的屬性工作表示每小時的前半小時。 已加入新的半小時屬性來代表每個小時的後半部。 引進了其他新的屬性來表示每日額度額度。

Web 內容篩選允許/封鎖清單匯出/匯入格式

-   不再支援 Web 內容篩選允許/封鎖清單匯出功能。

系列設定 WMI 提供者架構

-   已對 WpcUserSettings 類別進行下列新增，以反映時間限制的增強功能：
    -   `[write: ToInstance ToSubClass, Description("Logon Half-Hours (30 minute offset) mask for this user"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 LogonHalfHours[7];`
    -   `[write: ToInstance ToSubClass, Description("Daily minute allowance"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 AllowanceMinutes[7];`

> [!Note]  
> Windows 8 使用新的登錄機碼，表示已為指定的使用者啟用家庭安全 API。
>
> **HKLM** \\**Microsoft** \\**軟體** \\**Windows** \\**CurrentVersion** \\**家長監護** \\**使用者** \\ **{UserSid}** \\**Web** \\**篩選準則**

 

下列登錄機碼僅支援 Windows 7。

**HKLM** \\**Microsoft** \\**軟體** \\**Windows** \\**CurrentVersion** \\**家長監護** \\**使用者** \\ **{UserSid}** \\**家長** 監護

針對這兩個索引鍵，"0x00" (**DWORD**) 表示已停用目前使用者的功能，值為 "0x01" (**DWORD**) 表示已為目前使用者啟用此功能。 嘗試讀取這些索引鍵的值時，請將 "{UserSid}" 權杖取代為使用者的系統識別碼。

 

 




