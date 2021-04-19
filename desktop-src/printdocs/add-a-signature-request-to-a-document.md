---
description: 本主題說明如何將簽章要求新增至 XPS 檔。
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: 將簽名要求新增至 XPS 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994452"
---
# <a name="add-a-signature-request-to-an-xps-document"></a>將簽名要求新增至 XPS 檔

本主題說明如何將簽章要求新增至 XPS 檔。 簽章要求會在使用者同意簽章意圖時提示使用者簽署檔。

在您的程式中使用下列程式碼範例之前，請閱讀 [一般數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作中的免責聲明。

若要將簽章要求新增至 XPS 檔：

1.  將 XPS 檔載入到簽章管理員中，如初始化簽章 [管理員](initialize-the-signature-manager.md)中所述。
2.  將簽章區塊加入至簽章管理員。
3.  在新的簽章區塊中建立簽章要求。
4.  設定簽章要求的屬性：
    1.  設定簽章意圖。
    2.  設定 (要求的簽署者) 要求其簽章的人員名稱。
    3.  設定需要簽章的日期。
    4.  視需要設定其他簽章屬性。

下列程式碼範例說明如何將簽章要求加入至 XPS 檔。


```C++
HRESULT 
AddSignatureRequestToDocument (
    __in IXpsSignatureManager    *signatureManager,
    __in LPCWSTR                reasonForSignatureRequest,
    __in LPCWSTR                nameOfRequestedSigner,
    __in LPCWSTR                requestSignByDate
)
{
    HRESULT                  hr = S_OK;
    IXpsSignatureBlock       *signatureDefinition = NULL;
    IXpsSignatureRequest     *signatureRequest = NULL;
    
    // Create a new signature block and get a pointer to it
    hr = signatureManager->AddSignatureBlock (NULL, 0, &signatureDefinition);
    
    if (SUCCEEDED(hr)) {
        // Create a new signature request to use for this signature block
        hr = signatureDefinition->CreateRequest(NULL, &signatureRequest);
    }

    if (SUCCEEDED(hr)) {
        // Initialize the properties of the signature request

        //  Set the string that describes the purpose of the signature
        //  to the person who will sign the document.
        hr = signatureRequest->SetIntent(reasonForSignatureRequest);
    }

    if (SUCCEEDED(hr)) {
        //  Set the name of the person whose signature is requested.
        hr = signatureRequest->SetRequestedSigner(nameOfRequestedSigner);
    }

    if (SUCCEEDED(hr)) {
        //  Set the date that the person should sign the document.
        //  The person is requested to sign the document on or before
        //   the date specified in this field. Refer to the help text
        //   for the correct format of this string.
        hr = signatureRequest->SetRequestSignByDate(requestSignByDate);
    }

    if (NULL != signatureDefinition) signatureDefinition->Release();
    if (NULL != signatureRequest) signatureRequest->Release();

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**在本節中使用**
</dt> <dt>

[**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[**IXpsSignatureBlock::CreateRequest**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::AddSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[**IXpsSignatureRequest::SetIntent**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[**IXpsSignatureRequest::SetRequestedSigner**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[**IXpsSignatureRequest::SetRequestSignByDate**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[XPS 數位簽章 API 錯誤](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS 檔錯誤](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



