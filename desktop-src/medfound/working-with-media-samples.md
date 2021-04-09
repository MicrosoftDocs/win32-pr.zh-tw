---
description: 使用媒體範例
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: 使用媒體範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945600"
---
# <a name="working-with-media-samples"></a><span data-ttu-id="e5354-103">使用媒體範例</span><span class="sxs-lookup"><span data-stu-id="e5354-103">Working with Media Samples</span></span>

<span data-ttu-id="e5354-104">本主題說明如何使用 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面操作媒體範例物件。</span><span class="sxs-lookup"><span data-stu-id="e5354-104">This topic describes how to use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to manipulate media sample objects.</span></span> <span data-ttu-id="e5354-105">如需媒體範例的一般總覽，請參閱 [媒體範例](media-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="e5354-105">For a general overview of media samples, see [Media Samples](media-samples.md).</span></span>

<span data-ttu-id="e5354-106">若要建立新的媒體範例，請呼叫 [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) 函數。</span><span class="sxs-lookup"><span data-stu-id="e5354-106">To create a new media sample, call the [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) function.</span></span> <span data-ttu-id="e5354-107">一開始，範例的緩衝區清單是空的。</span><span class="sxs-lookup"><span data-stu-id="e5354-107">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="e5354-108">若要在清單結尾加入緩衝區，請呼叫 [**IMFSample：： AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer)。</span><span class="sxs-lookup"><span data-stu-id="e5354-108">To add a buffer to the end of the list, call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="e5354-109">下列程式碼示範如何建立範例，並在其中新增緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e5354-109">The following code shows how to create a sample and add a buffer to it.</span></span>


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="e5354-110">從範例取得緩衝區的建議方式是呼叫 [**IMFSample：： ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer)。</span><span class="sxs-lookup"><span data-stu-id="e5354-110">The recommended way to get the buffers from the sample is to call [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span></span> <span data-ttu-id="e5354-111">這個方法會傳回單一 continguous 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e5354-111">This method returns a single continguous buffer.</span></span>

<span data-ttu-id="e5354-112">若要逐一查看清單中的緩衝區，請從呼叫 [**IMFSample：： GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount)開始。</span><span class="sxs-lookup"><span data-stu-id="e5354-112">To iterate through the buffers in the list, start by calling [**IMFSample::GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span></span> <span data-ttu-id="e5354-113">這個方法會傳回緩衝區的數目。</span><span class="sxs-lookup"><span data-stu-id="e5354-113">This method returns the number of buffers.</span></span> <span data-ttu-id="e5354-114">然後呼叫 [**IMFSample：： GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) ，並指定要取出的緩衝區索引。</span><span class="sxs-lookup"><span data-stu-id="e5354-114">Then call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) and specify the index of the buffer to retrieve.</span></span> <span data-ttu-id="e5354-115">緩衝區是從零開始編制索引。</span><span class="sxs-lookup"><span data-stu-id="e5354-115">Buffers are indexed from zero.</span></span>

<span data-ttu-id="e5354-116">下列程式碼示範如何逐一查看範例中的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e5354-116">The following code shows how to iterate through the buffers in a sample.</span></span>


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



<span data-ttu-id="e5354-117">範例有時間戳記和持續時間。</span><span class="sxs-lookup"><span data-stu-id="e5354-117">Samples have a time stamp and a duration.</span></span> <span data-ttu-id="e5354-118">時間戳記會指出應轉譯樣本中的資料（相對於呈現時鐘）。</span><span class="sxs-lookup"><span data-stu-id="e5354-118">The time stamp indicates when the data in the sample should be rendered, relative to the presentation clock.</span></span> <span data-ttu-id="e5354-119">持續時間是應呈現資料的時間長度。</span><span class="sxs-lookup"><span data-stu-id="e5354-119">The duration is the length of time for which the data should be rendered.</span></span> <span data-ttu-id="e5354-120">通常產生資料的元件會設定初始時間戳記和持續時間。</span><span class="sxs-lookup"><span data-stu-id="e5354-120">Typically the component that generates the data sets the initial time stamp and duration.</span></span> <span data-ttu-id="e5354-121">媒體會話可能會修改這些值。</span><span class="sxs-lookup"><span data-stu-id="e5354-121">These values might get modified by the Media Session.</span></span> <span data-ttu-id="e5354-122">若要設定時間戳記，請呼叫 [**IMFSample：： SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)。</span><span class="sxs-lookup"><span data-stu-id="e5354-122">To set the time stamp, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="e5354-123">若要設定持續時間，請呼叫 [**IMFSample：： SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)。</span><span class="sxs-lookup"><span data-stu-id="e5354-123">To set the duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="e5354-124">範例也可以有屬性，其中包含有關範例的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="e5354-124">Samples can also have attributes, which contain additional information about the sample.</span></span> <span data-ttu-id="e5354-125">如需範例屬性的清單，請參閱 [範例屬性](sample-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="e5354-125">For a list of sample attributes, see [Sample Attributes](sample-attributes.md).</span></span> <span data-ttu-id="e5354-126">若要設定和取出屬性，請使用 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)繼承的 [**IMFAttributes 介面**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)。</span><span class="sxs-lookup"><span data-stu-id="e5354-126">To set and retrieve attributes, use the [**IMFAttributes Interface**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) inherits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5354-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5354-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5354-128">媒體範例</span><span class="sxs-lookup"><span data-stu-id="e5354-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="e5354-129">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="e5354-129">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



