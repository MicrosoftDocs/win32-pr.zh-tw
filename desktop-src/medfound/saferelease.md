---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983373"
---
# <a name="saferelease"></a><span data-ttu-id="e27b1-103">SafeRelease</span><span class="sxs-lookup"><span data-stu-id="e27b1-103">SafeRelease</span></span>


<span data-ttu-id="e27b1-104">本檔中的許多程式碼範例都會使用下列函式來釋放 COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="e27b1-104">Many of the code examples in this documentation use the following function to release COM interface pointers.</span></span>


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
> <span data-ttu-id="e27b1-105">SDK 標頭中未定義此函式。</span><span class="sxs-lookup"><span data-stu-id="e27b1-105">This function is not defined in an SDK header.</span></span> <span data-ttu-id="e27b1-106">若要使用此函式，您必須在自己的程式碼中定義它。</span><span class="sxs-lookup"><span data-stu-id="e27b1-106">To use this function, you must define it in your own code.</span></span>

 

<span data-ttu-id="e27b1-107">此函式會釋放指標 *ppT* ，並將其設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e27b1-107">This function releases the pointer *ppT* and sets it equal to **NULL**.</span></span>

<span data-ttu-id="e27b1-108">另一個選項是使用智慧型指標類別，例如在 Active Template Library (ATL) 中定義的 **CComPtr**。</span><span class="sxs-lookup"><span data-stu-id="e27b1-108">Another option is to use a smart pointer class, such as **CComPtr**, which is defined in the Active Template Library (ATL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e27b1-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="e27b1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e27b1-110">關於媒體基礎</span><span class="sxs-lookup"><span data-stu-id="e27b1-110">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="e27b1-111">**IUnknown：： Release**</span><span class="sxs-lookup"><span data-stu-id="e27b1-111">**IUnknown::Release**</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
