---
description: 您可以存取及使用任何 XML web service，即使該 XML web service 不是使用 COM + 或甚至 Microsoft Windows 建立的，只要 XML Web Service 發行其語法的 WSDL 描述即可。
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: 在 WKO 模式中存取 XML Web Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688775"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a><span data-ttu-id="a36e2-103">在 WKO 模式中存取 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="a36e2-103">Accessing XML Web Services in WKO Mode</span></span>

<span data-ttu-id="a36e2-104">您可以存取及使用任何 XML web service，即使該 XML web service 不是使用 COM + 或甚至 Microsoft Windows 建立的，只要 XML Web Service 發行其語法的 WSDL 描述即可。</span><span class="sxs-lookup"><span data-stu-id="a36e2-104">You can access and use any XML web service, even if that XML web service was not created using COM+ or even Microsoft Windows, as long as the XML Web Service publishes a WSDL description of its syntax.</span></span> <span data-ttu-id="a36e2-105">只要使用 soap： wsdl = URL 標記建立元件的實例，其中 URL 是您想要存取之 XML web service 的 WSDL 描述 URL。</span><span class="sxs-lookup"><span data-stu-id="a36e2-105">Just create an instance of the component by using the soap:wsdl=URL moniker, where URL is the URL of the WSDL description of the XML web service you want to access.</span></span> <span data-ttu-id="a36e2-106">這是已知的物件 (存取 XML web service 的 WKO) 模式。</span><span class="sxs-lookup"><span data-stu-id="a36e2-106">This is the well-known object (WKO) mode of accessing XML web services.</span></span>

<span data-ttu-id="a36e2-107">您可以呼叫物件的方法，而不需要任何特殊考慮。</span><span class="sxs-lookup"><span data-stu-id="a36e2-107">The object's methods can be called without any special considerations.</span></span> <span data-ttu-id="a36e2-108">XML web service 可透過 SOAP 查詢來存取，並以透明的方式解讀回應。</span><span class="sxs-lookup"><span data-stu-id="a36e2-108">The XML web service is accessed via a SOAP query, and the response is interpreted transparently.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="a36e2-109">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="a36e2-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="a36e2-110">不適用。</span><span class="sxs-lookup"><span data-stu-id="a36e2-110">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="a36e2-111">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a36e2-111">Visual Basic</span></span>

<span data-ttu-id="a36e2-112">下列 Microsoft Visual Basic 程式碼片段說明如何在 WKO 模式中使用 XML web service。</span><span class="sxs-lookup"><span data-stu-id="a36e2-112">The following Microsoft Visual Basic code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



<span data-ttu-id="a36e2-113">在此程式碼片段中，說明如何使用已公開為 XML web service 的 COM + 應用程式元件，servername 是提供 XML web service 之伺服器的完整功能變數名稱;vroot 是公開 XML web service 的 IIS 虛擬根目錄;progID 是您想要使用之元件的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="a36e2-113">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="cc"></a><span data-ttu-id="a36e2-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="a36e2-114">C/C++</span></span>

<span data-ttu-id="a36e2-115">下列程式碼片段說明如何在 WKO 模式中使用 XML web service。</span><span class="sxs-lookup"><span data-stu-id="a36e2-115">The following code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



<span data-ttu-id="a36e2-116">在此程式碼片段中，說明如何使用已公開為 XML web service 的 COM + 應用程式元件，servername 是提供 XML web service 之伺服器的完整功能變數名稱;vroot 是公開 XML web service 的 IIS 虛擬根目錄;progID 是您想要使用之元件的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="a36e2-116">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="a36e2-117">備註</span><span class="sxs-lookup"><span data-stu-id="a36e2-117">Remarks</span></span>

<span data-ttu-id="a36e2-118">在 WKO 模式中第一次存取 XML web service 時，COM + 會產生 proxy 用戶端，並在背景中進行編譯。</span><span class="sxs-lookup"><span data-stu-id="a36e2-118">When an XML web service is first accessed in WKO mode, COM+ generates a proxy client and compiles it in the background.</span></span> <span data-ttu-id="a36e2-119">此執行時間產生和在 WKO 模式中缺少持續連線，可大幅降低與 CAO 模式相比的效能。</span><span class="sxs-lookup"><span data-stu-id="a36e2-119">This run-time generation and the lack of persistent connections in WKO mode results in significantly reduced performance in comparison to CAO mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a36e2-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="a36e2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a36e2-121">以 CAO 模式存取 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="a36e2-121">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="a36e2-122">COM + SOAP 服務總覽</span><span class="sxs-lookup"><span data-stu-id="a36e2-122">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="a36e2-123">建立 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="a36e2-123">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="a36e2-124">保護 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="a36e2-124">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



