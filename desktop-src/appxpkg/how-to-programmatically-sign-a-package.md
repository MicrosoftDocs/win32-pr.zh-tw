---
title: '如何以程式設計方式簽署應用程式套件 (c + +) '
description: 瞭解如何使用 SignerSignEx2 函數來簽署應用程式套件。
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310ba2a934a6986809329a12afa8ee20b2f6591
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681703"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a><span data-ttu-id="687c8-103">如何以程式設計方式簽署應用程式套件 (c + +) </span><span class="sxs-lookup"><span data-stu-id="687c8-103">How to programmatically sign an app package (C++)</span></span>

<span data-ttu-id="687c8-104">瞭解如何使用 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函數來簽署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="687c8-104">Learn how to sign an app package by using the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span>

<span data-ttu-id="687c8-105">如果您想要使用 [封裝 API](interfaces.md)以程式設計方式建立 Windows 應用程式套件，您也必須先簽署應用程式套件，才能進行部署。</span><span class="sxs-lookup"><span data-stu-id="687c8-105">If you want to programmatically create Windows app packages by using the [Packaging API](interfaces.md), you also need to sign the app packages before they can be deployed.</span></span> <span data-ttu-id="687c8-106">封裝 API 未提供用來簽署應用程式套件的特殊方法。</span><span class="sxs-lookup"><span data-stu-id="687c8-106">The Packaging API doesn't provide a specialized method for signing app packages.</span></span> <span data-ttu-id="687c8-107">相反地，請使用標準 [密碼編譯功能](/windows/desktop/SecCrypto/cryptography-functions) 來簽署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="687c8-107">Instead, use the standard [cryptography functions](/windows/desktop/SecCrypto/cryptography-functions) to sign your app packages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="687c8-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="687c8-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="687c8-109">技術</span><span class="sxs-lookup"><span data-stu-id="687c8-109">Technologies</span></span>

-   <span data-ttu-id="687c8-110">[程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="687c8-110">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   [<span data-ttu-id="687c8-111">封裝、部署及查詢 Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="687c8-111">Packaging, deployment, and query of Windows apps</span></span>](appx-portal.md)
-   [<span data-ttu-id="687c8-112">密碼編譯功能</span><span class="sxs-lookup"><span data-stu-id="687c8-112">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a><span data-ttu-id="687c8-113">必要條件</span><span class="sxs-lookup"><span data-stu-id="687c8-113">Prerequisites</span></span>

-   <span data-ttu-id="687c8-114">您必須擁有已封裝的 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="687c8-114">You need to have a packaged Windows app.</span></span> <span data-ttu-id="687c8-115">如需建立應用程式套件的相關資訊，請參閱 [如何建立應用程式套件](how-to-create-a-package.md)。</span><span class="sxs-lookup"><span data-stu-id="687c8-115">For info about creating an app package, see [How to create an app package](how-to-create-a-package.md).</span></span>
-   <span data-ttu-id="687c8-116">您需要有適用于簽署應用程式套件的程式碼簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="687c8-116">You need to have a code signing certificate that is appropriate for signing the app package.</span></span> <span data-ttu-id="687c8-117">如需建立測試程式碼簽署憑證的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。</span><span class="sxs-lookup"><span data-stu-id="687c8-117">For info about creating a test code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span> <span data-ttu-id="687c8-118">將此簽署憑證載入至 [**憑證 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) 結構。</span><span class="sxs-lookup"><span data-stu-id="687c8-118">Load this signing certificate into a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="687c8-119">例如，您可以使用 [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) 和 [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) 載入簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="687c8-119">For example, you can use [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) and [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) to load a signing certificate.</span></span>
-   <span data-ttu-id="687c8-120">Windows 8 引進 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函式。</span><span class="sxs-lookup"><span data-stu-id="687c8-120">Windows 8 introduces the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span> <span data-ttu-id="687c8-121">當您簽署 Windows 應用程式套件時，請使用 **SignerSignEx2** 。</span><span class="sxs-lookup"><span data-stu-id="687c8-121">Use **SignerSignEx2** when you sign Windows app packages.</span></span>

## <a name="instructions"></a><span data-ttu-id="687c8-122">指示</span><span class="sxs-lookup"><span data-stu-id="687c8-122">Instructions</span></span>

### <a name="step-1-define-the-required-structures-for-signersignex2"></a><span data-ttu-id="687c8-123">步驟1：定義 SignerSignEx2 的必要結構</span><span class="sxs-lookup"><span data-stu-id="687c8-123">Step 1: Define the required structures for SignerSignEx2</span></span>

<span data-ttu-id="687c8-124">除了 Wincrypt .h 標頭之外， [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函式也取決於許多未在 SDK 標頭檔中定義的結構。</span><span class="sxs-lookup"><span data-stu-id="687c8-124">In addition to the Wincrypt.h header, the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function depends on many structures that aren't defined in any SDK header file.</span></span> <span data-ttu-id="687c8-125">若要使用 **SignerSignEx2**，您必須自行定義這些結構：</span><span class="sxs-lookup"><span data-stu-id="687c8-125">To use **SignerSignEx2**, you must define these structures yourself:</span></span>


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



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a><span data-ttu-id="687c8-126">步驟2：呼叫 SignerSignEx2 來簽署應用程式套件</span><span class="sxs-lookup"><span data-stu-id="687c8-126">Step 2: Call SignerSignEx2 to sign the app package</span></span>

<span data-ttu-id="687c8-127">定義上一個步驟中指定的必要結構之後，您可以使用 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函式上的任何可用選項來簽署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="687c8-127">After you define the required structures that are specified in the previous step, you can use any of the options available on the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function to sign an app package.</span></span> <span data-ttu-id="687c8-128">當您搭配使用 **SignerSignEx2** 與 Windows 應用程式套件時，適用下列限制：</span><span class="sxs-lookup"><span data-stu-id="687c8-128">When you use **SignerSignEx2** with Windows app packages, these restrictions apply:</span></span>

-   <span data-ttu-id="687c8-129">當您簽署應用程式封裝時，您必須提供指向 **APPX \_ SIP \_ 用戶端 \_ 資料** 結構的指標作為 *pSipData* 參數。</span><span class="sxs-lookup"><span data-stu-id="687c8-129">You must provide a pointer to an **APPX\_SIP\_CLIENT\_DATA** structure as the *pSipData* parameter when you sign an app package.</span></span> <span data-ttu-id="687c8-130">您必須使用您用來簽署應用程式套件的相同參數，填入 **APPX \_ SIP \_ 用戶端 \_ 資料** 的 **pSignerParams** 成員。</span><span class="sxs-lookup"><span data-stu-id="687c8-130">You must populate the **pSignerParams** member of **APPX\_SIP\_CLIENT\_DATA** with the same parameters that you use to sign the app package.</span></span> <span data-ttu-id="687c8-131">若要這樣做，請在 **簽署者 \_ SIGN \_ EX2 \_ PARAMS** 結構上定義您想要的參數，將此結構的位址指派給 **PSignerParams**，然後在您呼叫 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)時直接參考結構的成員。</span><span class="sxs-lookup"><span data-stu-id="687c8-131">To do this, define your desired parameters on the **SIGNER\_SIGN\_EX2\_PARAMS** structure, assign the address of this structure to **pSignerParams**, and then directly reference the structure's members as well when you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).</span></span>
-   <span data-ttu-id="687c8-132">呼叫 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)之後，您必須在 **PAppxSipState** 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （如果它不是 **Null**）來釋放 *pSipData* 上的 **pAppxSipState** 。</span><span class="sxs-lookup"><span data-stu-id="687c8-132">After you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), you must free the **pAppxSipState** on the *pSipData* by calling [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on **pAppxSipState** if it's not **NULL**.</span></span>
-   <span data-ttu-id="687c8-133">**簽署者簽章 \_ \_ 資訊** 結構的 **algidHash** 成員必須是建立應用程式封裝時所使用的相同雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="687c8-133">The **algidHash** member of the **SIGNER\_SIGNATURE\_INFO** structure must be the same hash algorithm that was used in creating the app package.</span></span> <span data-ttu-id="687c8-134">如需如何從應用程式套件判斷雜湊演算法的詳細資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。</span><span class="sxs-lookup"><span data-stu-id="687c8-134">For info about how to determine the hash algorithm from the app package, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="687c8-135">[MakeAppx](make-appx-package--makeappx-exe-.md)和 Visual Studio 用來建立應用程式套件的 Windows 8 預設演算法為 "ALGIDHASH = CALG \_ SHA \_ 256"。</span><span class="sxs-lookup"><span data-stu-id="687c8-135">The Windows 8 default algorithm that [MakeAppx](make-appx-package--makeappx-exe-.md) and Visual Studio use to create app packages is “algidHash = CALG\_SHA\_256”.</span></span>
-   <span data-ttu-id="687c8-136">如果您想要為應用程式套件上的簽章加上時間戳記，您必須在呼叫 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 期間，提供 **SignerSignEx2** 的選擇性時間戳記參數 (*dwTimestampFlags*、 *pszTimestampAlgorithmOid*、 *pwszHttpTimeStamp*、 *psRequest*) 。</span><span class="sxs-lookup"><span data-stu-id="687c8-136">If you want to time stamp the signature on the app package as well, you must do so during the call to [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) by providing **SignerSignEx2**'s optional time stamping parameters (*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*).</span></span> <span data-ttu-id="687c8-137">不支援在已簽署的應用程式套件上呼叫 [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) 或其 variant。</span><span class="sxs-lookup"><span data-stu-id="687c8-137">Calling [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) or its variants on an app package that is already signed is unsupported.</span></span>

<span data-ttu-id="687c8-138">以下是顯示如何呼叫 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)的一些範例程式碼：</span><span class="sxs-lookup"><span data-stu-id="687c8-138">Here is some example code that shows how to call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):</span></span>


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



## <a name="remarks"></a><span data-ttu-id="687c8-139">備註</span><span class="sxs-lookup"><span data-stu-id="687c8-139">Remarks</span></span>

<span data-ttu-id="687c8-140">簽署應用程式套件之後，您也可以使用 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) 函式搭配 **WINTRUST \_ 動作 \_ 一般 \_ 驗證 \_ V2**，嘗試以程式設計方式驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="687c8-140">After you sign the app package, you can also attempt to validate the signature programmatically by using the [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) function with **WINTRUST\_ACTION\_GENERIC\_VERIFY\_V2**.</span></span> <span data-ttu-id="687c8-141">在此情況下，不需要特別考慮使用 **WinVerifyTrust** 搭配 Windows 應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="687c8-141">There are no special considerations in this case for using **WinVerifyTrust** with Windows app packages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="687c8-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="687c8-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="687c8-143">[程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="687c8-143">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="687c8-144">封裝 API</span><span class="sxs-lookup"><span data-stu-id="687c8-144">Packaging API</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="687c8-145">密碼編譯功能</span><span class="sxs-lookup"><span data-stu-id="687c8-145">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 