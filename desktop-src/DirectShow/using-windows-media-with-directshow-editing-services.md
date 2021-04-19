---
description: 使用具有 DirectShow 編輯服務的 Windows Media
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: 使用具有 DirectShow 編輯服務的 Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986434"
---
# <a name="using-windows-media-with-directshow-editing-services"></a><span data-ttu-id="0f1a5-103">使用具有 DirectShow 編輯服務的 Windows Media</span><span class="sxs-lookup"><span data-stu-id="0f1a5-103">Using Windows Media With DirectShow Editing Services</span></span>

<span data-ttu-id="0f1a5-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0f1a5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0f1a5-105">本節說明如何在 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 應用程式中使用 Windows Media 內容。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-105">This section describes how to use Windows Media–based content in a [DirectShow Editing Services](directshow-editing-services.md) (DES) application.</span></span> <span data-ttu-id="0f1a5-106">有兩個主要案例：</span><span class="sxs-lookup"><span data-stu-id="0f1a5-106">There are two main scenarios:</span></span>

-   <span data-ttu-id="0f1a5-107">來源剪輯。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-107">Source clips.</span></span> <span data-ttu-id="0f1a5-108">DES 專案可以包含來自 Windows Media 檔案的音訊和影片剪輯。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-108">A DES project can contain audio and video clips from Windows Media files.</span></span>
-   <span data-ttu-id="0f1a5-109">目標格式。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-109">Target format.</span></span> <span data-ttu-id="0f1a5-110">Windows Media 是影片編輯專案最終輸出的理想格式。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-110">Windows Media is an ideal format for the final output of a video editing project.</span></span>

<span data-ttu-id="0f1a5-111">若要使用 Windows Media 檔案，應用程式必須提供軟體憑證，也稱為金鑰。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-111">To work with Windows Media files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="0f1a5-112">它會藉由執行金鑰提供者物件來完成這項工作。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-112">It does this by implementing a key provider object.</span></span> <span data-ttu-id="0f1a5-113">金鑰提供者是公開 **IServiceProvider** 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-113">The key provider is a COM object the exposes the **IServiceProvider** interface.</span></span> <span data-ttu-id="0f1a5-114">如需有關如何執行金鑰提供者的詳細資訊，請參閱 [解除鎖定 Windows Media FORMAT SDK](unlocking-the-windows-media-format-sdk.md)。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-114">For information about implementing the key provider, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="0f1a5-115">若要搭配使用 DES 與 Windows Media 檔案，下列 DES 物件需要軟體金鑰：</span><span class="sxs-lookup"><span data-stu-id="0f1a5-115">To use DES with Windows Media files, the following DES objects require the software key:</span></span>

-   <span data-ttu-id="0f1a5-116">轉譯引擎，用於預覽或寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-116">The render engine, for previewing or file writing.</span></span>
-   <span data-ttu-id="0f1a5-117">MediaDet 物件，用來從 ASF 檔案取得影片框架或媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-117">The MediaDet object, to get video frames or media types from ASF files.</span></span>
-   <span data-ttu-id="0f1a5-118">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="0f1a5-118">\[!Important\]</span></span>  
    > <span data-ttu-id="0f1a5-119">請勿使用智慧型轉譯引擎來讀取或寫入 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-119">Do not use the Smart Render Engine to read or write Windows Media files.</span></span> <span data-ttu-id="0f1a5-120">請一律使用基本轉譯引擎 (CLSID \_ RenderEngine) 。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-120">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

     

<span data-ttu-id="0f1a5-121">若要為物件提供軟體金鑰，請查詢 **IObjectWithSite** 介面的物件，並以您的金鑰提供者指標呼叫 **IObjectWithSite：： SetSite** 。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-121">To give an object the software key, query that object for the **IObjectWithSite** interface and call **IObjectWithSite::SetSite** with a pointer to your key provider.</span></span> <span data-ttu-id="0f1a5-122">例如，下列程式碼會提供軟體金鑰給轉譯引擎：</span><span class="sxs-lookup"><span data-stu-id="0f1a5-122">For example, the following code provides the software key to the render engine:</span></span>


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



<span data-ttu-id="0f1a5-123">若要在 DES 專案中使用 Windows Media source 剪輯，只要在轉譯引擎上呼叫 **IObjectWithSite：： SetSite** ，並使用您的金鑰提供者指標。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-123">To use Windows Media source clips in a DES project, simply call **IObjectWithSite::SetSite** on the render engine with a pointer to your key provider.</span></span>

<span data-ttu-id="0f1a5-124">如需撰寫 Windows Media 檔案的相關資訊，請參閱 [以 DES 撰寫 Windows media](writing-a-windows-media-file-in-des.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="0f1a5-124">For information about writing Windows Media files, see [Writing a Windows Media File in DES](writing-a-windows-media-file-in-des.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f1a5-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f1a5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f1a5-126">使用 DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="0f1a5-126">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



