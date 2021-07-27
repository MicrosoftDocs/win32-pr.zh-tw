---
title: SignTool
description: SignTool 是一種命令列工具，可數位簽署檔案、驗證檔案中的簽章，以及時間戳記檔案。
ms.assetid: aa59cb35-5fba-4ce8-97ea-fc767c83f88e
ms.topic: article
ms.date: 10/12/2020
ms.openlocfilehash: f738eddb6e47da12297bffd13a816398ba2c46c9
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436443"
---
# <a name="signtool"></a>SignTool

SignTool 是一種命令列工具，可數位簽署檔案、驗證檔案中的簽章，以及時間戳記檔案。 如需有關為什麼簽署檔案很重要的詳細資訊，請參閱程式 [代碼簽署簡介](cryptography-tools.md)。 此工具會安裝在 \\ Microsoft Windows 軟體開發套件 (SDK) 安裝路徑的 Bin 資料夾中 (範例： C:\Program Files (x86) \ Windows Kits\10\bin\10.0.19041.0\x64\signtool.exe) 。

SignTool 可做為 Windows SDK 的一部分，可供您下載 <https://developer.microsoft.com/windows/downloads/windows-10-sdk/> 。

> [!Note]  
> Windows 10 SDK、Windows 10 的 HLK、Windows 10 WDK 和 Windows 10 ADK **組建20236和更新版本** 現在都需要指定摘要演算法。 SignTool sign 命令需要在 `file digest algorithm` `timestamp digest algorithm` 簽署和時間戳記期間分別指定/fd 和/td 選項。 警告 (錯誤碼0，如果在簽署期間未指定/fd，而且在時間戳記期間未指定/td，則會擲回) 。 在 SignTool 的較新版本中，警告會變成錯誤。 建議您將 SHA256 視為比產業的 SHA1 更安全。  


## <a name="syntax"></a>語法  
  
```console  
signtool [command] [options] [file_name | ...]  
```  

## <a name="parameters"></a>參數  
  
|引數|描述|  
|----|----|  
|`command`|四個命令之一 (`catdb`、`sign`、`Timestamp` 或 `Verify`)，指定要對檔案執行的操作。 如需每個命令的描述，請參閱下一個表格。|  
|`options`|修改命令的選項。 除了全域 `/q` 和 `/v` 選項外，每個命令支援一組唯一的選項。|  
|`file_name`|要簽署之檔案的路徑。| 


SignTool 支援下列命令。

|命令|描述|  
|----|----|  
|`Catdb`|在目錄資料庫中加入或移除目錄檔。 目錄資料庫可以用來自動查閱目錄檔，並且是由 GUID 所識別。 如需 `catdb` 命令支援選項的清單，請參閱 [catdb 命令選項](/dotnet/framework/tools/signtool-exe#catdb-command-options)。|  
|`Sign`|數位簽署檔案。 數位簽章可以防止檔案遭到篡改，而且可讓使用者根據簽署憑證確認簽署者。 如需 `sign` 命令支援選項的清單，請參閱 [sign 命令選項](/dotnet/framework/tools/signtool-exe#sign-command-options)。|  
|`Timestamp`|為檔案加上時間戳記。 如需 `TimeStamp` 命令支援選項的清單，請參閱 [TimeStamp 命令選項](/dotnet/framework/tools/signtool-exe#timestamp-command-options)。|  
|`Verify`|藉由判斷簽署憑證是否由受信任的授權單位所發佈、簽署憑證是否已撤銷，以及簽署憑證是否為特定原則的有效憑證，來驗證檔案的數位簽章。 如需 `Verify` 命令支援選項的清單，請參閱 [Verify 命令選項](/dotnet/framework/tools/signtool-exe#verify-command-options)。|

 下列選項適用於所有簽署工具命令。  
  
|Global 選項|描述|  
|----|----|  
|**/q**|如果命令成功執行則不顯示任何輸出，如果命令失敗則顯示最少的輸出。|  
|**/v**|不論命令執行成功或失敗，都顯示詳細資訊輸出，並顯示警告訊息。|  
|**/debug**|顯示偵錯資訊。|  

 
## <a name="catdb-command-options"></a>Catdb 命令選項  

 下表列出可以搭配 `Catdb` 命令使用的選項。

| Catdb 選項 | 描述 |
|----|----| 
| **/d** | 指定要更新的預設目錄資料庫。 如果 **/d** 和 **/g** 選項都不是使用，SignTool 會更新系統元件和驅動程式資料庫。 |
| **/G** *GUID* | 指定由 GUID 所識別的目錄資料庫已更新。|
| **/r** | 從目錄資料庫移除指定的目錄。 如果未指定此選項，SignTool 會將指定的目錄新增至目錄資料庫。|
| **u** | 指定自動為新增的類別目錄檔案產生唯一的名稱。 必要時，目錄檔會重新命名，以避免與現有的目錄檔發生名稱衝突。 如果未指定此選項，SignTool 會覆寫任何與所加入之目錄同名的現有目錄。|

> [!Note]  
> 目錄資料庫是用來自動查閱目錄檔案。


## <a name="sign-command-options"></a>Sign 命令選項  

 下表列出可以搭配 `sign` 命令使用的選項。  
  
|Sign 命令選項|描述|  
|----|----| 
|`/a`|自動選取最佳的簽署憑證。 簽署工具會找到滿足所有指定條件的所有有效憑證，並且選取有效時間最長的一個。 如果沒有這個選項，簽署工具只需要找出一個有效的簽署憑證。|  
|`/ac`  *檔*|從 *file* 將其他憑證加入至簽章區塊。|  
|`/as`|附加這個簽章。 如果主要簽章不存在，則會設定這個簽章做為主要簽章。|  
|`/c`  *CertTemplateName*|指定適用於簽署憑證的「憑證範本名稱」(Certificate Template Name)，這是一個 Microsoft 擴充功能。|  
|`/csp`  *CSPName*|指定包含私密金鑰容器的密碼編譯服務提供者 (Cryptographic Service Provider，CSP)。|  
|`/d`  *Desc*|指定簽署內容的描述。|  
|`/dg`  *路徑*|產生要簽署的摘要和未簽署的 PKCS7 檔案。 輸出摘要和 PKCS7 檔案將會是： *Path\FileName.dig* 和 *Path\FileName.p7u*。 若要輸出額外的 XML 檔案，請參閱 <strong>/dxml</strong>。|  
|`/di`  *路徑*|藉由將簽署的摘要擷取至未簽署的 PKCS7 檔案來建立簽章。 輸入簽署的摘要和未簽署的 PKCS7 檔案應該是： *Path\FileName.dig.signed* 和 *Path\FileName.p7u*。|  
|`/dlib`  *DLL*|指定執行函式 <code>AuthenticodeDigestSign</code> 以簽署摘要的 DLL。 此選項相當於使用 <strong>SignTool</strong> 與 <strong>/dg</strong>、 <strong>/ds</strong>和 <strong>/di</strong> 參數分開，但這個選項會將三個全部叫用為一個不可部分完成的作業。|  
|`/dmdf`  *檔案名*|搭配 <strong>/dg</strong> 選項使用時，會將檔案的內容傳遞至函式， <code>AuthenticodeDigestSign</code> 而不需要修改。|  
|`/ds`  |只簽署摘要。 輸入檔應該是 <strong>/dg</strong> 選項所產生的摘要。 輸出檔案將會是： *file. 簽署*。|  
|`/du`  *URL*|為已簽署的內容之擴充描述指定統一資源定位器 (Uniform Resource Locator，URL)。|  
|`/dxml`  |搭配 <strong>/dg</strong> 選項使用時，會產生 XML 檔案。 輸出檔案將會是： *Path\FileName.dig.xml*。|  
|`/f`  *SignCertFile*|指定檔案中的簽署憑證。 如果檔案為「個人資訊交換」(PFX) 格式並且受密碼保護，請使用 `/p` 選項指定密碼。 如果檔案不包含私密金鑰，請使用 `/csp` 和 `/kc` 選項，以指定 CSP 和私密金鑰容器的名稱。|  
|`/fd`*alg*|指定要用於建立檔案簽章的檔案摘要演算法。 </br> **注意：** 如果在簽署時未提供 <strong>/fd</strong> 參數，則會產生警告。 預設的 alg 為 SHA1，但建議使用 SHA256。|
|`/fd`  *certHash*|指定字串 certHash 會預設為用於簽署憑證的演算法。 </br> **注意：** 僅在 Windows 10 套件中提供20236版和更新版本。|  
|`/i`  *IssuerName*|指定簽署憑證的簽發者名稱。 這個值可以是完整簽發者名稱的子字串。|  
|`/kc`  *PrivKeyContainerName*|指定私密金鑰容器名稱。|  
|`/n`  *SubjectName*|指定簽署憑證的主體名稱。 這個值可以是完整主體名稱的子字串。|  
|`/nph`|如果支援，則隱藏可執行檔的頁面雜湊。 預設取決於 SIGNTOOL_PAGE_HASHES 環境變數和 wintrust.dll 版本。 若為非 PE 檔案，則會忽略這個選項。|  
|`/p`  *密碼*|指定用來開啟 PFX 檔案的密碼  (使用 `/f` 選項指定 PFX 檔)。|  
|`/p7` *路徑*|指定為每個指定內容檔產生公開金鑰加密標準 (PKCS) #7 檔案。 PKCS #7 的檔案會 *命名為* \\ ** p7。|  
|`/p7ce` *值*|指定已簽署的 PKCS #7 內容的選項。 將 *Value* 設定為 "Embedded" 會將簽署內容內嵌在 PKCS #7 檔案中，設定為 "DetachedSignedData" 會產生已中斷連結的 PKCS #7 檔案的簽署資料部分。 如果未使用 `/p7ce` 選項，則預設會內嵌簽署的內容。|  
|`/p7co` *\<OID>*|指定識別已簽署 PKCS #7 內容的物件識別項 (OID)。|  
|`/ph`|如果支援，則產生可執行檔的頁面雜湊。|  
|`/r`  *RootSubjectName*|指定簽署憑證必須鏈結之根憑證的主體名稱。 這個值可以是完整根憑證主體名稱的子字串。|  
|`/s`  *StoreName*|指定搜尋憑證時要開啟的存放區。 如果沒有指定這個選項，則會開啟 `My` 存放區。|  
|`/sha1`  *雜湊*|指定簽署憑證的 SHA1 雜湊。 在多重憑證符合其餘參數指定的準則時，SHA1 雜湊最常被指定。|  
|`/sm`|指定使用電腦存放區，而非使用者存放區。|  
|`/t`  *URL*|指定時間戳記伺服器的 URL。 如果沒有這個選項 (或 `/tr`)，簽署的檔案就不會加上時間戳記。 如果加上時間戳記失敗，便會產生警告。 這個選項無法與 `/tr` 選項搭配使用。|  
|`/td`  *alg*|與 `/tr` 選項一起使用以要求 RFC 3161 時間戳記伺服器使用的摘要演算法。 </br> **注意：** 如果在時間戳記時未提供 <strong>/td</strong> 參數，則會產生警告。 預設的 alg 為 SHA1，但建議使用 SHA256。 <br/> <strong>/Td</strong>參數必須在<strong>/tr</strong>參數之後宣告，而不是在之前。 如果在<strong>/tr</strong>參數之前宣告<strong>/td</strong>參數，則傳回的時間戳記是來自 SHA1 演算法，而不是預期的 SHA256 演算法。 |
|`/tr`  *URL*|指定 RFC 3161 時間戳記伺服器的 URL。 如果沒有這個選項 (或 `/t`)，簽署的檔案就不會加上時間戳記。 如果加上時間戳記失敗，便會產生警告。 這個選項無法與 `/t` 選項搭配使用。|  
|`/u`  *使用量*|指定在簽署憑證時必須存在的增強金鑰使用方法 (Enhanced Key Usage，EKU)。 使用方法的值可以利用 OID 或字串指定。 預設的使用方法為 "Code Signing" (1.3.6.1.5.5.7.3.3)。|  
|`/uw`|指定「Windows 系統元件驗證」(1.3.6.1.4.1.311.10.3.6) 的使用方式。|  
  
 如需使用方式範例，請參閱[使用 SignTool 簽署檔案](using-signtool-to-sign-a-file.md)。  
  

## <a name="timestamp-command-options"></a>時間戳記命令選項  

 下表列出可以搭配 `TimeStamp` 命令使用的選項。  
  
|TimeStamp 選項|描述|  
|----|----|  
|`/p7`|為 PKCS #7 檔案加上時間戳記。|  
|`/t`  *URL*|指定時間戳記伺服器的 URL。 要加上時間戳記的檔案必須先經過簽署。 必須有 `/t` 或 `/tr` 任一選項。|  
|`/td`  *alg*|與 `/tr` 選項一起使用以要求 RFC 3161 時間戳記伺服器使用的摘要演算法。 </br> **注意：** 如果在時間戳記時未提供 <strong>/td</strong> 參數，則會產生警告。 預設的 alg 為 SHA1，但建議使用 SHA256。 <br/> <strong>/Td</strong>參數必須在<strong>/tr</strong>參數之後宣告，而不是在之前。 如果在<strong>/tr</strong>參數之前宣告<strong>/td</strong>參數，則傳回的時間戳記是來自 SHA1 演算法，而不是預期的 SHA256 演算法。 |
|`/tp`*索引*|在 *index* 的簽章加上時間戳記。|  
|`/tr`  *URL*|指定 RFC 3161 時間戳記伺服器的 URL。 要加上時間戳記的檔案必須先經過簽署。 必須有 `/tr` 或 `/t` 任一選項。|  


## <a name="verify-command-options"></a>驗證命令選項  

|Verify 選項|描述|
|----|----|
| **/a** | 指定所有方法都可以用來驗證檔案。 首先會搜尋目錄資料庫，判斷檔案是否已在目錄中簽署。 如果檔案未登入任何目錄，SignTool 會嘗試驗證檔案的內嵌簽章。 驗證不一定已在目錄中簽署的檔案時，建議您採用這個選項。 可能或可能未簽署的檔案範例包括 Windows 檔案或驅動程式。 |
| **/ad** | 使用預設目錄資料庫尋找目錄。 |
| **/all** | 驗證具有多個簽章之檔案中的所有簽章。 |
| **/as** | 使用系統元件 (驅動程式) 目錄資料庫尋找目錄。 |
| **/Ag** *CatDBGUID* | 在 **GUID** 所識別的目錄資料庫中尋找目錄。 |
| **/c** *CatFile* | 依名稱指定目錄檔。 |
| **/d** | 列印 [描述] 和 [描述] URL。<br/> **Windows Vista 及更早版本：** 不支援此旗標。<br/> |
| **/Ds** *索引* | 在特定位置驗證簽章。 |
| **/hash**{**SHA1** \| **SHA256**} | 指定在目錄中搜尋檔案時，要使用的選擇性雜湊演算法。 |
| **/kp** | 使用 x64 核心模式驅動程式簽署原則來執行驗證。 |
| **/ms** | 使用多個驗證語意。 這是 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 呼叫的預設行為。 |
| **/O** *版本* | 根據作業系統版本驗證檔案。 Version 參數的格式如下：<br/> *PlatformID ***：**_>vermajor_*_。_*_>Verminor_*_。_ *_BuildNumber_<br/> 建議使用 */o* 參數。 如果未指定 */o* ，SignTool 可能會傳回非預期的結果。 例如，如果您未包含 */o* 參數，則在較舊 os 上正確驗證的系統目錄可能無法在較新的作業系統上正確地進行驗證。 |
| **/p7** | 確認 PKCS \# 7 檔案。 PKCS 7 驗證不會使用任何現有的原則 \# 。 檢查簽章，並建置簽署憑證鏈結。 |
| **/pa** | 指定使用預設驗證驗證原則。 如果未指定 **/pa** 選項，SignTool 會使用 Windows 驅動程式驗證原則。 此選項不能與 **catdb** 選項搭配使用。 |
| **/Pg** *PolicyGUID* | 依 **GUID** 指定驗證原則。 **GUID** 對應于驗證原則的 ActionID。 此選項不能與 **catdb** 選項搭配使用。 |
| **/ph** | 列印並確認頁面雜湊值。<br/> **Windows Vista 及更早版本：** 不支援此旗標。<br/>  |
| **/R** *RootSubjectName* | 指定簽署憑證必須鏈結之根憑證的主體名稱。 這個值可以是完整根憑證主體名稱的子字串。 |
| **/tw** | 指定如果簽章未加上時間戳記，就會產生警告。|


SignTool **verify** 命令可判斷簽署憑證是否由受信任的授權單位發出、簽署憑證是否已撤銷，以及是否可選擇性地指定簽署憑證是否對特定原則有效。  

除非指定了選項來搜尋目錄 (/a、/ad、/as、/ag、/c) ，否則 SignTool **verify** 命令會輸出 **內嵌** 的簽章狀態。


## <a name="return-value"></a>傳回值  

 簽署工具終止時會傳回下列其中一個結束代碼。  
  
|結束碼|描述|  
|----|----| 
|0|執行成功。|  
|1|執行失敗。|  
|2|執行已完成，但出現警告。|


## <a name="examples"></a>範例  

 下列命令會將目錄檔 MyCatalogFileName.cat 加入至系統元件和驅動程式資料庫。 如有必要防止取代名為 `/u` 的現有目錄檔案，`MyCatalogFileName.cat` 選項會產生一個唯一的名稱。  
  
```console  
signtool catdb /v /u MyCatalogFileName.cat  
```  
  
 下列命令會使用最佳憑證自動簽署檔案。  
  
```console  
signtool sign /a /fd SHA256 MyFile.exe 
```  
  
 下列命令使用儲存在受密碼保護之 PFX 檔中的憑證存放區，對檔案進行數位簽署。  
  
```console  
signtool sign /f MyCert.pfx /p MyPassword /fd SHA256 MyFile.exe 
```  
  
 下列命令會對檔案進行數位簽署和時間戳記。 用於簽署檔案的憑證存放在 PFX 檔中。  
  
```console  
signtool sign /f MyCert.pfx /t http://timestamp.digicert.com /fd SHA256 MyFile.exe 
```  
  
 下列命令會使用位於主旨名稱為 `My` 之 `My Company Certificate` 存放區中的憑證來簽署檔案。  
  
```console  
signtool sign /n "My Company Certificate" /fd SHA256 MyFile.exe 
```  
  
 下列命令會簽署 ActiveX 控制項，並在提示使用者安裝該控制項時，提供由 Internet Explorer 顯示的資訊。  
  
```console  
Signtool sign /f MyCert.pfx /d: "MyControl" /du http://www.example.com/MyControl/info.html /fd SHA256 MyControl.exe 
```  
  
 下列命令會為已數位簽署的檔案加上時間戳記。  
  
```console  
signtool timestamp /t http://timestamp.digicert.com MyFile.exe
```  

下列命令會將使用 RFC 3161 時間戳記伺服器的檔案加上戳記。  
  
```console  
signtool timestamp /tr http://timestamp.digicert.com /td SHA256 MyFile.exe
```  
  
 下列命令會確認檔案是否已簽署。  
  
```console  
signtool verify MyFile.exe  
```  
  
 下列命令會驗證可能已在目錄中簽署的系統檔。  
  
```console  
signtool verify /a SystemFile.dll  
```  
  
 下列命令會驗證已在名為 `MyCatalog.cat` 之目錄中簽署的系統檔。  
  
```console  
signtool verify /c MyCatalog.cat SystemFile.dll  
```  
