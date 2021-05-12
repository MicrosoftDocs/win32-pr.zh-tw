---
description: 本主題提供獨立軟體廠商 (Isv) 提供在 Windows Vista 和更新版本中註冊及管理應用程式預設值所需步驟的快速指南。 提供有關每個章節主題的更深入文章的連結。
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: 管理預設應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc146858d197b96229edda49ac2e7249db51bf4c
ms.sourcegitcommit: 4d639170c06864e47ef66b2cfe6ca3d07cce0b02
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109812823"
---
# <a name="managing-default-applications"></a>管理預設應用程式

[ **設定程式存取和電腦預設值** ] (SPAD) 功能已新增至 windows XP 和更新版本的 windows，以管理每部電腦的預設值。 除了 SPAD 之外，Windows Vista 還引進了每個使用者預設應用程式的概念，以及主控台中的 **預設程式** 專案。

> [!IMPORTANT]
> 本主題不適用於 Windows 10。 預設檔案關聯在 Windows 10 中的運作方式有所變更。 如需詳細資訊，請參閱 [這篇文章](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)中有關 **Windows 10 如何處理預設應用程式的變更** 一節。

 

每個使用者的預設設定是系統上個別使用者帳戶的特定設定。 如果有個別使用者的預設設定，則會優先于該帳戶的相對應個別電腦預設值。 從 Windows 8 中，檔案類型和通訊協定預設值的擴充性系統會嚴格地依使用者和每一電腦的預設值加以忽略。 SPAD 也會在 Windows 8 中變更，以設定每個使用者的預設值。

-   在執行早于 Windows 8 的 Windows 版本的系統上，新建立的使用者帳戶會收到每一電腦預設值，直到建立每個使用者的預設值為止。 在 Windows Vista 和更新版本中，使用者可以使用主控台中的 [ **預設程式** ] 專案來設定或變更其每個使用者預設值。 此外，當應用程式第一次執行時，可以使用 [ [應用程式首次執行] 和 [預設值](#application-first-run-and-defaults) ] 區段中遵循的指導方針來設定每個使用者的預設值。
-   在執行 Windows 8 的系統上，新建立的使用者帳戶會依賴每位使用者的預設值，並在第一次執行時使用這些預設值，如 [應用程式第一次執行和預設值](#application-first-run-and-defaults) 一節中所述，不再支援。

應用程式必須同時註冊 SPAD 和預設程式功能，才能在 Windows Vista 和更新版本中提供作為預設程式。

本主題提供獨立軟體廠商 (Isv) 提供在 Windows Vista 和更新版本中註冊及管理應用程式預設值所需步驟的快速指南。 提供有關每個章節主題的更深入文章的連結。

-   [主控台中的預設程式專案](#default-programs-item-in-control-panel)
-   [設定程式存取和電腦預設值](#set-program-access-and-computer-defaults)
    -   [在 SPAD 中設定預設值](#setting-defaults-in-spad)
    -   [隱藏 SPAD 中的存取權](#hide-access-in-spad)
-   [註冊應用程式進入點](#registering-for-application-entry-points)
    -   [開啟方式](#open-with)
    -   [[開始] 功能表和快速啟動 Bar](#start-menu-and-quick-launch-bar)
-   [應用程式安裝和預設值](#application-installation-and-defaults)
-   [應用程式升級和預設值](#application-upgrades-and-defaults)
-   [應用程式第一次執行和預設值](#application-first-run-and-defaults)
-   [驗證預設值並要求使用者同意](#verifying-defaults-and-asking-for-user-consent)
-   [應用程式相容性秘訣](#application-compatibility-tips)
    -   [避免觸發 Per-User 虛擬化](#avoid-triggering-per-user-virtualization)
    -   [避免從程式相容性助理 AppCompat 警告或區塊](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [舊版 Windows 作業系統的支援](#support-for-previous-windows-operating-system-versions)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>主控台中的預設程式專案

**預設程式** 是 Windows Vista 中引進的功能，可直接從 [ **開始** ] 功能表和主控台存取。 它提供的新基礎結構可搭配標準使用者權限使用 () 不會提高許可權，而且是設計來讓使用者和應用程式管理每個使用者的預設值。 針對使用者，預設程式提供統一且容易存取的方式，來管理系統上所有應用程式的預設值、檔案關聯和自動播放設定。 針對應用程式，使用預設程式 Api 所提供的每個使用者範圍提供下列優點：

-   **無提高許可權**

    應用程式不需要將其許可權提升為宣告預設值。

-   **良好公民資格**

    在多使用者電腦上，每個使用者都可以選取不同的預設應用程式。

-   **預設管理**

    預設程式 Api 提供可靠且一致的機制，可自行檢查預設狀態並回收遺失的設定，而不需要直接寫入登錄。 不過，從 Windows 8，我們不建議應用程式查詢預設狀態，因為應用程式無法再變更預設設定，這些變更只能由使用者進行。

若要讓您的應用程式有效率地管理預設值，您必須將應用程式註冊為可能的預設程式。 如需註冊和使用預設程式 Api 的詳細資訊，請參閱 [預設程式](default-programs.md)。

預設程式也提供這兩種功能：

-   **可重複使用的預設 UI**

    程式預設值的 UI (**將預設程式設定**) 和檔案關聯 (將 **檔案類型或通訊協定與程式建立關聯**) 可以從應用程式內重複使用和呼叫。 這可讓應用程式提供標準使用者體驗來管理預設值，並讓 Isv 不必開發自訂或對等的 UI。

-   **包含 URL 和行銷資訊**

    在主控台的 [**預設程式**] 專案的 [**設定預設程式**] 頁面中，應用程式可以提供行銷資訊和廠商網站的連結。 此 URL 是從應用程式已簽署的 Authenticode 憑證所衍生。 這可防止誤用及未經授權地取代此連結。 如果應用程式具有包含內嵌 URL 的 Authenticode 憑證，Windows UI 會顯示該內嵌 URL。 Isv 應該利用這項功能，將使用者導向其網站，以進行更新和其他下載。

## <a name="set-program-access-and-computer-defaults"></a>設定程式存取和電腦預設值

**設定程式存取和電腦預設值** (SPAD) 可讓系統管理員管理整個電腦的所有新使用者所繼承的全電腦預設值。 在 Windows 8 之前，SPAD 也可讓系統管理員在程式從系統移除時，修復檔案關聯。 不過，從 Windows 8 起，SPAD 只會影響使用者特定的預設值。

如需在 SPAD 中註冊應用程式的詳細資訊，請參閱使用 [設定程式存取和電腦預設值 (SPAD) ](cpl-setprogramaccess.md) 和 [使用用戶端類型註冊程式](reg-middleware-apps.md)。 後續各節將討論特定的變更和新的建議。

### <a name="setting-defaults-in-spad"></a>在 SPAD 中設定預設值

每一使用者預設會覆寫每部電腦的預設值。

-   在 **Windows 8 之前**： SPAD (中設定的預設值) ，如果設定對應的每個使用者預設值，使用者就不會看到這些預設值。 如果使用者未設定每位使用者的預設值，系統會使用對應的電腦預設值。 電腦上的新使用者帳戶一開始會繼承電腦預設值。 使用者第一次執行應用程式時，應用程式應該會提示使用者指派其每個使用者預設值。 請參閱 [應用程式首次執行和預設值](#application-first-run-and-defaults)。
-   從 **Windows 8**：所有預設值都是依使用者，且會忽略任何個別電腦的預設設定。 應用程式無法再設定預設選項，因此他們無法透過指派這些預設值來引導使用者。

當預先 Windows 8 的應用程式在 SPAD 中 **設定為預設值** 時，應該遵循下列指導方針：

-   應用程式應該只透過 SPAD 宣告電腦層級的預設值。
-   應用程式 *不* 應該透過 SPAD 宣告每位使用者的預設值。

當 Windows 8 應用程式在 SPAD 中 **設定為預設值** 時，必須使用 SPAD 中使用的相同應用程式名稱，在 [預設程式](default-programs.md)中註冊其檔案類型和通訊協定。 這可讓 SPAD 中的變更反映為目前使用者的對應預設程式專案中的變更。

### <a name="hide-access-in-spad"></a>隱藏 SPAD 中的存取權

您可以使用下列兩種方式之一來存取 SPAD 中每個可能預設值的隱藏存取選項：

-   選擇 **非 microsoft** 的預設預設類別，這會移除所有 Microsoft 預設值的存取權。
-   選擇 [ **自訂** ] 類別，並清除 [ **啟用對這個程式的存取** ] 核取方塊。

先前，將其中一項動作移除至系統上適當應用程式的所有進入點。 這種情況的特定指導方針，就是要從下列位置移除快速鍵和圖示：

-   桌面
-   開始功能表
-   快速啟動 bar (Windows Vista 及更早版本) 
-   [通知] 區域
-   快顯功能表
-   資料夾工作區

建議廠商在應用程式的隱藏存取回呼函式中實施這些指導方針。

### <a name="alternate-hide-access-method-in-spad"></a>SPAD 中的替代隱藏存取方法

針對某些繼承應用程式，隱藏存取的完整執行可能不實用。 替代方法可達成相同的效果，但使用者不容易復原，而是將應用程式卸載。 以下顯示範例行為和執行此程式碼的範例程式碼。

此替代方案的建議使用者體驗如下所示：

-   當使用者清除 SPAD 中的 [ **啟用對這個程式的存取** ] 方塊時，會顯示下列的 UI。

    ![關於隱藏程式存取權的 vista 對話方塊](images/hideaccessvista.png)

-   當使用者按一下 **[確定]** 時，會顯示主控台中的 [ **程式和功能** ] 專案，讓使用者可以卸載應用程式。
-   Windows XP 使用者應該會看到下列對話方塊。

    ![關於隱藏程式存取權的 windows xp 對話方塊](images/hideaccessxp.png)

-   當 Windows XP 使用者按一下 **[確定]** 時，會顯示主控台中的 [ **新增或移除程式** ] 專案，讓使用者可以卸載應用程式。

下列程式碼針對隱藏存取功能提供可重複使用的執行，如先前所述。 它可用於 Windows XP、Windows Vista 和 Windows 7。


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



## <a name="registering-for-application-entry-points"></a>註冊應用程式進入點

應用程式在作業系統內可以有許多進入點。 以下是進入點的建議位置：

-   桌面
-   開始功能表
-   快速啟動 bar (Windows Vista 及更早版本) 
-   [通知] 區域
-   快顯功能表
-   資料夾工作區

本節著重于這些特定區域：

-   [開啟方式](#open-with)
-   [[開始] 功能表和快速啟動 Bar](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>開啟方式

[ **開啟** 檔案] 快速鍵功能表可讓使用者選取可處理特定檔案類型的應用程式。 **開啟** 時，可以用來開啟具有應用程式一次的檔案，也可以用來設定該副檔名的預設值。 因此，應用程式應該一律註冊以 **開啟** ，讓使用者可以選擇使用該應用程式。 應用程式可以註冊的檔案類型和通訊協定，以供 **開啟**。 在預設程式架構中註冊通訊協定的應用程式，會自動新增至 [ **開啟]，** 以取得通訊協定。

如需註冊 **Open With** 的詳細資訊，請參閱檔案 [關聯簡介](fa-intro.md)。

### <a name="start-menu-and-quick-launch-bar"></a>[開始] 功能表和快速啟動 Bar

為了更容易找到使用者，應用程式可以在 Windows 中將快捷方式新增至不同的位置。 新增快捷方式最常見的地方就是 [ **開始** ] 功能表。 在 Windows Vista 和更新版本中，應用程式會在隱藏的資料夾% ProgramData% Microsoft Windows [開始] 功能表程式中建立快捷方式， \\ \\ \\ \\ 以顯示在所有使用者的 [ **開始** ] 功能表的程式清單中。 通常，應用程式會新增包含快捷方式的子資料夾。

針對瀏覽器和電子郵件程式，Windows Vista [ **開始** ] 功能表也會在程式清單外面提供兩個專用連結，標準方式標題為 [ **網際網路** 及 **電子郵件**]。 在應用程式註冊這些類別之後，預設的程式架構可以管理透過這些連結啟動的專案。

> [!Note]  
> 從 Windows 7 開始， **網際網路** 和 **電子郵件** 專用的 [ **開始** ] 功能表連結不再存在。

 

為了進一步提高可探索性，應用程式也可以將快捷方式新增至桌面和快速啟動 bar。 應用程式應該在安裝期間或第一次執行) 之前要求使用者提供許可權 (，然後再將圖示新增至 [ **開始** ] 功能表、桌面或快速啟動列。

> [!Note]  
> Windows 7 不再提供快速啟動 bar。 Windows 7 的替代方案是讓應用程式釘選到工作列，但是無法以程式設計方式進行釘選，因為這是使用者選擇的絕對選項。

 

如需詳細資訊，請參閱下列主題：

-   [如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式](start-menu-reg.md)
-   [使用用戶端類型註冊程式](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>應用程式安裝和預設值

應用程式安裝程式在 Windows XP 之後根本沒有改變，但是執行的 Windows 版本高於 Windows 8 的系統有新的指導方針：在安裝時採用每一電腦的預設值，但在使用者第一次執行應用程式之前，並不會設定任何每個使用者的預設值。  (請參閱 [應用程式的第一次執行和預設值](#application-first-run-and-defaults)。 ) 應用程式在安裝期間不應設定依使用者的預設值，因為在某些情況下，安裝應用程式的人員不是預期的使用者。 從 Windows 8，不支援每部電腦預設值，而且應用程式無法變更每個使用者的預設設定。

在安裝期間，應用程式應該將其二進位檔複製到硬碟，並將其 Progid 寫入登錄中。 應用程式也應該註冊預設程式，並針對每個檔案關聯 **開啟** ，以供處理它的候選項目。 應用程式可以使用 **OpenWithProgIds** 子機碼來註冊 **Open with**。

如需詳細資訊，請參閱下列主題：

-   [預設程式](default-programs.md)
-   [檔案關聯簡介](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>應用程式升級和預設值

許多應用程式都能夠隨著時間進行升級。 此升級程式不應變更每個使用者預設值的狀態，因為該變更對使用者而言不是預期的。 但是，應用程式可接受檢查電腦層級的檔案關聯，並在其損毀時加以修復。

## <a name="application-first-run-and-defaults"></a>應用程式第一次執行和預設值

> [!Note]  
> 從 Windows 8，系統會代表所有應用程式處理此程式。 應用程式本身無法再查詢及變更預設值。 只有使用者可以這麼做。 因此，應用程式不應該嘗試查詢目前的預設值，或透過任何機制變更預設值。 不過，應用程式可以藉由呼叫 [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)介面的 [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui)方法，在主控台中提供預設程式的進入點。

 

隨著 Windows Vista 中的每個使用者預設值的推出，以熱門的副檔名為比賽的應用程式必須提供一般使用者體驗來宣告這些延伸模組。 因為這些預設值現在是在使用者的內容中設定，所以只有在使用者于安裝之後執行程式時，才會將本身呈現為預設的可能性。

建立每個使用者預設值的指導方針如下：第一次執行特定使用者的應用程式時，該應用程式應該為其本身的預設值和檔案關聯要求使用者喜好設定。

建議的 UI 應該為使用者提供兩個清楚的選擇：

1.  接受應用程式想要宣稱的所有預設值。 此選項也可以設定應用程式的其他預設屬性，例如 [隱私權] 或 [自動更新] 設定。 此選項可讓應用程式宣告其所有已註冊的預設值。
2.  藉由接受或不個別接受預設選項和程式設定來自訂。 此選項會提供進一步的 UI，讓使用者可以針對其預設選項進行更細微的選擇。

如需詳細資訊，請參閱 [預設程式](default-programs.md)。

## <a name="verifying-defaults-and-asking-for-user-consent"></a>驗證預設值並要求使用者同意

> [!Note]  
> Windows 8 不支援這項功能。

 

當應用程式在 Windows Vista 和更新版本中向預設程式註冊之後，應用程式就可以使用某些 Api。 例如，應用程式可能需要檢查它是否為預設程式。 [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)介面會提供方法來進行此作業。

任何想要宣告預設值的應用程式都必須先要求使用者，而且永遠不會宣告預設值（不含許可權）。 系統應詢問使用者是否要將應用程式設為預設值，或保留目前的預設值。 在使用者進行選擇後，應該也不會再詢問此問題。

如需詳細資訊，請參閱 [預設程式](default-programs.md)。

## <a name="application-compatibility-tips"></a>應用程式相容性秘訣

本節提供一些與 Windows 中的預設程式經驗相關的應用程式相容性秘訣。

### <a name="avoid-triggering-per-user-virtualization"></a>避免觸發 Per-User 虛擬化

使用「使用者帳戶控制」 (UAC) 環境中，應用程式一律會以標準使用者權限執行，以獲得最佳的客戶體驗。 基於安全性考慮，系統會封鎖具有標準使用者權限層級的應用程式，使其無法寫入登錄的特定部分和特定的系統檔案。 Windows Vista 和更新版本的 Windows (AppCompat) 層提供暫時性的應用程式相容性，以協助應用程式進行轉換。 封鎖寫入登錄或系統檔案的嘗試會「虛擬化」，讓應用程式繼續執行，但不會改變系統的機密區域。 不過，應用程式不應依賴 AppCompat 技術做為長期解決方案。 相反地，應用程式應該使用許多可用的工具來確認它們可以在標準使用者權限下順利執行。 應用程式的某些 reprogramming 可能是完成這項工作的必要項，但它應該是以長期相容性的方式來完成。

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>避免從程式相容性助理 AppCompat 警告或區塊

Windows Vista 和更新版本中提供「程式相容性助理」 (PCA) 。 其目的是要提供自動化的方法，讓相容性問題較舊的程式更能運作。 PCA 會監視程式的已知問題。 如果偵測到問題，則會在使用者再次執行程式之前，通知使用者有問題，並提供可套用有效解決方案的供應專案。 為了避免看到這些警告或區塊，Isv 應該使用許多可用的工具，以確保其應用程式與 Windows Vista、Windows 7 和更新版本相容。

### <a name="support-for-previous-windows-operating-system-versions"></a>舊版 Windows 作業系統的支援

在 Windows Vista 之前，Windows 作業系統上無法使用預設程式基礎結構。 因此，當應用程式移至新的預設程式基礎結構時，應該保留舊版的應用程式預設程式碼，以維持與舊版 Windows 的相容性。 應用程式應該在安裝時執行作業系統版本檢查，以判斷要執行的應用程式預設程式碼。

為了支援從 Windows XP 升級到 Windows Vista 或更新版本，應用程式應該新增預設程式所需的所有登錄專案，即使它們是安裝在執行 Windows XP 的電腦上也一樣。 註冊在執行 Windows XP 的電腦上不會有任何作用，但如果電腦稍後升級，應用程式將會註冊，而且能夠利用架構。

如需詳細資訊，請參閱 [**OSVERSIONINFO**](/windows/win32/api/winnt/ns-winnt-osversioninfoa)。

## <a name="additional-resources"></a>其他資源

-   [檔案關聯簡介](fa-intro.md)
-   [如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式](start-menu-reg.md)
-   [將應用程式註冊至 URI 配置](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案關聯的最佳作法](fa-best-practices.md)
</dt> <dt>

[檔案關聯範例案例](fa-sample-scenarios.md)
</dt> <dt>

[預設程式](default-programs.md)
</dt> <dt>

[使用設定程式存取和電腦預設值 (SPAD) ](cpl-setprogramaccess.md)
</dt> </dl>

 

 
