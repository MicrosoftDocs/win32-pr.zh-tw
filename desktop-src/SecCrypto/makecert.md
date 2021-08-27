---
description: 建立由測試根目錄金鑰或其他指定的金鑰簽署的 x.509 憑證，以將您的名稱系結至金鑰組的公開部分。 憑證會儲存至檔案、系統憑證存放區或兩者。
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff9fb79b5db5a6a71eee981166742b4e1680184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471924"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> MakeCert 已被取代。 若要建立自我簽署憑證，請使用 Powershell Cmdlet [New-new-selfsignedcertificate](/powershell/module/pki/new-selfsignedcertificate)。

 

MakeCert 工具會建立由測試根目錄金鑰或其他指定的機碼簽署的 [*x.509*](../secgloss/x-gly.md) 憑證，以將您的名稱系結至金鑰組的公開部分。 憑證會儲存至檔案、系統憑證存放區或兩者。 此工具會安裝在 \\ Microsoft Windows 軟體開發套件 (SDK) 安裝路徑的 Bin 資料夾中。

MakeCert 工具會使用下列命令語法：

**MakeCert** \[*BasicOptions* \|*ExtendedOptions* \]*OutputFile*

*OutputFile* 是將寫入憑證的檔案名。 如果憑證不是寫入檔案，您可以省略 *OutputFile* 。

## <a name="options"></a>選項

MakeCert 包含基本和擴充的選項。 基本選項是最常用來建立憑證的選項。 擴充選項則提供更多彈性。

MakeCert 的選項也可以分為三個功能群組：

-   僅限憑證存放區技術專用的基本選項。
-   僅限 SPC 檔案和私密金鑰技術專用的擴充選項。
-   適用于 SPC 檔案、私密金鑰和憑證存放區技術的擴充選項。

下表中提供的選項只可用於 Internet Explorer 4.0 或更新版本。




| 基本選項 | Description | 
|--------------|-------------|
| <strong>-a</strong> <strong></strong><em>演算法</em> | <a href="/windows/desktop/SecGloss/h-gly"><em>雜湊</em></a> 演算法。 必須設定為 <strong>sha-1</strong> 或 <strong>MD5</strong> (預設) 。 如需 MD5 的詳細資訊，請參閱 <a href="/windows/desktop/SecGloss/m-gly"><em>md5</em></a>。 | 
| <strong>-b</strong> <strong></strong><em>DateStart</em> | 憑證首次生效的日期。 預設值為建立憑證的時間。 <em>DateStart</em>的格式為 mm/dd/yyyy。 | 
| <strong>-cy</strong> <strong></strong><em>CertificateTypes</em> | 憑證類型。 <em>CertificateTypes</em> <strong>可用於終端</strong>實體或<a href="/windows/desktop/SecGloss/c-gly"><em>憑證授權單位</em></a>單位的<strong>授權</strong>單位。 | 
| <strong>-e</strong> <strong></strong><em>DateEnd</em> | 有效期間結束的日期。 預設值為2039年。 | 
| <strong>-eku</strong> <strong></strong><em>OID1</em><strong>、</strong><em>OID2</em> .。。 | 將一或多個以逗號分隔、<a href="/windows/desktop/SecGloss/e-gly"><em>增強金鑰使用</em></a>方法<a href="/windows/desktop/SecGloss/o-gly"><em>物件識別碼</em></a>的清單插入憑證 (oid) 。 例如， <strong>-eku 1.3.6.1.5.5.7.3.2</strong> 會插入用戶端驗證 OID。 如需允許 Oid 的定義，請參閱 CryptoAPI 2.0 中的 Wincrypt .h 檔案。 | 
| <strong>-h</strong> <strong></strong><em>NumChildren</em> | 此憑證下的樹狀結構最大高度。 | 
| <strong>-l</strong> <strong></strong><em>PolicyLink</em> | 與 SPC 機構原則資訊的連結 (例如，URL) 。 | 
| <strong>-m</strong> <strong></strong><em>nMonths</em> | 有效期間的持續時間。 | 
| <strong>-n</strong><strong>"</strong><em>Name</em><strong>"</strong> | 發行者憑證的名稱。 這個名稱必須符合 <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> 標準。 最簡單的方法是使用 "CN =<em>MyName</em>" 格式。 例如： <strong>-n "CN = Test"</strong>。 | 
| <strong>-nscp</strong> | 應包含 Netscape 用戶端驗證延伸模組。 | 
| <strong>-pe</strong> | 將私密金鑰標記為可匯出。 | 
| <strong>-r</strong> | 建立自我簽署憑證。 | 
| <strong>-sc</strong> <strong></strong><em>SubjectCertFile</em> | 包含要使用之現有主體公開金鑰的憑證檔案名。 | 
| <strong>-sk</strong> <strong></strong><em>SubjectKey</em> | 保存 <a href="/windows/desktop/SecGloss/p-gly"><em>私密金鑰</em></a>之主體金鑰容器的位置。 如果金鑰容器不存在，便會建立一個。 如果不使用 <strong>-sk</strong> 或 <strong>-sv</strong> 選項，預設會建立預設的金鑰容器並使用。 | 
| <strong>-天空</strong> <strong></strong><em>SubjectKeySpec</em> | 主體的金鑰規格。 <em>SubjectKeySpec</em> 必須是三個可能值的其中一個：<br /><ul><li>簽章 (AT_SIGNATURE 機<strong>碼</strong>規格) </li><li><strong>Exchange</strong> (AT_KEYEXCHANGE 金鑰規格) </li><li>整數，例如<strong>3</strong> 。</li></ul>如需詳細資訊，請參閱此表格後面的附注。<br /> | 
| <strong>-sp</strong> <strong></strong><em>SubjectProviderName</em> | Subject 的 CryptoAPI 提供者。 預設值是使用者的提供者。 如需 CryptoAPI 提供者的詳細資訊，請參閱 CryptoAPI 2.0 檔。 | 
| <strong>-sr</strong> <strong></strong><em>SubjectCertStoreLocation</em> | 主體憑證存放區的登錄位置。 <em>SubjectCertStoreLocation</em> 必須是 <strong>LocalMachine</strong> (登錄機碼 HKEY_LOCAL_MACHINE) 或 <strong>CurrentUser</strong> (登錄機碼 HKEY_CURRENT_USER) 。 預設值為<strong>CurrentUser</strong> 。 | 
| <strong>-ss</strong> <strong></strong><em>SubjectCertStoreName</em> | 將儲存所產生之憑證的主體憑證存放區名稱。 | 
| <strong>-sv</strong> <strong></strong><em>SubjectKeyFile</em> | 主體 pvk 檔案的名稱。 如果不使用 <strong>-sk</strong> 或 <strong>-sv</strong> 選項，預設會建立預設的金鑰容器並使用。 | 
| <strong>-sy</strong> <strong></strong><em>nSubjectProviderType</em> | Subject 的 CryptoAPI 提供者類型。 預設值為 <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>。 如需 CryptoAPI 提供者類型的詳細資訊，請參閱 CryptoAPI 2.0 檔。 | 
| <strong>-#</strong><strong></strong><em>SerialNumber</em> | 憑證的序號。 最大值為 2 ^ 31。 預設值是工具所產生的值，這個值保證是唯一的。 | 
| <strong>-$</strong><strong></strong><em>CertificateAuthority</em> | <a href="/windows/desktop/SecGloss/c-gly"><em>憑證授權單位</em></a>單位的類型。 <em>CertificateAuthority</em> 必須設定為 <strong>商業 (，才能讓商務軟體</strong> 發行者) 或個別軟體發行者) 使用憑證的 <strong>個別</strong> (。 | 
| <strong>-?</strong> | 顯示基本選項。 | 
| <strong>-!</strong> | 顯示擴充的選項。 | 




 

> [!Note]  
> 如果 Internet Explorer 4.0 版或更新版本中使用 **-天空** 金鑰規格選項，則規格必須符合 [*私密金鑰*](../secgloss/p-gly.md) 檔案或私密金鑰 [*容器*](../secgloss/k-gly.md)所指出的金鑰規格。 如果未使用金鑰規格選項，將會使用私密金鑰檔案或私密金鑰容器所指出的金鑰規格。 如果金鑰容器中有一個以上的金鑰規格，MakeCert 會先嘗試使用 AT \_ SIGNATURE key 規格。 如果失敗，MakeCert 會嘗試在 KEYEXCHANGE 中使用 \_ 。 因為大部分的使用者都有 AT \_ SIGNATURE key 或 at \_ KEYEXCHANGE 索引鍵，所以在大部分情況下都不需要使用此選項。

 

下列選項僅適用于 [*軟體 Publisher 憑證*](../secgloss/s-gly.md) (SPC) 檔案和私密金鑰技術。




| SPC 和私用金鑰選項 | Description | 
|----------------------------|-------------|
| <strong>-ic</strong> <strong></strong><em>IssuerCertFile</em> | 簽發者憑證的位置。 | 
| <strong>-ik</strong> <strong></strong><em>IssuerKey</em> | 簽發者金鑰容器的位置。 預設值為測試根目錄金鑰。 | 
| <strong>-iky</strong> <strong></strong><em>IssuerKeySpec</em> | 簽發者的金鑰規格，其必須是三個可能值的其中一個：<br /><ul><li>簽章 (AT_SIGNATURE 機<strong>碼</strong>規格) </li><li><strong>Exchange</strong> (AT_KEYEXCHANGE 金鑰規格) </li><li>整數，例如<strong>3</strong> 。</li></ul>如需詳細資訊，請參閱此表格後面的附注。<br /> | 
| <strong>-ip</strong> <strong></strong><em>IssuerProviderName</em> | 簽發者的 CryptoAPI 提供者。 預設值是使用者的提供者。 如需 CryptoAPI 提供者的詳細資訊，請參閱 CryptoAPI 2.0 檔。 | 
| <strong>-iv</strong> <strong></strong><em>IssuerKeyFile</em> | 簽發者的私密金鑰檔案。 預設值是測試根目錄。 | 
| <strong>-iy</strong> <strong></strong><em>nIssuerProviderType</em> | 簽發者的 CryptoAPI 提供者類型。 預設值為 <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>。 如需 CryptoAPI 提供者類型的詳細資訊，請參閱 CryptoAPI 2.0 檔。 | 




 

> [!Note]  
> 如果 Internet Explorer 4.0 或更新版本中使用 **-iky** 金鑰規格選項，則規格必須符合 [*私密金鑰*](../secgloss/p-gly.md) 檔案或私密金鑰 [*容器*](../secgloss/k-gly.md)所指出的金鑰規格。 如果未使用金鑰規格選項，將會使用私密金鑰檔案或私密金鑰容器所指出的金鑰規格。 如果金鑰容器中有一個以上的金鑰規格，MakeCert 會先嘗試使用 AT \_ SIGNATURE key 規格。 如果失敗，MakeCert 會嘗試在 KEYEXCHANGE 中使用 \_ 。 因為大部分的使用者都有 AT \_ SIGNATURE key 或 at \_ KEYEXCHANGE 索引鍵，所以在大部分情況下都不需要使用此選項。

 

下列選項僅適用于 [*憑證存放區*](../secgloss/c-gly.md) 技術。



| 憑證存放區選項          | Description                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-ic** *IssuerCertFile*          | 包含簽發者憑證的檔案。 MakeCert 會在憑證存放區中搜尋完全相符的憑證。                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | 簽發者憑證的一般名稱。 MakeCert 會在憑證存放區中搜尋一般名稱包含 *IssuerNameString* 的憑證。                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | 簽發者憑證存放區的登錄位置。 *IssuerCertStoreLocation* 必須是 **LocalMachine** (登錄機碼 HKEY \_ 本機 \_ 電腦) 或 **CurrentUser** (登錄機碼 HKEY \_ 目前 \_ 的使用者) 。 預設值為 **CurrentUser** 。                                                                                                |
| **-是** *IssuerCertStoreName*     | 簽發者的憑證存放區，其中包含簽發者的憑證及其相關聯的私密金鑰資訊。 如果存放區中有一個以上的憑證，則使用者必須使用 **-ic** 或 **-in** 選項來唯一識別它。 如果憑證存放區中的憑證無法唯一識別，MakeCert 將會失敗。 |



 

 

 
