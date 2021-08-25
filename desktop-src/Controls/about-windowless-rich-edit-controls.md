---
title: 關於無視窗的 Rich Edit 控制項
description: 無視窗的 rich edit 控制項（也稱為文字服務物件）是一種物件，可提供豐富編輯控制項的功能，而不需提供視窗。
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b68a2bc0317a884f0516b73b3674d104c4fa6c12f16bdc24960d7ea0ef8bbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922178"
---
# <a name="about-windowless-rich-edit-controls"></a>關於無視窗的 Rich Edit 控制項

無視窗的 rich edit 控制項（也稱為文字服務物件）是一種物件，可提供 [豐富編輯控制項](rich-edit-controls.md) 的功能，而不需提供視窗。 為了提供視窗的功能，例如接收訊息的能力，以及可以繪製的裝置內容，無視窗的豐富編輯控制項會使用一對介面： [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 和 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)。

若要建立無視窗的 rich edit 控制項，請呼叫 [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) 函式，並使用 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) 介面的實作為指標。 **CreateTextServices** 會傳回 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 指標，您可以查詢該指標來取得無視窗控制項之 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 實的指標。

Msftedit.dll 匯出 (IID **) 的介面識別碼，您 \_** 可以使用此識別碼來查詢 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices)介面的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)指標。 下列範例示範如何取出 **IID \_ ITextServices** ，並用它來取得 **ITextServices** 介面。


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



Msftedit.dll 也會匯出名為 **iid \_ ITextHost** 的介面識別碼 (iid) ，它可以用類似的方式來查詢 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) 介面。

[**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)介面具有可無視窗控制項呼叫的方法，以抓取視窗的相關資訊。 例如，文字服務物件會呼叫 [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) 方法，以抓取可以繪製的裝置內容。 無視窗控制項會呼叫 [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) 方法，以傳送通知給文字主機，例如豐富的編輯通知訊息。 文字服務物件會呼叫其他 **ITextHost** 方法，以要求文字主機執行其他與視窗相關的服務。 例如， [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) 方法會要求文字主機將矩形新增至視窗的更新區域。

標準 rich edit 控制項有一個視窗程式，可處理來自您應用程式的系統訊息和訊息。 您可以使用控制項的視窗控制碼來傳送訊息，以執行文字編輯和其他作業。 但是無視窗的 rich edit 控制項沒有視窗程式可接收和處理訊息。 相反地，它會提供 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 介面。 若要將訊息傳送至無視窗的 rich edit 控制項，請呼叫 [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) 方法。 您可以使用這個方法來傳送任何豐富的編輯郵件，或傳遞影響控制項的其他訊息，例如滑鼠或鍵盤輸入的系統訊息。

您也可以將文字服務物件建立為 [COM 匯總物件](/windows/desktop/com/aggregation)的一部分。 這可讓您輕鬆地使用無視窗元件物件模型來匯總文字服務物件 (COM) 物件。

 

 