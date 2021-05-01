---
description: Authenticode 時間戳記是以標準 PKCS \# 7 副署為基礎。 Microsoft 簽署的工具可讓開發人員在貼上 Authenticode 簽章時，同時貼上時間戳記。
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: 時間戳記 Authenticode 簽章
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0232853441d2c11d331c175ac7e8dfd120b341ff
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327183"
---
# <a name="time-stamping-authenticode-signatures"></a>時間戳記 Authenticode 簽章

Microsoft Authenticode 簽章提供二進位資料的作品和完整性保證。 Authenticode 時間戳記是以標準 PKCS \# 7 副署為基礎。 Microsoft 簽署的工具可讓開發人員在貼上 Authenticode 簽章時，同時貼上時間戳記。 時間戳記允許驗證 Authenticode 簽章，即使在用於簽章的憑證過期之後也是如此。

## <a name="a-brief-introduction-to-authenticode"></a>Authenticode 的簡介

[*Authenticode*](../secgloss/a-gly.md) 套用數位簽章技術，以保證二進位資料（如可安裝的軟體）的作品和完整性。 用戶端網頁瀏覽器（或其他系統元件）可以使用 Authenticode 簽章來確認下載或安裝軟體時的資料完整性。 Authenticode 簽章可以搭配許多軟體格式使用，包括 .cab、.exe、.ocx 和 .dll。

Microsoft 會維護公開憑證發行 [*機構*](/security/trusted-root/participants-list) 單位清單， (CAs) 。 Authenticode 憑證的簽發者目前包含 [SSL.com](https://www.ssl.com/)、 [Digicert](https://www.digicert.com/)、 [Sectigo certificate (Comodo) ](https://www.sectigo.com/)和 [GlobalSign](https://www.globalsign.com/)。

## <a name="about-cryptographic-time-stamping"></a>關於密碼編譯時間戳

在過去，已建議各種不同的密碼編譯時間戳方法。 如需 Haber 和 Stornetta Cryptology 中的「如何 Time-Stamp 數位檔」，請參閱 (1991) 和 Benaloh 與 de 請「單向累加器：「數位簽章的非集中式替代」 Springer link *-Verlag 的課程附注（位於電腦科學* 音量 765 (EUROCRYPT ' 93) ）。 您可以從 [Microsoft Research](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a)取得本文的擴充摘要。  (這些資源可能無法在某些語言及國家/地區中使用。 ) 由於時間是實體，而不是數學數量，因此這些方法通常會考慮如何連結化物件，以判斷其建立順序，或如何有效率地將所有可描述的物件視為同時建立。

據稱以數量來驗證時間的系統一律需要某種形式的信任。 在強形成對立設定中，您可以使用複雜的通訊協定來確保某種程度的同步。 不過，這些通訊協定需要在受影響的合作物件之間進行廣泛的互動。 在實務上，如果其中一項只需要來自信任來源的認證，則會提供簽署的語句 (認證) ，在指定的時間為簽章提供物件。

下列所實行之時間戳記的副署方法，即使簽署憑證已過期或已撤銷，也可以驗證簽章。 時間戳記可讓驗證器可靠地知道簽署簽章的時間，並藉此在當時有效時信任簽章。 時間戳記程式應該有可靠且受保護的時間來源。

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>PKCS \# 7 簽署的檔和副署

PKCS \# 7 是密碼編譯資料的標準格式，包括簽署的資料、憑證，以及 (crl) 的 [*憑證撤銷清單*](../secgloss/c-gly.md) 。 \#時間戳記內容中的特定 PKCS 7 類型是簽署的資料，對應至 PKCS \# 7 定義的 [**SignedData**](signeddata.md)內容類型。

PKCS \# 7 套件包含可識別實際內容的 [**SignedData**](signeddata.md) ，以及有關它和 SignerInfo 簽章區塊的特定資訊。 SignerInfo 本身可能包含副署，以遞迴方式為另一個 SignerInfo。 在主體中，可能會有這類副署的順序。 副署是與 SignerInfo 中簽章相關的未經驗證屬性;亦即，它可能會在原始簽章的後面貼上。 以大綱形式：

[**SignedData**](signeddata.md) (PKCS \# 7) 

-   PKCS 7 的版本 (\# ，通常是第1版) 
-   DigestAlgorithms SignerInfo 簽章區塊所使用的所有演算法的 (集合，以進行優化處理) 
-   ContentInfo (contentType 等於 [**SignedData**](signeddata.md)，加上內容或內容的參考) 
-   選用的憑證 (所有使用的憑證集合) 
-   選用 Crl (所有 Crl 的集合) 
-   SignerInfo 簽章區塊 (實際的簽章，由一或多個 SignerInfo 簽章區塊所組成) 

SignerInfo (簽章區塊) 

-   PKCS 7 的版本 (\# ，通常是第1版) 
-   憑證 (簽發者和序號來唯一識別簽署者在 [**SignedData**](signeddata.md) 中的憑證) 
-   DigestAlgorithm 加上 DigestEncryptionAlgorithm 加上摘要 (雜湊) ，再加上 EncryptedDigest (實際的簽章) 
-   選擇性 AuthenticatedAttributes (例如，由這個簽署者簽署) 
-   選擇性 UnauthenticatedAttributes (例如，此簽署者未簽署) 

驗證屬性的範例是 (OID 1.2.840.113549.1.9.5) 的簽署時間，因為它是時間戳記服務簽署的一部分。 未經驗證的屬性範例是「副署 (OID 1.2.840.113549.1.9.6) ，因為它可以在簽署後貼上。 在此情況下，SignerInfo 本身會包含 SignerInfo (副署) 。

> [!Note]  
> 在副署中簽署的物件是原始的簽章 (也就是原始 SignerInfo) 的 EncryptedDigest。

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool 和 Authenticode 流程

[SignTool](signtool.md) 適用于 Authenticode 簽署和時間戳記的二進位資料。 此工具會安裝在 \\ Microsoft Windows 軟體開發套件 (SDK) 安裝路徑的 Bin 資料夾中。

簽署和時間戳記的二進位資料在使用 [SignTool](signtool.md)時相當簡單。 發行者必須從商務程式碼簽署 CA 取得程式碼簽署憑證。 為了方便起見，Microsoft 會發佈並更新公用 Ca 清單，包括發出 Authenticode 憑證的 Ca。 準備發行時，會使用適當的命令列參數搭配 SignTool 工具來簽署物件檔案和時間戳記。 任何 SignTool 作業的結果一律是 PKCS \# 7 格式 [**SignedData**](signeddata.md)。

SignTool 會接受要簽署的原始二進位資料和時間戳記，或先前帶正負號的二進位資料要加上時間戳記。 先前已簽署的資料可以使用 **signtool timestamp** 命令來加上時間戳記。



| 引數             | 描述                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/T** *HTTPAddress* | 指出檔案是加上時間戳記。 指定必須提供時間戳記伺服器位址的 URL。 **/t** 可搭配 **signtool sign** 和 **signtool timestamp** 命令使用。 |



 

如需有關在此內容中可能有用之工具的詳細資訊，請參閱 [加密工具](cryptography-tools.md) 和 [SignTool](signtool.md)。

## <a name="implementation-details-and-wire-format"></a>執行詳細資料和電傳格式

[SignTool](signtool.md) 依賴 Windows Authenticode 實行來建立和時間戳記簽章。 [*Authenticode*](../secgloss/a-gly.md) 會在二進位檔案上運作，例如 .cab、.exe、.dll 或 .ocx。 Authenticode 會先建立簽章，產生 PKCS \# 7 [**SignedData**](signeddata.md)。 這是必須副署的 **SignedData** ，如 PKCS 9 所述 \# 。

副署進程會以四個步驟進行：

1.  從 PKCS 7 SignedData 的 SignerInfo 中複製簽章 (也就是 encryptedDigest) \# 。 [](signeddata.md)
2.  建立其內容為原始簽章的時間戳記要求。 將此傳送到時間戳記伺服器 [*抽象語法標記法 (一)*](../secgloss/a-gly.md) (asn.1) 編碼為 TimeStampRequest。
3.  接收時間戳記伺服器所傳回的時間戳記，格式為第二個 PKCS \# 7 [**SignedData**](signeddata.md)。
4.  將 SignerInfo 從時間戳記直接複製到原始 PKCS \# 7 [**SignedData**](signeddata.md)，如 PKCS \# 9 副署 (也就是在原始) 的 SignerInfo 中未經驗證的屬性。

## <a name="time-stamp-request"></a>時間戳記要求

時間戳記要求會在 HTTP 1.1 POST 訊息中傳送。 在 HTTP 標頭中，CacheControl 指示詞設定為 [無快取]，並將 [Content-type] 指示詞設定為 [應用程式/八位資料流程]。 HTTP 訊息的本文是 [*可辨別編碼規則*](../secgloss/d-gly.md) 的 base64 編碼， (DER) 時間戳記要求的編碼方式。

雖然目前未使用，但內容長度指示詞也應該用於建立 HTTP 訊息，因為它可協助時間戳記伺服器找出要求在 HTTP POST 內的位置。

其他 HTTP 標頭也可能存在，如果要求者或時間戳記伺服器無法理解這些標頭，則應該予以忽略。

時間戳記要求是一種 asn.1 編碼訊息。 要求的格式如下所示。

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

CountersignatureType 是 (OID) 的 [*物件識別碼*](../secgloss/o-gly.md) ，可將此識別碼識別為時間戳記副署，而且應該是確切的 OID 1.3.6.1.4.1.311.3.2.1。

時間戳記要求中目前未包含任何屬性。

內容是由 PKCS 7 所定義的 ContentInfo \# 。 內容是要簽署的資料。 針對簽章時間戳記，ContentType 應該是資料，而內容應該是 encryptedDigest (簽章) 從 PKCS 7 內容的 SignerInfo，再加上 \# 時間戳記。

## <a name="time-stamp-response"></a>時間戳記回應

時間戳記回應也會在 HTTP 1.1 訊息中傳送。 在 HTTP 標頭中，Content-type 指示詞也會設定為 application/八進位-stream。 HTTP 訊息的本文是一種 base64 編碼的時間戳記回應的 DER 編碼。

時間戳記回應是 \# 由時間戳記程式所簽署的 PKCS 7 簽署訊息。 PKCS 7 訊息的 ContentInfo 與 \# 時間戳記中收到的 ContentInfo 相同。 PKCS \# 7 內容包含「簽署時間驗證」屬性 (在 PKCS \# 99、OID 1.2.840.113549.9.5) 中定義。

在 Authenticode 從伺服器接收時間戳記之後，Authenticode 會將時間戳記併入原始 PKCS \# 7 [**SignedData**](signeddata.md) 中作為副署。 為了達成此目的，會捨棄傳回之 PKCS \# 7 **SignedData** 的 ContentInfo，並將傳回時間戳記的 SignerInfo 複製到原始 PKCS 7 SignedData SignerInfo 中的副署 \# 。  時間戳記程式的憑證鏈也會複製到原始 PKCS 7 SignedData 中的憑證 \# ， 做為原始簽署者未經驗證的屬性。

如需有關 PKCS 和其他安全性主體的詳細資訊，請參閱 [RSA 網站的內容庫](https://www.rsa.com/content_library.aspx)。

 

 
