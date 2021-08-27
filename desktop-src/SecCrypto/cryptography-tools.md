---
description: 密碼編譯工具提供了命令列工具，可用於程式碼簽署、簽章驗證和其他密碼編譯工作。
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: 密碼編譯工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9547ba1d3a13958859c2f0504c60a1a1bbe4a67403c9709bb57900b73ad3a50d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100978"
---
# <a name="cryptography-tools"></a>密碼編譯工具

密碼編譯工具提供了命令列工具，可用於程式碼簽署、簽章驗證和其他密碼編譯工作。

## <a name="introduction-to-code-signing"></a>程式碼簽署簡介

軟體產業必須提供使用者信任程式碼的方法，包括在網際網路上發佈的程式碼。 許多網頁都只包含可下載的靜態資訊，而且幾乎沒有風險。 不過，有些頁面包含要在使用者電腦上下載及執行的控制項和應用程式。 這些可執行檔可能會有風險，可供下載和執行。

封裝的軟體使用商標與受信任的銷售輸出，確保使用者的完整性，但在網際網路上傳輸程式碼時無法使用這些保證。 此外，網際網路本身也無法提供軟體建立者身分識別的任何保證。 也不能保證下載的任何軟體在建立之後都不會改變。 瀏覽器可能會顯示警告訊息，說明下載任何種類資料的可能危險，但瀏覽器無法驗證程式代碼是否為其所宣稱的結果。 您必須採取更主動的方法，讓網際網路成為發佈軟體的可靠媒體。

有一種方法可保證檔案的真實性和 [*完整性*](../secgloss/i-gly.md) ，會將 [*數位簽章*](../secgloss/d-gly.md) 附加至這些檔案。 附加至檔案的數位簽章會以正確的身分識別該檔案的散發者，並確保建立簽章之後，檔案的內容不會變更。

您可以使用 Microsoft 的密碼編譯 Api 來建立和驗證數位簽章。 如需密碼編譯和 [*CryptoAPI*](../secgloss/c-gly.md) 函數的背景資訊，請參閱 [密碼編譯基本](cryptography-essentials.md)資訊。

如需 [*數位簽章*](../secgloss/d-gly.md)、 [*憑證*](../secgloss/c-gly.md)和 [*憑證存放區*](../secgloss/c-gly.md)的詳細資訊，請參閱下列主題：

-   [雜湊和數位簽章](hashes-and-digital-signatures.md)
-   [數位憑證](digital-certificates.md)
-   [使用憑證存放區管理憑證](managing-certificates-with-certificate-stores.md)
-   [憑證信任驗證](certificate-trust-verification.md)

目前，CryptoAPI 工具支援 Microsoft Authenticode 技術，方法是允許軟體廠商簽署下列類型的檔案進行 Authenticode 驗證。



| 副檔名                             | 目錄                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .appx<br/>                                | Windows 存放區裝置應用程式的安裝程式檔案。<br/>                                                                                                                                                                            |
| .cab<br/>                                 | 獨立檔案，用於應用程式安裝和設定。 在封包檔中，會將多個檔案壓縮成一個檔案。 它們通常位於 Microsoft 軟體散發磁片上。<br/>                        |
| .cat<br/>                                 | 檔案，其中包含數個檔案的數位 [*指紋*](../secgloss/t-gly.md) 。 .Cat 檔案可以用來確保其包含其指紋的檔案完整性。<br/> |
| .dll<br/>                                 | 包含可執行檔的檔案。<br/>                                                                                                                                                                                   |
| .exe<br/>                                 | 包含可執行程式的檔案。<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | 適用于 JScript 的 Windows shell 檔案或 Microsoft Visual Basic 腳本版本 (VBScript) 。<br/>                                                                                                                                    |
| .msi<br/> .msp<br/> .mst<br/> | Windows 安裝程式檔案。<br/>                                                                                                                                                                                                   |
| .ocx<br/>                                 | 包含 Microsoft ActiveX 控制項的檔案。<br/>                                                                                                                                                                             |
| .ps1<br/>                                 | 包含 PowerShell 腳本的檔案。<br/>                                                                                                                                                                                     |
| stl<br/>                                 | 包含 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 的檔案。<br/>                                                                           |
| .sys<br/>                                 | 包含驅動程式二進位檔的檔案。<br/>                                                                                                                                                                                        |



 

如需有關數位簽章的詳細資訊，請參閱下列檔：

-   CCITT、推薦的 x.509、 *Directory-Authentication 架構*、諮詢委員會、國際電話和電報、國際電信聯集、Geneva、1989。
-   RSA 實驗室、 *PKCS \# 7：密碼編譯訊息語法標準*。 1.5、11月、1993版。
-   Schneier、Bruce、套用的 *密碼* 編譯、2d ed。 紐約： John Wiley & 兒子，1996。
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> 這些資源可能無法在某些語言及國家/地區中使用。

 

## <a name="microsoft-cryptography-tools"></a>Microsoft 密碼編譯工具

發行工具和簽署 DLL 安裝在 \\ MICROSOFT SDK 安裝的 Bin 目錄中。 其中包含下列檔案。



| 檔案名稱                    | 備註                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | 建立 [*軟體 Publisher 憑證*](../secgloss/s-gly.md) (SPC) 僅供測試用途。<br/> |
| [CertMgr.exe](certmgr.md)   | )  (Crl 來管理憑證、Ctl 和 [*憑證撤銷清單*](../secgloss/c-gly.md) 。<br/>             |
| [MakeCat.exe](makecat.md)   | 建立未簽署的類別目錄檔案，其中包含一組檔案的雜湊以及每個檔案的相關屬性。<br/>                                                               |
| [MakeCert.exe](makecert.md) | 建立僅供測試用途的 [*x.509*](../secgloss/x-gly.md) 憑證。<br/>                                                                      |
| Pvk2pfx.exe                  | 將軟體發行者憑證檔案 ( .spc) 或私密金鑰檔案 (. pvk) 轉換成個人資訊 Exchange (PFX) 檔案格式。<br/>                                                   |
| [SetReg.exe](setreg.md)     | 設定控制憑證驗證的登錄機碼。<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | 簽署檔案並為其加上時間戳記。 此外，也會檢查檔案的簽章。<br/>                                                                                                              |



 

 

 
