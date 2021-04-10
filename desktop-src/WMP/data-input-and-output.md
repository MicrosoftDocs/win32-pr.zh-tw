---
title: 資料輸入和輸出
description: 資料輸入和輸出
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Windows Media Player 外掛程式、資料輸入和輸出
- 外掛程式、資料輸入和輸出
- 數位信號處理外掛程式、資料輸入和輸出
- DSP 外掛程式、資料輸入和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092273"
---
# <a name="data-input-and-output"></a><span data-ttu-id="bb4e1-107">資料輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="bb4e1-107">Data Input and Output</span></span>

<span data-ttu-id="bb4e1-108">Windows Media Player 透過 Windows Media Player 所配置的輸入緩衝區，將音訊或影片資料提供給 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-108">Windows Media Player provides audio or video data to DSP plug-ins through an input buffer allocated by Windows Media Player.</span></span> <span data-ttu-id="bb4e1-109">DSP 外掛程式會透過 Windows Media Player 也配置的輸出緩衝區，將已處理的資料傳回 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-109">DSP plug-ins return processed data to Windows Media Player through an output buffer that is also allocated by Windows Media Player.</span></span> <span data-ttu-id="bb4e1-110">Windows Media Player 藉由呼叫外掛程式所執行的方法，管理在本身和 DSP 外掛程式之間傳遞資料的流程。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-110">Windows Media Player manages the process of passing data between itself and the DSP plug-in by calling methods implemented by the plug-in.</span></span> <span data-ttu-id="bb4e1-111">針對作為 DirectX 媒體物件的外掛程式 (]) ，此程式的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="bb4e1-111">For a plug-in acting as a DirectX Media Object (DMO), the process works as follows:</span></span>

1.  <span data-ttu-id="bb4e1-112">Windows Media Player 會呼叫 **IMediaObject：:P rocessinput**，將 **IMediaBuffer** 物件的指標傳遞至 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-112">Windows Media Player calls **IMediaObject::ProcessInput**, passing a pointer to an **IMediaBuffer** object to the DSP plug-in.</span></span>
2.  <span data-ttu-id="bb4e1-113">DSP 外掛程式會保留輸入緩衝區物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-113">The DSP plug-in keeps a reference count on the input buffer object.</span></span> <span data-ttu-id="bb4e1-114">DSP 外掛程式會傳回適當的成功或失敗 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-114">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
3.  <span data-ttu-id="bb4e1-115">Windows Media Player 會呼叫 **IMediaObject：:P rocessoutput**，將指標傳遞至 **Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區** 結構的陣列， (其中包含指向 DSP 外掛程式) 的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-115">Windows Media Player calls **IMediaObject::ProcessOutput**, passing a pointer to an array of **DMO\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
4.  <span data-ttu-id="bb4e1-116">DSP 外掛程式會處理輸入緩衝區中的資料，然後將資料複製到適當的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-116">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="bb4e1-117">當緩衝區中的所有資料都已處理時，DSP 外掛程式會釋放輸入緩衝區物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-117">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="bb4e1-118">然後，DSP 外掛程式會傳回適當的成功或失敗 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-118">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
5.  <span data-ttu-id="bb4e1-119">Windows Media Player 在輸出緩衝區中呈現內容。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-119">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="bb4e1-120">針對作為媒體基礎轉換 (MFT) 的外掛程式，此程式的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="bb4e1-120">For a plug-in acting as a Media Foundation Transform (MFT), the process works as follows:</span></span>

-   <span data-ttu-id="bb4e1-121">Windows Media Player 會呼叫 **IMFTransform：:P rocessinput**，將 **IMFSample** 介面物件的指標傳遞至 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-121">Windows Media Player calls **IMFTransform::ProcessInput**, passing a pointer to an **IMFSample** interface object to the DSP plug-in.</span></span>
    1.  <span data-ttu-id="bb4e1-122">DSP 外掛程式會保留 **IMFSample** 介面上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-122">The DSP plug-in keeps a reference count on the **IMFSample** interface.</span></span> <span data-ttu-id="bb4e1-123">DSP 外掛程式會傳回適當的成功或失敗 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-123">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
    2.  <span data-ttu-id="bb4e1-124">Windows Media Player 會呼叫 **IMFTransform：:P rocessoutput**，將指標傳遞至包含 DSP 外掛程式) 之輸出緩衝區的的 **MFT \_ 輸出 \_ 資料 \_ 緩衝區** 結構 (。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-124">Windows Media Player calls **IMFTransform::ProcessOutput**, passing a pointer to an array of **MFT\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
    3.  <span data-ttu-id="bb4e1-125">DSP 外掛程式會處理輸入緩衝區中的資料，然後將資料複製到適當的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-125">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="bb4e1-126">當緩衝區中的所有資料都已處理時，DSP 外掛程式會釋放輸入緩衝區物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-126">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="bb4e1-127">然後，DSP 外掛程式會傳回適當的成功或失敗 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-127">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
    4.  <span data-ttu-id="bb4e1-128">Windows Media Player 在輸出緩衝區中呈現內容。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-128">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="bb4e1-129">此程式會在外掛程式已啟用且 Windows Media Player 有要轉譯的內容時持續重複。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-129">This process repeats continuously while the plug-in is enabled and Windows Media Player has content to render.</span></span>

> [!Note]  
> <span data-ttu-id="bb4e1-130">請勿撰寫將資料寫入輸入緩衝區或從輸出緩衝區讀取資料的程式碼。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-130">Do not write code that writes data to the input buffer or reads data from the output buffer.</span></span> <span data-ttu-id="bb4e1-131">不當存取資料緩衝區可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="bb4e1-131">Incorrectly accessing data buffers may yield unexpected results.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bb4e1-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb4e1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb4e1-133">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="bb4e1-133">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




