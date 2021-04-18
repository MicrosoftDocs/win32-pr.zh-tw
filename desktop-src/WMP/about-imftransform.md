---
title: 關於 IMFTransform
description: 關於 IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Windows Media Player 外掛程式，介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- DSP 外掛程式，介面
- 介面、DSP 外掛程式
- Windows Media Player 外掛程式、IMFTransform 介面
- 外掛程式，IMFTransform 介面
- 數位信號處理外掛程式，IMFTransform 介面
- DSP 外掛程式，IMFTransform 介面
- IMFTransform 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965562"
---
# <a name="about-imftransform"></a><span data-ttu-id="c4bb4-113">關於 IMFTransform</span><span class="sxs-lookup"><span data-stu-id="c4bb4-113">About IMFTransform</span></span>

<span data-ttu-id="c4bb4-114">**IMFTransform** 介面是必須由雙重模式的 DSP 外掛程式所執行的其中一個介面。</span><span class="sxs-lookup"><span data-stu-id="c4bb4-114">The **IMFTransform** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="c4bb4-115">Windows Media Player 會呼叫 **IMFTransform** 介面的方法，以提供資料給外掛程式，並從外掛程式取回已處理的資料。</span><span class="sxs-lookup"><span data-stu-id="c4bb4-115">Windows Media Player calls the methods of the **IMFTransform** interface to provide data to the plug-in and to retrieve processed data back from the plug-in.</span></span> <span data-ttu-id="c4bb4-116">如需 **IMFTransform** 介面的完整檔，請參閱 Windows SDK 的媒體基礎一節。</span><span class="sxs-lookup"><span data-stu-id="c4bb4-116">For complete documentation of the **IMFTransform** interface, see the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="c4bb4-117">**IMFTransform** 的方法可分類如下。</span><span class="sxs-lookup"><span data-stu-id="c4bb4-117">The methods of **IMFTransform** can be categorized as follows.</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="c4bb4-118">處理格式協調的方法</span><span class="sxs-lookup"><span data-stu-id="c4bb4-118">Methods That Handle Format Negotiation</span></span>

<span data-ttu-id="c4bb4-119">Windows Media Player 會呼叫下列方法，以取得外掛程式所支援之資料格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4bb4-119">Windows Media Player calls the following methods to get information about the data formats supported by the plug-in.</span></span>

-   <span data-ttu-id="c4bb4-120">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-120">**GetStreamCount**</span></span>
-   <span data-ttu-id="c4bb4-121">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-121">**GetStreamLimits**</span></span>
-   <span data-ttu-id="c4bb4-122">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-122">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="c4bb4-123">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-123">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="c4bb4-124">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-124">**GetInputAvailableType**</span></span>
-   <span data-ttu-id="c4bb4-125">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-125">**GetOutputAvailableType**</span></span>
-   <span data-ttu-id="c4bb4-126">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-126">**SetInputType**</span></span>
-   <span data-ttu-id="c4bb4-127">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-127">**SetOutputType**</span></span>
-   <span data-ttu-id="c4bb4-128">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-128">**GetAttributes**</span></span>
-   <span data-ttu-id="c4bb4-129">**GetInputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-129">**GetInputStreamAttributes**</span></span>
-   <span data-ttu-id="c4bb4-130">**GetOutputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-130">**GetOutputStreamAttributes**</span></span>
-   <span data-ttu-id="c4bb4-131">**GetStreamIDs**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-131">**GetStreamIDs**</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="c4bb4-132">指定或取得狀態資訊的方法</span><span class="sxs-lookup"><span data-stu-id="c4bb4-132">Methods That Specify or Retrieve State Information</span></span>

<span data-ttu-id="c4bb4-133">Windows Media Player 會呼叫下列方法來取得或設定與外掛程式目前狀態相關的值。</span><span class="sxs-lookup"><span data-stu-id="c4bb4-133">Windows Media Player calls the following methods to get or set values related to the current state of the plug-in.</span></span>

-   <span data-ttu-id="c4bb4-134">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-134">**SetInputType**</span></span>
-   <span data-ttu-id="c4bb4-135">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-135">**SetOutputType**</span></span>
-   <span data-ttu-id="c4bb4-136">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-136">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="c4bb4-137">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-137">**GetOutputCurrentType**</span></span>
-   <span data-ttu-id="c4bb4-138">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-138">**GetInputStatus**</span></span>
-   <span data-ttu-id="c4bb4-139">**AddInputStreams**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-139">**AddInputStreams**</span></span>
-   <span data-ttu-id="c4bb4-140">**DeleteInputStreams**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-140">**DeleteInputStreams**</span></span>
-   <span data-ttu-id="c4bb4-141">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-141">**GetOutputStatus**</span></span>
-   <span data-ttu-id="c4bb4-142">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-142">**SetOutputBounds**</span></span>

> [!Note]  
> <span data-ttu-id="c4bb4-143">**SetInputType** 和 **SetOutputType** 用於格式化協商以及指定和取得狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="c4bb4-143">**SetInputType** and **SetOutputType** are used both for format negotiation and for specifying and retrieving state information.</span></span>

 

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="c4bb4-144">處理緩衝處理和處理資料的方法</span><span class="sxs-lookup"><span data-stu-id="c4bb4-144">Methods That Handle Buffering and Processing Data</span></span>

<span data-ttu-id="c4bb4-145">Windows Media Player 會呼叫下列方法，以起始外掛程式執行的各種處理常式，以執行數位信號處理。</span><span class="sxs-lookup"><span data-stu-id="c4bb4-145">Windows Media Player calls the following methods to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span>

-   <span data-ttu-id="c4bb4-146">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-146">**ProcessInput**</span></span>
-   <span data-ttu-id="c4bb4-147">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-147">**ProcessOutput**</span></span>
-   <span data-ttu-id="c4bb4-148">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-148">**ProcessMessage**</span></span>
-   <span data-ttu-id="c4bb4-149">**In processevent.<**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-149">**ProcessEvent**</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4bb4-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4bb4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4bb4-151">**必要的介面**</span><span class="sxs-lookup"><span data-stu-id="c4bb4-151">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




