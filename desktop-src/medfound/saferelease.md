---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46359821dd1f7741f6038ddb2f33cec591aacdf1bf9fc7fd3e6004e9d7601e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034866"
---
# <a name="saferelease"></a>SafeRelease


本檔中的許多程式碼範例都會使用下列函式來釋放 COM 介面指標。


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> SDK 標頭中未定義此函式。 若要使用此函式，您必須在自己的程式碼中定義它。

 

此函式會釋放指標 *ppT* ，並將其設定為 **Null**。

另一個選項是使用智慧型指標類別，例如在 Active Template Library (ATL) 中定義的 **CComPtr**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於媒體基礎](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
