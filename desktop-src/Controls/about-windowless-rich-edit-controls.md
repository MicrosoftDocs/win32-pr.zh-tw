---
title: 關於無視窗的 Rich Edit 控制項
description: 無視窗的 rich edit 控制項（也稱為文字服務物件）是一種物件，可提供豐富編輯控制項的功能，而不需提供視窗。
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933633"
---
# <a name="about-windowless-rich-edit-controls"></a><span data-ttu-id="7fb6f-103">關於無視窗的 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="7fb6f-103">About Windowless Rich Edit Controls</span></span>

<span data-ttu-id="7fb6f-104">無視窗的 rich edit 控制項（也稱為文字服務物件）是一種物件，可提供 [豐富編輯控制項](rich-edit-controls.md) 的功能，而不需提供視窗。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-104">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span> <span data-ttu-id="7fb6f-105">為了提供視窗的功能，例如接收訊息的能力，以及可以繪製的裝置內容，無視窗的豐富編輯控制項會使用一對介面： [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 和 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-105">To provide the functionality of a window, such as the ability to receive messages and a device context into which it can draw, windowless rich edit controls use a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

<span data-ttu-id="7fb6f-106">若要建立無視窗的 rich edit 控制項，請呼叫 [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) 函式，並使用 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) 介面的實作為指標。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-106">To create a windowless rich edit control, call the [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function with a pointer to your implementation of the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span> <span data-ttu-id="7fb6f-107">**CreateTextServices** 會傳回 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 指標，您可以查詢該指標來取得無視窗控制項之 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 實的指標。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-107">**CreateTextServices** returns an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer that you can query to retrieve a pointer to the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) implementation of the windowless control.</span></span>

<span data-ttu-id="7fb6f-108">Msftedit.dll 匯出 (IID **) 的介面識別碼，您 \_** 可以使用此識別碼來查詢 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices)介面的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)指標。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-108">Msftedit.dll exports an interface identifier (IID) called **IID\_ITextServices** that you can use to query the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer for the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="7fb6f-109">下列範例示範如何取出 **IID \_ ITextServices** ，並用它來取得 **ITextServices** 介面。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-109">The following example shows how to retrieve **IID\_ITextServices** and use it to get the **ITextServices** interface.</span></span>


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



<span data-ttu-id="7fb6f-110">Msftedit.dll 也會匯出名為 **iid \_ ITextHost** 的介面識別碼 (iid) ，它可以用類似的方式來查詢 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) 介面。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-110">Msftedit.dll also exports an interface identifier (IID) called **IID\_ITextHost** that can be used in a similar manner to query for the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span>

<span data-ttu-id="7fb6f-111">[**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)介面具有可無視窗控制項呼叫的方法，以抓取視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-111">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface has methods that the windowless control calls to retrieve information about your window.</span></span> <span data-ttu-id="7fb6f-112">例如，文字服務物件會呼叫 [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) 方法，以抓取可以繪製的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-112">For example, the text services object calls the [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) method to retrieve a device context into which it can draw.</span></span> <span data-ttu-id="7fb6f-113">無視窗控制項會呼叫 [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) 方法，以傳送通知給文字主機，例如豐富的編輯通知訊息。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-113">The windowless control calls the [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method to send notifications, such as the rich edit notification messages, to the text host.</span></span> <span data-ttu-id="7fb6f-114">文字服務物件會呼叫其他 **ITextHost** 方法，以要求文字主機執行其他與視窗相關的服務。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-114">The text services object calls other **ITextHost** methods to request the text host to perform other window-related services.</span></span> <span data-ttu-id="7fb6f-115">例如， [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) 方法會要求文字主機將矩形新增至視窗的更新區域。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-115">For example, the [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) method requests the text host to add a rectangle to the window's update region.</span></span>

<span data-ttu-id="7fb6f-116">標準 rich edit 控制項有一個視窗程式，可處理來自您應用程式的系統訊息和訊息。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-116">A standard rich edit control has a window procedure that processes system messages and messages from your application.</span></span> <span data-ttu-id="7fb6f-117">您可以使用控制項的視窗控制碼來傳送訊息，以執行文字編輯和其他作業。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-117">You can use the control's window handle to send it messages for performing text editing and other operations.</span></span> <span data-ttu-id="7fb6f-118">但是無視窗的 rich edit 控制項沒有視窗程式可接收和處理訊息。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-118">But a windowless rich edit control has no window procedure to receive and process messages.</span></span> <span data-ttu-id="7fb6f-119">相反地，它會提供 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 介面。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-119">Instead, it provides an [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="7fb6f-120">若要將訊息傳送至無視窗的 rich edit 控制項，請呼叫 [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) 方法。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-120">To send messages to a windowless rich edit control, call the [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) method.</span></span> <span data-ttu-id="7fb6f-121">您可以使用這個方法來傳送任何豐富的編輯郵件，或傳遞影響控制項的其他訊息，例如滑鼠或鍵盤輸入的系統訊息。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-121">You can use this method to send any of the rich edit messages or to pass on other messages that affect the control, such as system messages for mouse or keyboard input.</span></span>

<span data-ttu-id="7fb6f-122">您也可以將文字服務物件建立為 [COM 匯總物件](/windows/desktop/com/aggregation)的一部分。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-122">You can also create the text services object as part of a [COM-aggregated object](/windows/desktop/com/aggregation).</span></span> <span data-ttu-id="7fb6f-123">這可讓您輕鬆地使用無視窗元件物件模型來匯總文字服務物件 (COM) 物件。</span><span class="sxs-lookup"><span data-stu-id="7fb6f-123">This makes it easy to aggregate the text services object with a windowless Component Object Model (COM) object.</span></span>

 

 