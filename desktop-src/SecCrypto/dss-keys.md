---
description: 說明如何產生、取出、驗證及匯出 DSS 金鑰和簽章。
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: DSS 金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6ab8adcc4d551c4196e99ce48f5afdd380dc3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995816"
---
# <a name="dss-keys"></a>DSS 金鑰

-   [產生和取出 DSS 金鑰](#generating-and-retrieving-dss-keys)
-   [產生 DSS 簽章](#generating-dss-signatures)
-   [驗證 DSS 簽章](#verifying-a-dss-signature)
-   [匯出 DSS 金鑰](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>產生和取出 DSS 金鑰

DSS 金鑰可以藉由呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函數來產生。 呼叫 **CryptGenKey** 需要在 \_ \_ \_ *Algid* 引數中傳遞 SIGNATURE 或 CALG DSS SIGN。 此呼叫將會產生 P (質數模數) 、Q (質數) 、G (產生器) 、X (秘密指數) 和 Y (公開金鑰) 值，並將其保存在本機儲存體的 [*金鑰 BLOB*](../secgloss/k-gly.md) 中。

**產生 DSS 簽章金鑰組**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 函數，以取得 Microsoft DSS 密碼編譯提供者的控制碼。
2.  呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 以產生金鑰。 在 \_ 簽章或 CALG \_ DSS \_ SIGN 上必須傳入 *Algid* 引數，且 *dwFlags* 引數的上16位必須設定為所需的金鑰大小。 如果上層16位為零，則會使用預設的金鑰大小1024位。 [**HCRYPTKEY**](hcryptkey.md)控制碼會在 *hKey* 引數中傳回。

**取出先前產生之簽章金鑰的指標**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 以取得 Microsoft DSS 密碼編譯提供者的控制碼。
2.  呼叫 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) 函數，並將 *dwKeySpec* 引數設定為 \_ SIGNATURE 或 CALG \_ DSS \_ SIGN。

**取出 P、Q 和 G 值**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 以取得 Microsoft DSS 密碼編譯提供者的控制碼。
2.  呼叫 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) ，並將 *dwKeySpec* 引數設定為 \_ SIGNATURE 或 CALG \_ DSS \_ SIGN。
3.  使用 *hKey* 引數設定為上一個步驟中所抓取指標的呼叫 [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) 。 *DwParam* 引數必須設定為所需的旗標;KP \_ P、kp \_ Q 或 KP \_ G。 此值會在 *>pbdata* 引數中傳回，而且資料的長度會在 *pdwDataLen* 引數中傳回。 傳回的值不含標頭資訊，而是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式傳回。

## <a name="generating-dss-signatures"></a>產生 DSS 簽章

要簽署的資料必須先使用 [*SHA*](../secgloss/s-gly.md)演算法進行 [*雜湊*](../secgloss/h-gly.md)處理。 雜湊該資料之後，會呼叫 [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha)函數來產生 [*DSS*](../secgloss/d-gly.md)簽章。

**產生 DSS 簽章**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 以取得 Microsoft DSS 密碼編譯提供者的控制碼。
2.  呼叫 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) ，並將 *Algid* 引數設定為 CALG \_ sha，以取得 SHA 雜湊物件的控制碼。
3.  呼叫 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) ，並將 *hHash* 引數設定為上一個步驟中抓取的控制碼。 這會建立資料的雜湊，並將控制碼傳回給 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)函式呼叫的 *phHash* 引數中的雜湊。
4.  呼叫 [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) ，並將 *hHash* 引數設定為上一個步驟中抓取的控制碼。 可以在 \_ \_ \_ *dwKeySpec* 參數中傳遞 SIGNATURE 或 CALG DSS SIGN。 簽章會傳回給 *pbSignature* 引數中提供的位址，而且簽章的長度會傳回給 *pdwSigLen* 引數中提供的位址。 **Null** 指標可能會在 *pbSignature* 引數中傳遞，而在此情況下，不會產生簽章，但簽章的長度會傳回給 *pdwSigLen* 參數中提供的位址。

## <a name="verifying-a-dss-signature"></a>驗證 DSS 簽章

若要驗證 DSS 簽章，必須匯入簽署者的 DSS 公開金鑰、簽署的 [*資料*](../secgloss/s-gly.md) 必須經過雜湊處理，然後才能驗證簽章。

**驗證 DSS 簽章**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 以取得 Microsoft DSS 密碼編譯提供者的控制碼。
2.  呼叫 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 以匯入簽署者的 DSS 公開金鑰。
3.  呼叫 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) ，並將 *Algid* 引數設定為 CALG \_ sha，以取得 SHA 雜湊物件的控制碼。
4.  呼叫 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) ，並將 *hHash* 引數設定為上一個步驟中抓取的控制碼，並將 *>pbdata* 指向已簽署的資料。 這會建立資料的雜湊，並將控制碼傳回給 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)函式呼叫的 *phHash* 引數中的雜湊。
5.  使用下列設定呼叫 [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) ：

    *hHash* 會設定為上一個步驟中所執行雜湊的控制碼。

    *pbSignature* 指向要驗證的簽章。

    *dwSigLen* 會設定為簽章的長度。

    *hPubKey* 會設為步驟2中匯入之公開金鑰的控制碼。

    *dwFlags* 設定為零。

## <a name="exporting-dss-keys"></a>匯出 DSS 金鑰

當您將 [*簽署的資料*](../secgloss/s-gly.md) 傳送給必須由收件者驗證簽章的人員時，必須提供簽署者的公開金鑰給收件者，且通常會與簽署的資料一起傳送。 因此，必須能夠以 [*金鑰 BLOB*](../secgloss/k-gly.md)格式匯出 [*DSS*](../secgloss/d-gly.md)金鑰。

**匯出 DSS 公開金鑰**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 以取得 Microsoft DSS 密碼編譯提供者的控制碼。
2.  呼叫 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) ，並將 *dwKeySpec* 引數設定為 \_ SIGNATURE 或 CALG \_ DSS \_ SIGN。
3.  呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) ，並將 *hKey* 設定為上一個步驟中抓取的控制碼、 *DwBlobType* 設定為 PUBLICKEYBLOB， *dwFlags* 設定為零。 DSS [*公開金鑰 blob*](../secgloss/p-gly.md) 會在 *>pbdata* 中傳回，而 [*金鑰 Blob*](../secgloss/k-gly.md) 的長度會在 *pdwDataLen* 中傳回。 **Null** 指標可能會在 *>pbdata* 中傳遞，而在此情況下，只會傳回 DSS 金鑰 BLOB 的長度。 對 **CryptExportKey** 進行呼叫時所傳回的 BLOB 會採用 [DSS 提供者金鑰 blob](dss-provider-key-blobs.md)中所述的格式。

**匯出 DSS 私密金鑰**

-   遵循與匯出 DSS 公開金鑰相同的程式，但在對 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)進行呼叫時， *dwBlobType* 會設定為 PRI加值稅EKEYBLOB。 對 **CryptExportKey** 進行呼叫時所傳回的 BLOB 會採用 [DSS 提供者金鑰 blob](dss-provider-key-blobs.md)中所述的格式。

 

 
