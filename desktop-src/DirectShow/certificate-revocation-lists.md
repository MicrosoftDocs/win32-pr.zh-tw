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
# <a name="certificate-revocation-lists"></a>憑證撤銷清單

本主題說明使用認證的輸出保護通訊協定 (COPP) 時，如何檢查憑證撤銷清單 (CRL) 是否已撤銷驅動程式。

CRL 包含已撤銷憑證的摘要，而且只能由 Microsoft 提供及簽署。 CRL 是透過數位版權管理 (DRM) 授權散發。 CRL 可以撤銷驅動程式憑證鏈中的任何憑證。 如果鏈中有任何憑證遭到撤銷，則該憑證和鏈中的所有憑證也會一併撤銷。

若要取得 CRL，應用程式必須使用 Windows Media Format SDK 9 版或更新版本，然後執行下列步驟：

1.  呼叫 **WMCreateReader** 來建立 Windows MEDIA Format SDK 讀取器物件。
2.  查詢 **IWMDRMReader** 介面的 reader 物件。
3.  呼叫 **IWMDRMReader：： GetDRMProperty** ，其值為 g \_ wszWMDRMNet \_ 撤銷以取得 CRL。 您必須呼叫這個方法兩次：一次是取得要配置的緩衝區大小，以及一次填滿緩衝區。 第二個呼叫會傳回包含 CRL 的字串。 整個字串是以64為基礎的編碼。
4.  將 base-64 編碼的字串解碼。 您可以使用 **CryptStringToBinary** 函數來執行此動作。 此函數是 CryptoAPI 的一部分。

> [!Note]  
> 若要使用 **IWMDRMReader** 介面，您必須從 Microsoft 取得靜態 DRM 程式庫，並將您的應用程式連結至此程式庫檔案。 如需詳細資訊，請參閱 Windows Media Format SDK 檔中的「取得必要的 DRM 程式庫」主題。

 

如果使用者的電腦上沒有 CRL， **GetDRMProperty** 方法會傳回 NS \_ E \_ DRM \_ 不受支援的 \_ 屬性。 目前，取得 CRL 的唯一方法是取得 DRM 授權。

下列程式碼顯示會傳回 CRL 的函式：


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



接下來，應用程式必須確認 CRL 是否有效。 若要這樣做，請確認 crl 憑證（屬於 CRL 的一部分）是由 Microsoft 根憑證直接簽署，且 SignCRL 元素值設定為1。 此外，請確認 CRL 的簽章。

在 CRL 經過驗證之後，應用程式便可加以儲存。 您也應該在儲存之前檢查 CRL 版本號碼，讓應用程式一律儲存最新版本。

CRL 的格式如下。



| 區段            | 目錄                                                             |
|--------------------|----------------------------------------------------------------------|
| 標頭             | 32位 CRL version32 位專案數                           |
| 撤銷專案 | 多個160位撤銷專案                                  |
| 憑證        | 32位憑證 lengthVariable 長度憑證                 |
| 簽名          | 8位簽章 type16 位簽章 lengthVariable 長度簽名 |



 

> [!Note]  
> 所有整數值都不帶正負號，而且會以位元組由大到小的 (網路位元組順序表示) 標記法。

 

CRL 區段描述

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>頭
</dt> <dd>

標頭包含 crl 的版本號碼，以及 CRL 中的撤銷專案數目。 CRL 可以包含零或多個專案。

</dd> <dt>

<span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>撤銷專案
</dt> <dd>

每個撤銷專案都是已撤銷憑證的160位摘要。 將此摘要與憑證中的 DigestValue 元素做比較。

</dd> <dt>

<span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>證書
</dt> <dd>

憑證區段包含32位的值，指出 XML 憑證與其憑證鏈的長度 (位元組) ，以及包含憑證授權單位單位之 XML 憑證 (CA) 的位元組陣列，以及具有 Microsoft 做為根的憑證鏈。 憑證必須由有權發出 Crl 的 CA 簽署。

> [!Note]  
> 憑證不得以 null 終止。

 

</dd> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>簽名
</dt> <dd>

Signature 區段包含簽章類型和長度，以及數位簽章本身。 8位類型設定為2，表示它使用 SHA-1 與1024位 RSA 加密。 長度為16位值，其中包含數位簽章的長度（以位元組為單位）。 數位簽章是在 CRL 的所有先前區段中計算。

簽章是使用 PKCS 1 中定義的 RSASSA-PKCS-PSS 數位簽章配置來計算 \# (2.1 版) 。 雜湊函式是 SHA-1，在聯邦資訊處理標準 (FIPS) 180-2 中定義，而遮罩產生函數則是及 MGF1，它是在 PKCS \# 1 () 2.1 版的第 b. 節中定義。 RSASP1 和 RSAVP1 作業會使用 RSA 搭配1024位模數，並具有65537的驗證指數。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



