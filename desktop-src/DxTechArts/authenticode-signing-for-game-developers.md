---
title: 遊戲開發人員的 Authenticode 簽署
description: 本文討論如何開始驗證您的遊戲，以及如何將驗證整合到每日組建流程。
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256b1cec0693787e76cfa479940524fca28d508e
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436453"
---
# <a name="authenticode-signing-for-game-developers"></a>遊戲開發人員的 Authenticode 簽署

對遊戲開發人員而言，資料驗證越來越重要。 WindowsVista 和 Windows 7 有一些功能（例如家長監護），這些功能都需要適當簽署遊戲，以確保沒有人會篡改資料。 Microsoft Authenticode 可讓終端使用者和作業系統驗證程式代碼來自正當擁有者，而且該程式碼未遭到惡意改變或意外損毀。 本文討論如何開始驗證您的遊戲，以及如何將驗證整合到每日組建流程。

-   [背景](#background)
-   [快速入門](#getting-started)
-   [使用受信任的憑證授權單位單位](#using-a-trusted-certificate-authority)
-   [使用測試憑證的範例](#example-using-a-test-certificate)
-   [將程式碼登入整合到每日組建系統](#integrating-code-signing-into-the-daily-build-system)
-   [撤銷](#revocation)
-   [程式碼簽署驅動程式](#code-signing-drivers)
-   [總結](#summary)
-   [詳細資訊](#more-information)

> [!Note]  
> 自2016年1月1日起，Windows 7 和更新版本不再信任到期日為2016或更新版本的任何 sha-1 程式碼簽署憑證。 如需詳細資訊，請參閱[Windows Authenticode 程式碼簽署和時間戳記的強制執行](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx)。

 

## <a name="background"></a>背景

數位憑證是用來建立作者的身分識別。 數位憑證是由信任的協力廠商（稱為憑證授權單位單位 (CA) ，例如 VeriSign 或 Thawte）發行。 CA 負責確認擁有者不會宣告錯誤識別。 將憑證套用至憑證的 CA 之後，商業開發人員在兩周內都能預期對其應用程式的回應。

在 CA 決定符合其原則準則之後，它會產生符合 x.509 的程式碼簽署憑證，該憑證格式符合國際電信聯集所建立的產業標準憑證格式（含第3版延伸模組）。 此憑證會識別您的公開金鑰並包含公開金鑰。 它是由 CA 儲存以供參考，並以電子方式提供複本給您。 同時，您也可以建立私用金鑰，而您必須保持安全，且不能與任何人共用，即使是 CA 也一樣。

擁有公開和私密金鑰之後，您就可以開始散發已簽署的軟體。 Microsoft 提供在 Windows SDK 中進行這項作業的工具。 這些工具會使用單向雜湊、產生固定長度的摘要，並使用私密金鑰產生加密簽章。 然後，他們會將該加密簽章與您的憑證和認證合併成一個稱為簽章區塊的結構，並將它內嵌到可執行檔的檔案格式中。 可以簽署任何類型的可執行二進位檔案，包括 Dll、可執行檔和封包檔。

您可以透過多種方式來驗證簽章。 程式可以呼叫 CertVerifyCertificateChainPolicy 函式，而 SignTool (signtool.exe) 可以用來從命令提示字元驗證簽章。 WindowsExplorer 在 [檔案屬性] 中也有 [數位簽章] 索引標籤，可顯示已簽署之二進位檔案的每個憑證。  (數位簽章] 索引標籤只會出現在已簽署檔案的檔案屬性中 ) 。此外，您也可以使用 [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy)，自行驗證應用程式。

Authenticode 簽章不僅適用于使用者所進行的資料驗證，也需要用於修補受限的使用者帳戶以及 Windows Vista 和 Windows 7 中的家長監護。 此外，Windows 作業系統中的未來技術也可能需要簽署程式碼，因此強烈建議所有 professional 和總是業餘開發人員從 CA 取得程式碼簽署憑證。 如需如何完成此操作的詳細資訊，請參閱本文稍後 [使用受信任的憑證授權單位](#using-a-trusted-certificate-authority)單位。

遊戲程式碼、patchers 和安裝程式可透過驗證程式代碼中的檔案是否為真，進一步利用 Authenticode 簽署。 這可用於反相關和一般網路安全性。 檢查檔案是否已簽署的範例程式碼，可以在這裡找到： [範例 C 程式：驗證 PE 檔案的](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)簽章，以及在已簽署檔案上檢查簽署憑證擁有權的範例程式碼： [如何從 Authenticode 簽署的可執行檔取得資訊](https://support.microsoft.com/kb/323809)。

## <a name="getting-started"></a>開始使用

為了開始使用，Microsoft 提供了 Visual Studio 2005 和 Visual Studio 2008，以及[Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)中的工具，可協助您執行及驗證程式代碼簽署程式。 安裝 Visual Studio 或 Windows SDK 之後，此技術檔中所述的工具位於安裝的子目錄中，其中可能包含下列一或多個專案：

-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 8 \\ SDK v2.0 \\ \\ Bin
-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 8 \\ VC \\ PlatformSDK \\ Bin
-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 9.0 \\ SmartDevices \\ SDK \\ SDKTools\\
-   % SystemDrive% \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 a \\ bin\\

下列工具最適合用於簽署程式碼：

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>憑證建立工具 (MakeCert.exe) 
</dt> <dd>

將 x.509 憑證以 .cer 檔案的形式產生，該檔案包含您的公開金鑰和私密金鑰（pvk 檔案）。 此憑證僅供內部測試之用，無法公開使用。

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

從一對 .cer 和 pvk 檔案建立個人資訊 Exchange ( .pfx) 檔。 .Pfx 檔案包含您的公開和私密金鑰。

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe) 
</dt> <dd>

使用 .pfx 檔案來簽署檔案。 SignTool 支援簽署 DLL 檔案、可執行檔、Windows Installer (.msi) 檔和封包 (.cab) 檔。

</dd> </dl>

> [!Note]  
> 閱讀其他檔時，您可能會找到 Signcode.exe (SignCode.exe) 的參考，但這項工具已淘汰且不再支援，請改用 SignTool。

 

## <a name="using-a-trusted-certificate-authority"></a>使用受信任的憑證授權單位單位

若要取得受信任的憑證，您必須將 (CA) 的憑證授權單位單位（例如 VeriSign 或 Thawte）套用至憑證授權單位單位。 Microsoft 不建議使用任何 CA，但如果您想要整合至 Windows 錯誤報告 (WER) 服務，您應該考慮使用 verisign 來發出憑證，因為存取 WER 資料庫需要 WinQual 帳戶，需要 VeriSign 識別碼。 如需信任的協力廠商憑證授權單位單位的完整清單，請參閱 [Microsoft 根憑證計畫成員](/previous-versions/ms995347(v=msdn.10))。 如需使用 WER 註冊的詳細資訊，請參閱[ISV 區域](https://msdn.microsoft.com/)中的「[簡介 Windows 錯誤報告](https://msdn.microsoft.com/)」。

當您收到來自 CA 的憑證之後，您可以使用 SignTool 簽署您的程式，並將您的程式發行至公用。 不過，您必須小心保護您的私密金鑰，這是包含在 .pfx 和 pvk 檔案中的金鑰。 請務必將這些檔案保存在安全的位置。

## <a name="example-using-a-test-certificate"></a>使用測試憑證的範例

下列步驟將示範如何建立程式碼簽署憑證以供測試之用，然後使用此測試憑證來簽署 Direct3D 範例程式 (呼叫 BasicHLSL.exe) 。 此程式會建立 .cer 和 pvk 檔案（分別是您的公開和私密金鑰），這些檔案不能用於公開認證。

在此範例中，也會將時間戳記加入簽章。 時間戳記會在憑證過期時防止簽章變成無效。 簽署但缺少時間戳記的程式碼將不會在憑證到期後進行驗證。 因此，所有公開發行的程式碼都應該有時間戳記。

**建立憑證並簽署程式**

1.  使用 (MakeCert.exe) 的憑證建立工具建立測試憑證和私密金鑰。

    下列命令列範例會將 MyPrivateKey 指定為私密金鑰的檔案名 (. pvk) file、MyPublicKey 作為憑證的檔案名 ( .cer) 檔和 MySoftwareCompany 作為憑證的名稱。 它也會讓憑證自我簽署，使其不受信任的根授權單位。

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  從您的私密金鑰建立個人資訊 Exchange ( .pfx) 檔案 (. 使用) pvk ( 檔案和憑證) .cer pvk2pfx.exe 檔案。

    .Pfx 檔案會將您的公開金鑰和私密金鑰合併成單一檔案。 下列命令列範例會使用來自上一個步驟的 pvk 和 .cer 檔案，以密碼來建立名為 MyPFX 的 .pfx 檔案 \_ ：

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  使用 SignTool 將您的個人資訊 Exchange ( .pfx) 檔簽署您的程式。

    您可以在命令列上指定數個選項。 下列命令列範例會使用來自上一個步驟的 .pfx 檔案、將您 \_ 的密碼指定為密碼、將 BasicHLSL 指定為要簽署的檔案，以及從指定的伺服器抓取時間戳記：

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > 時間戳記服務的 URL 是由 CA 提供，而且是選擇性的，可供測試。 生產簽章必須包含有效的時間戳記授權單位，否則簽章將無法在憑證到期時進行驗證。

     

4.  確認程式是使用 SignTool 簽署的。

    下列命令列範例指定 SignTool 應該嘗試使用所有可用的方法來驗證 BasicHLSL.exe 上的簽章，同時提供詳細資訊輸出：

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    在此範例中，SignTool 應該指出憑證已附加，同時也指出它不受信任，因為它不是由 CA 所發行。

5.  信任測試憑證。

    針對測試憑證，您需要信任該憑證。 您應略過 CA 提供的憑證的這個步驟，因為這些憑證會預設為受信任。

    在您想要信任測試憑證的電腦上，執行下列動作：

    ```
    certmgr.msc
    ```

    

    然後以滑鼠右鍵按一下 [信任的根憑證授權單位]，然後選擇 [所有工作匯 \| 入] 然後，流覽至您建立的 .pfx 檔案，然後依照嚮導步驟，將憑證放在受信任的根憑證授權單位中。

    當嚮導完成時，您可以使用該電腦上的受信任憑證來開始測試。

## <a name="integrating-code-signing-into-the-daily-build-system"></a>將程式碼登入整合到每日組建系統

若要將程式碼登入至專案，您可以建立批次檔或腳本來執行命令列工具。 建立專案之後，請使用適當的設定執行 SignTool， (如範例) 的步驟3所示。

在您的組建程式中特別謹慎，以確保 .pfx 和 pvk 檔案的存取限制為最少的電腦和使用者。 最佳做法是，開發人員只應使用測試憑證來簽署程式碼，直到準備好寄送。 同樣地，私密金鑰 ( pvk) 應該保留在安全的位置，例如安全或鎖定的空間，而且在理想的情況下，像是智慧卡。

使用 Microsoft Authenticode 來簽署 Windows Installer (MSI) 封裝本身，以提供另一層保護。 這有助於防止 MSI 套件遭受篡改和意外損毀。 如需如何使用 Authenticode 簽署套件的詳細資訊，請參閱 MSI 建立工具的檔。

## <a name="revocation"></a>撤銷

如果私密金鑰的安全性遭到入侵，或某些安全性相關事件呈現 Code-Signing 憑證無效，則開發人員必須撤銷憑證。 這樣做會降低開發人員的完整性和簽署程式碼的效率。 CA 也可以發出特定時間的撤銷;在撤銷時間之前使用時間戳簽署的程式碼仍會被視為有效，但是具有後續時間戳記的程式碼將會無效。 憑證撤銷會影響任何以已撤銷的憑證簽署之應用程式中的程式碼。

## <a name="code-signing-drivers"></a>Code-Signing 驅動程式

驅動程式可以而且應該是 Authenticode 簽署的。 核心模式驅動程式有其他需求：64位版本的 Windows Vista 和 Windows 7 會防止安裝所有未簽署的核心模式驅動程式，而當使用者嘗試安裝未簽署的驅動程式時，所有的 Windows 版本都會出現警告提示。 此外，系統管理員可以設定群組原則，以防止未簽署的驅動程式安裝在 Microsoft Windows Server 2003、Windows XP Professional x64 Edition 和32位版本的 Windows Vista 和 Windows 7。

許多類型的驅動程式都可以使用 Microsoft 信任的簽章進行簽署，這是[Windows 硬體品質實驗室](https://www.microsoft.com/whdc/whql/) (WHQL) 或非分類的簽章[程式](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (先前命名為驅動程式可靠性簽章) 的 Windows 認證方案的一部分，可讓系統完全信任這些驅動程式，並在沒有系統管理認證的情況下安裝它們。

驅動程式至少應該是 Authenticode 簽署的，因為未經簽署或自我簽署 (的驅動程式（使用測試憑證) 簽署）將無法安裝在許多以 Windows 為基礎的平臺上。 如需有關簽署驅動程式和程式碼和相關功能的詳細資訊，請參閱[Windows 硬體開發人員中心](https://www.microsoft.com/whdc/)上[Windows 的驅動程式簽署需求](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx)。

## <a name="summary"></a>總結

使用 Microsoft Authenticode 是相當簡單的流程。 一旦取得 CER 並建立私密金鑰之後，就可以使用 Microsoft 所提供的工具，簡單明瞭。 然後，您可以在 Windows Vista 和 Windows 7 （例如家長監護）中啟用重要功能，並讓客戶知道您的產品直接來自其正當擁有者。

## <a name="more-information"></a>詳細資訊

如需有關與簽署程式碼相關之工具和程式的詳細資訊，請參閱下列連結：

-   [密碼編譯工具](/windows/desktop/SecCrypto/cryptography-tools)
-   [加密 API 工具參考](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Authenticode 總覽和 Turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [數位憑證](/windows/desktop/SecCrypto/digital-certificates)
-   [部署 Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [如何：建立要在開發期間使用的暫時憑證](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 
