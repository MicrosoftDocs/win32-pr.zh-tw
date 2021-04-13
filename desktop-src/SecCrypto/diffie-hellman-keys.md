---
description: 說明如何產生、交換、匯入和匯出 Diffie-Hellman 金鑰。
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Diffie-Hellman 金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321035"
---
# <a name="diffie-hellman-keys"></a>Diffie-Hellman 金鑰

-   [產生 Diffie-Hellman 金鑰](#generating-diffie-hellman-keys)
-   [交換 Diffie-Hellman 金鑰](#exchanging-diffie-hellman-keys)
-   [匯出 Diffie-Hellman 的私密金鑰](#exporting-a-diffie-hellman-private-key)
-   [範例程式碼](#example-code)

## <a name="generating-diffie-hellman-keys"></a>產生 Diffie-Hellman 金鑰

若要產生 Diffie-Hellman 金鑰，請執行下列步驟：

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 函數，以取得 Microsoft Diffie-Hellman 密碼編譯提供者的控制碼。
2.  產生新的金鑰。 有兩種方式可以完成這項工作，方法是讓 CryptoAPI 產生 G、P 和 X 的所有新值，或使用 G 和 P 的現有值，並為 X 產生新的值。

    **藉由產生所有新值來產生金鑰**

    1.  呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函式，傳遞 **CALG \_ DH \_ SF** (儲存和轉送) 或 **CALG \_ DH \_ EPHEM** (暫時性) 在 *Algid* 參數中。 系統將使用 G 和 P 的新隨機值、X 的新計算值來產生金鑰，而且會在 *phKey* 參數中傳回其控制碼。
    2.  新的金鑰現在已準備好可供使用。 G 和 P 的值必須連同金鑰 (傳送給收件者，或由其他方法) 在進行 [*金鑰交換*](../secgloss/e-gly.md)時傳送。

    **若要使用預先定義的 G 和 P 值產生金鑰**

    1.  呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 傳遞 **CALG \_ DH \_ SF** (儲存和轉送) 或 **CALG \_ DH \_ EPHEM** (暫時) 在 *Algid* 參數和 **CRYPT \_ PREGEN** 中， *dwFlags* 參數。 將會產生金鑰控制碼，並在 *phKey* 參數中傳回。
    2.  將 **>pbdata** 成員設定為 P 值的 [**CRYPT \_ 資料 \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))結構初始化。 [*BLOB*](../secgloss/b-gly.md)不包含任何標頭資訊，而且 **>pbdata** 成員採用 [*位元組*](../secgloss/l-gly.md)由小到大格式。
    3.  P 的值是藉由呼叫 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)函式來設定，並傳遞在 *hKey* 參數的步驟 a 中取出的金鑰控制碼、 *dwParam* 參數中的 **KP \_ P** 旗標，以及 *>pbdata* 參數中包含 P 值之結構的指標。
    4.  將 **>pbdata** 成員設定為 G 值的 [**CRYPT \_ 資料 \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))結構初始化。 BLOB 不包含任何標頭資訊，而且 **>pbdata** 成員採用位元組由小到大格式。
    5.  G 的值是藉由呼叫 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)函式來設定，並傳遞在 *hKey* 參數的步驟 a 中取出的金鑰控制碼、 *dwParam* 參數中的 **KP \_ G** 旗標，以及 *>pbdata* 參數中包含 G 值之結構的指標。
    6.  X 的值是藉由呼叫 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)函式來產生，並傳遞在 *hKey* 參數的步驟 a 中取出的金鑰控制碼、 *dwParam* 參數中的 **KP \_ X** 旗標，以及 *>pbdata* 參數中的 **Null** 。
    7.  如果所有函式呼叫都成功，Diffie-Hellman 的公開金鑰已可供使用。

3.  當不再需要索引鍵時，請將金鑰控制碼傳遞至 [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) 函式加以終結。

如果在先前的程式中指定了 **CALG \_ DH \_ SF** ，則每次呼叫 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)時，都會將金鑰值保存至儲存體。 然後，您可以使用 [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) 函數來抓取 G 和 P 值。 某些 Csp 可能會有硬式編碼的 G 和 P 值。 在此情況下，如果使用 *dwParam* 參數中指定的 **Kp \_ G** 或 **kp \_ P** 來呼叫 **CryptSetKeyParam** ，則會傳回不 **超過的 \_ FIXEDPARAMETER** 錯誤。 如果呼叫 **CryptDestroyKey** ，則會終結金鑰的控制碼，但金鑰值會保留在 CSP 中。 但是，如果指定了 **CALG \_ DH \_ EPHEM** ，則會終結金鑰的控制碼，並從 CSP 清除所有值。

## <a name="exchanging-diffie-hellman-keys"></a>交換 Diffie-Hellman 金鑰

Diffie-Hellman 演算法的目的是讓兩個或更多個合作物件可以透過不安全的網路共用資訊，來建立和共用相同的秘密工作階段金鑰。 透過網路共用的資訊是以一些常數值和 Diffie-Hellman 公開金鑰的形式呈現。 兩個金鑰交換合作物件所使用的程式如下所示：

-   雙方都同意 (P) 的質數 Diffie-Hellman 參數，以及 (G) 的產生器編號。
-   第1方會將其 Diffie-Hellman 公開金鑰傳送給第2方。
-   第2方會使用其私密金鑰和合作物件1的公開金鑰所包含的資訊來計算秘密工作階段金鑰。
-   第2方會將其 Diffie-Hellman 公開金鑰傳送給第1方。
-   第1方1會使用其私密金鑰和第二方公開金鑰中所含的資訊來計算秘密工作階段金鑰。
-   雙方現在都有相同的工作階段金鑰，可用於加密和解密資料。 下列程式顯示這項操作所需的步驟。

**準備 Diffie-Hellman 公開金鑰以進行傳輸**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 函數，以取得 Microsoft Diffie-Hellman 密碼編譯提供者的控制碼。
2.  藉由呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函式來建立新的金鑰，或藉由呼叫 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) 函式來取出現有的金鑰，以建立 Diffie-Hellman 索引鍵。
3.  藉由呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)並傳遞 **Null** 做為 *>pbdata* 參數，以取得保存 Diffie-Hellman 金鑰 BLOB 所需的大小。 將會在 *pdwDataLen* 中傳回所需的大小。
4.  配置金鑰 BLOB 的記憶體。
5.  藉由呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)函式來建立 Diffie-Hellman [*公開金鑰 BLOB*](../secgloss/p-gly.md) ，並在 *dwBlobType* 參數中傳遞 **PUBLICKEYBLOB** ，並將控制碼傳遞至 *hKey* 參數中 Diffie-Hellman 的索引鍵。 此函式呼叫會導致計算公開金鑰值（ (G ^ X) mod P）。
6.  如果上述所有函式呼叫都成功，Diffie-Hellman 的公開金鑰 BLOB 現在已準備好進行編碼和傳輸。

**匯入 Diffie-Hellman 公開金鑰並計算秘密工作階段金鑰**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 函數，以取得 Microsoft Diffie-Hellman 密碼編譯提供者的控制碼。
2.  藉由呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函式來建立新的金鑰，或藉由呼叫 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) 函式來取出現有的金鑰，以建立 Diffie-Hellman 索引鍵。
3.  若要將 Diffie-Hellman 公開金鑰匯入至 CSP，請呼叫 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 函式，將指標傳遞至 *>pbdata* 參數中的公開金鑰 blob、 *dwDataLen* 參數中 BLOB 的長度，以及 *hPubKey* 參數中 Diffie-Hellman 索引鍵的控制碼。 這會導致執行計算（ (Y ^ X) mod P），進而建立共用的秘密金鑰，並完成 [*金鑰交換*](../secgloss/e-gly.md)。 此函式呼叫會在 *hKey* 參數中傳回新的、秘密、工作階段金鑰的控制碼。
4.  此時，匯入的 Diffie-Hellman 是 **CALG \_ AGREEDKEY \_ ANY** 類型。 您必須先將金鑰轉換成工作階段金鑰類型，才能使用金鑰。 這是藉由呼叫 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) 函式，並將 *DwParam* 設定為 **KP \_ ALGID** ，並將 *>pbdata* 設定為代表工作階段金鑰的 [**ALG \_ 識別碼**](alg-id.md) 值指標（例如 **CALG \_ RC4**）來完成。 在 [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) 或 [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) 函數中使用共用金鑰之前，必須先轉換金鑰。 在轉換金鑰類型之前對這些函式進行的呼叫將會失敗。
5.  秘密工作階段金鑰現在已準備好用於加密或解密。
6.  當不再需要索引鍵時，請呼叫 [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) 函式來終結金鑰控制碼。

## <a name="exporting-a-diffie-hellman-private-key"></a>匯出 Diffie-Hellman 的私密金鑰

若要匯出 Diffie-Hellman 的私密金鑰，請執行下列步驟：

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 函數，以取得 Microsoft Diffie-Hellman 密碼編譯提供者的控制碼。
2.  藉由呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函式來建立新的金鑰，或藉由呼叫 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) 函式來取出現有的金鑰，以建立 Diffie-Hellman 索引鍵。
3.  藉由呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)函式來建立 Diffie-Hellman 的 [*私密金鑰 BLOB*](../secgloss/p-gly.md) ，並在 *dwBlobType* 參數中傳遞 **PRI加值稅EKEYBLOB** ，並將控制碼傳遞至 *hKey* 參數中 Diffie-Hellman 的索引鍵。
4.  當不再需要金鑰控制碼時，請呼叫 [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) 函式來終結金鑰控制碼。

## <a name="example-code"></a>範例程式碼

下列範例顯示如何建立、匯出、匯入和使用 Diffie-Hellman 金鑰來執行金鑰交換。


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
