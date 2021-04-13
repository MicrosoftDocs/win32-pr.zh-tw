---
description: 使用 MFT 媒體緩衝區和範例
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: 使用 MFT 媒體緩衝區和範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321511"
---
# <a name="working-with-mft-media-buffers-and-samples"></a><span data-ttu-id="236c4-103">使用 MFT 媒體緩衝區和範例</span><span class="sxs-lookup"><span data-stu-id="236c4-103">Working with MFT Media Buffers and Samples</span></span>

<span data-ttu-id="236c4-104">編解碼器 MFTs 使用媒體緩衝區和範例來回傳遞媒體資料。</span><span class="sxs-lookup"><span data-stu-id="236c4-104">Codec MFTs pass media data back and forth by using media buffers and samples.</span></span>

<span data-ttu-id="236c4-105">媒體緩衝區是管理記憶體區塊的 COM 物件，通常是用來保存媒體資料。</span><span class="sxs-lookup"><span data-stu-id="236c4-105">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="236c4-106">當資料傳遞至或從 MFT 傳遞時，一律會以媒體緩衝區的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="236c4-106">When data is passed to or from an MFT, it is always passed in the form of a media buffer.</span></span>

<span data-ttu-id="236c4-107">所有媒體緩衝區都會公開 **IMFMediaBuffer** 介面。</span><span class="sxs-lookup"><span data-stu-id="236c4-107">All media buffers expose the **IMFMediaBuffer** interface.</span></span> <span data-ttu-id="236c4-108">此介面是針對任何類型的資料所設計。</span><span class="sxs-lookup"><span data-stu-id="236c4-108">This interface is designed for any type of data.</span></span> <span data-ttu-id="236c4-109">包含影片資料的緩衝區通常也會公開 **IMF2DBuffer**。</span><span class="sxs-lookup"><span data-stu-id="236c4-109">Buffers containing video data often also expose **IMF2DBuffer**.</span></span>

<span data-ttu-id="236c4-110">媒體緩衝區的大小上限是配置給緩衝區的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="236c4-110">A media buffer has a maximum size, which is the amount of memory allocated for the buffer.</span></span> <span data-ttu-id="236c4-111">若要尋找大小上限，請呼叫 **IMFMediaBuffer：： GetMaxLength**。</span><span class="sxs-lookup"><span data-stu-id="236c4-111">To find the maximum size, call **IMFMediaBuffer::GetMaxLength**.</span></span> <span data-ttu-id="236c4-112">在任何時間點，媒體緩衝區也都有目前的長度，也就是緩衝區中的有效資料量，範圍從零個位元組到最大的大小。</span><span class="sxs-lookup"><span data-stu-id="236c4-112">At any point in time, a media buffer also has a current length, which is the amount of valid data in the buffer, ranging from zero bytes up to the maximum size.</span></span> <span data-ttu-id="236c4-113">若要取得目前的長度，請呼叫 **IMFMediaBuffer：： GetCurrentLength**。</span><span class="sxs-lookup"><span data-stu-id="236c4-113">To get the current length, call **IMFMediaBuffer::GetCurrentLength**.</span></span> <span data-ttu-id="236c4-114">建立緩衝區時，目前的長度為零。</span><span class="sxs-lookup"><span data-stu-id="236c4-114">When the buffer is created, the current length is zero.</span></span> <span data-ttu-id="236c4-115">如果您將資料寫入緩衝區，請呼叫 **IMFMediaBuffer：： SetCurrentLength** 來更新目前的長度。</span><span class="sxs-lookup"><span data-stu-id="236c4-115">If you write data to the buffer, call **IMFMediaBuffer::SetCurrentLength** to update the current length.</span></span>

<span data-ttu-id="236c4-116">若要存取緩衝區中的記憶體，請呼叫 **IMFMediaBuffer：： Lock**。</span><span class="sxs-lookup"><span data-stu-id="236c4-116">To access the memory in the buffer, call **IMFMediaBuffer::Lock**.</span></span> <span data-ttu-id="236c4-117">這個方法會傳回記憶體區塊開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="236c4-117">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="236c4-118">當您使用指標完成時，請呼叫 **IMFMediaBuffer：： Unlock**。</span><span class="sxs-lookup"><span data-stu-id="236c4-118">When you are done using the pointer, call **IMFMediaBuffer::Unlock**.</span></span> <span data-ttu-id="236c4-119">**鎖定** 方法不是執行緒同步處理機制;它不保證其他執行緒無法存取緩衝區。</span><span class="sxs-lookup"><span data-stu-id="236c4-119">The **Lock** method is not a thread synchronization mechanism; it does not guarantee that other threads cannot access the buffer.</span></span> <span data-ttu-id="236c4-120">**鎖定** 方法是用來確保在您呼叫 **解除鎖定** 方法之前，存取的記憶體會保持有效。</span><span class="sxs-lookup"><span data-stu-id="236c4-120">The **Lock** method is used to assure that the memory accessed will remain valid until you call the **Unlock** method.</span></span>

<span data-ttu-id="236c4-121">媒體基礎 SDK) 內容中 (的媒體範例物件，是包含零或多個緩衝區的已排序清單的物件。</span><span class="sxs-lookup"><span data-stu-id="236c4-121">A media sample object (in the context of the Media Foundation SDK) is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="236c4-122">媒體範例會公開 **IMFSample** 介面。</span><span class="sxs-lookup"><span data-stu-id="236c4-122">Media samples expose the **IMFSample** interface.</span></span>

<span data-ttu-id="236c4-123">若要建立新的範例，請呼叫 **MFCreateSample** 函數。</span><span class="sxs-lookup"><span data-stu-id="236c4-123">To create a new sample, call the **MFCreateSample** function.</span></span> <span data-ttu-id="236c4-124">一開始，範例的緩衝區清單是空的。</span><span class="sxs-lookup"><span data-stu-id="236c4-124">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="236c4-125">若要在清單結尾加入緩衝區，請呼叫 **IMFSample：： AddBuffer**。</span><span class="sxs-lookup"><span data-stu-id="236c4-125">To add a buffer to the end of the list, call **IMFSample::AddBuffer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="236c4-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="236c4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="236c4-127">使用編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="236c4-127">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> <dt>

[<span data-ttu-id="236c4-128">使用編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="236c4-128">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



