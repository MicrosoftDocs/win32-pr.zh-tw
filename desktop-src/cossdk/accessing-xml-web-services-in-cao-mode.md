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
# <a name="accessing-xml-web-services-in-cao-mode"></a><span data-ttu-id="adf92-103">以 CAO 模式存取 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="adf92-103">Accessing XML Web Services in CAO Mode</span></span>

<span data-ttu-id="adf92-104">如果您想要存取的 XML web service 是藉由公開 COM + 應用程式所建立，請考慮在用戶端啟動的物件中存取它， (CAO) 模式，這樣可避免產生 proxy 的執行時間，並使用持續連線來提高效能。</span><span class="sxs-lookup"><span data-stu-id="adf92-104">If the XML web service you want to access was created by exposing a COM+ application, consider accessing it in client-activated object (CAO) mode, which avoids the run-time generation of a proxy and increases performance by using persistent connections.</span></span> <span data-ttu-id="adf92-105">若要以 CAO 模式存取 XML web service，請先從您的伺服器在 proxy 模式中 [匯出](exporting-a-soap-enabled-application.md) 對應的啟用 SOAP 的應用程式，然後將應用程式匯 [入](importing-a-soap-enabled-application.md) 至您想要將應用程式當作 XML web service 存取的用戶端。</span><span class="sxs-lookup"><span data-stu-id="adf92-105">To access an XML web service in CAO mode, first [export](exporting-a-soap-enabled-application.md) the corresponding SOAP-enabled application from your server in proxy mode and then [import](importing-a-soap-enabled-application.md) the application into the client from which you want to access the application as an XML web service.</span></span> <span data-ttu-id="adf92-106">然後，應用程式的元件可以在用戶端上具現化，就像是本機應用程式的元件一樣，例如，使用 **GetObject** 和 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="adf92-106">The application's components can then be instantiated on the client just like the components of local applications—for example, using **GetObject** and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="user-interface"></a><span data-ttu-id="adf92-107">使用者介面</span><span class="sxs-lookup"><span data-stu-id="adf92-107">User Interface</span></span>

<span data-ttu-id="adf92-108">不適用。</span><span class="sxs-lookup"><span data-stu-id="adf92-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="adf92-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="adf92-109">Visual Basic</span></span>

<span data-ttu-id="adf92-110">下列 Visual Basic 程式碼片段說明如何使用以 CAO 模式公開為 XML web service 的 COM + 應用程式的元件。</span><span class="sxs-lookup"><span data-stu-id="adf92-110">The following Visual Basic code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a><span data-ttu-id="adf92-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="adf92-111">C/C++</span></span>

<span data-ttu-id="adf92-112">下列程式碼片段說明如何使用以 CAO 模式公開為 XML web service 的 COM + 應用程式的元件。</span><span class="sxs-lookup"><span data-stu-id="adf92-112">The following code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a><span data-ttu-id="adf92-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="adf92-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf92-114">在 WKO 模式中存取 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="adf92-114">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="adf92-115">COM + SOAP 服務總覽</span><span class="sxs-lookup"><span data-stu-id="adf92-115">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="adf92-116">建立 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="adf92-116">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="adf92-117">保護 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="adf92-117">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 
