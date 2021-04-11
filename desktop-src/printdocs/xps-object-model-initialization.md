---
description: 說明如何初始化 XPS OM，以允許程式建立 XPS 檔。
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: 初始化 XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318908"
---
# <a name="initialize-an-xps-om"></a><span data-ttu-id="b8785-103">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="b8785-103">Initialize an XPS OM</span></span>

<span data-ttu-id="b8785-104">說明如何初始化 XPS OM，以允許程式建立 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="b8785-104">Describes how to initialize an XPS OM, which allows a program to create an XPS document.</span></span>

<span data-ttu-id="b8785-105">XPS 檔 API 的介面是由 [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) 介面所建立。</span><span class="sxs-lookup"><span data-stu-id="b8785-105">The interfaces of the XPS Document API are created by an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface.</span></span> <span data-ttu-id="b8785-106">若要取得可在程式中使用之 **IXpsOMObjectFactory** 的指標，請呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="b8785-106">To obtain a pointer to an **IXpsOMObjectFactory** that can be used in your program, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="b8785-107">在您的程式中使用下列程式碼範例之前，請閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="b8785-107">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="b8785-108">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="b8785-108">Code Example</span></span>

<span data-ttu-id="b8785-109">下列範例會建立將在其他範例中用來建立 XPS OM 介面的物件 factory。</span><span class="sxs-lookup"><span data-stu-id="b8785-109">The following example creates the object factory that will be used to create XPS OM interfaces in other examples.</span></span>


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a><span data-ttu-id="b8785-110">最佳做法</span><span class="sxs-lookup"><span data-stu-id="b8785-110">Best Practices</span></span>

<span data-ttu-id="b8785-111">當您第一次需要呼叫 **IXpsOMObjectFactory** 來建立介面，然後儲存指標以用於程式的其他區域時，您可以藉由取得 [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)介面的指標，讓程式更有效率。</span><span class="sxs-lookup"><span data-stu-id="b8785-111">You can make your program more efficient by obtaining a pointer to an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface the first time that you need to call **IXpsOMObjectFactory** to create an interface, and then saving the pointer for use in other areas of the program.</span></span> <span data-ttu-id="b8785-112">當程式不再需要物件 factory，或一段時間不需要它時，可以釋放指標。</span><span class="sxs-lookup"><span data-stu-id="b8785-112">When the program no longer needs the object factory, or will not need it for a while, the pointer can be released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8785-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8785-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b8785-114">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="b8785-114">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="b8785-115">建立空白的 XPS OM</span><span class="sxs-lookup"><span data-stu-id="b8785-115">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

<span data-ttu-id="b8785-116">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="b8785-116">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="b8785-117">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="b8785-117">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="b8785-118">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b8785-118">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

<span data-ttu-id="b8785-119">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="b8785-119">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="b8785-120">包裝</span><span class="sxs-lookup"><span data-stu-id="b8785-120">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="b8785-121">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="b8785-121">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="b8785-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="b8785-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
