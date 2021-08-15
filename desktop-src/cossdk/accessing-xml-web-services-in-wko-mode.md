---
description: 您可以存取及使用任何 xml web service，即使該 xml web service 不是使用 com + 或甚至 Microsoft Windows 建立的，只要 xml web service 發佈其語法的 WSDL 描述即可。
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: 在 WKO 模式中存取 XML Web Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f412a1ec6493e713d2635136b2c4e82063cde56c30358653e476f300ffd2ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129400"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>在 WKO 模式中存取 XML Web Service

您可以存取及使用任何 xml web service，即使該 xml web service 不是使用 com + 或甚至 Microsoft Windows 建立的，只要 xml web service 發佈其語法的 WSDL 描述即可。 只要使用 soap： wsdl = URL 標記建立元件的實例，其中 URL 是您想要存取之 XML web service 的 WSDL 描述 URL。 這是已知的物件 (存取 XML web service 的 WKO) 模式。

您可以呼叫物件的方法，而不需要任何特殊考慮。 XML web service 可透過 SOAP 查詢來存取，並以透明的方式解讀回應。

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

不適用。

## <a name="visual-basic"></a>Visual Basic

下列 Microsoft Visual Basic 程式碼片段說明如何在 WKO 模式中使用 XML web service。


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



在此程式碼片段中，說明如何使用已公開為 XML web service 的 COM + 應用程式元件，servername 是提供 XML web service 之伺服器的完整功能變數名稱;vroot 是公開 XML web service 的 IIS 虛擬根目錄;progID 是您想要使用之元件的 ProgID。

## <a name="cc"></a>C/C++

下列程式碼片段說明如何在 WKO 模式中使用 XML web service。


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



在此程式碼片段中，說明如何使用已公開為 XML web service 的 COM + 應用程式元件，servername 是提供 XML web service 之伺服器的完整功能變數名稱;vroot 是公開 XML web service 的 IIS 虛擬根目錄;progID 是您想要使用之元件的 ProgID。

## <a name="remarks"></a>備註

在 WKO 模式中第一次存取 XML web service 時，COM + 會產生 proxy 用戶端，並在背景中進行編譯。 此執行時間產生和在 WKO 模式中缺少持續連線，可大幅降低與 CAO 模式相比的效能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[以 CAO 模式存取 XML Web Service](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[COM + SOAP 服務總覽](com--soap-service-overview.md)
</dt> <dt>

[建立 XML Web Service](creating-xml-web-services.md)
</dt> <dt>

[保護 XML Web Service](securing-xml-web-services.md)
</dt> </dl>

 

 



