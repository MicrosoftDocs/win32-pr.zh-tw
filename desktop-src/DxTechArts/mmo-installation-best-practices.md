---
title: 大量多人連線遊戲的安裝最佳做法
description: 本文說明如何為大量多人的線上遊戲建立一環信任設計， (MMOG) 用戶端安裝和自訂遊戲更新系統，以搭配 Windows Vista 和 Windows 7 的 Windows 和安全性模型一起運作。
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b574bdf2ae98b28fabed97340d6aa38b1a864c24519bb6532d0aa4069882efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815431"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>大量多人連線遊戲的安裝最佳做法

本文說明如何為大量多人的線上遊戲建立一環信任設計， (MMOG) 用戶端安裝和自訂遊戲更新系統，以搭配 Windows Vista 和 Windows 7 的 Windows 和安全性模型一起運作。 此方法的設計目的是要在支援標準使用者帳戶（其對硬碟機和系統登錄的存取受到限制）時，啟用 MMOG 標題的修補。

-   [為什麼 MMOG 用戶端對傳統零售版遊戲有不同的需求](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [一環信任方法的總覽](#overview-of-a-chain-of-trust-approach)
-   [所有專案都會在伺服器上進行驗證，如果我的用戶端遭到駭客入侵，為什麼應該擔心？](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Trust-Worthy 載入器應用程式的結構](#construction-of-the-trust-worthy-loader-application)
    -   [背景讀取](#background-reading)
    -   [安裝受信任的載入器和 Patcher](#installation-of-the-trusted-loader-and-patcher)
    -   [安裝遊戲可執行檔、Dll 和資料](#installation-of-the-game-executables-dlls-and-data)
    -   [存取控制清單修改程式碼](#access-control-list-modification-code)
    -   [Advanced Users 的安裝](#installations-for-advanced-users)
    -   [載入器的信任驗證](#the-loaders-verification-of-trust)
    -   [資料驗證](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>為什麼 MMOG 用戶端對傳統零售版遊戲有不同的需求

Mmog 持續連線和演進的本質，讓它能夠提供用戶端程式代碼和內容的定期更新，以修正安全性弱點並擴充遊戲體驗。 有了幾乎每日更新的可能性，MMOG 案例需要謹慎的管理，以確保使用者易懂的體驗。 這與傳統零售購買模型不同，可能會在產品的零售出貨日期附近提供少量的修補程式。 作業系統提供的 Windows Installer 有限使用者修補技術的設計目的，是要處理少量的應用程式修補程式，而不是 mmog 所需的大量和高頻率。 因此，通常需要開發自訂修補系統來解決 Mmog 的需求，包括所開發之特定 MMOG 特定的任何特殊需求。

因為許多電腦都連接到網際網路，Windows Vista 和 Windows 7 都有難上加難的安全性限制和保護，可限制應用程式對硬碟的不同區域的存取權。 不同于 Windows XP，這些限制會針對使用者帳戶的預設模式啟用。 設計遊戲的配置、可執行檔和資料，以及其相關聯的修補系統時，必須考慮這些限制。 如需作業系統所提供之安全性措施的詳細資訊，請參閱 [遊戲開發人員的使用者帳戶控制](/windows/desktop/DxTechArts/user-account-control-for-game-developers)。

## <a name="overview-of-a-chain-of-trust-approach"></a>一環信任方法的總覽

本白皮書中所提供的自訂更新方法，是以可信賴的載入器應用程式安裝到受保護的 Program Files 資料夾，同時將遊戲可執行檔和資料保留在共用的全部使用者存取區域中。 信任鏈從載入器開始，它會在啟動前執行遊戲二進位檔和資料的有效性檢查。

![信任鏈從可信任的載入器開始](images/mmo-installation-best-practices-01.gif)

值得信賴的載入器必須有足夠的邏輯，才能確認遊戲的可執行檔和其他二進位檔在啟動遊戲之前都未遭到篡改。 載入器也可以視需要驗證遊戲資料，不過，遊戲資料的大小通常太大，因此每次都能在單一行程中進行檢查。 替代方法是使用取樣模式，以確保整個資料集的驗證會在一段長時間內進行。 載入器應用程式可能包含一個遊戲修補引擎，它提供了信任的方法來整合更新與已安裝的遊戲。

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>所有專案都會在伺服器上進行驗證，如果我的用戶端遭到駭客入侵，為什麼應該擔心？

不可能信任用戶端未遭到入侵;因此，MMOG 伺服器通常會驗證從用戶端接收的所有資料。 雖然此處理可以識別遊戲 universe 內遭入侵或作弊的遊戲用戶端，但是伺服器無法輕易地識別出遊戲用戶端可以公開的所有問題。 請務必強化保護，避免駭客想要使用您的用戶端做為您的服務、其他使用者的攻擊平臺，甚至只是做為攻擊用戶端機器本身的向量。 程式碼簽署和資料驗證技術的應用在執行之前，可以協助偵測遭入侵的用戶端。 由於修補機制需要公開不受程式檔標準唯讀許可權保護的可執行檔和 DLL 二進位檔，因此在啟動之前先驗證這些檔案，對整體系統安全性很重要。

此模型並不會嘗試處理可能會遭到入侵的惡意管理員使用者案例，而是將焦點放在保護標準使用者不小心執行遭篡改的程式碼。 傳統的伺服器用戶端驗證技術其實是惡意用戶端系統管理員的唯一可能緩和措施。

## <a name="construction-of-the-trust-worthy-loader-application"></a>Trust-Worthy 載入器應用程式的結構

### <a name="background-reading"></a>背景讀取

讀者應該熟悉下列檔，其中提供基礎技術的詳細資料，以確保軟體型信任的最佳作法。

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>程式碼簽署
</dt> <dd>

[遊戲開發人員的 Authenticode 簽署](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool
</dt> <dd>

MSDN 上的[SignTool](/windows/desktop/SecCrypto/signtool)

</dd> </dl>

下一節將詳細說明用來建立載入器應用程式的 Api，其支援安裝和驗證信任檢查的光碟版面配置。

### <a name="installation-of-the-trusted-loader-and-patcher"></a>安裝受信任的載入器和 Patcher

受信任的載入器和 patcher 公用程式的基底版本應該安裝在 HDD 上的 [受保護的程式檔案] 資料夾底下，就像傳統安裝一樣。 安裝和修補載入器應用程式需要系統管理員許可權，因此請務必將載入器的更新頻率降到最低，以確保使用者不需要經常提高許可權，但 Windows Installer 限制的使用者修補可用來避免提高載入器修補程式的許可權。

請參閱 Windows XP、Windows Vista 和 Windows 7 中修補遊戲軟體的文章。

### <a name="installation-of-the-game-executables-dlls-and-data"></a>安裝遊戲可執行檔、Dll 和資料

若要在沒有系統管理許可權的情況下，協助標準使用者更新遊戲，必須將遊戲可執行檔、Dll 和資料安裝到可供所有使用者存取的硬碟區域。 作業系統提供「所有使用者應用程式資料」區域，可用來做為安裝的預設位置。 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 應該搭配 CSIDL \_ 一般 \_ APPDATA 索引鍵使用，以決定此區域的檔案路徑。 請勿對此金鑰傳回的路徑進行任何假設，因為它可能是使用者可設定的。

安裝必須改變或管理資料夾許可權，才能達到更新標題所需的所有使用者共用寫入存取權。 使用正確的許可權，載入器程式的遊戲更新程式功能可以輕鬆地修補遊戲，而不需要任何使用者帳戶的特殊許可權，包括標準使用者啟動時的時間。

### <a name="access-control-list-modification-code"></a>存取控制清單修改程式碼

針對 Windows XP，您將需要執行程式碼，以手動方式 (ACL) 變更存取控制清單，以下是示範如何執行這項作業的範例函數：

``` syntax
HRESULT ChangeACLtoAllowUserRW( WCHAR* strDir )
{
    EXPLICIT_ACCESS explicitaccess;
    PACL NewAcl = NULL;
    DWORD dwError;

    BuildExplicitAccessWithName( &explicitaccess, L"BUILTIN\\Users",
                                 GENERIC_ALL, GRANT_ACCESS,
                                 SUB_CONTAINERS_AND_OBJECTS_INHERIT );
                                 
    dwError = SetEntriesInAcl( 1, &explicitaccess, NULL, &NewAcl );
    if( dwError == ERROR_SUCCESS) 
    {
        dwError = SetNamedSecurityInfo( strDir, SE_FILE_OBJECT,
                                        DACL_SECURITY_INFORMATION,
                                        NULL, NULL, NewAcl, NULL );
        if( dwError == ERROR_SUCCESS)
        {
            if( NewAcl != NULL ) AccFree( NewAcl );
            return S_OK;
        }
    }

    if( NewAcl != NULL ) AccFree( NewAcl );
    return E_FAIL;
}
```

這個程式碼範例也適用于 Windows Vista 和 Windows 7;不過，它們也會提供命令列公用程式 icacls，以編輯您可以選擇改用的檔案 ACL。

不過，此工具會在執行時提供詳細的說明，此工具的其中一個範例使用方式為：

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

此使用方式會授與使用者 >rex 刪除和寫入 DAC 許可權至硬碟的所有使用者區域中所儲存的遊戲資料夾。

### <a name="installations-for-advanced-users"></a>Advanced Users 的安裝

針對先進的使用者安裝案例，使用者可能會想要手動指定遊戲安裝路徑。 目錄選取範圍應限制為程式檔之外的一個，以確保該資料夾位於硬碟的真正可共用區域中。 使用者選取的路徑應僅用於遊戲 exe 和資料，因為遊戲載入器和 Patcher exe 應該一律安裝在 [安全程式檔案] 資料夾下，以提升安全性。

### <a name="the-loaders-verification-of-trust"></a>載入器的信任驗證

Windows 提供檢查已簽署程式碼有效性的 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)函式，並以作業系統中的密碼編譯服務為基礎。 此函式完整記載于 MSDN： **WinVerifyTrust** 函數。

下列 MSDN 上的範例程式詳細說明如何使用函式來判斷程式可執行檔是否使用有效的憑證簽署： [範例 C 程式：驗證 PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)檔案的簽章。

為了確認已簽署的遊戲可執行檔可在載入器內執行，一般驗證動作將足夠：

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

WINTRUST \_ 動作 \_ 一般 \_ 驗證 \_ V2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>意義
</dt> <dd>

使用 Authenticode 原則提供者驗證檔案或物件。

</dd> </dl>

函數會採用輸入結構引數，其中包含信任提供者處理指定動作所需的資訊。 一般來說，如上述範例所示，結構所包含的資訊會識別信任提供者必須評估的物件。

結構的格式是特定于動作識別碼。 MSDN 上的下列主題詳細說明 WinTrust 提供者的範例結構： [**WinTrust \_ 資料**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) 結構。

如果信任提供者確認主體受限於指定的動作，則傳回值為零。 除了零以外的其他值都不應視為成功的傳回值。

### <a name="data-validation"></a>資料驗證

codesigning 機制只支援簽署一些特定類型的檔案，包括可執行檔、dll、Windows Installer 套件 (.msi 檔案) 以及封包 (.cab) 檔。 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) API 不應用來確認大型資料檔案 (.cab 檔案（例如) 尚未遭篡改），因為在驗證非常大型的檔案時，有一些效能和穩定性問題。 程式可執行檔通常很小，可使用 WinTrust 提供者進行完全信任檢查，但是遊戲的資料檔案通常是大小的 gb 範圍。 載入器用來驗證遊戲資料的方法，應該是在遊戲的執行時間測試資料集的小型樣本。 這種方法可將驗證測試的成本散佈在遊戲播放體驗的存留期內，並可提供順暢的使用者體驗，而不需要長時間等候。 為了達成此目的，您可能需要謹慎地組織資料。 有些 Mmog 採用資料庫方法來協助管理、維護及驗證一段時間的遊戲資產是否正確。

從安全性的觀點來看，用戶端程式代碼應該設計為不信任資料檔案，即使使用某種類型的基本資料驗證與受信任的載入器也一樣。 應該採用標頭檢查、雜湊和其他傳統的完整性檢查。 強化用戶端 i/o 程式碼的工作也應該使用模糊測試之類的技術來完成，以及利用自動靜態程式碼分析工具（例如 Visual Studio 2005 中的 **/analyze** 參數），以及 Windows SDK) 隨附的免費編譯器中的 Visual Studio 2008 Visual Studio (。

如需軟體安全性的詳細資訊，請參閱 [遊戲開發的最佳安全性作法](/windows/desktop/DxTechArts/best-security-practices-in-game-development)。

 

 