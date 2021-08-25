---
description: 概述 Windows 7 中引進的 Windows 家長監護的變更。
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Windows 7 家長監護有哪些新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7b545c6791d286e51ae7a36ed65623d1697a7e742b1ae956e3ef4aaf3425e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951818"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Windows 7 父母控制項的新功能

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Windows 7 的家長監護變更總覽

本檔的目的是概述 Windows 7 中所引進 Windows 家長監護的變更，並讓協力廠商家長監護解決方案提供者能夠利用這些變更。 本檔假設讀者對 Windows Vista 的家長監護有熟悉，而且只會反映在與協力廠商家長監護開發相關的 Windows 7 中所做的這項功能變更。 MSDN Windows 家長監護檔的完整更新將在稍後的日期之後進行。

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Windows 7 家長監護變更的關鍵設計決策

Windows 7 中所引進之家長監護的變更，可繼續提升協力廠商家長監護解決方案與隨用隨的功能共存的主要目標。 變更為：

-   從內建家長監護功能移除 web 篩選和活動報告。 內建的家長監護提供核心離線 Microsoft 實行的限制，例如時間限制、應用程式限制和遊戲限制。 Microsoft 或協力廠商家長監護解決方案可以提供 web 篩選、活動報告和其他功能。 例如，Windows Live 家長監護服務解決方案提供網路篩選、遠端系統管理和活動監視，以及所有 Windows 即時應用程式的連絡人管理。
-   啟用協力廠商解決方案來取代內建提供者的設定使用者介面，同時仍依賴內建的時間、應用程式和遊戲限制的執行。
-    (系統管理員帳戶) ，啟用在電腦上探索和啟用的協力廠商解決方案。

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>家長監護 Windows 7 中最上層的消費者介面變更

Windows 7 會將下列變更提供給上層使用者介面主控台的家長監護：

-   另外也引進了可從下拉式清單方塊中選取提供其他功能的控制項（例如，web 篩選、活動報告等等）的控制項區段。 Microsoft 或協力廠商提供者必須向 Windows 7 家長監護註冊解決方案，才能從 [其他控制項] 下拉式清單方塊中選取這些控制項。 如需註冊解決方案的詳細資訊，請參閱本主題稍後的「提供者註冊」) 。
-   目前所選提供者的標誌影像會顯示在頁面的右上角。
-   受管理的使用者磚可顯示目前所選取提供者所提供之家長設定的摘要。

目前選取的提供者可能會選擇針對受管理使用者的使用者控制項畫面使用自己的使用者介面，也可能會選擇依賴此畫面的內建 WPC 執行。 內建的實作為其元素的下列變更：

-   已移除活動報告區段。
-   已移除用來查看活動報告的連結。

## <a name="parental-controls-api-overview-windows-7-changes"></a>家長監護 API 總覽： Windows 7 變更

協力廠商解決方案提供者的整合機制已擴充為允許：

-   提供者註冊。 註冊時，提供者會在 [家長監護] 主控台畫面上的 [其他控制項] 下拉式清單方塊中變成可選取。
-   正在查詢目前選取的提供者。 公開的 COM 介面可以用來啟用這項功能。
-   此外，新的是要由提供者所執行的一組 COM 介面，以允許：
    -   藉由在使用者選取其他控制項時 WPC 來啟用或停用提供者。
    -   WPC 將控制權傳遞給提供者，以設定受管理使用者的家長監護設定。
    -   WPC，查詢提供者以取得受管理使用者之家長監護設定的摘要。

## <a name="third-party-provider-integration"></a>協力廠商提供者整合

### <a name="provider-registration"></a>提供者註冊

若要向家長監護註冊新的提供者，必須將登錄值寫入 Windows 家長監護的提供者金鑰。 值名稱是用來識別提供者的唯一 GUID。 值資料會是 **HKEY \_ 本機 \_ 電腦** 中包含提供者資訊的登錄機碼路徑。

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

在指定的登錄機碼位置，預期會有下列值。



| 詞彙                                                                                                                 | 描述                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**<br/>         | 具有提供者標誌影像負資源識別碼之資源二進位檔的完整路徑 (儲存為 **影像 \_ 點陣圖**) 。<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**<br/> | 資源二進位檔的完整路徑，具有提供者名稱的負資源識別碼。 **DisplayName** 長度不應超過50個字元。<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**<br/> | 資源二進位檔的完整路徑，具有提供者描述的負資源識別碼。 描述長度不應超過200個字元。<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | 實 IWPCProviderState 之提供者類別的類別識別碼。<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | 提供者類別的類別識別碼，它會執行 IWPCProviderConfig。 **StateCLSID** 和 **ConfigCLSID** 可以相同。<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | 選用的 **DWORD** 非零值，指定在選取提供者作為新的目前提供者之後，Windows 家長監護會顯示遊戲評等系統畫面的連結。<br/> |



 

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

當選取該提供者時，家長監護主控台會使用 **LogoImage**、 **DisplayName** 和 **Description** 來變更家長監護主控台的主頁面。 啟用或停用提供者時，會使用 **StateCLSID** 值。 當使用者介面取得每位使用者的動態資訊時，會使用 **ConfigCLSID** 值 (這只是) 提供者目前已選取的情況。

 

 




