---
description: 本主題說明如何初始化簽章管理員以搭配 XPS 檔使用。
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: 初始化簽章管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984734"
---
# <a name="initialize-the-signature-manager"></a>初始化簽章管理員

本主題說明如何初始化簽章管理員以搭配 XPS 檔使用。

在您的程式中使用下列程式碼範例之前，請閱讀 [一般數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作中的免責聲明。

若要使用密碼編譯 API 的 Windows 7 功能，請定義 **CRYPT \_ OID \_ 資訊 \_ 具有 \_ 額外的 \_ 欄位** 符號，如下所示：


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



接下來，呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)以具現化 [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)介面，如下列程式碼範例所示。


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)具現化的介面只能由一個 XPS 檔使用，必須先呼叫 [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile)或 [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream)載入，然後再呼叫任何其他方法。

在具現化 [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) 介面並載入 XPS 檔之後，簽章管理員便已可供使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[簽署檔](sign-a-document.md)
</dt> <dt>

[將簽名要求新增至 XPS 檔](add-a-signature-request-to-a-document.md)
</dt> <dt>

[驗證檔簽章](verify-document-signatures.md)
</dt> <dt>

**在本節中使用**
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[XPS 數位簽章 API 錯誤](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS 檔錯誤](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
