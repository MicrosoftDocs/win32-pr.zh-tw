---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: 與 HKEY \_ 本機電腦軟體相關的登錄 \_ 值 \\ \\ \\ 會控制預設的啟動和存取權限設定，以及未呼叫 CoInitializeSecurity 的 COM 應用程式的呼叫層級安全性功能。
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02406bca5dd69098f8cd49c2fba5f067852fcc5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022010"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Ole

與 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ \\** 相關的登錄值會控制預設的啟動和存取權限設定，以及未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的 COM 應用程式的呼叫層級安全性功能。

只有系統管理員、物件建立者和系統具有登錄的這個部分的完整存取權。 所有其他使用者都具有唯讀存取權。



| 登錄值                                                                         | Description                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md)                 | 針對元件啟動和啟用的失敗要求，設定事件記錄檔專案的詳細資訊。                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | 設定有關元件呼叫失敗的事件記錄檔專案詳細程度。                                                                                                     |
| [**DCOMSCMRemoteCallFlags**](dcomscmremotecallflags.md)                               | 控制從本機 DCOM 服務控制管理員 (DCOMSCM) 至遠端 DCOMSCM 的呼叫行為。                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | 定義電腦的預設存取權限清單。                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | 定義電腦的預設啟動 ACL。                                                                                                                                  |
| [**EnableDCOM**](enabledcom.md)                                                       | 設定電腦的全域啟用原則。                                                                                                                           |
| [**InvalidSecurityDescriptorLoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | 針對元件啟動和存取權限的無效安全描述項，設定事件記錄檔專案的詳細資訊。                                                       |
| [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)                         | 設定預設驗證層級。                                                                                                                                        |
| [**LegacyImpersonationLevel**](legacyimpersonationlevel.md)                           | 設定預設的模擬層級。                                                                                                                                         |
| [**LegacySecureReferences**](legacysecurereferences.md)                               | 判斷 **AddRef** / **發行** 調用的安全性層級。                                                                                                              |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | 針對元件存取設定整個電腦的限制原則。                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | 設定元件啟動和啟用的全電腦限制原則。                                                                                                |
| [**NonRedist**](nonredist.md)                                                         | 將名稱加入至封裝中的 COM + 應用程式在其他電腦上安裝時，不應該匯出的檔案清單。 請注意，這是子機碼，而不是值。 |
| [**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)                   | 判斷 ActivateAsActivator 啟用期間是否使用軟體限制原則 (SRP) 信任層級。                                                            |
| [**SRPRunningObjectChecks**](srprunningobjectchecks.md)                               | 決定是否要針對相容的軟體限制原則（ (SRP) 信任層級）篩選連接到執行中物件的嘗試。                                         |



 

 

 




