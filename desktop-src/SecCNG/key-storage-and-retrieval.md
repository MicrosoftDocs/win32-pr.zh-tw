---
description: CNG 提供私密金鑰儲存的模型，可讓您根據目前和未來建立使用加密功能（例如公用或私密金鑰加密）的應用程式，以及儲存金鑰資料的需求。
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: 金鑰儲存體和抓取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b2100f005f0ff293e34a3f4c0a7460b7a4d4e9c2b15fbe0b3577b5e52394a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907681"
---
# <a name="key-storage-and-retrieval"></a>金鑰儲存體和抓取

-   [主要儲存體架構](#key-storage-architecture)
-   [金鑰類型](#key-types)
-   [支援的演算法](#supported-algorithms)
-   [金鑰目錄和檔案](#key-directories-and-files)

## <a name="key-storage-architecture"></a>主要儲存體架構

CNG 提供私密金鑰儲存的模型，可讓您根據目前和未來建立使用加密功能（例如公用或私密金鑰加密）的應用程式，以及儲存金鑰資料的需求。 金鑰儲存路由器是此模型中的中央常式，並在 Ncrypt.dll 中執行。 應用程式會透過金鑰儲存路由器 (在系統上 Ksp) 來存取金鑰儲存提供者，這會從應用程式和存放裝置提供者本身隱藏詳細資料，例如金鑰隔離。 下圖顯示 CNG 金鑰隔離架構的設計和功能。

![cng 金鑰儲存提供者](images/cng-key-storage-provider.png)

為了符合 (CC) 需求的通用準則，必須隔離長時間的金鑰，使其永遠不會出現在應用程式進程中。 CNG 目前支援使用隨附于 Windows Server 2008 和 Windows Vista 的 Microsoft 軟體 KSP 來儲存非對稱私密金鑰，並預設安裝。

預設會啟用 Windows Server 2008 和 Windows Vista 中的金鑰隔離。 在這些平臺之前，您無法在平臺上使用金鑰隔離功能。 此外，協力廠商 Ksp 不會載入 (LSA 進程) 的金鑰隔離服務中。 只有 Microsoft KSP 會在金鑰隔離服務中載入。

LSA 處理常式是用來將效能最大化的金鑰隔離程式。 私密金鑰的所有存取都是透過金鑰儲存路由器，它會公開一組完整的功能來管理和使用私密金鑰。

CNG 會將預存金鑰的公開部分與私用部分分開儲存。 金鑰組的公開部分也會在金鑰隔離服務中維護，並且使用本機遠端程序呼叫 (LRPC) 來存取。 在呼叫金鑰隔離程式時，金鑰儲存路由器會使用 LRPC。 私密金鑰的所有存取都是透過私密金鑰路由器，並且由 CNG 進行審核。

如上所述，您可以支援各種不同的硬體儲存體裝置。 在每個案例中，所有這些儲存裝置的介面都相同。 它包含執行各種私密金鑰作業的函式，以及與金鑰儲存和管理相關的功能。

CNG 提供一組 Api，可用來建立、儲存和取出密碼編譯金鑰。 如需這些 Api 的清單，請參閱[CNG 金鑰儲存體](cng-key-storage-functions.md)函式。

## <a name="key-types"></a>索引鍵類型

CNG 支援下列金鑰類型：

-   Diffie-Hellman 公開和私密金鑰。
-   數位簽章演算法 (DSA、FIPS 186-2) 公開和私密金鑰。
-   RSA (PKCS \# 1) 公開和私密金鑰。
-   有幾個舊版 (CryptoAPI) 公開和私用金鑰。
-   橢圓曲線密碼編譯公用和私密金鑰。

## <a name="supported-algorithms"></a>支援的演算法

CNG 支援下列金鑰演算法。

| 演算法 | 金鑰/雜湊長度 (位)              |
|-----------|------------------------------------|
| RSA       | 512至16384，以64位遞增 |
| DH        | 512至16384，以64位遞增 |
| DSA       | 512至1024，以64位遞增  |
| ECDSA     | P-256、P-384、P-521 (NIST 曲線)   |
| ECDH      | P-256、P-384、P-521 (NIST 曲線)   |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>金鑰目錄和檔案

Microsoft 舊版 CryptoAPI Csp 將私密金鑰儲存在下列目錄中。

| 金鑰類型                | 目錄                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 使用者私用            | % APPDATA% \\ Microsoft \\ 加密 \\ RSA \\ *使用者 SID*\\<br/>% APPDATA% \\ Microsoft \\ 加密 \\ DSS \\ *使用者 SID*\\<br/>                                                   |
| 本機系統私用    | % ALLUSERSPROFILE% \\ 應用程式資料 \\ Microsoft \\ 加密 \\ RSA \\ S-1-5-18\\<br/>% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ DSS \\ S-1-5-18\\<br/>   |
| 本機服務私用   | % ALLUSERSPROFILE% \\ 應用程式資料 \\ Microsoft \\ 加密 \\ RSA \\ S-1-5-19\\<br/>% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ DSS \\ S-1-5-19\\<br/>   |
| 網路服務私用 | % ALLUSERSPROFILE% \\ 應用程式資料 \\ Microsoft \\ 加密 \\ RSA \\ S-1-5-20\\<br/>% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ DSS \\ S-1-5-20\\<br/>   |
| 共用私用          | % ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ RSA \\ MachineKeys<br/>% ALLUSERSPROFILE% \\ \\ Microsoft \\ 加密 \\ DSS \\ MachineKeys 的應用程式資料<br/> |



 

CNG 將私密金鑰儲存在下列目錄中。

| 金鑰類型                | 目錄                                                          |
|-------------------------|--------------------------------------------------------------------|
| 使用者私用            | % APPDATA% \\ Microsoft \\ 加密 \\ 金鑰                                 |
| 本機系統私用    | % ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ SystemKeys |
| 本機服務私用   | % WINDIR% \\ ServiceProfiles \\ LocalService                            |
| 網路服務私用 | % WINDIR% \\ ServiceProfiles \\ NetworkService                          |
| 共用私用          | % ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ 金鑰       |



 

以下是 CryptoAPI 和 CNG 金鑰容器之間的一些差異。

-   CNG 使用的金鑰檔名稱，與 Rsaenh.dll 和 Dssenh.dll 舊版 Csp 所建立的金鑰檔不同。 舊版金鑰檔的副檔名也是副檔名，但是 CNG 金鑰檔沒有副檔名。
-   CNG 完全支援 Unicode 金鑰容器名稱;CNG 使用 Unicode 容器名稱的雜湊，而 CryptoAPI 則使用 ANSI 容器名稱的雜湊。
-   CNG 對於 RSA 金鑰組有更大的彈性。 例如，CNG 支援大於32位的公用指數長度，並支援 p 和 q 的長度不同的索引鍵。
-   在 CryptoAPI 中，金鑰容器檔案儲存在目錄中，其名稱是與使用者 SID 相等的文字。 這不再是 CNG 中的情況，因此不會遺失所有私用金鑰，因而免除將使用者從某個網域移到另一個網域的困難。
-   CNG KSP 和金鑰名稱會限制為 **最大 \_ 路徑** Unicode 字元。 CryptoAPI CSP 和金鑰名稱會限制為 **最大 \_ 路徑** ANSI 字元。
-   CNG 提供使用者定義索引鍵屬性的功能。 使用者可以建立自訂屬性並將其與金鑰建立關聯，並以保存的金鑰儲存它們。

保存金鑰時，CNG 可以建立兩個檔案。 第一個檔案包含新的 CNG 格式的私密金鑰，而且一律會建立此金鑰。 舊版 CryptoAPI Csp 無法使用這個檔案。 第二個檔案包含舊版 CryptoAPI 金鑰容器中的相同私密金鑰。 第二個檔案符合 Rsaenh.dll 所使用的格式和位置。 當呼叫 [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey)函式來完成 RSA 金鑰時，如果指定了 **NCRYPT \_ 寫入 \_ 金鑰 \_ 至 \_ 舊版 \_ 存放區 \_ 旗** 標旗標，就會建立第二個檔案。 這項功能不支援 DSA 和 DH 金鑰。

當應用程式嘗試開啟現有的保存金鑰時，CNG 會先嘗試開啟原生的 CNG 檔。 如果此檔案不存在，則 CNG 會嘗試在舊版 CryptoAPI 金鑰容器中找出相符的金鑰。

當您從來源電腦移動或複製 CryptoAPI 金鑰至具有 Windows 消費者狀態移轉工具 (USMT) 的目的電腦時，CNG 將無法存取目的電腦上的金鑰。 若要存取這類已遷移的金鑰，您必須使用 CryptoAPI。

 

 




