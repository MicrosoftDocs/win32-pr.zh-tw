---
description: 如果您想要存取的 XML web service 是藉由公開 COM + 應用程式所建立，請考慮在用戶端啟動的物件中存取它， (CAO) 模式，這樣可避免產生 proxy 的執行時間，並使用持續連線來提高效能。
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: 以 CAO 模式存取 XML Web Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970722"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>以 CAO 模式存取 XML Web Service

如果您想要存取的 XML web service 是藉由公開 COM + 應用程式所建立，請考慮在用戶端啟動的物件中存取它， (CAO) 模式，這樣可避免產生 proxy 的執行時間，並使用持續連線來提高效能。 若要以 CAO 模式存取 XML web service，請先從您的伺服器在 proxy 模式中 [匯出](exporting-a-soap-enabled-application.md) 對應的啟用 SOAP 的應用程式，然後將應用程式匯 [入](importing-a-soap-enabled-application.md) 至您想要將應用程式當作 XML web service 存取的用戶端。 然後，應用程式的元件可以在用戶端上具現化，就像是本機應用程式的元件一樣，例如，使用 **GetObject** 和 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。

## <a name="user-interface"></a>使用者介面

不適用。

## <a name="visual-basic"></a>Visual Basic

下列 Visual Basic 程式碼片段說明如何使用以 CAO 模式公開為 XML web service 的 COM + 應用程式的元件。


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

下列程式碼片段說明如何使用以 CAO 模式公開為 XML web service 的 COM + 應用程式的元件。


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 WKO 模式中存取 XML Web Service](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[COM + SOAP 服務總覽](com--soap-service-overview.md)
</dt> <dt>

[建立 XML Web Service](creating-xml-web-services.md)
</dt> <dt>

[保護 XML Web Service](securing-xml-web-services.md)
</dt> </dl>

 

 
