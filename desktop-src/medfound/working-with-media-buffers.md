---
description: 使用媒體緩衝區
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: '使用媒體緩衝區 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853428"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a><span data-ttu-id="d2cbe-103">使用媒體緩衝區 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="d2cbe-103">Working with Media Buffers (Microsoft Media Foundation)</span></span>

<span data-ttu-id="d2cbe-104">本主題說明如何使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面存取媒體緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-104">This topic describes how to use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface to access the data in a media buffer.</span></span> <span data-ttu-id="d2cbe-105">所有媒體緩衝區都會公開 **IMFMediaBuffer**，這是針對任何類型的資料所設計。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-105">All media buffers expose **IMFMediaBuffer**, which is designed for any type of data.</span></span> <span data-ttu-id="d2cbe-106">未壓縮的影片畫面是特殊案例，如 [未壓縮的影片緩衝區](uncompressed-video-buffers.md)主題所述。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-106">Uncompressed video frames are a special case, described in the topic [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="buffer-size"></a><span data-ttu-id="d2cbe-107">緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="d2cbe-107">Buffer Size</span></span>

<span data-ttu-id="d2cbe-108">媒體緩衝區有兩種與其相關聯的大小：</span><span class="sxs-lookup"><span data-stu-id="d2cbe-108">A media buffer has two sizes associated with it:</span></span>

-   <span data-ttu-id="d2cbe-109">*最大長度* 是配置給緩衝區之記憶體的實體大小。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-109">The *maximum length* is the physical size of the memory that is allocated for the buffer.</span></span> <span data-ttu-id="d2cbe-110">當建立緩衝區時，就會設定此值，而且在緩衝區存留期內不會變更。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-110">This value is set when the buffer is created and does not change during the lifetime of the buffer.</span></span> <span data-ttu-id="d2cbe-111">最大長度表示可儲存在緩衝區中的資料量。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-111">The maximum length indicates how much data can be stored in the buffer.</span></span> <span data-ttu-id="d2cbe-112">若要尋找大小上限，請呼叫 [**IMFMediaBuffer：： GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength)。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-112">To find the maximum size, call [**IMFMediaBuffer::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span></span>

-   <span data-ttu-id="d2cbe-113">目前的 *長度* 是目前在緩衝區中的有效資料量。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-113">The *current length* is the amount of valid data that is currently in the buffer.</span></span> <span data-ttu-id="d2cbe-114">第一次配置緩衝區時，目前的長度為零，因為緩衝區中沒有有效的資料。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-114">When the buffer is first allocated, the current length is zero, because there is no valid data in the buffer.</span></span> <span data-ttu-id="d2cbe-115">如果您將任何資料寫入至緩衝區，則必須藉由呼叫 [**IMFMediaBuffer：： SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength)來更新目前的長度。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-115">If you write any data to the buffer, you must update the current length by calling [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span></span> <span data-ttu-id="d2cbe-116">例如，如果您將100個位元組的資料寫入緩衝區，請使用值100來呼叫 **SetCurrentLength** 。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-116">For example, if you write 100 bytes of data into the buffer, call **SetCurrentLength** with the value 100.</span></span> <span data-ttu-id="d2cbe-117">如果您從媒體緩衝區讀取資料，請呼叫 [**IMFMediaBuffer：： GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) ，以找出緩衝區目前的資料量。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-117">If you read data from a media buffer, call [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) to find out how much data is currently in the buffer.</span></span> <span data-ttu-id="d2cbe-118">請勿讀取超過目前的長度。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-118">Do not read past the current length.</span></span> <span data-ttu-id="d2cbe-119">目前的長度絕不能超過緩衝區的最大長度。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-119">The current length can never exceed the maximum length of the buffer.</span></span>

## <a name="accessing-the-buffer-memory"></a><span data-ttu-id="d2cbe-120">存取緩衝區記憶體</span><span class="sxs-lookup"><span data-stu-id="d2cbe-120">Accessing the Buffer Memory</span></span>

<span data-ttu-id="d2cbe-121">若要存取緩衝區中的記憶體，請呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock)。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-121">To access the memory in the buffer, call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="d2cbe-122">這個方法會傳回記憶體區塊開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-122">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="d2cbe-123">它也會傳回最大長度和目前的長度。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-123">It also returns the maximum length and the current length.</span></span> <span data-ttu-id="d2cbe-124">當您使用指標完成時，請呼叫 [**IMFMediaBuffer：： Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock)。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-124">When you are done using the pointer, call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="d2cbe-125">若要將資料寫入媒體緩衝區：</span><span class="sxs-lookup"><span data-stu-id="d2cbe-125">To write data into a media buffer:</span></span>

1.  <span data-ttu-id="d2cbe-126">呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以取得記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-126">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="d2cbe-127">方法也會傳回緩衝區的最大長度。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-127">The method also returns the buffer's maximum length.</span></span>
2.  <span data-ttu-id="d2cbe-128">將您的資料寫入記憶體，最多可達緩衝區的最大長度。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-128">Write your data into the memory, up to the buffer's maximum length.</span></span>
3.  <span data-ttu-id="d2cbe-129">呼叫 [**IMFMediaBuffer：： SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) ，以更新目前的長度。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-129">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the current length.</span></span> <span data-ttu-id="d2cbe-130">將目前的長度設為等於您在步驟2中所撰寫的資料量。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-130">Set the current length equal to the amount of data that you wrote in step 2.</span></span>
4.  <span data-ttu-id="d2cbe-131">呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-131">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

<span data-ttu-id="d2cbe-132">從媒體緩衝區讀取資料：</span><span class="sxs-lookup"><span data-stu-id="d2cbe-132">To read data from a media buffer:</span></span>

1.  <span data-ttu-id="d2cbe-133">呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以取得記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-133">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="d2cbe-134">方法也會傳回緩衝區目前的長度 (緩衝區) 中的有效資料量。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-134">The method also returns the buffer's current length (the amount of valid data in the buffer).</span></span>
2.  <span data-ttu-id="d2cbe-135">讀取記憶體的內容，最多可達目前的長度。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-135">Read the contents of the memory, up to the current length.</span></span>
3.  <span data-ttu-id="d2cbe-136">呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-136">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

## <a name="creating-system-memory-buffers"></a><span data-ttu-id="d2cbe-137">建立系統記憶體緩衝區</span><span class="sxs-lookup"><span data-stu-id="d2cbe-137">Creating System Memory Buffers</span></span>

<span data-ttu-id="d2cbe-138">系統記憶體緩衝區是管理系統記憶體區塊的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-138">The system memory buffer is a media buffer that manages a block of system memory.</span></span> <span data-ttu-id="d2cbe-139">若要建立這個物件的實例，請呼叫 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) 或 [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) ，並指定緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-139">To create an instance of this object, call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) or [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) and specify a buffer size.</span></span> <span data-ttu-id="d2cbe-140">這兩個函數都會配置記憶體區塊，並傳回 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 指標。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-140">Both functions allocate a block of memory and return an [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pointer.</span></span> <span data-ttu-id="d2cbe-141">當媒體緩衝區的參考計數到達零且物件已損毀時，就會自動釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-141">The memory is automatically released when the media buffer's reference count reaches zero and the object is destroyed.</span></span>

<span data-ttu-id="d2cbe-142">下列範例示範如何建立系統記憶體緩衝區，並寫入至緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d2cbe-142">The following example shows how to create a system memory buffer and write to the buffer.</span></span>


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d2cbe-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2cbe-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2cbe-144">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="d2cbe-144">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="d2cbe-145">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="d2cbe-145">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



