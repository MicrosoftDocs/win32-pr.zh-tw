---
description: 本主題討論主控台中找到的 (SPAD) 功能設定程式存取和電腦預設值。
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: " (SPAD) 設定程式存取和電腦預設值"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978749171366e3091738ac22c78e04cd92123a75d2288f7c83200ee8532d232c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861460"
---
# <a name="set-program-access-and-computer-defaults-spad"></a> (SPAD) 設定程式存取和電腦預設值

本主題討論主控台中找到的 **(SPAD) 功能設定程式存取和電腦預設值** 。 SPAD 位於 Windows Vista 和更新版本的 Windows 的 [[預設程式](default-programs.md)] 主控台專案下。 在 Windows XP 中，它位於 [**新增或移除程式**] 專案中，並且標題為 [**設定程式存取和預設值**]。

> [!IMPORTANT]
> 本主題不適用於 Windows 10。 預設檔案關聯在 Windows 10 中的運作方式有所變更。 如需詳細資訊，請參閱 [這篇文章](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)中有關 **Windows 10 如何處理預設應用程式的變更** 一節。

 

-   [使用 [設定程式存取和電腦預設值] 工具](#using-the-set-program-access-and-computer-defaults-tool)
    -   [設定程式存取和電腦預設值的總覽](#an-overview-of-set-program-access-and-computer-defaults)
    -   [LastUserInitiatedDefaultChange 登錄值](#the-lastuserinitiateddefaultchange-registry-value)
-   [篩選新增或移除程式清單](#filtering-the-add-or-remove-programs-list)
-   [其他資源](#filtering-the-add-or-remove-programs-list)
-   [相關主題](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>使用 [設定程式存取和電腦預設值] 工具

> [!Note]  
> 從 Windows 8，SPAD 會針對目前的使用者，以每個使用者為基礎來設定預設值。 在 Windows 8 之前，SPAD 設定每一電腦預設值。 當使用者尚未設定每位使用者的預設值時，系統會提示他們設定每位使用者預設值，而不是回復每部電腦的預設值。 Windows Vista 中的使用者永遠看不到每一電腦預設值，而如果他們先前設定了每個使用者預設值，則可能 Windows 7，因為依使用者的預設值會覆寫這些作業系統中的每一電腦預設值。

 

在 Windows XP 中，**設定程式存取和預設值** 是主控台的 [**新增或移除程式**] 專案中，以選項的形式找到的工具。 在 Windows Vista 和更新版本中，它位於 [[預設程式](default-programs.md)] 主控台專案下。 針對 [已註冊](reg-middleware-apps.md) 的程式，它會執行下列功能：

-   可為每個用戶端類型選擇預設程式 (最多 Windows 7) 。
-   可控制程式圖示、快捷方式和功能表項目的顯示。
-   提供一組預設的預設程式選項。  (Windows XP Service Pack 1 (SP1) 僅) 

這項工具會用於下列五種用戶端類型。

-   瀏覽器
-   電子郵件
-   立即的傳送程式
-   媒體播放器
-   適用于 JAVA 的虛擬機器

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>設定程式存取和電腦預設值的總覽

下列螢幕擷取畫面顯示 Windows 8 **設定程式存取和電腦預設值**] 頁面。

![[設定程式存取和電腦預設值] 專案視圖的螢幕擷取畫面](images/spad-initial.png)

有三個可能的設定選項會顯示給使用者，讓 Oem 有選項顯示名為「電腦製造商」的第四個選項。

-   [Microsoft Windows](#microsoft-windows)
-   [非 Microsoft](#non-microsoft)
-   [Custom](#custom)
-   [電腦製造商](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

**Microsoft Windows** 設定是由一組隨附于 Windows 的預設程式所組成，如下列螢幕擷取畫面所示。

![[設定程式存取和預設 microsoft 選項] 的螢幕擷取畫面](images/mspage.png)

選取 [ **Microsoft Windows** 設定也可讓您顯示針對五種用戶端類型中任一種註冊之程式的圖示、快捷方式或功能表項目。 使用者可以在 [ **開始** ] 功能表或開始畫面、桌面上以及新增的所有其他位置，使用這些圖示、快捷方式和功能表項目。

### <a name="non-microsoft"></a>非 Microsoft

下列螢幕擷取畫面中所示的 **非 microsoft** 設定，可用於使用者系統上不是由 Microsoft 所產生的已註冊應用程式。 這些應用程式可以預先安裝在使用者的系統上，也可以是使用者已安裝的非 Microsoft 應用程式。

> [!Note]  
> 應用程式必須註冊才能顯示在此頁面上。 如需註冊應用程式的指示，請參閱 [使用用戶端類型註冊程式](reg-middleware-apps.md)。

 

![[設定程式存取和預設非 microsoft 選項] 選項的螢幕擷取畫面](images/nonmspage.png)

選取 [**非 Microsoft** ] 選項也會移除所有具有這些專案之用戶端類型的 [ [microsoft Windows](#microsoft-windows)設定] 中所列 microsoft 程式的圖示、快捷方式和功能表項目的存取權。 這些 Microsoft 圖示、快捷方式和功能表項目會從 [ **開始** ] 功能表、桌面及新增這些專案的其他位置移除。

### <a name="custom"></a>自訂

**自訂** 設定（如下列螢幕擷取畫面所示）可讓使用者使用 Microsoft 和非 microsoft 程式的任何組合（註冊為五個用戶端類型的預設可能性）來自訂其系統。 這是 Windows 2000 Service Pack 3 (SP3) 中唯一提供的四個選項之一。

![[設定程式存取] 和 [預設自訂] 選項的螢幕擷取畫面](images/custompage.png)

[Microsoft Windows](#microsoft-windows)和 [非 microsoft](#non-microsoft)設定中提供的所有選項都可供 **自訂** 區段中的使用者使用，以及任何其他不屬於 Windows 的其他已安裝 microsoft 應用程式。 [ **使用我目前的網頁瀏覽器** ] 選項按鈕已預先選取，如先前的螢幕擷取畫面所示。 沒有任何方法可以從 UI 判斷目前的預設瀏覽器。 在 Windows 中叫用 web 連結或檔案，是探索目前預設瀏覽器的唯一方法。

當使用者選取某個程式的 [**啟用對這個程式的存取**] 核取方塊時，該程式的圖示、快捷方式和功能表項目會顯示在 [開始] 功能表或開始畫面、桌面上或已安裝的任何其他位置。 清除此選項應該會移除這些圖示、快捷方式和功能表項目，不過這些選項的行為方式完全取決於應用程式廠商。 Windows 不會控制在整個 UI 中啟用或移除存取的方式。 也請務必瞭解，應用程式不需要註冊 **設定程式存取和電腦預設值**。

### <a name="computer-manufacturer"></a>電腦製造商

第四個名為「電腦製造商」的類別，可以出現在某些系統的 SPAD 視窗中。 電腦製造商可以選擇使用一組自訂的預設值來預先設定電腦，並從 [自訂](#custom) 設定中提供的相同選項中進行選擇。  (為了方便說明，我們會註冊一組稱為 LitWare 的虛構應用程式，以搭配所有用戶端類型使用。您可以選擇 [**電腦製造商**] 選項，) 使用者隨時返回電腦製造商的預設設定，如下列 Windows XP 螢幕擷取畫面所示。

> [!Note]  
> 此設定不會出現在所有系統上。 如需詳細資訊，請參閱 OEM 預先安裝套件 (OPK) 。

 

![[設定程式存取和預設電腦製造商] 選項的螢幕擷取畫面](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>LastUserInitiatedDefaultChange 登錄值

LastUserInitiatedDefaultChange 值已新增至登錄，以協助應用程式辨識和尊重使用者的預設選項。 值 \_ 以 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構的形式來保存 REG 二進位資料，其中包含上次使用者透過 [ **設定程式存取和電腦預設值** ] 工具變更預設值時，國際標準時間 (UTC) ) 的日期和時間 (。 您可以在下列子機碼底下找到此值。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

下列案例會針對監視檔案關聯的應用程式使用此值。

1.  應用程式會在安裝時記錄最後將時間設定為其用戶端類型預設程式的時間， (在安裝期間或稍後) 。
2.  應用程式會偵測到其用戶端類型的預設程式已變更為本身以外的程式，或在背景 helper 程式) 的情況下，它所代表的應用程式 (。 Windows 8 不支援。
3.  應用程式會讀取 LastUserInitiatedDefaultChange 的值 (上次使用者起始之預設變更) 的時間戳記，並將其與儲存作為預設值的時間戳記值進行比較。
4.  如果 LastUserInitiatedDefaultChange 晚于應用程式的儲存值，則該應用程式不應採取任何動作，因為使用者透過 [ **設定程式存取和預設值** ] 工具明確要求變更。
5.  應用程式在再次選擇為預設值之前，不會再監視該檔案關聯。 Windows 8 不支援。

藉由遵守這種配置，將會遵守使用者的期望，並維護其系統的最終擁有權。

## <a name="filtering-the-add-or-remove-programs-list"></a>篩選新增或移除程式清單

> [!Note]  
> 本節適用于 Windows XP Service Pack 2 (SP2) 和更新版本，以及 Windows Server 2003 和更新版本。

 

在 Windows XP 和 Windows Server 2003 中，[**新增或移除程式**] 底下的 [**變更或移除程式**] 索引標籤中所顯示的應用程式清單，可以由使用者篩選以排除應用程式更新的專案。 在這些版本的 Windows 中，您可以透過視窗頂端的 [**顯示更新**] 核取方塊來完成這項作業。 預設不會選取 [ **顯示更新** ] 選項，因此除非使用者選擇顯示更新，否則 *不* 會顯示更新。 當 [ **新增或移除程式** ] 關閉時，對核取方塊狀態的變更會保持不變;如果使用者選擇顯示更新，則會繼續顯示，直到使用者清除核取方塊為止。

> [!Note]  
> Windows XP SP2 更新本身是篩選的例外狀況。 無論核取方塊的狀態為何，一律會顯示它。

 

在 Windows Vista 和更新版本中，應用程式更新會顯示在單獨的頁面上，主控台專用於單獨更新。 當使用者按一下 [ **已安裝的更新** ] 工作連結時，就會顯示此頁面。 沒有使用者可選取的選項，無法在與已安裝的程式相同的頁面上顯示更新。 儘管 UI 的變更，註冊為已安裝程式更新的機制仍會與舊版 Windows 中的相同。

使用 Windows Installer 的 microsoft 和非 microsoft 應用程式不需要進一步進行更新，就能被辨識為更新。 未使用 Windows Installer 的非 Microsoft 應用程式必須在安裝時宣告登錄中的特定值，才能將其辨識為現有程式的更新。

下列範例說明要宣告哪些登錄值，以將安裝識別為現有程式的更新。

1.  父應用程式必須在 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **uninstall** 子機碼下的子機碼中新增其卸載資訊。 如需使用 **卸載** 子機碼的詳細資訊，請參閱 [安裝](/previous-versions/ms997548(v=msdn.10))主題。
2.  對該父應用程式的每個更新也必須將其資訊新增為 **Uninstall** 子機碼的子機碼。 它應該使用其選擇的特定命名慣例，以避免可能與其他程式發生衝突。 Microsoft 會將下列慣例保留為子機碼名稱，以用於 Windows 更新。
    -   IEUpdate
    -   OEUpdate
    -   "KB" 後面接著六位數，例如 "KB123456"
    -   "Q" 後面接著六位數，例如 "Q123456"
    -   六位數，例如 "123456"
3.  除了針對父應用程式新增的標準卸載資訊之外，每個更新的子機碼還必須包含下列三個專案的其中兩個。 其值的型別為 REG \_ SZ。
    -   **ParentKeyName**。 這是必要的值。 這是在步驟1中宣告的父系子機碼名稱。 這會將更新與程式產生關聯。
    -   **ParentDisplayName**。 這是必要的值。 如果沒有子機碼符合在 ParentKeyName 中所指定的子機碼，此值會用來做為要在 [ **新增或移除程式**] 中顯示的預留位置父程式。
    -   **InstallDate**。 這是選擇性的值。 它應該使用表單 `yyyymmdd` 來指定日期。 此日期可用於顯示在 UI 中更新專案旁的 **已安裝** 資訊。 如果沒有 **InstallDate** 專案，或存在但未指派任何值，則會發生下列情況：
        -   Windows Vista 和 Windows 7 以外的作業系統版本：未顯示任何 **已安裝的** 資訊。
        -   WindowsVista 和更新版本：使用預設日期。 這是該更新子機碼下任何專案的「上次修改日期」。 這通常是更新新增至登錄的日期。 不過，因為它是「上次修改日期」，所以任何子機碼專案的後續變更都會使 InstallDate 值變更為該變更的日期。

下列範例顯示 LitWare Deluxe 應用程式更新的相關登錄專案。

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

未提供適當登錄資訊的非 Microsoft 應用程式（例如，在此選項可用之前所產生的更新）仍會在已安裝的程式清單中繼續正常顯示，且不會被篩選掉。

在 Windows Vista 和 Windows 7 以外的作業系統版本中，更新篩選通常是使用者控制的設定，而且應該依照應用程式的方式來遵守。 不過，在企業環境中，系統管理員可以控制使用者是否可透過 DontGroupPatches 登錄值篩選更新，如下列範例所示。

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

此值的型別為 REG \_ DWORD，如下所示。



| DontGroupPatches 值             | 意義                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | 使用者會看到 [ **顯示更新** ] 核取方塊。 篩選取決於使用者是否已核取此方塊。                                                                                         |
| 1                                  | [ **顯示更新** ] 核取方塊會從 UI 中移除。 更新不會從清單中篩選。 在引進「**顯示更新**」功能之前，此值基本上會還原為 Windows XP SP1 行為。 |
| DontGroupPatches 專案不存在 | 這相當於將值設定為0。                                                                                                                                                                       |



 

DontGroupPatches 在 Windows Vista 和 Windows 7 沒有任何作用，因為 UI 不包含任何核取方塊，且已註冊的更新一律會進行篩選。

> [!Note]  
> 原則只會由系統管理員設定。 應用程式不應變更此值。 如需有關如何設定以登錄為基礎的群組原則的詳細資訊，請參閱[群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page)或[Windows 伺服器群組原則](/windows/deployment/deploy-whats-new)。

 

## <a name="additional-resources"></a>其他資源

-   [使用用戶端類型註冊程式](reg-middleware-apps.md)
-   [安裝](/previous-versions/ms997548(v=msdn.10))
-   [使用 Windows Installer 設定新增/移除程式](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案關聯的最佳作法](fa-best-practices.md)
</dt> <dt>

[檔案關聯範例案例](fa-sample-scenarios.md)
</dt> <dt>

[在 Windows Vista 和更新版本中管理預設應用程式的指導方針](vista-managing-defaults.md)
</dt> <dt>

[預設程式](default-programs.md)
</dt> </dl>

 

 
