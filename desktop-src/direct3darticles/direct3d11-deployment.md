---
title: 遊戲開發人員的 Direct3D 11 部署
description: 本文說明如何在必要時，將 Direct3D 11 元件部署到系統上。
ms.assetid: 1fd43638-0d67-4a94-3be6-8789095f491e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd935aedee23ba731bc74e52c0773e6f02e5b5fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186063"
---
# <a name="direct3d-11-deployment-for-game-developers"></a>遊戲開發人員的 Direct3D 11 部署

本文說明如何在必要時，將 Direct3D 11 元件部署到系統上。

-   [概觀](#overview)
-   [Direct3D 11。3](#direct3d-113)
-   [Direct3D 11。2](#direct3d-112)
-   [Direct3D 11。1](#direct3d-111)
-   [D3D11InstallHelper.dll](#d3d11installhelperdll)
-   [D3D11Install.exe](#d3d11installexe)
-   [整合至安裝程式](#integrating-into-installation-programs)
    -   [整合至 InstallShield](#integrating-into-installshield)
    -   [整合至 MSI 套件](#integrating-into-an-msi-package)
-   [調試秘訣](#debugging-tips)
-   [公司設定](#corporate-settings)
-   [相關文章](#related-articles)

## <a name="overview"></a>概觀

Direct3D 11 API 透過動態著色器連結，擴充了現有的 Direct3D 10.1 API，並支援多執行緒轉譯和資源建立、計算著色器、硬體鑲嵌、BC6H/BC7 材質壓縮和 HLSL 著色器模型5.0。 除了 Direct3D 11 元件之外，DirectX 11 執行時間還包含一些額外的圖形元件： Direct3D 11、DXGI 1.1、10level9 功能層級、WARP10 software 轉譯裝置、Direct2D、DirectWrite，以及支援10level9 和 WARP10 的更新 Direct3D 10.1。 如需這些和其他 Windows 圖形元件的詳細資訊，請參閱 [Windows 中的圖形 api](graphics-apis-in-windows-vista.md)。

所有這些新的圖形元件都內建于 Windows 7 和 Windows Server 2008 R2 作業系統中。 您也可以使用 Windows Update 中的系統更新，在 Windows Vista 上安裝 Direct3D 11 API 和相關元件。請參閱知識庫文章 [KB 971644](https://support.microsoft.com/kb/971644)。 此更新需要 Windows Vista 和 Service Pack 2。 如此一來，已啟用自動更新的使用者就可能已安裝 Direct3D 11 元件，如同所有 Windows 7 使用者。

D3D11InstallHelper 範例的設計目的是為了簡化 Direct3D 11 API 的偵測、自動安裝系統更新（如果適用于使用者的電腦），並在需要更新的 Service Pack 時，為使用者提供適當的訊息以手動程式進行。

> [!Note]  
> HLSL 編譯器 (D3DCompile \*) 和 Direct3D 11 (D3DX11 的 D3DX 公用程式 \*) 程式庫不會內建于任何版本的 Windows 作業系統中，但是可以使用現有的 DirectSetup 技術將它們部署為應用程式安裝程式的一部分; 如需使用 DirectSetup 的詳細資訊，請參閱 [遊戲開發人員的 DirectX 安裝](/windows/desktop/DxTechArts/directx-setup-for-game-developers)。 「效果11」可作為 [Direct3D 11 更新效果](https://github.com/Microsoft/FX11)的共用來源支援程式庫，而且您可以直接將它包含在應用程式中， (與 DXUT 公用程式程式庫) 很類似。 因此，它不會有任何額外的執行時間轉散發需求。

## <a name="direct3d-113"></a>Direct3D 11。3

Windows 10 隨附于內建的 Direct3D 11.3 API。 如需 Direct3D 11.3 API 的新功能清單，請參閱 [direct3d 11.3 功能](/windows/desktop/direct3d11/direct3d-11-3-features) 。

## <a name="direct3d-112"></a>Direct3D 11。2

Windows 8.1 和 Windows Server 2012 R2 隨附內建的 Direct3D 11.2 API。 如需 Direct3D 11.2 API 的新功能清單，請參閱 [direct3d 11.2 功能](/windows/desktop/direct3d11/direct3d-11-2-features) 。

## <a name="direct3d-111"></a>Direct3D 11。1

Windows 8 和 Windows Server 2012 隨附于內建的 [Direct3D 11.1 API](/windows/desktop/direct3d11/direct3d-11-1-features) 。 您可以在 Windows 7 或 Windows Server 2008 R2 上，安裝適用于 [windows 7 的平臺更新](https://support.microsoft.com/kb/2670838) ，來取得 DIRECT3D 11.1 API 的部分支援。 如需 Windows 7 平臺更新的詳細資訊，請參閱 [windows 7 的平臺更新](platform-update-for-windows-7.md)。

## <a name="d3d11installhelperdll"></a>D3D11InstallHelper.dll

D3D11InstallHelper.dll 裝載偵測 Direct3D 11 元件的核心功能，並透過 Windows Update 服務執行系統更新（如果適用）。 DLL 不會直接顯示任何訊息或對話方塊。

DLL 包含下列進入點：

<dl> <dt>

<span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status
</dt> <dd>

此函式會執行必要的檢查，並傳回這部電腦上 Direct3D 11 的狀態。 此函數不需要系統管理員許可權。

-   已安裝的 D3D11IH \_ 狀態狀態 \_ 表示已在電腦上安裝 Direct3D 11，並已可供使用。
-   \_不支援的 D3D11IH 狀態 \_ \_ 表示此版本的 Windows 不支援 Direct3D 11 或相關技術。
-   D3D11IH 狀態的狀態 \_ \_ 需要 \_ 最新的 \_ SP，表示使用者必須安裝最新的 Windows Vista Service Pack。
-   最後，D3D11IH 狀態的狀態 \_ \_ 需要 \_ 更新，表示系統未安裝 Direct3D 11，但系統更新適用于此版本的 Windows。

</dd> <dt>

<span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11
</dt> <dd>

此函式會使用 Windows Update API，在此系統上執行安裝 Direct3D 11 的系統更新（如果適用）。 請注意，此功能需要 Windows Update 的網路連線才能成功，以及系統管理許可權。 它會採用選擇性的進度回呼函式和使用者內容指標，並在完成時傳回最終的結果碼。

-   D3D11IH \_ 結果 \_ 成功結果指出已套用系統更新並可供使用，而 D3D11IH \_ 結果 \_ 成功 \_ 重新開機表示系統更新需要電腦在完成前重新開機。 請注意，此函式不會排程系統重新開機。
-   \_ \_ 不 \_ 支援的 D3D11IH 結果表示系統更新不適用於此版本的 Windows。 如果只有在取得 D3D11IH 狀態時，才會呼叫此函式， \_ 則 \_ 需要 \_ 來自 CheckDirect3D11Status 的更新狀態。
-   找不到 D3D11IH \_ 結果 \_ 更新的結果 \_ \_ 指出 Windows Update 伺服器上找不到系統更新套件。
-   如果 Windows Update 下載或安裝失敗，則 \_ \_ 會傳回 D3D11IH 結果更新 \_ 下載 \_ 失敗或 D3D11IH \_ 結果 \_ 更新 \_ 安裝 \_ 失敗的結果。
-   如果 Windows Update API 傳回網路連線錯誤，則 \_ \_ 會傳回 D3D11IH 結果 WU \_ 服務 \_ 錯誤結果，指出問題可能是間歇性的或與網路設定或防火牆設定相關的問題。 再次嘗試更新功能可能會成功。

</dd> </dl>

如需有關 Windows Update API 的詳細資訊，請參閱 [Windows Update AGENT API](/windows/desktop/Wua_Sdk/portal-client)。

## <a name="d3d11installexe"></a>D3D11Install.exe

> [!Note]  
> D3D11Install.exe 需要 D3D11InstallHelper.dll 才能執行。

D3D11Install.exe 是一種工具，可讓您以 UI 和使用者訊息的形式使用 D3D11InstallHelper.dll 作為獨立安裝程式，也可以做為適當使用 DLL 的範例。 如果已安裝 Direct3D 11，則程式會結束，如果系統更新在不需要重新開機系統的情況下成功套用，則需要安裝 Service Pack，或這部電腦不支援 Direct3D 11。 如果成功套用系統更新，且需要重新開機系統才能完成，則會傳回1。 針對其他錯誤狀況，則會傳回2。 請注意，這個可執行檔需要系統管理員許可權才能執行，而且它的資訊清單會在啟用 UAC 的 Windows Vista 或 Windows 7 上執行時要求提升許可權。 D3D11Install.exe 可以用來作為獨立工具來部署 Direct3D 11 更新，也可以直接由安裝程式使用。

它支援下列命令列參數：

<dl> <dt>

<span id="_quiet__"></span><span id="_QUIET__"></span>/quiet 
</dt> <dd>

不顯示任何訊息、提示、進度對話方塊或錯誤訊息。

</dd> <dt>

<span id="_passive__"></span><span id="_PASSIVE__"></span>/passive 
</dt> <dd>

不顯示任何訊息、提示或錯誤訊息，但會顯示 [進度] 對話方塊。

</dd> <dt>

<span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal 
</dt> <dd>

只顯示較短的提示。

</dd> <dt>

<span id="_y__"></span><span id="_Y__"></span>/y 
</dt> <dd>

針對標準和最短的安裝，隱藏提示以確認安裝更新（如有需要）。

</dd> <dt>

<span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/langid decimal 
</dt> <dd>

強制顯示使用者訊息和對話方塊資源時要使用的語言識別項代碼。 預設值是1024，它會使用系統預設語言設定。

</dd> <dt>

<span id="_wu__"></span><span id="_WU__"></span>/wu 
</dt> <dd>

強制使用 Windows Update 而不是系統預設值，這可能是在受管理的伺服器上執行的 (WSUS) 或其他非標準的設定 Windows Server Update Services。

</dd> </dl>

## <a name="integrating-into-installation-programs"></a>整合至安裝程式

為了符合支援的簡易安裝，適用于 [Windows 遊戲的技術需求 3.1](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006)，必須小心，讓任何使用者提示都能在安裝程式初期出現，並確保不會有多個與 UAC 相關的提高許可權提示。 有三個可達成此目標的基本選擇：

1.  最基本的方法是使用命令列參數 **/minimal** 來執行 D3D11Install.exe。 這應該在安裝程式 Q&中提早完成，而且安裝應使用傳回值1，表示應該在安裝結束時排定重新開機。 執行程式需要系統管理許可權。
2.  您可以直接使用 D3D11InstallHelper.dll 來偵測更新的需求，並提供狀態 D3D11IH 狀態需要最新的 SP 所需的任何使用者訊息，而 \_ \_ \_ \_ 解決方案需要手動使用者操作。 [不支援的 D3D11IH 狀態] 狀態結果 \_ \_ \_ 可用來控制安裝 direct3d 11 相關的資產，或做為僅限 direct3d 11 （僅限應用程式）的錯誤情況，但不一定是有用的終端使用者訊息。 針對狀態 D3D11IH \_ 狀態 \_ 需要 \_ 更新，安裝程式可以直接使用 DLL 進入點 DoUpdateForDirect3D11 來執行更新，並處理各種產生的終端使用者訊息。 您可以檢查 D3D11Install.exe 對話方塊和字串資料表資源，找到標準訊息的範例。 更新進入點需要系統管理員許可權。
3.  混合式方法是使用 D3D11InstallHelper.dll 檢查狀態，如果狀態碼 D3D11IH \_ 狀態 \_ 需要 \_ 最新的 \_ SP 或 D3D11IH \_ 狀態需要 \_ \_ 更新，可以使用參數 **/minimal** 和 **/y** 來執行 D3D11Install.exe，以顯示對話方塊或視需要執行更新。 這些步驟應該在安裝程式早期執行（通常是在 Q&A 之後立即執行，而且執行可執行檔需要系統管理許可權）。

### <a name="integrating-into-installshield"></a>整合至 InstallShield

使用 D3D11InstallHelper 範例，即可輕鬆地從 InstallShield 的 InstallScript 處理 Direct3D 11 部署。 使用 InstallScript 與 InstallShield 整合所需的步驟如下所示 (使用方法3，如下一節所述) ：

1.  在 InstallShield 編輯器中開啟 InstallScript 專案。
2.  在 **支援** 檔案中新增 D3D11InstallHelper.dll 並 D3D11Install.exe 至專案。

    **將檔案新增至 InstallShield 專案**

    1.  在 [**安裝設計** 工具] 索引標籤的左側導覽窗格中，按一下 [**行為和邏輯**] 下的 [支援檔案] **/[公告欄**]。
    2.  按一下 [**語言獨立**]，然後以滑鼠右鍵按一下 [檔案] 視窗並選取 [**插入** 檔案]。 流覽以新增 D3D11InstallHelper.dll 和 D3D11Install.exe。 這些檔案的預設位置為： SDK 根 \\ 範例 \\ c + + \\ 其他 \\ Bin \\ x86

3.  在 [InstallScript explorer] 中，按一下 [InstallScript] 檔案， (通常是 rul) 將呼叫 DLL 或可執行檔（位於左側導覽窗格中的 [ **行為] 和 [邏輯** ] 下）。
4.  將下列 InstallScript 貼到靠近頂端的檔案中：

    ``` syntax
#define D3D11IH_STATUS_INSTALLED       0
#define D3D11IH_STATUS_NOT_SUPPORTED   1
#define D3D11IH_STATUS_REQUIRES_UPDATE 2
#define D3D11IH_STATUS_NEED_LATEST_SP  3
#define D3D11IH_STATUS_ERROR           -1
    prototype NUMBER D3D11InstallHelper.CheckDirect3D11StatusIS();

#define D3D11IH_RESULT_SUCCESS                0
#define D3D11IH_RESULT_SUCCESS_REBOOT         1
#define D3D11IH_RESULT_NOT_SUPPORTED          2
#define D3D11IH_RESULT_UPDATE_NOT_FOUND       3
#define D3D11IH_RESULT_UPDATE_DOWNLOAD_FAILED 4
#define D3D11IH_RESULT_UPDATE_INSTALL_FAILED  5
#define D3D11IH_RESULT_WU_SERVICE_ERROR       6
#define D3D11IH_RESULT_ERROR                  -1
    prototype NUMBER D3D11InstallHelper.DoUpdateForDirect3D11IS(BOOL);
    ```

5.  將下列 InstallScript 貼入 **OnFirstUIBefore** 函式中的檔案，在傳回0之前：

    ``` syntax
    Dlg_D3D11:
        UseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        nResult = D3D11InstallHelper.CheckDirect3D11StatusIS();   
        UnUseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        
        if ( nResult = D3D11IH_STATUS_REQUIRES_UPDATE
             || nResult = D3D11IH_STATUS_NEED_LATEST_SP) then
            nResult = LaunchAppAndWait(
    SUPPORTDIR^"D3D11Install.exe",
    "/minimal /y", WAIT);
            if ( nResult < 0 ) then
                MessageBox("Unable to launch D3D11Install.exe",
     SEVERE);
            elseif ( nResult == 1 ) then
                BATCH_INSTALL = 1;
            endif;          
        endif;
    ```

### <a name="integrating-into-an-msi-package"></a>整合至 MSI 套件

以下是使用 MSI 自訂動作整合 Direct3D 11 部署所需步驟的高階描述， (使用) 本主題稍早所述的方法3：

1.  將屬性新增至名為 **RelativePathToD3D11IH** 的 MSI 屬性工作表，其中包含在安裝期間 D3D11Install.exe 和 D3D11InstallHelper.dll 的相對路徑 (這通常會在媒體影像) 中。 這也會將 MSI 屬性 D3D11IH \_ 狀態設定為 CheckDirect3D11Status 所傳回的狀態 (字串屬性等於列舉符號或「錯誤」 ) 。
2.  在 CostFinalize 動作之後，以立即自訂動作的形式呼叫 D3D11InstallHelper.dll 函式 **SetD3D11InstallMSIProperties** ，以針對其他自訂動作設定適當的 MSI 屬性。
3.  安裝時，會在呼叫 D3D11InstallHelper.dll 函式 **DoD3D11InstallUsingMSI** 的 InstallFiles 動作之後，觸發延遲的自訂動作。 自訂動作必須將旗標 msidbCustomActionTypeNoImpersonate 設定為在提高許可權的內容中執行。
4.  在 InstallFinalize 動作之後，如有需要，請以立即自訂動作的形式呼叫 D3D11InstallHelper.dll 函數 **FinishD3D11InstallUsingMSI** ，以處理成功的重新開機要求結果碼。

下列指示會詳細說明此程式，其描述可使用 MSI 編輯器（例如 [Orca 編輯器](/windows/desktop/Msi/orca-exe)）完成的程式。 有些 MSI 編輯器具有可簡化其中一些設定步驟的嚮導。

**設定 MSI 套件以與 D3D11InstallHelper.dll整合**

1.  以 Orca 開啟 MSI 套件。
2.  將下表中顯示的資料列加入至 MSI 封裝中的二進位資料表。

    | Name    | 資料                                         |
    |---------|----------------------------------------------|
    | D3D11IH | DLL 的檔案路徑 \\D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > 此檔案將內嵌在 MSI 套件中，因此您必須在每次重新編譯 D3D11InstallHelper.dll 時執行此步驟。

     

3.  將下表中顯示的資料列加入至 MSI 封裝中的 CustomAction 資料表。 

    | 動作              | 類型                                                                                                                                                                   | 來源  | 目標                       |
    |---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------|
    | Direct3D11SetProps  | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | SetD3D11InstallMSIProperties |
    | Direct3D11DoInstall | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137 | D3D11IH | DoD3D11InstallUsingMSI       |
    | Direct3D11Finish    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | FinishD3D11InstallUsingMSI   |

    

     

4.  將下表中的 [動作]、[條件] 和 [順序] 所顯示的值，加入至 MSI 封裝中的 InstallExecuteSequence 資料表。 

    | 動作              | 條件     | 順序 | 備註                                                                                                                                                          |
    |---------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Direct3D11SetProps  |               | 1016     | 序號會在 CostFinalize 之後立即放置動作。                                                                                                 |
    | Direct3D11DoInstall | 未安裝 | 4004     | 此自訂動作只會在所有使用者的新安裝期間發生。 序號會將動作放在 InstallFiles 之後和復原之後。 |
    | Direct3D11Finish    |               | 6615     | 序號會在 InstallFinalize 之後立即放置動作。                                                                                              |

    

     

5.  將下表中顯示的資料列加入至 MSI 封裝中的 **屬性** 資料表。 

    | 屬性              | 值                                                                        |
    |-----------------------|------------------------------------------------------------------------------|
    | RelativePathToD3D11IH | 包含 D3D11Install.exe 和 D3D11InstallHelper.dll 的相對檔案路徑 |

    

     

    > [!Note]  
    > 路徑所指定的位置是相對於安裝路徑所指定的位置，例如「可轉散發套件」 \\ 。

     

6.  儲存 MSI 套件。 如需有關 MSI 封裝和 Windows Installer 的詳細資訊，請參閱 [Windows Installer](/windows/desktop/Msi/windows-installer-portal)。

## <a name="debugging-tips"></a>偵錯秘訣

D3D11InstallHelper.dll 和 D3D11Install.exe 都可以使用 Visual Studio 中的 Debug 設定來建立，而這些版本會將訊息列印至標準的 Windows 調試輸出機制。

## <a name="corporate-settings"></a>公司設定

D3D11InstallHelper 範例是針對透過 Windows Update 的標準部署而設計，這是使用消費者安裝遊戲的最常見案例。 不過，許多遊戲開發人員都是使用發行者和開發工作室，在具有本機受控伺服器的企業設定中，使用 Windows Server Update Services (WSUS) 技術來提供軟體更新。 在這種環境中，本機 IT 系統管理員可以核准控制公司網路內的電腦可以使用哪些更新，且無法使用標準取用者版本的 update KB 971644。

在公司/企業設定中部署 DirectX 11 的基本解決方案有三種：

-   在某些設定中，您可以直接檢查 Windows Update，而不是使用本機管理的 WSUS 伺服器。 基於這個理由，D3D11InstallHelper 支援 **/wu** 命令列參數。 不過，並非所有的公司網路都允許與公用 Microsoft 伺服器的連線。
-   本機 IT 系統管理員可以核准 KB 971512，這是從 WSUS 部署且包含 Direct3D 11 API 的企業支援更新。 這是標準使用者在完全鎖定的環境中取得 Direct3D 11 更新的唯一選項。
-   或者，您可以手動安裝 [KB 971512](https://support.microsoft.com/kb/971512/) 。

玩家的電腦很罕見只能從本機管理的 WSUS 伺服器取得更新，而這只是大型組織中可能在這類環境中的開發人員。

## <a name="related-articles"></a>相關文章

[適用于遊戲開發人員的 Windows 防火牆](/windows/desktop/DxTechArts/games-and-firewalls)

[適用于遊戲開發人員的 Windows 遊戲瀏覽器](/windows/desktop/DxTechArts/windows-game-explorer-integration)