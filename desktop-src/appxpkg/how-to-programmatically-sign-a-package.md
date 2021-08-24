---
title: '如何以程式設計方式簽署應用程式套件 (c + +) '
description: 瞭解如何使用 SignerSignEx2 函數來簽署應用程式套件。
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a91cf2c7b7be674ff14d1ceada59be593a300d7ebf1964ddce4a7a5340ab74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130240"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a>如何以程式設計方式簽署應用程式套件 (c + +) 

瞭解如何使用 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函數來簽署應用程式套件。

如果您想要使用[封裝 API](interfaces.md)以程式設計方式建立 Windows 應用程式套件，您也必須先簽署應用程式套件，才能進行部署。 封裝 API 未提供用來簽署應用程式套件的特殊方法。 相反地，請使用標準 [密碼編譯功能](/windows/desktop/SecCrypto/cryptography-functions) 來簽署應用程式套件。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Windows 應用程式的封裝、部署和查詢](appx-portal.md)
-   [密碼編譯功能](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a>必要條件

-   您需要有封裝的 Windows 應用程式。 如需建立應用程式套件的相關資訊，請參閱 [如何建立應用程式套件](how-to-create-a-package.md)。
-   您需要有適用于簽署應用程式套件的程式碼簽署憑證。 如需建立測試程式碼簽署憑證的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。 將此簽署憑證載入至 [**憑證 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) 結構。 例如，您可以使用 [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) 和 [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) 載入簽署憑證。
-   Windows 8 引進 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)函式。 當您簽署 Windows 應用程式套件時，請使用 **SignerSignEx2** 。

## <a name="instructions"></a>指示

### <a name="step-1-define-the-required-structures-for-signersignex2"></a>步驟1：定義 SignerSignEx2 的必要結構

除了 Wincrypt .h 標頭之外， [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函式也取決於許多未在 SDK 標頭檔中定義的結構。 若要使用 **SignerSignEx2**，您必須自行定義這些結構：


```C++
typedef struct _SIGNER_FILE_INFO
{
    DWORD cbSize;
    LPCWSTR pwszFileName;
    HANDLE hFile;
}SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
 
typedef struct _SIGNER_BLOB_INFO
{
    DWORD cbSize;
    GUID *pGuidSubject;
    DWORD cbBlob;
    BYTE *pbBlob;
    LPCWSTR pwszDisplayName;
}SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
 
typedef struct _SIGNER_SUBJECT_INFO
{
    DWORD cbSize;
    DWORD *pdwIndex;
    DWORD dwSubjectChoice;
    union
    {
        SIGNER_FILE_INFO *pSignerFileInfo;
        SIGNER_BLOB_INFO *pSignerBlobInfo;
    };
}SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
 
// dwSubjectChoice should be one of the following:
#define SIGNER_SUBJECT_FILE    0x01
#define SIGNER_SUBJECT_BLOB    0x02
 
typedef struct _SIGNER_ATTR_AUTHCODE
{
    DWORD cbSize;
    BOOL fCommercial;
    BOOL fIndividual;
    LPCWSTR pwszName;
    LPCWSTR pwszInfo;
}SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
 
typedef struct _SIGNER_SIGNATURE_INFO
{
    DWORD cbSize;
    ALG_ID algidHash;
    DWORD dwAttrChoice;
    union
    {
        SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
    };
    PCRYPT_ATTRIBUTES psAuthenticated;
    PCRYPT_ATTRIBUTES psUnauthenticated;
}SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
 
// dwAttrChoice should be one of the following:
#define SIGNER_NO_ATTR          0x00
#define SIGNER_AUTHCODE_ATTR    0x01
 
typedef struct _SIGNER_PROVIDER_INFO
{
    DWORD cbSize;
    LPCWSTR pwszProviderName;
    DWORD dwProviderType;
    DWORD dwKeySpec;
    DWORD dwPvkChoice;
    union
    {
        LPWSTR pwszPvkFileName;
        LPWSTR pwszKeyContainer;
    };
}SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
 
//dwPvkChoice should be one of the following:
#define PVK_TYPE_FILE_NAME       0x01
#define PVK_TYPE_KEYCONTAINER    0x02
 
typedef struct _SIGNER_SPC_CHAIN_INFO
{
    DWORD cbSize;
    LPCWSTR pwszSpcFile;
    DWORD dwCertPolicy; 
    HCERTSTORE hCertStore;
}SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
 
typedef struct _SIGNER_CERT_STORE_INFO
{
    DWORD cbSize;
    PCCERT_CONTEXT pSigningCert;
    DWORD dwCertPolicy;
    HCERTSTORE hCertStore;
}SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
 
//dwCertPolicy can be a combination of the following flags:
#define SIGNER_CERT_POLICY_STORE            0x01
#define SIGNER_CERT_POLICY_CHAIN            0x02
#define SIGNER_CERT_POLICY_SPC              0x04
#define SIGNER_CERT_POLICY_CHAIN_NO_ROOT    0x08
 
typedef struct _SIGNER_CERT
{
    DWORD cbSize;
    DWORD dwCertChoice;
    union
    {
        LPCWSTR pwszSpcFile;
        SIGNER_CERT_STORE_INFO *pCertStoreInfo;
        SIGNER_SPC_CHAIN_INFO *pSpcChainInfo;
    };
    HWND hwnd;
}SIGNER_CERT, *PSIGNER_CERT;
 
//dwCertChoice should be one of the following
#define SIGNER_CERT_SPC_FILE     0x01
#define SIGNER_CERT_STORE        0x02
#define SIGNER_CERT_SPC_CHAIN    0x03
 
typedef struct _SIGNER_CONTEXT
{
    DWORD cbSize;
    DWORD cbBlob;
    BYTE *pbBlob;
}SIGNER_CONTEXT, *PSIGNER_CONTEXT;
 
typedef struct _SIGNER_SIGN_EX2_PARAMS
{
    DWORD dwFlags;
    PSIGNER_SUBJECT_INFO pSubjectInfo;
    PSIGNER_CERT pSigningCert;
    PSIGNER_SIGNATURE_INFO pSignatureInfo;
    PSIGNER_PROVIDER_INFO pProviderInfo;
    DWORD dwTimestampFlags;
    PCSTR pszAlgorithmOid;
    PCWSTR pwszTimestampURL;
    PCRYPT_ATTRIBUTES pCryptAttrs;
    PVOID pSipData;
    PSIGNER_CONTEXT *pSignerContext;
    PVOID pCryptoPolicy;
    PVOID pReserved;
} SIGNER_SIGN_EX2_PARAMS, *PSIGNER_SIGN_EX2_PARAMS;
 
typedef struct _APPX_SIP_CLIENT_DATA
{
    PSIGNER_SIGN_EX2_PARAMS pSignerParams;
    IUnknown* pAppxSipState;
} APPX_SIP_CLIENT_DATA, *PAPPX_SIP_CLIENT_DATA;
```



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a>步驟2：呼叫 SignerSignEx2 來簽署應用程式套件

定義上一個步驟中指定的必要結構之後，您可以使用 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函式上的任何可用選項來簽署應用程式套件。 當您搭配 Windows 應用程式套件使用 **SignerSignEx2** 時，適用下列限制：

-   當您簽署應用程式封裝時，您必須提供指向 **APPX \_ SIP \_ 用戶端 \_ 資料** 結構的指標作為 *pSipData* 參數。 您必須使用您用來簽署應用程式套件的相同參數，填入 **APPX \_ SIP \_ 用戶端 \_ 資料** 的 **pSignerParams** 成員。 若要這樣做，請在 **簽署者 \_ SIGN \_ EX2 \_ PARAMS** 結構上定義您想要的參數，將此結構的位址指派給 **PSignerParams**，然後在您呼叫 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)時直接參考結構的成員。
-   呼叫 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)之後，您必須在 **PAppxSipState** 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （如果它不是 **Null**）來釋放 *pSipData* 上的 **pAppxSipState** 。
-   **簽署者簽章 \_ \_ 資訊** 結構的 **algidHash** 成員必須是建立應用程式封裝時所使用的相同雜湊演算法。 如需如何從應用程式套件判斷雜湊演算法的詳細資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。 [MakeAppx](make-appx-package--makeappx-exe-.md)和 Visual Studio 用來建立應用程式套件的 Windows 8 預設演算法為 "algidHash = CALG \_ SHA \_ 256"。
-   如果您想要為應用程式套件上的簽章加上時間戳記，您必須在呼叫 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 期間，提供 **SignerSignEx2** 的選擇性時間戳記參數 (*dwTimestampFlags*、 *pszTimestampAlgorithmOid*、 *pwszHttpTimeStamp*、 *psRequest*) 。 不支援在已簽署的應用程式套件上呼叫 [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) 或其 variant。

以下是顯示如何呼叫 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)的一些範例程式碼：


```C++
HRESULT SignAppxPackage(
    _In_ PCCERT_CONTEXT signingCertContext,
    _In_ LPCWSTR packageFilePath)
{
    HRESULT hr = S_OK;
 
    // Initialize the parameters for SignerSignEx2
    DWORD signerIndex = 0;
 
    SIGNER_FILE_INFO fileInfo = {};
    fileInfo.cbSize = sizeof(SIGNER_FILE_INFO);
    fileInfo.pwszFileName = packageFilePath;
 
    SIGNER_SUBJECT_INFO subjectInfo = {};
    subjectInfo.cbSize = sizeof(SIGNER_SUBJECT_INFO);
    subjectInfo.pdwIndex = &signerIndex;
    subjectInfo.dwSubjectChoice = SIGNER_SUBJECT_FILE;
    subjectInfo.pSignerFileInfo = &fileInfo;
 
    SIGNER_CERT_STORE_INFO certStoreInfo = {};
    certStoreInfo.cbSize = sizeof(SIGNER_CERT_STORE_INFO);
    certStoreInfo.dwCertPolicy = SIGNER_CERT_POLICY_CHAIN_NO_ROOT;
    certStoreInfo.pSigningCert = signingCertContext;
 
    SIGNER_CERT cert = {};
    cert.cbSize = sizeof(SIGNER_CERT);
    cert.dwCertChoice = SIGNER_CERT_STORE;
    cert.pCertStoreInfo = &certStoreInfo;
 
    // The algidHash of the signature to be created must match the
    // hash algorithm used to create the app package
    SIGNER_SIGNATURE_INFO signatureInfo = {};
    signatureInfo.cbSize = sizeof(SIGNER_SIGNATURE_INFO);
    signatureInfo.algidHash = CALG_SHA_256; 
    signatureInfo.dwAttrChoice = SIGNER_NO_ATTR;
 
    SIGNER_SIGN_EX2_PARAMS signerParams = {};
    signerParams.pSubjectInfo = &subjectInfo;
    signerParams.pSigningCert = &cert;
    signerParams.pSignatureInfo = &signatureInfo;
 
    APPX_SIP_CLIENT_DATA sipClientData = {};
    sipClientData.pSignerParams = &signerParams;
    signerParams.pSipData = &sipClientData;
 
    // Type definition for invoking SignerSignEx2 via GetProcAddress
    typedef HRESULT (WINAPI *SignerSignEx2Function)(
        DWORD,
        PSIGNER_SUBJECT_INFO,
        PSIGNER_CERT,
        PSIGNER_SIGNATURE_INFO,
        PSIGNER_PROVIDER_INFO,
        DWORD,
        PCSTR,
        PCWSTR,
        PCRYPT_ATTRIBUTES,
        PVOID,
        PSIGNER_CONTEXT *,
        PVOID,
        PVOID); 
 
    // Load the SignerSignEx2 function from MSSign32.dll
    HMODULE msSignModule = LoadLibraryEx(
        L"MSSign32.dll", 
        NULL, 
        LOAD_LIBRARY_SEARCH_SYSTEM32);

    if (msSignModule)
    {
        SignerSignEx2Function SignerSignEx2 = reinterpret_cast<SignerSignEx2Function>(
            GetProcAddress(msSignModule, "SignerSignEx2"));
        if (SignerSignEx2)
        {
            hr = SignerSignEx2(
                signerParams.dwFlags,
                signerParams.pSubjectInfo,
                signerParams.pSigningCert,
                signerParams.pSignatureInfo,
                signerParams.pProviderInfo,
                signerParams.dwTimestampFlags,
                signerParams.pszAlgorithmOid,
                signerParams.pwszTimestampURL,
                signerParams.pCryptAttrs,
                signerParams.pSipData,
                signerParams.pSignerContext,
                signerParams.pCryptoPolicy,
                signerParams.pReserved);
        }
        else
        {
            DWORD lastError = GetLastError();
            hr = HRESULT_FROM_WIN32(lastError);
        }
 
        FreeLibrary(msSignModule);
    }
    else
    {
        DWORD lastError = GetLastError();
        hr = HRESULT_FROM_WIN32(lastError);
    }
 
    // Free any state used during app package signing
    if (sipClientData.pAppxSipState)
    {
        sipClientData.pAppxSipState->Release();
    }
 
    return hr;
}
```



## <a name="remarks"></a>備註

簽署應用程式套件之後，您也可以使用 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) 函式搭配 **WINTRUST \_ 動作 \_ 一般 \_ 驗證 \_ V2**，嘗試以程式設計方式驗證簽章。 在此情況下，不需要特別考慮搭配 Windows 應用程式套件使用 **WinVerifyTrust** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[封裝 API](interfaces.md)
</dt> <dt>

[密碼編譯功能](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 