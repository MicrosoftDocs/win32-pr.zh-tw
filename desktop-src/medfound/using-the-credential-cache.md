---
description: 使用認證快取
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: 使用認證快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974349"
---
# <a name="using-the-credential-cache"></a>使用認證快取

媒體基礎提供 [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) 介面的預設實作為。 執行 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面的應用程式可以使用預設的認證快取物件來儲存使用者的認證。

若要建立預設的認證快取物件，請呼叫 [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) 函數。


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



建立認證快取之後，應用程式可以使用下列方法來取得認證物件、設定使用者認證，以及指定快取選項。

-   若要取得 URL 的認證物件，請呼叫 [**IMFNetCredentialCache：： GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)。

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    如果指定之 URL 的認證不存在於認證快取中， [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) 會建立一個新的認證物件，其中包含空的使用者名稱和密碼值。

-   若要設定 credential 物件的使用者名稱和密碼，請呼叫 [**IMFNetCredential：： SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) 和 [**IMFNetCredential：： SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword)。
-   若要設定 credential 物件的快取選項，請呼叫 [**IMFNetCredentialCache：： SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions)。

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    *DwOptionsFlags* 參數值是在 [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions)列舉中定義。 若要在持續性儲存體中儲存 URL 的使用者認證，請設定 MFNET \_ 認證 \_ 儲存旗標。 如果 [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) 呼叫成功完成，則後續的 [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) 呼叫會搜尋持續性儲存體中的認證。 如果找到相符的結果，這個方法會傳回包含資訊之 credential 物件的指標。

    根據預設，透過網路傳送的使用者認證會經過加密。 若要將此變更為純文字，請設定 MFNET \_ 認證 \_ 允許 \_ 純 \_ 文本旗標。

    若要從登錄中移除資訊，請呼叫 [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) 以取得認證物件，然後呼叫 [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) 並將 *dwOptionsFlags* 設定為 MFNET credential 沒有快取 \_ \_ \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路來源驗證](network-source-authentication.md)
</dt> </dl>

 

 



