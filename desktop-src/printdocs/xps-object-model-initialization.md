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
# <a name="initialize-an-xps-om"></a>初始化 XPS OM

說明如何初始化 XPS OM，以允許程式建立 XPS 檔。

XPS 檔 API 的介面是由 [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) 介面所建立。 若要取得可在程式中使用之 **IXpsOMObjectFactory** 的指標，請呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)。

在您的程式中使用下列程式碼範例之前，請閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。

## <a name="code-example"></a>程式碼範例

下列範例會建立將在其他範例中用來建立 XPS OM 介面的物件 factory。


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



## <a name="best-practices"></a>最佳做法

當您第一次需要呼叫 **IXpsOMObjectFactory** 來建立介面，然後儲存指標以用於程式的其他區域時，您可以藉由取得 [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)介面的指標，讓程式更有效率。 當程式不再需要物件 factory，或一段時間不需要它時，可以釋放指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[建立空白的 XPS OM](create-a-blank-xps-om.md)
</dt> <dt>

**在本節中使用**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[包裝](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XPS 檔 API 參考](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
