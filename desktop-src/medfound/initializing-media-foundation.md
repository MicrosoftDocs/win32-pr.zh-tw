---
description: 正在初始化媒體基礎
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: 正在初始化媒體基礎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981748"
---
# <a name="initializing-media-foundation"></a><span data-ttu-id="ef57d-103">正在初始化媒體基礎</span><span class="sxs-lookup"><span data-stu-id="ef57d-103">Initializing Media Foundation</span></span>

<span data-ttu-id="ef57d-104">使用任何 Microsoft 媒體基礎物件或介面之前，您必須呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函數。</span><span class="sxs-lookup"><span data-stu-id="ef57d-104">Before using any Microsoft Media Foundation objects or interfaces, you must call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="ef57d-105">傳入常數 **MF \_ 版本**。</span><span class="sxs-lookup"><span data-stu-id="ef57d-105">Pass in the constant **MF\_VERSION**.</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



<span data-ttu-id="ef57d-106">[**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)函式會初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="ef57d-106">The [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function initializes the Media Foundation platform.</span></span> <span data-ttu-id="ef57d-107">如果 **MFStartup** 傳回 MF \_ E \_ 不良 \_ \_ 的啟動版本，這表示您的應用程式是使用不符合系統上媒體基礎 dll 的媒體基礎標頭版本進行編譯。</span><span class="sxs-lookup"><span data-stu-id="ef57d-107">If **MFStartup** returns MF\_E\_BAD\_STARTUP\_VERSION, it means your application was compiled using a version of the Media Foundation headers that does not match the Media Foundation DLLs on your system.</span></span>

<span data-ttu-id="ef57d-108">對於 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)的每個呼叫，您的應用程式都必須呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。</span><span class="sxs-lookup"><span data-stu-id="ef57d-108">For every call to [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), your application must call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>


```C++
MFShutdown();
```



## <a name="related-topics"></a><span data-ttu-id="ef57d-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef57d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef57d-110">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="ef57d-110">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="ef57d-111">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="ef57d-111">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



