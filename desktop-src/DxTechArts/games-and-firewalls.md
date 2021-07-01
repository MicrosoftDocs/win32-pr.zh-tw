---
title: 適用于遊戲開發人員的 Windows 防火牆
description: 本文說明 Windows 防火牆的原因、其存在的原因，以及其運作方式。 最重要的是，它會說明如何設定您的遊戲來與防火牆搭配運作。
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c7ff3c9b651b6264703732f0eec57054784034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120233"
---
# <a name="windows-firewall-for-game-developers"></a>適用于遊戲開發人員的 Windows 防火牆

本文說明 Windows 防火牆的原因、其存在的原因，以及其運作方式。 最重要的是，它會說明如何設定您的遊戲來與防火牆搭配運作。

內容: 

-   [什麼是防火牆？](#what-is-a-firewall)
-   [如何判斷遊戲是否受到影響？](#how-can-i-tell-if-my-game-is-affected)
-   [Windows XP SP2 之前的防火牆](#the-firewall-before-windows-xp-sp2)
-   [Windows XP SP2 防火牆更好用](#windows-xp-sp2-firewall-is-better)
-   [使用 Windows 防火牆](#working-with-the-windows-firewall)
-   [使用 InstallShield InstallScript 整合](#integrating-using-installshield-installscript)
-   [Windows Installer 的明智整合](#integrating-into-wise-for-windows-installer)
-   [整合至 Windows Installer](#integrating-into-windows-installer)
-   [建議](#recommendations)

## <a name="what-is-a-firewall"></a>什麼是防火牆？

防火牆可針對網路型入侵提供阻礙。 它會封鎖未經要求的連入流量，並藉由拒絕 (ICMP) 要求的網際網路控制訊息通訊協定，讓系統在網際網路上大多不可見。 這表示 ping 和 tracert 將無法運作。 防火牆也會尋找並拒絕不正確封包。

此屏障可防止隨機攻擊。 攻擊是藉由尋找具有相同弱點的許多系統來散佈。 防火牆可以針對目前未使用的功能，加上「請勿打擾」符號，來對抗許多攻擊;攻擊會被忽略，且不會被刪除。 Windows 防火牆的基本優點是，未使用的功能和應用程式無法作為攻擊的途徑。

使用者將系統設定為識別所需的應用程式和功能，並應對網路開放。 當應用程式已安裝，或是當應用程式嘗試對網路開啟本身時，就會發生這種情況。

## <a name="how-can-i-tell-if-my-game-is-affected"></a>如何判斷遊戲是否受到影響？

隨著 Windows XP SP2 的抵達，Windows 防火牆已廣泛部署。 所有多人遊戲的 Windows 遊戲都會受到某種程度的影響。 用戶端通常是在良好的圖形中，而伺服器、主機和對等的對等都需要設定防火牆才能繼續運作。 具體而言，會捨棄傳入的未經要求流量。 防火牆會根據封包內容和最近的網路活動來攔截網路流量篩選封包。 防火牆會使用 [內容] 和 [活動] 來決定要轉寄或捨棄封包。 一旦正確設定防火牆之後，遊戲就能像之前一樣接受輸入的未經要求流量。

誰有輸入未經要求的流量？

-   用戶端/伺服器：所有參與者連接到中央伺服器。 中央伺服器是具有連入未經要求流量的伺服器。 連線到伺服器的用戶端會請求傳回流量，如果遵循用戶端的規則，系統就會允許該流量通過防火牆。 中央伺服器必須設定為接受未經要求的流量，才能讓用戶端流量通過防火牆。
-   大量多人 (MMP) ：所有參與者都連線至資料中心。 這相當於複雜的用戶端/伺服器關聯性，因為資料中心具有輸入的未經要求流量。 參與者是用戶端，而且通常不需要接受未經要求的流量。
-   點對點，也就是所有參與者都直接彼此連接：所有參與者都必須準備好接受來自加入群組之任何新玩家的未經要求流量。 就某種意義而言，每個參與者都必須以主機的形式運作，因此必須全部設定為主機。

用戶端通常是不錯的圖形。 其連出的傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 連線可以正常運作，因為輸出使用者資料包協定 (UDP) 訊息，以及及時回應這些訊息，防火牆會在每個外寄訊息之後，將埠保持開啟狀態達90秒，以預期回復。

## <a name="the-firewall-before-windows-xp-sp2"></a>Windows XP SP2 之前的防火牆

Windows XP 和 Windows Server 2003 中的網際網路連線防火牆 (ICF) 是具狀態的封包篩選器，可處理網際網路通訊協定第4版 (IPv4) 和網際網路通訊協定第6版 (IPv6) 。 不過，它並不會預設為開啟，且不支援協力廠商網路堆疊，在世界中有很大的數位，例如大型的網際網路提供者（包括全國電話公司）。

針對不在 Windows XP SP2 上的，強烈建議開啟 ICF。 請參閱中的「使用網際網路防火牆」， https://www.microsoft.com/security/protect 作為保護您電腦的第一步。 網際網路連線防火牆 (ICF) 提供埠對應以覆寫封包篩選器。 基本上，您會指定要開啟的埠，並在關閉它之前保持開啟狀態。 如果使用者在關閉之前重新開機，它將保持開啟狀態，直到特別關閉為止。 防火牆的控制和埠對應的管理是透過 [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) 和 [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6) 來完成。

適用于 Windows XP SP2 的 Windows 防火牆是更完整的解決方案，可支援協力廠商網路堆疊，並更聰明地處理埠：只有在需要它們的應用程式仍在使用中時，埠才會保持開啟狀態。

## <a name="windows-xp-sp2-firewall-is-better"></a>Windows XP SP2 防火牆更好用

Windows XP SP2 將安全性選項和設定放在前方。 目標是要預設保護，並允許使用者對其電腦上允許執行哪些應用程式做出明智的選擇。

Windows XP SP2 和 Windows Server 2003 Service Pack 1 (SP1) 都有提供新的 Windows 防火牆。 就像 ICF 一樣，它是一種同時支援 IPv4 和 IPv6 的軟體防火牆，但不同于 ICF 的 Windows 防火牆：

-   具有系統的開機時間保護，在開機期間消除一小部分的弱點。
-   支援協力廠商網路堆疊。
-   具有「開啟但沒有例外狀況」模式，會封鎖所有未經要求的連入封包。 當您使用公用網路（例如機場或咖啡廳）時，這就很好用。

在「沒有例外狀況的開啟」模式中，所有的靜態洞都會關閉。 允許用來開啟靜態洞的 API 呼叫，但會延後;也就是說，在防火牆切換回正常作業之前，它們都不會套用。 應用程式的所有接聽要求也會被忽略。 輸出連接仍然會成功。

針對新的應用程式，請在安裝期間將您的應用程式新增至「例外狀況清單」。 您可以使用 [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) 介面來新增應用程式，並提供完整的路徑。 我們將在此討論範例中的詳細資料。

請注意，您可能會想知道它是否有安全性風險，也就是應用程式可以從例外狀況清單中新增和移除應用程式，以因應使用者的介入，或您認為較大的風險是，應用程式可以完全停用防火牆。 若要執行這些無比理智，應用程式必須具有系統管理員許可權。 如果您在系統上以系統管理員模式執行惡意程式碼，則遊戲已經結束，而且駭客已經獲勝。 駭客停用防火牆的功能只需要使用註腳。

繼承應用程式（包括在使用者升級至 Windows XP SP2 之前安裝的應用程式）會以例外狀況清單快顯視窗來處理 (請參閱 [圖 1]) 。 此對話方塊會顯示當應用程式嘗試為連入流量開啟埠時，可能是使用非零埠的 UDP 呼叫 bind () ，或接受 TCP/IP 通訊協定的 () 。 您必須以系統管理員身分執行，才能「解除封鎖」應用程式，而「稍後詢問我」則不允許這段時間，但會在下一次重新詢問。

這是未封鎖的系統強制回應對話方塊。 執行全螢幕的 Microsoft Direct3D 應用程式時，對話方塊會出現在下方;然後使用者可以在應用程式結束全螢幕模式或 alt 索引標籤回桌面時處理它。 不過，使用者在遊戲執行全螢幕時，不一定會看到這個對話方塊出現的情況，因此請務必避免使用 [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) 介面讓這個對話方塊出現，如下所述。

**圖1。例外狀況清單快顯視窗對話方塊**

![例外狀況清單快顯視窗對話方塊](images/firewalls1.jpg)

您將會注意到快顯視窗知道應用程式的名稱和發行者。 這裡沒有什麼神奇之處-它是從可執行檔的版本資訊中提取。 這項資訊是很重要的系統管理工具;它甚至可以用來進行應用程式相容性工作。 有些應用程式會忽略將此版本資訊保持在最新狀態。

使用者也可以透過使用者介面 (UI 來新增其應用程式)  (請參閱圖 2) 

**[圖 2]設定防火牆**

![設定防火牆](images/firewalls2.jpg)

**圖3。將程式新增至防火牆例外清單**

![將程式新增至防火牆例外清單](images/firewalls3.jpg)

最佳情況是從例外狀況清單自動進行新增和移除。 執行這些新增和移除的最佳時機是在安裝和卸載程式期間。 在防火牆例外清單中新增或移除需要系統管理員許可權，因此請務必將此納入考慮。

## <a name="working-with-the-windows-firewall"></a>使用 Windows 防火牆

同樣地，大部分的遊戲都只需要新增到防火牆例外清單中，如果它們可以作為伺服器或執行對等通訊協定。 FirewallInstallHelper.dll 是可從安裝程式呼叫的範例 DLL。 如果您想要將來源直接整合到自己的應用程式，則會提供來源。 您可以在這裡找到範例：



|             | 檔案                                                                             |
|-------------|------------------------------------------------------------------------------|
| **來源：**     |  (SDK 根) \\ 範例 \\ c + + \\ 其他 \\ FirewallInstallHelper                        |
| **可執行：** |  (SDK 根) \\ 範例 \\ c + + \\ 其他 \\ Bin \\ <arch> \\FirewallInstallHelper.dll |



 

此 DLL 匯出的函式如下：

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**
</dt> <dd>

此函式會將應用程式新增至例外狀況清單。 它會取得可執行檔的完整路徑，以及將出現在防火牆例外清單中的易記名稱。 此函數需要系統管理員許可權。

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**
</dt> <dd>

**AddApplicationToExceptionListW** 的 ANSI 版本

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**
</dt> <dd>

此函數會從例外狀況清單中移除應用程式。 它會取得可執行檔的完整路徑。 此函數需要系統管理員許可權

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**
</dt> <dd>

**RemoveApplicationFromExceptionListW** 的 ANSI 版本

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**
</dt> <dd>

此函數會報告應用程式是否已停用或從例外狀況清單中移除。 您應該在每次執行遊戲時呼叫它。 函數會取得可執行檔的完整路徑。 此函數不需要系統管理員許可權。

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**
</dt> <dd>

**CanLaunchMultiplayerGameW** 的 ANSI 版本

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**
</dt> <dd>

只有當您在 Windows Installer 中使用自訂動作時，才需要呼叫此項。 詳細資訊請見下文。

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**
</dt> <dd>

只有當您在 Windows Installer 中使用自訂動作時，才需要呼叫此項。 詳細資訊請見下文。

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**
</dt> <dd>

只有當您在 Windows Installer 中使用自訂動作時，才需要呼叫此項。 詳細資訊請見下文。

</dd> </dl>

下列各節說明從 InstallShield、明智或 Windows Installer 的封裝中，呼叫從此 FirewallInstallHelper 匯出之 DLL 函數的特定方法。 所有方法都會轉譯相同的結果，並由開發人員決定要執行的方法。

## <a name="integrating-using-installshield-installscript"></a>使用 InstallShield InstallScript 整合

使用防火牆 Api 的替代方法是將函式呼叫新增至 InstallShield InstallScript。 整合所需的步驟相當簡單：

1.  在 InstallShield 編輯器中開啟 InstallScript 專案。
2.  將 FirewallInstallHelper.dll 新增至專案做為支援檔。

    1.  在 [專案助理] 索引標籤底下開啟 [應用程式檔] 索引標籤。
    2.  按一下 [新增檔案] 按鈕，將檔案新增至應用程式目的檔案夾。
    3.  流覽至您所建立的 FirewallInstallHelper.dll，或使用 DirectX SDK 中所提供的，並將它新增至專案。

3.  將 InstallScript 新增至專案。

    1.  開啟安裝設計工具視圖，然後按一下 [行為] 和 [邏輯] \| InstallScript
    2.  按一下 InstallScript 檔案， (通常設定 rul) 在編輯器中開啟它
    3.  將下列程式碼貼入 InstallScript 檔案：

    ``` syntax
    #include "ifx.h"

    prototype BOOL FirewallInstallHelper.AddApplicationToExceptionListW( WSTRING, WSTRING );
    prototype BOOL FirewallInstallHelper.RemoveApplicationFromExceptionListW( WSTRING );

    function OnMoved()
        WSTRING path[256];
    begin
        // The DLL has been installed into the TARGETDIR
        if !MAINTENANCE then // TRUE when installing
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.AddApplicationToExceptionListW( path, "TODO: change to friendly app name" );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
          

    function OnMoving()
        WSTRING path[256];
    begin
        // The DLL is about to be removed from TARGETDIR
        if MAINTENANCE && UNINST != "" then // TRUE when uninstalling
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.RemoveApplicationFromExceptionListW( path );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
    ```

    4.  使用將顯示在防火牆例外清單中的應用程式名稱，以及與安裝目錄相關之遊戲可執行檔的路徑，來變更 TODO 批註。

## <a name="integrating-into-wise-for-windows-installer"></a>Windows Installer 的明智整合

若要 Windows Installer 的明智整合，必須執行下列步驟：

1.  以您的 Windows Installer 專案為您開放。
2.  選取底部的 [安裝專家] 索引標籤。
3.  按一下 [檔案]，然後將 FirewallInstallHelper.dll 從 DXSDK 新增至遊戲的安裝目錄。
4.  選取底部的 [MSI 腳本] 索引標籤。
5.  選取靠近底部的 [立即執行] 索引標籤。
6.  CostFinalize 之後，新增「設定屬性」動作，將 FULLPATH 設定為「 \[ \] 從安裝目錄 INSTALLDIR 可執行檔的相對路徑」。 例如，" \[ INSTALLDIR \]game.exe"，沒有引號
7.  選取靠近底部的 [執行延後] 索引標籤。
8.  PublishProduct 之後，請將 "If 語句" 加入條件為「未安裝」 (區分大小寫的) 。
9.  在 If 區塊內，新增「從目的地呼叫自訂 DLL」動作。

    1.  將 [DLL 檔案] 欄位設定為 [ \[ INSTALLDIR \]FirewallInstallHelper.dll]。
    2.  將 [函數名稱] 欄位設定為 "AddApplicationToExceptionListA"。
    3.  新增類型為 "string 指標"、值來源為 "Property" 和屬性名稱 "FULLPATH" 的參數。
    4.  新增類型為「字串指標」、值來源為「常數」的第二個參數，並將常數值設定為您想要在防火牆例外清單中顯示的易記應用程式名稱。
    5.  藉由新增 "End 語句" 來關閉 If 區塊。

10. 在靠近頂端的 RemoveFiles 動作正上方，新增另一個 If block，條件為 "REMOVE ~ =" ALL "" (區分大小寫，且不含外部引號) 。
11. 在第二個 If 區塊內，新增「從目的地呼叫自訂 DLL」動作。

    1.  將 [DLL 檔案] 欄位設定為 [ \[ INSTALLDIR \]FirewallInstallHelper.dll]。
    2.  將 [函數名稱] 欄位設定為 "RemoveApplicationFromExceptionListA"。
    3.  新增類型為 "string 指標"、值來源為 "Property" 和屬性名稱 "FULLPATH" 的參數。
    4.  藉由新增「結束語句」來關閉第二個 If 區塊。

## <a name="integrating-into-windows-installer"></a>整合至 Windows Installer

若要與高階 Windows Installer 整合，必須執行這些步驟。 以下將詳細說明這些步驟：

-   新增2個屬性 "FriendlyNameForFirewall" 和 "RelativePathToExeForFirewall"，如下所述。
-   在 CostFinalize 動作之後，請在立即自訂動作中呼叫 "SetMSIFirewallProperties"，以針對其他自訂動作設定適當的 MSI 屬性。
-   在安裝 InstallFiles 動作之後，請呼叫使用 FirewallInstallHelper 之 "AddToExceptionListUsingMSI" 函式的延遲自訂動作。
-   在 InstallFiles 動作之後的卸載期間，呼叫使用 FirewallInstallHelper 之 "RemoveFromExceptionListUsingMSI" 函式的延遲自訂動作。
-   在復原期間，呼叫延遲的自訂動作，此動作也會呼叫 FirewallInstallHelper 的 "RemoveFromExceptionListUsingMSI" 函式。

以下是使用 MSI 編輯器（例如在 Platform SDK 中找到的 Orca）執行這項作業所需的步驟。 請注意，有些編輯器具有可簡化其中一些步驟的嚮導：

1.  以 Orca 開啟 MSI 套件。
2.  將下列內容新增至二進位資料表：

    

    | Name     | 資料                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 防火牆 | 將它指向 FirewallInstallHelper.dll。 此檔案將內嵌在 MSI 套件中，因此每次重新編譯 FirewallInstallHelper.dll 時，您都必須執行此步驟。 |

    

     

3.  將下列內容新增至 CustomAction 資料表：

    

    | 動作                   | 類型                                                                                                                                                                                                   | 來源   | 目標                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | FirewallSetMSIProperties | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | 防火牆 | SetMSIFirewallProperties        |
    | FirewallAdd              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | 防火牆 | AddToExceptionListUsingMSI      |
    | FirewallRemove           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | 防火牆 | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackAdd      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | 防火牆 | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackRemove   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | 防火牆 | AddToExceptionListUsingMSI      |

    

     

4.  將下列內容新增至 InstallExecuteSequence 資料表：

    

    | 動作                   | 條件     | 順序 | 備註                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FirewallSetMSIProperties |               | 1010     | CostFinalize 之後，就會有這種情況。                                                                                                                                       |
    | FirewallAdd              | 未安裝 | 4021     | 此自訂動作只會在全新安裝期間發生。 序號會將動作放在 InstallFiles 之後和復原之後。                              |
    | FirewallRollBackAdd      | 未安裝 | 4020     | 只有在取消全新安裝時，才會發生此自訂動作。 序號會將動作放在 InstallFiles 之後，以及加入自訂動作之前。          |
    | FirewallRemove           | 已安裝     | 3461     | 此自訂動作只會在卸載期間發生。 序號會在 RemoveFiles 之前和復原之後直接放置動作。                           |
    | FirewallRollBackRemove   | 未安裝 | 3460     | 只有在取消卸載時，才會發生此自訂動作。 序號會在 RemoveFiles 之前，以及在移除自訂動作之前，直接放置動作。 |

    

     

5.  將下列內容新增至屬性工作表：

    

    | 屬性                     | 值                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | FriendlyNameForFirewall      | 必須是例外狀況清單會顯示的名稱。 例如，「範例遊戲」 |
    | RelativePathToExeForFirewall | 必須是遊戲已安裝的可執行檔。 例如，"ExampleGame.exe"  |

    

     

如需 Windows Installer 的詳細資訊，請參閱 [Windows Installer](/windows/desktop/Msi/windows-installer-portal)。

## <a name="recommendations"></a>建議

防火牆在此保持不變。 這些建議會為您的客戶提供良好的 Windows 遊戲防火牆體驗：

-   不要告訴使用者停用防火牆來播放您的遊戲。 這樣一來，即使電腦不在玩遊戲時，也會讓整個電腦容易受到攻擊。
-   讓您的使用者無縫設定防火牆。 在安裝期間將您的應用程式新增至例外狀況清單，並在安裝期間從例外清單中移除您的應用程式。
-   如果有多人遭到防火牆狀態封鎖，請將意見反應提供給使用者。 例如，如果網路功能無法運作，請停用它們，因為應用程式不允許或因為系統處於「無例外狀況」模式。

 

 