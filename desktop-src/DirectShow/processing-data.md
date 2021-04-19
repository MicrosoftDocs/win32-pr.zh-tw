---
description: 處理資料
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: 處理資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbece449df36c2de88414f313d477b8a16ba896
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106986235"
---
# <a name="processing-data"></a><span data-ttu-id="3ce65-103">處理資料</span><span class="sxs-lookup"><span data-stu-id="3ce65-103">Processing Data</span></span>

<span data-ttu-id="3ce65-104">**剖析媒體資料**</span><span class="sxs-lookup"><span data-stu-id="3ce65-104">**Parsing Media Data**</span></span>

<span data-ttu-id="3ce65-105">如果您的篩選器會剖析媒體資料，請勿信任標題或內容中的其他自我描述資料。</span><span class="sxs-lookup"><span data-stu-id="3ce65-105">If your filter parses media data, do not trust headers or other self-describing data in the content.</span></span> <span data-ttu-id="3ce65-106">例如，不信任出現在 AVI RIFF 區塊或 MPEG 封包中的大小值。</span><span class="sxs-lookup"><span data-stu-id="3ce65-106">For example, do not trust size values that appear in AVI RIFF chunks or MPEG packets.</span></span> <span data-ttu-id="3ce65-107">這類錯誤的常見範例包括：</span><span class="sxs-lookup"><span data-stu-id="3ce65-107">Common examples of this kind of error include:</span></span>

-   <span data-ttu-id="3ce65-108">讀取 *n* 位元組的資料，其中 *n* 的值來自內容，而不會針對緩衝區的實際大小檢查 *n* 。</span><span class="sxs-lookup"><span data-stu-id="3ce65-108">Reading *N* bytes of data, where the value of *N* came from the content, without checking *N* against the actual size of your buffer.</span></span>
-   <span data-ttu-id="3ce65-109">跳到緩衝區內的位元組位移，而不驗證位移是否落在緩衝區內。</span><span class="sxs-lookup"><span data-stu-id="3ce65-109">Jumping to a byte offset within a buffer, without verifying that the offset falls within the buffer.</span></span>

<span data-ttu-id="3ce65-110">另一個常見的錯誤類別，則不會驗證內容中所找到的格式描述。</span><span class="sxs-lookup"><span data-stu-id="3ce65-110">Another common class of errors involves not validating format descriptions that are found in the content.</span></span> <span data-ttu-id="3ce65-111">例如：</span><span class="sxs-lookup"><span data-stu-id="3ce65-111">For example:</span></span>

-   <span data-ttu-id="3ce65-112">[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構後面可以加上色彩表。</span><span class="sxs-lookup"><span data-stu-id="3ce65-112">A [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure can be followed by a color table.</span></span> <span data-ttu-id="3ce65-113">**BITMAPINFO** 結構定義為 **BITMAPINFOHEADER** 結構，後面接著組成色彩表的 **RGBQUAD** 值陣列。</span><span class="sxs-lookup"><span data-stu-id="3ce65-113">The **BITMAPINFO** structure is defined as a **BITMAPINFOHEADER** structure followed by an array of **RGBQUAD** values that make up the color table.</span></span> <span data-ttu-id="3ce65-114">陣列的大小取決於 **biClrUsed** 的值。</span><span class="sxs-lookup"><span data-stu-id="3ce65-114">The size of the array is determined by the value of **biClrUsed**.</span></span> <span data-ttu-id="3ce65-115">絕對不要將色彩表複製到 **BITMAPINFO** ，而不需要先檢查已配置給 **BITMAPINFO** 結構的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="3ce65-115">Never copy a color table into a **BITMAPINFO** without first checking the size of the buffer that was allocated for the **BITMAPINFO** structure.</span></span>
-   <span data-ttu-id="3ce65-116">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構可能會在結構上附加額外的格式資訊。</span><span class="sxs-lookup"><span data-stu-id="3ce65-116">A [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure might have extra format information appended to the structure.</span></span> <span data-ttu-id="3ce65-117">**CbSize** 成員會指定額外資訊的大小。</span><span class="sxs-lookup"><span data-stu-id="3ce65-117">The **cbSize** member specifies the size of the extra information.</span></span>

<span data-ttu-id="3ce65-118">在連接 pin 期間，篩選應確認所有格式結構的格式是否正確，而且包含合理的值。</span><span class="sxs-lookup"><span data-stu-id="3ce65-118">During pin connection, a filter should verify that all format structures are well-formed and contain reasonable values.</span></span> <span data-ttu-id="3ce65-119">如果沒有，則會拒絕連接。</span><span class="sxs-lookup"><span data-stu-id="3ce65-119">If not, reject the connection.</span></span> <span data-ttu-id="3ce65-120">在驗證格式結構的程式碼中，請特別小心算術溢位。</span><span class="sxs-lookup"><span data-stu-id="3ce65-120">In the code that validates the format structure, be especially careful about arithmetic overflow.</span></span> <span data-ttu-id="3ce65-121">例如，在 **BITMAPINFOHEADER** 中，寬度和高度是32位的 **long** 值，但影像大小 (這是兩個) 產品的函式，只是 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="3ce65-121">For example, in a **BITMAPINFOHEADER**, the width and height are 32-bit **long** values but the image size (which is a function of the product of the two) is only a **DWORD** value.</span></span>

<span data-ttu-id="3ce65-122">如果來源的格式資料大於您配置的緩衝區，請勿截斷來源資料，以便將它複製到您的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3ce65-122">If format data from the source is larger than your allocated buffer, do not truncate the source data in order to copy it into your buffer.</span></span> <span data-ttu-id="3ce65-123">這麼做可以建立一個結構，其隱含大小大於實際大小。</span><span class="sxs-lookup"><span data-stu-id="3ce65-123">Doing so can create a structure whose implicit size is larger than its actual size.</span></span> <span data-ttu-id="3ce65-124">例如，點陣圖標頭可能會指定不再存在的調色板資料表。</span><span class="sxs-lookup"><span data-stu-id="3ce65-124">For example, a bitmap header might specify a palette table which no longer exists.</span></span> <span data-ttu-id="3ce65-125">請改為重新配置緩衝區，或直接使連接失敗。</span><span class="sxs-lookup"><span data-stu-id="3ce65-125">Instead, reallocate the buffer or simply fail the connection.</span></span>

<span data-ttu-id="3ce65-126">**串流期間的錯誤**</span><span class="sxs-lookup"><span data-stu-id="3ce65-126">**Errors During Streaming**</span></span>

<span data-ttu-id="3ce65-127">當圖形正在執行時，如果您的篩選器收到格式不正確的內容，則應終止串流。</span><span class="sxs-lookup"><span data-stu-id="3ce65-127">When the graph is running, if your filter receives malformed content, it should terminate streaming.</span></span> <span data-ttu-id="3ce65-128">執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="3ce65-128">Do the following:</span></span>

-   <span data-ttu-id="3ce65-129">從 **Receive** 傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3ce65-129">Return an error code from **Receive**.</span></span>
-   <span data-ttu-id="3ce65-130">在下游篩選器上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 。</span><span class="sxs-lookup"><span data-stu-id="3ce65-130">Call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream filter.</span></span>
-   <span data-ttu-id="3ce65-131">呼叫 [**CBaseFilter：： NotifyEvent**](cbasefilter-notifyevent.md) 以張貼 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="3ce65-131">Call [**CBaseFilter::NotifyEvent**](cbasefilter-notifyevent.md) to post an [**EC\_ERRORABORT**](ec-errorabort.md) event.</span></span>

<span data-ttu-id="3ce65-132">**格式變更**</span><span class="sxs-lookup"><span data-stu-id="3ce65-132">**Format Changes**</span></span>

<span data-ttu-id="3ce65-133">有幾個機制可供篩選器變更中間資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="3ce65-133">Several mechanisms exist for filters to change formats mid-stream.</span></span> <span data-ttu-id="3ce65-134">其中每個步驟都牽涉到一個以上的步驟，這會產生錯誤接受的可能性。</span><span class="sxs-lookup"><span data-stu-id="3ce65-134">Each of them involves more than one step, which creates the potential for false acceptances.</span></span> <span data-ttu-id="3ce65-135">如果您的篩選器取得動態格式變更的要求，則必須拒絕要求，或在到達時接受新的格式。</span><span class="sxs-lookup"><span data-stu-id="3ce65-135">If your filter gets a request for a dynamic format change, then it must either reject the request, or else honor the new format when it arrives.</span></span> <span data-ttu-id="3ce65-136">同樣地，除非其他篩選準則同意，否則絕不會切換格式。</span><span class="sxs-lookup"><span data-stu-id="3ce65-136">Similarly, never switch formats unless the other filter agrees.</span></span> <span data-ttu-id="3ce65-137">如需詳細資訊，請參閱 [動態格式變更](dynamic-format-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="3ce65-137">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

 

 
