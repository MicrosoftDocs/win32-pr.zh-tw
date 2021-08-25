---
title: WCS 登錄機碼
description: WCS 使用登錄機碼來表示已發生特定色彩設定檔事件。 應用程式應該查詢這些登錄機碼，以取得更新的系統色彩設定檔狀態。
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows色彩系統 (WCS) 、登錄機碼
- WCS (Windows 色彩系統) 、登錄機碼
- 影像色彩管理、登錄機碼
- 色彩管理，登錄機碼
- 色彩、登錄機碼
- WCS 參考，登錄機碼
- WCS 的參考，登錄機碼
- Windows色彩系統 (WCS) ，登錄
- WCS (Windows Color System) ，registry
- 影像色彩管理，登錄
- 色彩管理，登錄
- 色彩，登錄
- WCS 參考，登錄
- WCS、registry 的參考
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c12047d83ccc2f80c26521a59a040fa45df0c21e9bb035efff6ed5d38e8827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814348"
---
# <a name="wcs-registry-keys"></a>WCS 登錄機碼

WCS 使用登錄機碼來表示已發生特定色彩設定檔事件。 應用程式應該查詢這些登錄機碼，以取得更新的系統色彩設定檔狀態。

## <a name="active-color-profile-changed"></a>現用色彩設定檔已變更

應用程式可能會想要回應監視裝置的色彩設定檔變更事件;這可確保即使使用者或其他應用程式已變更裝置的使用中設定檔，它們的目標一律會有正確的色彩資訊。

### <a name="desktop-applications"></a>傳統型應用程式

桌面應用程式應該接聽登錄的變更，以判斷色彩設定檔關聯何時使用 [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue)變更。 應用程式應該針對每個使用者設定檔的關聯變更，以及進行全系統的變更註冊。

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) 應該使用 [**REGOPENKEYEX**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)提供的 HKEY 來初始化。 **RegOpenKeyEx** 應使用下列登錄樹狀目錄位置進行初始化：



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 每個使用者設定檔關聯    | **HKEY \_ 目前的 \_ 使用者軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ 顯示 \\ {4d36e96e-e325-11ce-bfc1-08002be10318}** |
| 全系統設定檔關聯 | **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Class \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**                                        |



 

當應用程式收到登錄機碼變更的通知時，它應該會先使用呼叫 [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)來查詢是否正在使用每個使用者或整個系統的關聯。 接著，它應該使用正確的 [**WCS \_ 設定檔 \_ 管理 \_ 範圍**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)值來呼叫 [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) ，以取得監視器的新現用色彩設定檔。 請注意，並非所有登錄機碼變更都會對應到目前作用中色彩設定檔中的實際變更;應用程式必須會檢查 **WcsGetDefaultColorProfile** 所傳回的設定檔是否確實變更。

### <a name="universal-windows-uwp-apps"></a> (UWP) 應用程式的通用 Windows

通用 Windows 應用程式沒有上述登錄機碼的存取權。 相反地，它們應該註冊 [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) 事件的處理常式。 每當應用程式執行所在之監視的現用色彩設定檔變更時，就會引發此事件。 ColorProfileChanged 會考慮每個使用者或整個系統設定檔關聯是否正在使用中;這項資訊是從 UWP 應用程式抽象化。

回應 ColorProfileChanged 事件時，應用程式應該使用 DisplayInformation 來查詢目前作用中的設定檔 [**。**](/uwp/api/Windows.Graphics.Display.DisplayInformation)

 

 