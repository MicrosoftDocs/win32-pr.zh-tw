---
description: 憑證撤銷清單
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: 憑證撤銷清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106998423"
---
# <a name="certificate-revocation-lists"></a><span data-ttu-id="28f94-103">憑證撤銷清單</span><span class="sxs-lookup"><span data-stu-id="28f94-103">Certificate Revocation Lists</span></span>

<span data-ttu-id="28f94-104">本主題說明使用認證的輸出保護通訊協定 (COPP) 時，如何檢查憑證撤銷清單 (CRL) 是否已撤銷驅動程式。</span><span class="sxs-lookup"><span data-stu-id="28f94-104">This topic describes how to examine the certificate revocation list (CRL) for revoked drivers when using Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="28f94-105">CRL 包含已撤銷憑證的摘要，而且只能由 Microsoft 提供及簽署。</span><span class="sxs-lookup"><span data-stu-id="28f94-105">The CRL contains digests of revoked certificates and can be provided and signed only by Microsoft.</span></span> <span data-ttu-id="28f94-106">CRL 是透過數位版權管理 (DRM) 授權散發。</span><span class="sxs-lookup"><span data-stu-id="28f94-106">The CRL is distributed through digital rights management (DRM) licenses.</span></span> <span data-ttu-id="28f94-107">CRL 可以撤銷驅動程式憑證鏈中的任何憑證。</span><span class="sxs-lookup"><span data-stu-id="28f94-107">The CRL can revoke any certificate in the driver's certificates chain.</span></span> <span data-ttu-id="28f94-108">如果鏈中有任何憑證遭到撤銷，則該憑證和鏈中的所有憑證也會一併撤銷。</span><span class="sxs-lookup"><span data-stu-id="28f94-108">If any certificate in the chain is revoked, then that certificate and all of the certificates below it in the chain are also revoked.</span></span>

<span data-ttu-id="28f94-109">若要取得 CRL，應用程式必須使用 Windows Media Format SDK 9 版或更新版本，然後執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="28f94-109">To get the CRL, the application must use the Windows Media Format SDK, version 9 or later, and perform the following steps:</span></span>

1.  <span data-ttu-id="28f94-110">呼叫 **WMCreateReader** 來建立 Windows MEDIA Format SDK 讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="28f94-110">Call **WMCreateReader** to create the Windows Media Format SDK reader object.</span></span>
2.  <span data-ttu-id="28f94-111">查詢 **IWMDRMReader** 介面的 reader 物件。</span><span class="sxs-lookup"><span data-stu-id="28f94-111">Query the reader object for the **IWMDRMReader** interface.</span></span>
3.  <span data-ttu-id="28f94-112">呼叫 **IWMDRMReader：： GetDRMProperty** ，其值為 g \_ wszWMDRMNet \_ 撤銷以取得 CRL。</span><span class="sxs-lookup"><span data-stu-id="28f94-112">Call **IWMDRMReader::GetDRMProperty** with a value of g\_wszWMDRMNet\_Revocation to get the CRL.</span></span> <span data-ttu-id="28f94-113">您必須呼叫這個方法兩次：一次是取得要配置的緩衝區大小，以及一次填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="28f94-113">You must call this method twice: Once to get the size of the buffer to allocate, and once to fill the buffer.</span></span> <span data-ttu-id="28f94-114">第二個呼叫會傳回包含 CRL 的字串。</span><span class="sxs-lookup"><span data-stu-id="28f94-114">The second call returns a string that contains the CRL.</span></span> <span data-ttu-id="28f94-115">整個字串是以64為基礎的編碼。</span><span class="sxs-lookup"><span data-stu-id="28f94-115">The entire string is base-64 encoded.</span></span>
4.  <span data-ttu-id="28f94-116">將 base-64 編碼的字串解碼。</span><span class="sxs-lookup"><span data-stu-id="28f94-116">Decode the base-64 encoded string.</span></span> <span data-ttu-id="28f94-117">您可以使用 **CryptStringToBinary** 函數來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="28f94-117">You can use the **CryptStringToBinary** function to do this.</span></span> <span data-ttu-id="28f94-118">此函數是 CryptoAPI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="28f94-118">This function is part of CryptoAPI.</span></span>

> [!Note]  
> <span data-ttu-id="28f94-119">若要使用 **IWMDRMReader** 介面，您必須從 Microsoft 取得靜態 DRM 程式庫，並將您的應用程式連結至此程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="28f94-119">To use the **IWMDRMReader** interface, you must obtain a static DRM library from Microsoft and link your application to this library file.</span></span> <span data-ttu-id="28f94-120">如需詳細資訊，請參閱 Windows Media Format SDK 檔中的「取得必要的 DRM 程式庫」主題。</span><span class="sxs-lookup"><span data-stu-id="28f94-120">For more information, see the topic "Obtaining the Required DRM Library" in the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="28f94-121">如果使用者的電腦上沒有 CRL， **GetDRMProperty** 方法會傳回 NS \_ E \_ DRM \_ 不受支援的 \_ 屬性。</span><span class="sxs-lookup"><span data-stu-id="28f94-121">If the CRL is not present on the user's computer, the **GetDRMProperty** method returns NS\_E\_DRM\_UNSUPPORTED\_PROPERTY.</span></span> <span data-ttu-id="28f94-122">目前，取得 CRL 的唯一方法是取得 DRM 授權。</span><span class="sxs-lookup"><span data-stu-id="28f94-122">Currently, the only way to obtain the CRL is to acquire a DRM license.</span></span>

<span data-ttu-id="28f94-123">下列程式碼顯示會傳回 CRL 的函式：</span><span class="sxs-lookup"><span data-stu-id="28f94-123">The following code shows a function that returns the CRL:</span></span>


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



<span data-ttu-id="28f94-124">接下來，應用程式必須確認 CRL 是否有效。</span><span class="sxs-lookup"><span data-stu-id="28f94-124">Next, the application must verify that the CRL is valid.</span></span> <span data-ttu-id="28f94-125">若要這樣做，請確認 crl 憑證（屬於 CRL 的一部分）是由 Microsoft 根憑證直接簽署，且 SignCRL 元素值設定為1。</span><span class="sxs-lookup"><span data-stu-id="28f94-125">To do so, verify that the CRL certificate, which is part of the CRL, is directly signed by the Microsoft Root Certificate and has the SignCRL element value set to 1.</span></span> <span data-ttu-id="28f94-126">此外，請確認 CRL 的簽章。</span><span class="sxs-lookup"><span data-stu-id="28f94-126">Also, verify the signature of the CRL.</span></span>

<span data-ttu-id="28f94-127">在 CRL 經過驗證之後，應用程式便可加以儲存。</span><span class="sxs-lookup"><span data-stu-id="28f94-127">After the CRL is verified, the application can store it.</span></span> <span data-ttu-id="28f94-128">您也應該在儲存之前檢查 CRL 版本號碼，讓應用程式一律儲存最新版本。</span><span class="sxs-lookup"><span data-stu-id="28f94-128">The CRL version number should also be checked before storing so that the application always stores the newest version.</span></span>

<span data-ttu-id="28f94-129">CRL 的格式如下。</span><span class="sxs-lookup"><span data-stu-id="28f94-129">The CRL has the following format.</span></span>



| <span data-ttu-id="28f94-130">區段</span><span class="sxs-lookup"><span data-stu-id="28f94-130">Section</span></span>            | <span data-ttu-id="28f94-131">目錄</span><span class="sxs-lookup"><span data-stu-id="28f94-131">Contents</span></span>                                                             |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="28f94-132">標頭</span><span class="sxs-lookup"><span data-stu-id="28f94-132">Header</span></span>             | <span data-ttu-id="28f94-133">32位 CRL version32 位專案數</span><span class="sxs-lookup"><span data-stu-id="28f94-133">32-bit CRL version32-bit number of entries</span></span>                           |
| <span data-ttu-id="28f94-134">撤銷專案</span><span class="sxs-lookup"><span data-stu-id="28f94-134">Revocation Entries</span></span> | <span data-ttu-id="28f94-135">多個160位撤銷專案</span><span class="sxs-lookup"><span data-stu-id="28f94-135">Multiple 160-bit revocation entries</span></span>                                  |
| <span data-ttu-id="28f94-136">憑證</span><span class="sxs-lookup"><span data-stu-id="28f94-136">Certificate</span></span>        | <span data-ttu-id="28f94-137">32位憑證 lengthVariable 長度憑證</span><span class="sxs-lookup"><span data-stu-id="28f94-137">32-bit certificate lengthVariable-length certificate</span></span>                 |
| <span data-ttu-id="28f94-138">簽名</span><span class="sxs-lookup"><span data-stu-id="28f94-138">Signature</span></span>          | <span data-ttu-id="28f94-139">8位簽章 type16 位簽章 lengthVariable 長度簽名</span><span class="sxs-lookup"><span data-stu-id="28f94-139">8-bit signature type16-bit signature lengthVariable-length signature</span></span> |



 

> [!Note]  
> <span data-ttu-id="28f94-140">所有整數值都不帶正負號，而且會以位元組由大到小的 (網路位元組順序表示) 標記法。</span><span class="sxs-lookup"><span data-stu-id="28f94-140">All integer values are unsigned and are represented in big-endian (network byte order) notation.</span></span>

 

<span data-ttu-id="28f94-141">CRL 區段描述</span><span class="sxs-lookup"><span data-stu-id="28f94-141">CRL Section Descriptions</span></span>

<dl> <dt>

<span data-ttu-id="28f94-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>頭</span><span class="sxs-lookup"><span data-stu-id="28f94-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="28f94-143">標頭包含 crl 的版本號碼，以及 CRL 中的撤銷專案數目。</span><span class="sxs-lookup"><span data-stu-id="28f94-143">The header contains the version number of the CRL and the number of revocation entries in the CRL.</span></span> <span data-ttu-id="28f94-144">CRL 可以包含零或多個專案。</span><span class="sxs-lookup"><span data-stu-id="28f94-144">A CRL can contain zero or more entries.</span></span>

</dd> <dt>

<span data-ttu-id="28f94-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>撤銷專案</span><span class="sxs-lookup"><span data-stu-id="28f94-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Revocation entries</span></span>
</dt> <dd>

<span data-ttu-id="28f94-146">每個撤銷專案都是已撤銷憑證的160位摘要。</span><span class="sxs-lookup"><span data-stu-id="28f94-146">Each revocation entry is the 160-bit digest of a revoked certificate.</span></span> <span data-ttu-id="28f94-147">將此摘要與憑證中的 DigestValue 元素做比較。</span><span class="sxs-lookup"><span data-stu-id="28f94-147">Compare this digest with the DigestValue element within the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="28f94-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>證書</span><span class="sxs-lookup"><span data-stu-id="28f94-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span></span>
</dt> <dd>

<span data-ttu-id="28f94-149">憑證區段包含32位的值，指出 XML 憑證與其憑證鏈的長度 (位元組) ，以及包含憑證授權單位單位之 XML 憑證 (CA) 的位元組陣列，以及具有 Microsoft 做為根的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="28f94-149">The certificate section contains a 32-bit value indicating the length (in bytes) of the XML certificate and its certificate chain, along with a byte array that contains both the XML certificate of the Certificate Authority (CA) and the certificate chain that has Microsoft as the Root.</span></span> <span data-ttu-id="28f94-150">憑證必須由有權發出 Crl 的 CA 簽署。</span><span class="sxs-lookup"><span data-stu-id="28f94-150">The certificate must be signed by a CA that has the authority to issue CRLs.</span></span>

> [!Note]  
> <span data-ttu-id="28f94-151">憑證不得以 null 終止。</span><span class="sxs-lookup"><span data-stu-id="28f94-151">The certificate must not be null-terminated.</span></span>

 

</dd> <dt>

<span data-ttu-id="28f94-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>簽名</span><span class="sxs-lookup"><span data-stu-id="28f94-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="28f94-153">Signature 區段包含簽章類型和長度，以及數位簽章本身。</span><span class="sxs-lookup"><span data-stu-id="28f94-153">The signature section contains the signature type and length, and the digital signature itself.</span></span> <span data-ttu-id="28f94-154">8位類型設定為2，表示它使用 SHA-1 與1024位 RSA 加密。</span><span class="sxs-lookup"><span data-stu-id="28f94-154">The 8-bit type is set to 2 to indicate that it uses SHA-1 with 1024-bit RSA encryption.</span></span> <span data-ttu-id="28f94-155">長度為16位值，其中包含數位簽章的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="28f94-155">The length is a 16-bit value containing the length of the digital signature in bytes.</span></span> <span data-ttu-id="28f94-156">數位簽章是在 CRL 的所有先前區段中計算。</span><span class="sxs-lookup"><span data-stu-id="28f94-156">The digital signature is calculated over all prior sections of the CRL.</span></span>

<span data-ttu-id="28f94-157">簽章是使用 PKCS 1 中定義的 RSASSA-PKCS-PSS 數位簽章配置來計算 \# (2.1 版) 。</span><span class="sxs-lookup"><span data-stu-id="28f94-157">The signature is calculated using the RSASSA-PSS digital signature scheme that is defined in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="28f94-158">雜湊函式是 SHA-1，在聯邦資訊處理標準 (FIPS) 180-2 中定義，而遮罩產生函數則是及 MGF1，它是在 PKCS \# 1 () 2.1 版的第 b. 節中定義。</span><span class="sxs-lookup"><span data-stu-id="28f94-158">The hash function is SHA-1, which is defined in Federal Information Processing Standard (FIPS) 180-2, and the mask generation function is MGF1, which is defined in section B.2.1 in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="28f94-159">RSASP1 和 RSAVP1 作業會使用 RSA 搭配1024位模數，並具有65537的驗證指數。</span><span class="sxs-lookup"><span data-stu-id="28f94-159">The RSASP1 and RSAVP1 operations use RSA with a 1024-bit modulus with a verification exponent of 65537.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="28f94-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="28f94-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f94-161">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="28f94-161">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



