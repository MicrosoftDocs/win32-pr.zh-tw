---
description: Windows 7 及更新版本系統中的工作列會廣泛使用 (AppUserModelIDs) 的應用程式使用者模型識別碼，以將處理常式、檔案和視窗與特定應用程式產生關聯。
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: '應用程式使用者模型識別碼 (AppUserModelIDs) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b79f0bdd7fb5e6c4d5c41caa3cd6be3f4fb57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511067"
---
# <a name="application-user-model-ids-appusermodelids"></a>應用程式使用者模型識別碼 (AppUserModelIDs) 

Windows 7 及更新版本系統中的工作列會廣泛使用 (AppUserModelIDs) 的應用程式使用者模型識別碼，以將處理常式、檔案和視窗與特定應用程式產生關聯。 在某些情況下，就足以依賴系統指派給進程的內部 AppUserModelID。 不過，擁有多個處理常式或在主機進程中執行之應用程式的應用程式可能需要明確地識別其本身，如此它就可以在單一工作列按鈕下將其另一個不同的視窗分組，並控制該應用程式捷徑清單的內容。

-   [應用程式定義和 System-Defined AppUserModelIDs](#application-defined-and-system-defined-appusermodelids)
-   [如何形成 Application-Defined AppUserModelID](#how-to-form-an-application-defined-appusermodelid)
-   [要在哪裡指派 AppUserModelID](#where-to-assign-an-appusermodelid)
-   [將應用程式註冊為主機進程](#registering-an-application-as-a-host-process)
-   [工作列釘選和最近/頻繁清單的排除清單](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [相關主題](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined 和 System-Defined AppUserModelIDs

有些應用程式不會宣告明確的 AppUserModelID。 它們是選擇性的。 在這種情況下，系統會使用一系列的啟發學習法來指派內部 AppUserModelID。 但是，為了避免這些計算，有一個效能上的好處，而明確的 AppUserModelID 是保證確切使用者體驗的唯一方法。 因此，強烈建議您設定明確的識別碼。 應用程式無法取出系統指派的 AppUserModelID。

如果應用程式使用明確的 AppUserModelID，則也必須將相同的 AppUserModelID 指派給所有執行中的 windows 或進程、快捷方式和檔案關聯。 當您透過 [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)或 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)的任何呼叫自訂其捷徑清單時，也必須使用 AppUserModelID。

> [!Note]  
> 如果應用程式沒有明確的 AppUserModelID，則必須呼叫 [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)、 [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)和 [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) 方法，以及從應用程式內 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) 。 如果從另一個進程（例如安裝程式或卸載程式）呼叫這些方法，系統就無法產生正確的 AppUserModelID，而且這些呼叫將不會有任何作用。

 

下列專案描述需要明確 AppUserModelID 的一般案例。 它們也指出應該使用多個明確 AppUserModelIDs 的情況。

-   具有多個模式的 UI 的單一可執行檔，會以個別的應用程式顯示給使用者，應該將不同的 AppUserModelIDs 指派給每個模式。 例如，使用者看到的部分應用程式，可以與應用程式的其餘部分分開釘選並從工作列啟動，而與主要體驗不同的是，它會有自己的 AppUserModelID。
-   具有不同引數的多個快捷方式，全都會導致使用者看到的相同應用程式，應該使用一個 AppUserModelID 來處理所有的快捷方式。 例如，Windows Internet Explorer 針對不同的模式有不同的快捷方式 (例如，啟動但不含附加元件) 但它們都應該以單一 Internet Explorer 實例的形式呈現給使用者。
-   做為主機進程並以應用程式形式執行目標內容的可執行檔必須 [註冊為主應用程式](#registering-an-application-as-a-host-process)，之後才能將不同的 AppUserModelIDs 指派給它所裝載的每個察覺體驗。 或者，主機進程可以允許裝載的程式設定其 AppUserModelIDs。 無論是哪一種情況，主機進程都必須保留 AppUserModelIDs 來源（本身或裝載的應用程式）的記錄。 在此情況下，沒有目標內容的主機進程的主要使用者體驗。 例如，Windows 遠端應用程式整合在本機 (滑軌) 應用程式、JAVA 執行時間、RunDLL32.exe 或 DLLHost.exe。

    如果是現有的託管應用程式，系統會嘗試識別個別的體驗，但新的應用程式應該使用明確的 AppUserModelIDs 來保證預期的使用者體驗。

-   對使用者而言，合作或連鎖的程式必須套用至每個進程的相同 AppUserModelID。 範例包括具有啟動器流程的遊戲 (連結) 和 Microsoft Windows Media Player，其中包含在一個進程中執行的第一次執行/安裝體驗，以及在另一個進程中執行的主要應用程式 (合作) 。
-   Shell 命名空間延伸模組可作為個別的應用程式，而不是流覽和管理 Windows 檔案總管中的內容，應該在其資料夾屬性中指派 AppUserModelID。 主控台的範例。
-   在部署架構之類的虛擬化環境中，虛擬化環境應該將不同的 AppUserModelIDs 指派給其所管理的每個應用程式。 在這些情況下，應用程式啟動器會使用中繼程式來設定環境，然後將作業交給不同的進程來執行應用程式。 請注意，這會導致系統無法使執行中的目標進程與快捷方式產生關聯，因為快捷方式指向中繼進程。

    如果有任何應用程式有多個視窗、快捷方式或程式，該應用程式指派的 AppUserModelID 也應套用至虛擬化環境中的每個部分。

    這種情況的其中一個範例是 ClickOnce 架構，它會代表它所管理的應用程式，正確指派 AppUserModelIDs。 如同在所有這類環境中，ClickOnce 部署及管理的應用程式不應該指派明確的 AppUserModelIDs，因為這樣做會與 ClickOnce 指派的 AppUserModelIDs 發生衝突，並導致非預期的結果。

## <a name="how-to-form-an-application-defined-appusermodelid"></a>如何形成 Application-Defined AppUserModelID

應用程式必須以下列格式提供其 AppUserModelID。 它不能超過128個字元，而且不能包含空格。 每個區段的大小寫都應該是 pascal。

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` 和都 `ProductName` 應該使用，而且 `SubProduct` 和 `VersionInformation` 部分是選擇性的，且取決於應用程式的需求。 `SubProduct` 允許包含數個 subapplications 的主要應用程式，為每個 subapplication 和其相關聯的視窗提供個別的工作列按鈕。 `VersionInformation` 允許兩個版本的應用程式在視為離散實體時並存。 如果應用程式不是以這種方式使用，則 `VersionInformation` 應該省略，使升級的版本可以使用與所取代版本相同的 AppUserModelID。

## <a name="where-to-assign-an-appusermodelid"></a>要在哪裡指派 AppUserModelID

當應用程式使用一或多個明確的 AppUserModelIDs 時，應該將這些 AppUserModelIDs 套用至下列位置和情況：

-   在應用程式快捷方式檔案的 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性中。 快速鍵 (為 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)、CLSID \_ ShellLink 或 .lnk 檔案) 透過 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 和整個 Shell 中使用的其他屬性設定機制來支援屬性。 這可讓工作列識別適當的快捷方式來釘選，並確保屬於該進程的 windows 會適當地與工作列按鈕相關聯。
    > [!Note]  
    > 建立快捷方式時，應將 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性套用至快捷方式。 使用 Microsoft Windows Installer (MSI) 安裝應用程式時， [MsiShortcutProperty](../msi/msishortcutproperty-table.md) 表格可在安裝期間建立 AppUserModelID 以套用至快捷方式。

     

-   做為任何應用程式執行中視窗的屬性。 這可以透過下列兩種方式之一來設定：

    1.  如果一個進程擁有不同的視窗需要不同的 AppUserModelIDs 來控制工作列群組，請使用 [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) 取出視窗的屬性存放區，並將 AppUserModelID 設定為視窗屬性。
    2.  如果程式中的所有視窗都使用相同的 AppUserModelID，請在 [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)上設定流程的 appusermodelid。 應用程式必須呼叫 **SetCurrentProcessExplicitAppUserModelID** ，以在應用程式呈現任何 UI 之前，在應用程式的初始啟動常式中設定其 AppUserModelID、對其跳躍清單進行任何操作，或 (，或讓系統) 任何對 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)的呼叫。

    視窗層級 AppUserModelID 會覆寫進程層級的 AppUserModelID。

    當應用程式在視窗層級設定明確的 AppUserModelID 時，應用程式可以為其工作列按鈕提供其重新開機命令的詳細資訊。 若要提供該資訊，請使用下列屬性：

    -   [AppUserModel. RelaunchCommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [AppUserModel. RelaunchDisplayNameResource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [AppUserModel. RelaunchIconResource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > 如果有啟動應用程式的快捷方式，應用程式應該將 AppUserModelID 套用為快捷方式的屬性，而不是使用重新開機屬性。 在此情況下，會使用命令列、圖示和快捷方式的文字來提供與重新開機屬性相同的資訊。

     

    視窗層級的明確 AppUserModelID 也可以使用 [AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) 屬性來指定它不應該用於釘選或重新執行。

-   在自訂或更新 ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)) 的呼叫中，取得 ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) ，或清除 (應用程式) 的捷徑清單 [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations) 。
-   在檔案關聯註冊 (透過其 [ProgID](fa-progids.md)) 如果應用程式使用系統自動產生的 **最新** 或 **經常** 的目的地清單。 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)會參考此關聯資訊。 這項資訊也會在透過 [**ICustomDestinationList：： AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory)將 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)目的地新增至自訂跳躍清單時使用。
-   在任何呼叫中，應用程式會直接進行 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)。 如果應用程式相依于 [一般檔案] 對話方塊來代表其呼叫 **SHAddToRecentDocs** ，則只有在整個進程已設定 AppUserModelID 時，這些呼叫才可以推算明確的 appusermodelid。 如果應用程式在其視窗上設定 AppUserModelIDs，而不是在處理常式上，則應用程式必須使用其明確的 AppUserModelID 來進行 **SHAddToRecentDocs** 本身的所有呼叫，以及防止 [一般檔案] 對話方塊進行自己的呼叫。 您必須在開啟專案時完成這項操作，以確保應用程式捷徑清單的 **最新** 或 **經常** 區段正確無誤。

下列專案描述常見的案例，以及在這些案例中套用明確 AppUserModelIDs 的位置。

-   當單一進程包含多個應用程式時，請使用 [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) 來取出視窗的屬性存放區，並將 AppUserModelID 設定為視窗屬性。
-   當應用程式使用多個進程時，請將 AppUserModelID 套用至每個進程。 您是否在每個程式上使用相同的 AppUserModelID，取決於您想要每個進程顯示為主要應用程式的一部分或個別實體。
-   若要將特定視窗與相同程式中的集合分開，請使用視窗的屬性存放區，將單一 AppUserModelID 套用至您想要分隔的視窗，然後將不同的 AppUserModelID 套用至該流程。 該進程中未以視窗層級的 AppUserModelID 明確標示的任何視窗，會繼承程式的 AppUserModelID。
-   如果檔案類型與應用程式相關聯，請在檔案類型的 [ProgID](fa-progids.md) 註冊中指派 AppUserModelID。 如果單一可執行檔以不同的模式啟動，並以不同的應用程式形式出現，則每種模式都需要個別的 AppUserModelID。 在這種情況下，檔案類型必須有多個 ProgID 註冊，每個都有不同的 AppUserModelID 註冊。
-   當有多個快捷方式位置可讓使用者啟動應用程式時， (在 [ **開始** ] 功能表、桌面上或其他地方) 抓取快捷方式的屬性存放區，將單一 AppUserModelID 套用至所有快速鍵做為快捷方式屬性。
-   當應用程式對 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) 進行明確呼叫時，請在呼叫中使用 AppUserModelID。 當使用 [一般檔案] 對話方塊來開啟或儲存檔案時，對話方塊會代表應用程式呼叫 **SHAddToRecentDocs** 。 該呼叫可以從流程推斷明確的 AppUserModelID。 但是，如果將明確的 AppUserModelID 套用為視窗屬性，則 [一般檔案] 對話方塊無法判斷正確的 AppUserModelID。 在這種情況下，應用程式本身必須明確呼叫 **SHAddToRecentDocs** ，並提供正確的 AppUserModelID。 此外，應用程式必須藉由在 \_ [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)或 [**IFILESAVEDIALOG**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)的 **GetOptions** 方法中設定 FOS DONTADDTORECENT 旗標，來防止 [一般檔案] 對話方塊代表其呼叫 SHAddToRecentDocs。

## <a name="registering-an-application-as-a-host-process"></a>將應用程式註冊為主機進程

應用程式可以設定 IsHostApp 登錄專案，讓工作列能夠將可執行檔的進程視為主機進程。 這會影響其群組和預設捷徑清單專案。

下列範例顯示必要的登錄專案。 請注意，不會指派值給專案。其目前狀態是必要的。 它是 REG \_ Null 值。

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

如果處理常式本身或用來啟動進程的快捷方式檔案有明確的 AppUserModelID，則會忽略主機進程清單，並將應用程式視為一般的應用程式。 應用程式的執行中視窗會以單一工作列按鈕分組，並將應用程式釘選到工作列。

如果只知道執行中進程的可執行檔名稱（沒有明確的 AppUserModelID），而且該可執行檔位於主機進程清單中，則會將進程的每個實例視為工作列群組的個別實體。 與進程之任何特定實例相關聯的工作列按鈕，不會顯示 [釘選/取消釘選] 選項，也不會顯示新進程實例的啟動圖示。 此程式也不符合在 [ **開始** ] 功能表中最常使用的 (MFU) 清單中包含的資格。 但是，如果程式是透過包含啟動引數的快捷方式來啟動， (通常是以「應用程式」 ) 的目標內容，系統就會判斷身分識別，而且可以釘選和 relaunched 應用程式。

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>工作列釘選和最近/頻繁清單的排除清單

應用程式、處理常式和 windows 可以選擇使其無法釘選到工作列，或包含在 [ **開始** ] 功能表的 最常使用清單中。 有三種機制可達成此目的：

1.  將 NoStartPage 專案新增至應用程式的註冊，如下所示：

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    與 NoStartPage 專案相關聯的資料會被忽略。 只需要存在專案。 因此，NoStartPage 的理想型別為 REG \_ NONE。

    請注意，任何使用明確的 AppUserModelID 都會覆寫 NoStartPage 專案。 如果已將明確的 AppUserModelID 套用至快捷方式、程式或視窗，它就會變成可釘選，而且符合 [ **開始** ] 功能表的 最常使用清單的資格。

2.  在 windows 和快捷方式上設定 [AppUserModel PreventPinning](../properties/props-system-appusermodel-preventpinning.md) 屬性。 您必須在 [PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) 屬性之前的視窗上設定這個屬性。
3.  將明確的 AppUserModelID 新增為下列登錄子機碼底下的值，如下所示：

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    每個專案都是 \_ 具有 AppUserModelID 名稱的 REG Null 值。 這份清單中所找到的任何 AppUserModelID 都不會可釘選，也不適合包含在 [ **開始** ] 功能表的 最常使用清單中。

請注意，某些可執行檔以及包含其名稱中特定字串的快捷方式，會自動排除，不要釘選和包含在 最常使用清單中。

> [!Note]  
> 您可以套用明確的 AppUserModelID 來覆寫此自動排除。

 

如果下列任何一個字串（不論大小寫）都包含在快捷方式名稱中，則不會可釘選程式，也不會顯示在最常使用的清單中 (不適用於 Windows 10) ：

-   文件
-   Help
-   安裝
-   其他資訊
-   自述
-   先閱讀
-   讀我檔案
-   移除
-   設定
-   支援
-   新功能

下列程式清單不是可釘選，而且會從最常使用的清單中排除。

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

上述的清單會儲存在下列登錄值中。

> [!Note]  
> 應用程式不應修改這些清單。 使用先前所列的其中一個排除清單方法來獲得相同的體驗。

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)
</dt> <dt>

[**GetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid)
</dt> <dt>

[工作列擴充功能](taskbar-extensions.md)
</dt> <dt>

[**ICustomDestinationList::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[**IApplicationDocumentLists::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[**IApplicationDestinations::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
