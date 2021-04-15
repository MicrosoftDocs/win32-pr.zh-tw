---
title: 使用輸入
description: 使用輸入
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media Format SDK，使用輸入
- Advanced Systems Format (ASF) ，使用輸入
- ASF (Advanced Systems Format) ，使用輸入
- 設定檔，使用輸入
- 資料流程，使用輸入
- 編解碼器，使用輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462144"
---
# <a name="working-with-inputs"></a><span data-ttu-id="07864-109">使用輸入</span><span class="sxs-lookup"><span data-stu-id="07864-109">Working with Inputs</span></span>

<span data-ttu-id="07864-110">就像設定檔中的適當串流設定需要取得編解碼器來壓縮資料流程一樣，您也必須確定您傳遞給寫入器的未壓縮媒體類型已正確描述。</span><span class="sxs-lookup"><span data-stu-id="07864-110">Just as the proper stream configuration in the profile is required to get the codec to compress a stream, you must also ensure that the type of uncompressed media you pass to the writer is accurately described.</span></span> <span data-ttu-id="07864-111">每個 Windows Media 編解碼器都有相關聯的預設輸入類型，但支援數種輸入類型。</span><span class="sxs-lookup"><span data-stu-id="07864-111">Every Windows Media codec has an associated default input type, but several input types are supported.</span></span> <span data-ttu-id="07864-112">您可以檢查支援的輸入，並選取符合您資料的輸入。</span><span class="sxs-lookup"><span data-stu-id="07864-112">You can examine the supported inputs and select the one that matches your data.</span></span> <span data-ttu-id="07864-113">使用輸入的程式會在下列步驟中摘要說明：</span><span class="sxs-lookup"><span data-stu-id="07864-113">The process of working with inputs is summarized in the following steps:</span></span>

1.  <span data-ttu-id="07864-114">當您載入要使用之寫入器的設定檔時，寫入器物件會為設定檔中的每個連接指派輸入編號。</span><span class="sxs-lookup"><span data-stu-id="07864-114">When you load a profile for the writer to use, the writer object assigns an input number for each connection in the profile.</span></span> <span data-ttu-id="07864-115">如需載入寫入器設定檔的詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。</span><span class="sxs-lookup"><span data-stu-id="07864-115">For more information about loading profiles for the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="07864-116">除非您使用依位速率的互斥，否則每個串流都有一個連接。</span><span class="sxs-lookup"><span data-stu-id="07864-116">Unless you are using mutual exclusion by bit rate, there is one connection for each stream.</span></span> <span data-ttu-id="07864-117">位元速率互斥的資料流程會共用單一連接。</span><span class="sxs-lookup"><span data-stu-id="07864-117">Streams that are mutually exclusive by bit rate share a single connection.</span></span>
2.  <span data-ttu-id="07864-118">您的應用程式應該識別檔案的輸入編號。</span><span class="sxs-lookup"><span data-stu-id="07864-118">Your application should identify the input numbers for the file.</span></span> <span data-ttu-id="07864-119">如需識別輸入數位的詳細資訊，請參閱 [以數位識別](to-identify-inputs-by-number.md)輸入。</span><span class="sxs-lookup"><span data-stu-id="07864-119">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="07864-120">針對每個輸入，您應該確保輸入格式符合您的資料。</span><span class="sxs-lookup"><span data-stu-id="07864-120">For each input, you should ensure that the input format matches your data.</span></span> <span data-ttu-id="07864-121">您可以列舉 SDK 所支援的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="07864-121">You can enumerate the input formats supported by the SDK.</span></span> <span data-ttu-id="07864-122">如需詳細資訊，請參閱 [來列舉輸入格式](to-enumerate-input-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="07864-122">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span> <span data-ttu-id="07864-123">您無法列舉已壓縮之任意資料流程或資料流程的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="07864-123">You cannot enumerate the input formats of arbitrary streams or streams that are already compressed.</span></span> <span data-ttu-id="07864-124">如需這些特殊案例的詳細資訊，請參閱 [任意和 Precompressed 的資料流程輸入](arbitrary-and-precompressed-stream-inputs.md)。</span><span class="sxs-lookup"><span data-stu-id="07864-124">For more information about these special cases, see [Arbitrary and Precompressed Stream Inputs](arbitrary-and-precompressed-stream-inputs.md).</span></span>
4.  <span data-ttu-id="07864-125">為每個連接指派正確的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="07864-125">Assign the correct input format for each connection.</span></span> <span data-ttu-id="07864-126">如需詳細資訊，請參閱 [指派輸入格式](assigning-input-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="07864-126">For more information, see [Assigning Input Formats](assigning-input-formats.md).</span></span>
5.  <span data-ttu-id="07864-127">某些編解碼器和寫入器功能是在編碼時間進行設定，而不是在設定檔中設定。</span><span class="sxs-lookup"><span data-stu-id="07864-127">Some codec and writer features are configured at encoding time instead of in the profile.</span></span> <span data-ttu-id="07864-128">若要設定這些功能，您必須使用輸入設定。</span><span class="sxs-lookup"><span data-stu-id="07864-128">To configure these features, you must use input settings.</span></span> <span data-ttu-id="07864-129">如需詳細資訊，請參閱 [設定輸入](to-set-input-settings.md)設定。</span><span class="sxs-lookup"><span data-stu-id="07864-129">For more information, see [To Set Input Settings](to-set-input-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="07864-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="07864-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07864-131">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="07864-131">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




