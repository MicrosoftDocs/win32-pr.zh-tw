---
title: Windows適用于遊戲開發人員的遊戲瀏覽器
description: 本文概述如何使用新的 GDF 架構，在 Windows Vista 和 Windows 7 上向遊戲瀏覽器和家長監護註冊遊戲的流程。
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6420b4783cfad7afd82483d45448ccb219342b4a7b88aa54e36c2de15ca0f778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070418"
---
# <a name="windows-games-explorer-for-game-developers"></a>Windows適用于遊戲開發人員的遊戲瀏覽器

WindowsVista 透過包含遊戲瀏覽器，改善了 Windows 遊戲的使用者體驗。 [遊戲瀏覽器] 會在 Windows Vista [開始] 功能表中公開為 [遊戲] 資料夾，並提供用來存取遊戲的集中位置。

從 DirectX SDK 2009 年3月版本開始，新的遊戲定義檔 (GDF) 架構可用來支援 Windows 7、遊戲提供者和 RSS 摘要以及 IGameExplorer2 中的功能。 IGameExplorer2 是 Windows 7 的新介面，可簡化將遊戲與遊戲 Explorer 整合的流程。

本文概述如何使用新的 GDF 架構，在 Windows Vista 和 Windows 7 上向遊戲瀏覽器和家長監護註冊遊戲的流程。

內容: 

-   [必要條件](#prerequisites)
-   [與安裝程式整合](#integrating-with-an-installer)
-   [整合流程](#integration-process)
-   [遊戲瀏覽器工作](#games-explorer-tasks)
-   [整合至 InstallScript](#integrating-into-installscript)
-   [整合至 MSI 套件](#integrating-into-an-msi-package)
-   [提示的調試](#debugging-tips)
    -   [使用範例程式碼進行測試](#test-with-sample-code)
    -   [確定您的遊戲已正確移除](#make-sure-that-your-game-was-removed-properly)
    -   [務必使用 Authenticode 簽署](#be-sure-to-sign-using-authenticode)
    -   [確定可以使用家長監護](#be-sure-that-parental-controls-are-available)
    -   [確認工作的類型正確](#verify-that-tasks-are-of-the-correct-type)
    -   [確認 GDF 二進位檔中的資料](#verify-the-data-in-gdf-binary)
-   [總結](#summary)

## <a name="prerequisites"></a>必要條件

您必須先建立遊戲定義檔 (GDF) ，才能將遊戲整合至 [遊戲] Explorer。 GDF 是一個 XML 檔案，其中包含描述遊戲的中繼資料。 在2009年3月的 DirectX SDK 版本中，已將遊戲提供者、RSS 摘要和遊戲工作的區段新增至 GDF 架構。 若要使用本文中的指示，您必須使用這個新的 GDF 格式來建立您的 GDF 檔案。

Microsoft 提供的工具可讓您在 DirectX SDK 的遊戲定義檔編輯器中撰寫 GDFs，讓此建立程式更容易。 這項工具也可協助您建立當地語系化版本的 GDF。

撰寫和當地語系化 GDF 之後，它必須封裝在二進位檔案的資源區段內， (可執行檔或 DLL) ，以及遊戲的縮圖和圖示。 GDF 包含與遊戲相關聯的所有中繼資料，包括遊戲的評等。 Windows家長監護會使用遊戲的評等來允許家長監護遊戲的存取。 包含 GDF 的二進位檔案必須使用有效的 Authenticode 憑證以數位方式簽署;否則，[遊戲瀏覽器] 和 [家長監護] 系統會忽略遊戲的評等，因為無法信任評等資訊而不需要認證。 如需使用 Authenticode 簽署程式碼的詳細資訊，請參閱 [遊戲開發人員的 Authenticode 簽署](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)。

## <a name="integrating-with-an-installer"></a>與安裝程式整合

為了簡化遊戲瀏覽器整合，GameUXInstallHelper 範例提供可在 Windows XP、Windows Vista 和 Windows 7 上呼叫的通用 API。 它是設計用來處理 InstallShield 和取向安裝系統，以及 MSI 自訂動作和自訂安裝工具的腳本。 系統會在此範例 DLL 內處理作業系統的偵測，因此呼叫端不需要擔心用戶端是否執行 Windows XP、Windows Vista 或 Windows 7。

此 DLL 匯出的函式如下：

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**
</dt> <dd>

在指定 GDF 二進位檔的路徑、安裝遊戲之資料夾的完整路徑，以及安裝範圍的情況下，向遊戲瀏覽器註冊遊戲。

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**
</dt> <dd>

使用遊戲瀏覽器註冊遊戲;ANSI 版本的 **GameExplorerInstallW**。

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**
</dt> <dd>

藉由指定 GDF 二進位檔的路徑，移除遊戲瀏覽器註冊的遊戲。

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**
</dt> <dd>

使用遊戲瀏覽器移除註冊遊戲;ANSI 版本的 **GameExplorerUninstallW**。

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**
</dt> <dd>

針對 MSI 延後自訂安裝的動作設定 CustomActionData 屬性。 本文稍後會詳細說明此函數的使用方式。

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**
</dt> <dd>

將遊戲新增至遊戲瀏覽器;供 MSI 自訂動作安裝期間使用。

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**
</dt> <dd>

從遊戲瀏覽器移除遊戲;供 MSI 自訂動作安裝期間使用。

</dd> </dl>

這些函數會在 GameUXInstallHelper 標頭中進一步說明。

## <a name="integration-process"></a>整合流程

一旦將 GDF 和相關的檔案新增至二進位資源之後，就可以將該遊戲與遊戲瀏覽器整合。 使用 **GameUXInstallHelper** 將簡化整合程式。 若要向遊戲瀏覽器註冊遊戲，請使用 GDF 二進位檔的路徑來呼叫 **GameExplorerInstall** 、安裝遊戲之資料夾的完整路徑，以及安裝領域。 若要移除遊戲的註冊，請使用 GDF 二進位檔的路徑來呼叫 **GameExplorerUninstall** 。

請注意，移除流程只會移除一個唯一的安裝。 如果遊戲已安裝多次，則必須針對每個獨特的安裝重複此程式。

## <a name="games-explorer-tasks"></a>遊戲瀏覽器工作

[遊戲瀏覽器] 工作將會出現在 [遊戲瀏覽器] 中專案的內容功能表中。 工作分為「播放」工作和支援工作。 「播放」工作會將遊戲啟動為特定模式，而支援工作則提供任何其他用途，包括連結至網站。

在 Windows Vista 中，工作只是位於特定資料夾中的快捷方式。 播放工作和支援工作會儲存在具有對應名稱 PlayTasks 和 SupportTasks 的資料夾中。 GameUXInstallHelper 可以從 GDF 的二進位檔讀取遊戲的工作資訊，並自動建立所有的快捷方式。

在 Windows 7 中不需要工作的快捷方式，因為遊戲瀏覽器會直接從 GDF 二進位檔案取得所有工作資訊。

## <a name="integrating-into-installscript"></a>整合至 InstallScript

使用 GameUXInstallHelper 範例，可讓您輕鬆地從 InstallShield 的 InstallScript 呼叫遊戲瀏覽器 Api。 與 InstallShield 整合所需的步驟如下：

1.  在 InstallShield 編輯器中開啟 InstallScript 專案。
2.  將 GameUXInstallHelper.dll 新增至要安裝到目標目錄的專案。

    **若要將 GameUXInstallHelper.dll 加入至 InstallScript 專案：**

    1.  在 [ **安裝設計** 工具] 索引標籤上，按一下左側導覽窗格中的 [ **應用程式資料** ]。
    2.  按一下 [檔案 **和資料夾** ]，然後在 **來源電腦的資料夾** 中流覽，以找出 **來源電腦** 檔案中的 GameUXInstallerHelper.dll。

        GameUXInstallerHelper.dll 的預設位置為 DirectX SDK 根 \\ 範例 \\ c + + \\ 其他 \\ Bin \\ x86。

    3.  在 [ **目的地電腦的資料夾**] 下，按一下 [ **應用程式目的檔案夾**]。
    4.  將 GameUXInstallerHelper.dll 從 **來源電腦的** 檔案拖曳至 **目的地電腦的** 檔案。

3.  在 [InstallScript explorer] 中，按一下 InstallScript 檔案， (通常是 rul) 呼叫 DLL 函式。
4.  將下列 InstallScript 貼到檔案中：

    ``` syntax
    typedef GUID
    begin
    LONG  Data1;
    SHORT Data2;
    SHORT Data3;
    CHAR  Data4(8);
    end;

    prototype LONG GameUXInstallHelper.GameExplorerInstallW(WSTRING, WSTRING, NUMBER);
    prototype LONG GameUXInstallHelper.GameExplorerUninstallW(WSTRING);

    function OnMoved()

    WSTRING gdfbin[256];
    WSTRING path[256];
    NUMBER scope;

    begin

    if !MAINTENANCE then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    path = TARGETDIR;
    gdfbin = TARGETDIR ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    if ALLUSERS == 1 then
    scope = 3;
    else
    scope = 2;
    endif;

    GameUXInstallHelper.GameExplorerInstallW( gdfbin, path, scope);

    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;

    function OnMoving()

    WSTRING gdfbin[256];

    begin

    if MAINTENANCE && UNINST != "" then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    gdfbin = path ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    GameUXInstallHelper.GameExplorerUninstallW(gdfbin);
    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;
    ```

## <a name="integrating-into-an-msi-package"></a>整合至 MSI 套件

以下是使用 MSI 自訂動作呼叫遊戲瀏覽器 Api 所需步驟的高階描述：

1.  將屬性新增至名為 "RelativePathToGDF" 的 MSI 屬性工作表，其中包含 GDF 二進位檔的相對路徑。
2.  在 CostFinalize 動作之後，請在立即自訂動作中呼叫 GameUXInstallHelper DLL 函式 **SetMSIGameExplorerProperties** ，以針對其他自訂動作設定適當的 MSI 屬性。
3.  在安裝時，會在呼叫 GameUXInstallHelper DLL 函式 **AddToGameExplorerUsingMSI** 的 InstallFiles 動作之後觸發延遲的自訂動作。 如果安裝適用于所有使用者，則自訂動作必須設定旗標 msidbCustomActionTypeNoImpersonate;否則，它不能設定這個旗標。 因此，會定義兩個幾乎相同的自訂動作： GameUXAddAsAdmin 和 GameUXAddAsCurUser。
4.  移除安裝之後，在呼叫 GameUXInstallHelper DLL 函式 **RemoveFromGameExplorerUsingMSI** 的 RemoveFiles 動作之前觸發延遲的自訂動作。 如果是針對所有使用者進行安裝，則自訂動作必須設定旗標 msidbCustomActionTypeNoImpersonate;否則，它不能設定這個旗標。 因此，會定義兩個幾乎相同的自訂動作： GameUXRemoveAsAdmin 和 GameUXRemoveAsCurUser。
5.  定義復原自訂動作，以處理使用者在其中一個自訂動作已發生之後取消安裝或移除的情況。 這會產生額外4個自訂動作： GameUXRollBackAddAsAdmin、GameUXRollBackAddAsCurUser、GameUXRollBackRemoveAsAdmin 和 GameUXRollBackRemoveAsCurUser。

下列指示會詳細說明此程式，其描述可使用 MSI 編輯器（例如在 Platform SDK 中找到的 Orca 編輯器）完成的程式。 有些 MSI 編輯器具有可簡化其中一些設定步驟的嚮導。

**設定 MSI 套件以與遊戲瀏覽器整合**

1.  以 Orca 開啟 MSI 套件。
2.  將下表中顯示的資料列加入至 MSI 封裝中的 **二進位** 資料表。 

    | 名稱   | 資料                                          |
    |--------|-----------------------------------------------|
    | GAMEUX | DLL 的檔案路徑 \\GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > 此檔案將內嵌在 MSI 套件中，因此您必須在每次重新編譯 GameUXInstallHelper.dll 時執行此步驟。

     

3.  將下表中顯示的資料列加入至 MSI 封裝中的 **CustomAction** 資料表。

    | 動作                        | 類型                                                                                                                                                                                                   | 來源 | 目標                         |
    |-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------------------------------|
    | GameUXSetMSIProperties        | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | GAMEUX | SetMSIGameExplorerProperties   |
    | GameUXAddAsAdmin              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXAddAsCurUser            | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackAddAsAdmin      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackAddAsCurUser    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsAdmin           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsCurUser         | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackRemoveAsAdmin   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackRemoveAsCurUser | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | AddToGameExplorerUsingMSI      |

    

     

4.  將下表中的 [動作]、[條件] 和 [順序] 所顯示的值，加入至 MSI 封裝中的 **InstallExecuteSequence** 資料表。

    | 動作                        | 條件                      | 順序 | 備註                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | GameUXSetMSIProperties        |                                | 1015     | 序號會在 CostFinalize 之後立即放置動作。                                                                                                                                   |
    | GameUXAddAsAdmin              | 未安裝和 ALLUSERS     | 4003     | 此自訂動作只會在所有使用者的全新安裝期間發生。 序號會將動作放在 InstallFiles 之後和復原之後。                                 |
    | GameUXAddAsCurUser            | 未安裝且未進行 ALLUSERS | 4004     | 此自訂動作只會在目前使用者的全新安裝期間發生。 序號會將動作放在 InstallFiles 之後和復原之後。                     |
    | GameUXRollBackAddAsAdmin      | 未安裝和 ALLUSERS     | 4001     | 只有在所有使用者的全新安裝都已取消時，才會發生這個自訂動作。 序號會將動作放在 InstallFiles 之後，以及加入自訂動作之前。             |
    | GameUXRollBackAddAsCurUser    | 未安裝且未進行 ALLUSERS | 4002     | 只有當目前使用者的全新安裝取消時，才會發生這個自訂動作。 序號會將動作放在 InstallFiles 之後，以及加入自訂動作之前。 |
    | GameUXRemoveAsAdmin           | 移除 ~ = "ALL" 和 ALLUSERS     | 3452     | 此自訂動作只會在所有使用者的移除期間發生。 序號會在 RemoveFiles 之前和復原之後直接放置動作。                                     |
    | GameUXRemoveAsCurUser         | 移除 ~ = "ALL" 而非 ALLUSERS | 3453     | 此自訂動作只會在移除目前使用者的期間發生。 序號會在 RemoveFiles 之前和復原之後直接放置動作。                              |
    | GameUXRollBackRemoveAsAdmin   | 移除 ~ = "ALL" 和 ALLUSERS     | 3450     | 只有在所有使用者的移除動作都已取消時，才會發生這個自訂動作。 序號會在 RemoveFiles 之前，以及在移除自訂動作之前，直接放置動作。              |
    | GameUXRollBackRemoveAsCurUser | 移除 ~ = "ALL" 而非 ALLUSERS | 3451     | 只有在取消目前使用者的移除時，才會發生這個自訂動作。 序號會在 RemoveFiles 之前，以及在移除自訂動作之前，直接放置動作。       |

    

     

5.  將下表中顯示的資料列加入至 MSI 封裝中的屬性資料表。

    | 屬性          | 值                                                         |
    |-------------------|---------------------------------------------------------------|
    | RelativePathToGDF | \\包含 GDF 之二進位檔案的相對檔案路徑名稱 |

    

     

    > [!Note]  
    > 路徑所指定的位置是相對於安裝路徑所指定的位置。 例如，bin \\GDF.dll。

     

6.  儲存 MSI 套件。

如需有關 MSI 封裝和 Windows Installer 的詳細資訊，請參閱[Windows Installer](/windows/desktop/Msi/windows-installer-portal)。

## <a name="debugging-tips"></a>提示的調試

以下是一些秘訣，可協助您在呼叫遊戲瀏覽器 Api 時，偵測問題：

### <a name="test-with-sample-code"></a>使用範例程式碼進行測試

建立 GameUXInstallHelper 範例解決方案將會建立 GameUXInstallHelper.dll 和 GDFInstall.exe。 GDFInstall.exe 是使用 GameUXInstallHelper.dll 的範例應用程式。 如果您想要從遊戲瀏覽器安裝或移除 GDF 二進位檔，執行 GDFInstall.exe 將會提示。 您可以測試 GDF 二進位檔案，方法是將它傳入做為 GDFInstall.exe 的第一個命令列參數。

如果您沒有 GDF 二進位檔或無法安裝，請嘗試使用 DirectX SDK 中的範例 GDF。 GDFExampleBinary 範例可在 DirectX SDK 中找到，而且只是一個只包含 GDF 檔案的 DLL。 此外，來源中也包含它的 GDFMaker 專案。 您可以使用 GDFInstall.exe 來建立並測試。 您也可以將其 XML 與您的 XML 進行比較，以精確找出問題所在。

### <a name="make-sure-that-your-game-was-removed-properly"></a>確定您的遊戲已正確移除

如果遊戲已安裝在遊戲瀏覽器中，後續對 **IGameExplorer：： AddGame** 的呼叫將會傳回 E \_ 失敗，因此請確定您的遊戲未在測試之前安裝。 如果您只為目前的使用者安裝 GDF，然後嘗試為所有使用者安裝 GDF，這也適用。 您必須先移除目前使用者的遊戲， **IGameExplorer：： AddGame** 才會成功。

如果您執行 **GDFInstall.exe enum**，範例應用程式將會進入不同的模式，以列舉所有已安裝的遊戲管理器遊戲並提示您移除它們。 您也可以在 HKEY \_ LOCAL \_ MACHINE Software Microsoft Windows CurrentVersion GameUX 中流覽和搜尋登錄， \\ \\ \\ \\ \\ 確定未針對系統上的其他使用者安裝您的遊戲。 不過，請勿改變這些登錄設定的任何其他用途，因為它們在作業系統的未來版本中不保證會保持相容。

### <a name="be-sure-to-sign-using-authenticode"></a>務必使用 Authenticode 簽署

如果您已提供評等，但未在 [遊戲] Explorer 中看到它，請確定您已使用 Authenticode 來簽署包含評等的可執行檔或 DLL 檔案。 遊戲瀏覽器會忽略未簽署檔案中的分級資訊。 如需 Authenticode 的詳細資訊，請參閱 [遊戲開發人員的 Authenticode 簽署](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)。

### <a name="be-sure-that-parental-controls-are-available"></a>確定可以使用家長監護

確定您是在提供家長監護的 Windows Vista 版本上測試家長監護： home Basic、home 進階版或旗艦版。 Windowsvista Business 和 Windows vista Enterprise 不提供家長監護，不過如果您要測試 Windows Vista 旗艦版，而且測試電腦已加入網域，您必須變更群組原則設定，讓家長監護成為可見。 若要這樣做，請參閱 [使用遊戲瀏覽器開始使用](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85))。

### <a name="verify-that-tasks-are-of-the-correct-type"></a>確認工作的類型正確

如果您指定的支援工作並未出現在 [遊戲瀏覽器] 中，請確認它們都是網頁連結。 任何其他快速鍵工作都必須建立為播放工作。 這些工作會在這篇文章的 [ [遊戲] Explorer](#games-explorer-tasks)工作中討論。

### <a name="verify-the-data-in-gdf-binary"></a>確認 GDF 二進位檔中的資料

GDFTrace.exe 是在 DirectX SDK 中找到的工具。 您可以在 GDF 二進位檔上執行 GDFTrace.exe，它會針對每個支援的語言輸出包含在二進位檔中的所有 GDF 中繼資料，以進行快速驗證。 它也會顯示遺漏或過時資訊的任何警告。

## <a name="summary"></a>摘要

Windows Vista 中的遊戲瀏覽器提供簡單、可自訂的方式，讓您的遊戲可提供給 Windows Vista 的使用者，但也需要您在安裝過程中向系統註冊遊戲。 GameUXInstallHelper 範例大幅簡化了開發人員的流程。

 

 