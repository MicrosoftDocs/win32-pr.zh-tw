---
title: Windows遊戲開發人員的安裝程式
description: 本文概述 Windows Installer，特別是以遊戲開發人員為目標。 如需本文所述之功能和 api 的詳細檔，請參閱 Windows Platform SDK。
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc587725ce2a2a675c9db835fabb503bc44ffa62c07ee1ce80578aef9432cf9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290388"
---
# <a name="windows-installer-for-game-developers"></a>Windows遊戲開發人員的安裝程式

示範如何使用 Windows Installer 在終端使用者電腦上安裝遊戲。 Windows安裝程式會提供自訂使用者介面的完整支援，以及修補程式。

Microsoft Windows Installer 是在 Windows 電腦上安裝軟體的慣用 API。 雖然 Windows Installer 的許多功能都是為了支援在公司環境中部署商務應用程式而設計，Windows Installer 也完全適用于在終端使用者電腦上安裝遊戲。 使用 Windows Installer 進行遊戲安裝的主要優點如下：

-   可靠卸載
-   視需要安裝內容的能力
-   支援完全自訂的使用者介面
-   有效率的修補

本文概述 Windows Installer，特別是以遊戲開發人員為目標。 如需本文所述之功能和 api 的詳細檔，請參閱 Windows Platform SDK。

-   [概觀](#overview)
-   [重要 Windows Installer 概念](#key-windows-installer-concepts)
    -   [Components](#components)
    -   [功能](#features)
-   [安裝狀態](#install-states)
-   [隨選安裝](#install-on-demand)
-   [自訂使用者介面](#custom-user-interface)
-   [修補](#patching)
-   [其他資源](#other-resources)

## <a name="overview"></a>概觀

所有以 Windows Installer 為基礎的安裝程式都會使用稱為 MSI 檔案的安裝資料庫檔案來描述應用程式的安裝方式。 MSI 檔案包含要安裝哪些檔案、登錄機碼、桌面快捷方式、檔案關聯和其他應用程式元素的相關資訊。 實際要安裝的檔案可在 MSI 檔案本身內壓縮、配套並壓縮成個別的「封包檔」，或是儲存在安裝媒體上的其他位置，作為個別的未壓縮檔案。 MSI 檔案也可以參考外部執行的自訂動作，以允許 MSI 檔案原本不允許的動作。

MSI 檔案可以選擇性地包含使用者介面，以引導使用者完成安裝程式。 此 UI 適用于大部分的應用程式。 不過，它具有一般 Windows 應用程式的外觀和風格，而許多遊戲開發人員偏好讓其安裝應用程式保有遊戲本身的外觀和操作，以提供更一致的終端使用者體驗。 為了支援這個完全自訂的 ui 案例，安裝應用程式可以關閉 Windows Installer 的內建 ui，並處理整個使用者介面本身。 Windows Installer API 會公開回呼機制，讓自訂的安裝程式 UI 可以收到安裝進度的通知，以及重要事件，例如磁片變更要求。

Windows安裝程式不是建立安裝程式的端對端解決方案。 它是一種 API，可供安裝程式用來實際安裝檔案、登錄機碼、桌面快捷方式，以及應用程式的其他元素。 所有主要商用設定工具的最新版本 (例如，InstallShield、取向、Microsoft Visual Studio) 支援 Windows Installer。 這些工具提供便利的使用者介面來建立遊戲的設定，但它們依賴 Windows Installer API 來進行大部分的實際安裝。 這些工具也可以用來建立包含安裝套件的 MSI 資料庫，然後從自訂撰寫的安裝程式 UI 來安裝它。 作為協力廠商工具的替代方案，Windows Installer API 提供以程式設計方式建立和操作 msi 資料庫所需的所有功能，而 Windows Platform SDK 則包含稱為 Orca 的裸機資料庫編輯工具。

## <a name="key-windows-installer-concepts"></a>重要 Windows Installer 概念

以下是 Windows Installer 的元件和功能。

### <a name="components"></a>單元

應用程式是由一個或多個元件所組成，由 GUID 元件識別碼來識別。 元件是不可部分完成的單位;完整安裝或完全沒有安裝。 元件可以包含單一檔案、多個檔案、登錄機碼、桌面快捷方式或某些組合。 資源 (檔案等) 元件內的元件對該元件而言必須是唯一的，而且兩個元件都不能包含相同的資源。 絕對不會明確安裝元件;它只會安裝為功能的一部分 (請參閱下列) 。

### <a name="features"></a>功能

功能是一組元件，由 GUID 功能識別碼識別。 與元件不同的是，多個功能可能包含相同的元件。 如果已安裝這些功能的任何一項，則會安裝多個功能之間共用的元件，而且只有在已卸載參考元件的所有功能時，才會移除該元件。 安裝功能可以在產品安裝過程中自動完成，也可以使用 [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) API 手動完成。

雖然有些遊戲有多個可獨立安裝的「功能」，但功能的 Windows Installer 概念仍很有用。 由於 Windows Installer 功能不只是一組可一起安裝的元件，因此遊戲可以使用功能將遊戲特定階段所需的所有內容分組在一起。 例如，層級導向的遊戲可以定義每個層級的一個功能，其中包含該層級所需的所有內容。 這可讓遊戲一次從遊戲本身安裝內容一層，而不是在初始安裝期間安裝所有層級的所有內容。

## <a name="install-states"></a>安裝狀態

每個元件或功能都有相關聯的安裝狀態，可判斷元件或功能是否可用，如果是，則會安裝元件或功能的檔案。 功能的可能安裝狀態為：

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>缺席
</dt> <dd>

這項功能未安裝，因此無法存取。

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>當地
</dt> <dd>

這項功能可供使用，而且會安裝成從本機硬碟執行。

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>源
</dt> <dd>

此功能可供使用，而且會安裝成從原始來源媒體執行， (通常是 CD 或 DVD) 。

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>廣告
</dt> <dd>

尚未安裝此功能，但可使用 [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) API 隨選安裝。 實際安裝功能時，可以將它安裝到本機或來源的狀態。

</dd> </dl>

元件可以有上述任何一個狀態，但「已公告」除外。 如果元件是已公告功能的一部分，則在安裝此功能之前，元件會顯示為「未存在」。

## <a name="install-on-demand"></a>隨選安裝

Windows安裝程式可讓應用程式將功能標示為已公告，這表示該功能尚未安裝，但在需要時可在執行時間安裝。 在執行時間安裝功能稱為「隨選安裝」。 遊戲可以使用隨選安裝來大幅縮短初始遊戲設定所需的時間，方法是延後安裝遊戲內容，直到執行時間需要為止。 在執行時間安裝內容所需的延遲，通常可以透過在背景執行緒中執行隨選安裝來部分或完全隱藏，而使用者則會被視為該遊戲。

## <a name="custom-user-interface"></a>自訂使用者介面

雖然 Windows Installer 提供可引導使用者完成應用程式安裝的預設使用者介面，但這個介面看起來像是標準 Windows 應用程式。 許多遊戲開發人員偏好其安裝 UI 與遊戲本身具有相同的外觀和操作，讓使用者可以感受遊戲的 ambiance。 為了支援此功能，Windows Installer 可完全停用其內建使用者介面，讓開發人員能夠提供完全自訂的 UI。

自訂安裝程式會先使用 [**MsiSetInternalUI**](/windows/desktop/api/msi/nf-msi-msisetinternalui) API 來停用 Windows Installer 的內建使用者介面，以將 UI 層級設定為 [無 INSTALLUILEVEL] \_ 。 然後，它會呼叫 [**MsiSetExternalUI**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) API，以指定要在安裝過程中呼叫的回呼函式，以便在安裝期間通知安裝程式的重要事件。

然後藉由呼叫 [**MsiInstallProduct**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) API 來啟動實際的安裝程式。 此 API 接受參數字串，以允許呼叫者指定命名屬性的值。 這些屬性可以在安裝資料庫本身內使用，以自訂應用程式的安裝方式。 這些屬性可以用來指定：

-   要在其中安裝應用程式的目錄
-   要在本機安裝哪些功能，以及要從 CD/DVD 安裝哪些功能 (例如，讓您可以在最基本安裝和完整安裝之間進行選擇) 
-   是否應該為電腦的所有使用者安裝應用程式，或僅針對目前的使用者安裝應用程式

在安裝過程中，安裝程式會使用傳送至回呼函式的通知訊息，以判斷何時更新其進度指標 UI、何時提示使用者插入下一張 CD，或何時通知使用者安裝程式發生錯誤。

## <a name="patching"></a>修補

Windows安裝程式可透過套用修補檔案來修補已安裝的應用程式。 修補檔案包含修補程式所要加入的新檔案、由修補程式修改的檔案，以及對安裝資料庫所做的變更清單。 為了節省空間，而不是儲存修補程式所變更之檔案的完整內容，修補檔案實際上只包含檔案原始版本與新版本檔案之間的差異。

若要建立修補程式，您需要應用程式的每個版本的安裝映射，您希望修補程式從中升級，以及應用程式新升級版本的安裝映射。 安裝映射是由 MSI 資料庫和應用程式的所有實際資料檔案所組成。 若要為新的應用程式版本建立安裝映射，最好的方法是從繼承應用程式複製安裝映射，然後進行任何必要的變更，以將該複本更新為修補過的版本。

當您擁有所有必要的安裝映射之後，就可以使用 Msimsp.exe 建立修補程式，這是 Platform SDK 中所提供的修補程式建立工具。 此工具會詢問每個設定影像的位置，然後判斷如何有效率地表示後續版本之間的差異。 此工具的輸出是延伸 MSP)  (所識別的最終修補檔。 為了以程式設計的方式安裝修補程式，請呼叫 [**MsiApplyPatch**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) API。 使用者也可以在 [Explorer] 中按兩下 MSP 檔案，以手動方式安裝修補程式。

## <a name="other-resources"></a>其他資源

-   如需 Windows Installer API 的詳細資訊，請參閱[Windows Installer](/windows/desktop/Msi/windows-installer-portal)。
-   如需遊戲安裝的最佳作法資訊，請參閱 [遊戲的安裝與維護](/windows/desktop/DxTechArts/installation-and-maintenance-of-games)。

 

 