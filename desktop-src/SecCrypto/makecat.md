---
description: 建立類別目錄檔案的 CryptoAPI 工具。
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3b9d8698e3c3694368813b19bd3be692c6c8f3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623143"
---
# <a name="makecat"></a>MakeCat

MakeCat 工具是用來建立類別目錄檔案的 CryptoAPI 工具。 MakeCat 適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK) 的一部分，預設會安裝在 \\ SDK 安裝路徑的 Bin 資料夾中。

MakeCat 工具會使用下列命令語法：

**MakeCat** \[**-n** \|**-r** \|**-v** \]*檔案名*

## <a name="parameters"></a>參數



| 參數             | 描述                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-n**<br/>     | 請勿在可復原的錯誤上停止。<br/>                                                                                                                           |
| **-r**<br/>     | 如果遇到可復原的錯誤，則強制 MakeCat 結束。 具體而言，它會在檔的 [類別目錄檔案] 區段中處理專案時結束。<br/> |
| **-v**<br/>     | 詳細。 顯示所有進度和錯誤訊息。<br/>                                                                                                            |
| *FileName*<br/> | 要剖析的 cdf 檔案名。 如需必要的結構和內容，請參閱備註。<br/>                                                                         |



 

## <a name="remarks"></a>備註

您必須使用下列規格來建立此 cdf 檔案。

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> 專案中的最後一個專案必須在行尾必須有明確的分行符號。

 

\[CatalogHeader \] 區段會定義整個類別目錄檔案的相關資訊。



| 選項                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 名稱<br/>           | 類別目錄檔案的名稱，包括它的副檔名。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| >\dreplayclient\resultdir<br/>      | 將放置建立之 .cat 檔案的目錄。 如果未指定，則會使用預設的目前的目錄。 如果目錄不存在，則會建立該目錄。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PublicVersion<br/>  | 不支援這個選項。 <br/> **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 目錄版本。 如果保留空白，則會使用預設值1。<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CatalogVersion<br/> | 目錄版本。 如果版本不存在或設定為1，則會將 "0x100" 傳遞給 [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)函式的 *dwPublicVersion* 參數，並建立第1版的類別目錄檔案。 HashAlgorithms 選項必須空白或包含 SHA1。<br/> 如果版本設定為2，則會將 "0x200" 傳遞給 [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)函式的 *dwPublicVersion* 參數，並建立第2版的類別目錄檔案。 HashAlgorithms 選項必須包含 SHA256。<br/> 如果這個選項存在，但包含1或2以外的任何值，MakeCat 工具將會發生錯誤。<br/> **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 不支援此選項。<br/> <br/> |
| HashAlgorithms<br/> | 使用的雜湊演算法名稱。 如需詳細資訊，請參閱 CatalogVersion 選項。<br/> **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 不支援此選項。<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PageHashes<br/>     | 指定是否將 <HASH> \[ CatalogFiles \] 區段中的選項所列的檔案雜湊<br/> **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 不支援此選項。<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| EncodingType<br/>   | 使用的訊息編碼類型。 如果保留空白，預設 Edi.encodingtype 為 PKCS \_ 7 \_ ASN \_ 編碼 \| X509 \_ ASN \_ 編碼，0x00010001。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

\[CatalogFiles \] 區段會定義每個類別目錄檔案的成員，並在不同的群組中包含各種類型的檔案和不同類型的屬性。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>選項</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>參考標記<br/></td>
<td>檔案的文字參考。 這可以包含任何 ASCII 文字字元，但等號 (=) 除外。 安裝之後，系統必須能夠重現此標記。 <br/> 用 <HASH> 做檔案名的前置詞。 這會導致標記成為 ASCII 字串格式的檔案雜湊。 <br/></td>
</tr>
<tr class="even">
<td>檔案路徑和名稱<br/></td>
<td>檔案名，包括要剖析的副檔名和檔案的相對路徑。 可使用 SignTool 簽署的任何檔案類型都可以新增至目錄。 例如，具有下列副檔名的檔案名（以及其他副檔名）可以新增至目錄： .exe、.cab、.cat、.ocx、.dll 和 stl。<br/></td>
</tr>
<tr class="odd">
<td>ALTSIPID<br/></td>
<td>用於雜湊的 SIP GUID，而不是根據檔案類型的標準 SIP。 這是選用項目。 如果省略此專案，則會使用預設的 SIP 來雜湊成員。 如果找不到預設安裝的 SIP，則會使用一般 SIP。<br/></td>
</tr>
<tr class="even">
<td>guid<br/></td>
<td>GUID 的文字標記法。<br/></td>
</tr>
<tr class="odd">
<td>ATTRx<br/></td>
<td>選擇性。 檔案或內容的相關屬性或語句。 您可以有任意數目的屬性，包括 none。<br/></td>
</tr>
<tr class="even">
<td>類型<br/></td>
<td>定義要在格式 0x00000000 (文字) 中加入的屬性類型。 這個選項可以是零或多個下列值的位<strong>or</strong> 組合：<br/>
<ul>
<li>0x10000000 驗證的屬性 (簽署，包含在雜湊) 中。</li>
<li>0x20000000 未驗證的屬性 (不帶正負號，不包含在雜湊中，無法驗證) 。</li>
<li>0x01000000 屬性不會複寫到 CatalogVersion 2 目錄中的 SHA1 專案。</li>
<li>0x00010000 屬性會以純文字表示。 不會進行任何轉換。</li>
<li>0x00020000 屬性以64編碼方式表示。 這會用來代表二進位資料。</li>
<li>0x00000001 屬性是成對的名稱/值。 針對名稱使用 oid 選項。 這個屬性很慢;因此，請謹慎使用此選項。</li>
<li> (OID) 的 <a href="/windows/desktop/SecGloss/o-gly"><em>物件識別碼</em></a> 參考了0x00000002 屬性。</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>oid<br/></td>
<td>屬性參考索引鍵的文字標記法。 它是以點符四標記法的文字字串格式的 OID (例如，b.) 或文字名稱。<br/></td>
</tr>
<tr class="even">
<td>值<br/></td>
<td>屬性值的文字表示。 使用的文字表示型別取決於 type 選項的值。 EOL 字元會決定長度。<br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td>雜湊指定的檔案。<br/></td>
</tr>
</tbody>
</table>



 

產生的類別目錄檔案未簽署。 如果要在傳送前簽署，則會使用 [SignTool](signtool.md)進行簽署。

 

 
