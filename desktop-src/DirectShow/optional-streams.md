---
description: 選用資料流程
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: 選用資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940be49196396aa2d1fa71502213b0d4fbacb5ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972925"
---
# <a name="optional-streams"></a><span data-ttu-id="b90a6-103">選用資料流程</span><span class="sxs-lookup"><span data-stu-id="b90a6-103">Optional Streams</span></span>

<span data-ttu-id="b90a6-104">SQL-DMO 可以將部分輸出資料流程指定為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b90a6-104">A DMO can designate some of its output streams as optional.</span></span> <span data-ttu-id="b90a6-105">選擇性的資料流程會產生應用程式可以捨棄的資料，無論是完全或偶爾的範例。</span><span class="sxs-lookup"><span data-stu-id="b90a6-105">An optional stream produces data that the application can discard, either completely or on occasional samples.</span></span> <span data-ttu-id="b90a6-106">例如，選擇性資料流程可能包含有關主要資料流程的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="b90a6-106">For example, an optional stream might contain additional information about a primary stream.</span></span>

<span data-ttu-id="b90a6-107">若要查詢資料流程是否為選擇性，請呼叫 [**IMediaObject：： GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) 方法，並檢查 *pdwFlags* 參數。</span><span class="sxs-lookup"><span data-stu-id="b90a6-107">To query whether a stream is optional, call the [**IMediaObject::GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) method and check the *pdwFlags* parameter.</span></span> <span data-ttu-id="b90a6-108">選擇性資料流程會傳回 SQL-DMO \_ output \_ STREAMF \_ DISCARDABLE 旗標或 Sql-dmo \_ output \_ STREAMF \_ 選擇性旗標。</span><span class="sxs-lookup"><span data-stu-id="b90a6-108">Optional streams return either the DMO\_OUTPUT\_STREAMF\_DISCARDABLE flag or the DMO\_OUTPUT\_STREAMF\_OPTIONAL flag.</span></span> <span data-ttu-id="b90a6-109">這些旗標表示幾乎相同的內容;稍後將會說明其中的一個小差異。</span><span class="sxs-lookup"><span data-stu-id="b90a6-109">These flags mean almost the same thing; one minor difference between them will be explained shortly.</span></span>

<span data-ttu-id="b90a6-110">如果資料流程是選擇性的，用戶端可以指示當該資料流程處理輸出時，從該資料流程捨棄資料。</span><span class="sxs-lookup"><span data-stu-id="b90a6-110">If a stream is optional, the client can instruct the DMO to discard data from that stream when it processes the output.</span></span> <span data-ttu-id="b90a6-111">若要這樣做，請呼叫 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) 方法，並將每個要捨棄的資料流程的輸出緩衝區設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b90a6-111">To do so, call the [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) method and set the output buffer to **NULL** for each stream that you wish to discard.</span></span> <span data-ttu-id="b90a6-112"> (在 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer)的 **pBuffer** 成員中指定輸出緩衝區。 ) \_ \_ \_ \_ \_ \_ 在 *DWFLAGS* 參數中沒有任何緩衝區旗標時，也請設定 [sql-dmo 進程輸出捨棄]。</span><span class="sxs-lookup"><span data-stu-id="b90a6-112">(The output buffer is specified in the **pBuffer** member of the [**DMO\_OUTPUT\_DATA\_BUFFER**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer).) Also set the DMO\_PROCESS\_OUTPUT\_DISCARD\_WHEN\_NO\_BUFFER flag in the *dwFlags* parameter.</span></span>

<span data-ttu-id="b90a6-113">針對 *pBuffer* 指標為 **Null** 的每個資料流程，每個資料流程都會嘗試捨棄資料。</span><span class="sxs-lookup"><span data-stu-id="b90a6-113">For each stream where the *pBuffer* pointer is **NULL**, the DMO will attempt to discard the data.</span></span> <span data-ttu-id="b90a6-114">如果資料流程是選擇性的，則會保證會捨棄資料。</span><span class="sxs-lookup"><span data-stu-id="b90a6-114">If the stream is optional, the DMO is guaranteed to discard the data.</span></span> <span data-ttu-id="b90a6-115">如果資料流程不是選擇性的，則會盡可能捨棄資料，但不保證會這樣做。</span><span class="sxs-lookup"><span data-stu-id="b90a6-115">If the stream is not optional, the DMO discards the data when possible, but is not guaranteed to do so.</span></span> <span data-ttu-id="b90a6-116">如果它無法捨棄資料，它會設定 [SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ 不完整] 旗標。</span><span class="sxs-lookup"><span data-stu-id="b90a6-116">If it cannot discard the data, it sets the DMO\_OUTPUT\_DATA\_BUFFERF\_INCOMPLETE flag.</span></span> <span data-ttu-id="b90a6-117">如果您將 *pBuffer* 指標設定為 **Null** ，但未設定 [ \_ \_ \_ \_ 當無緩衝區旗標時]，則會捨棄 []，而不 \_ \_ 會捨棄資料。</span><span class="sxs-lookup"><span data-stu-id="b90a6-117">If you set a *pBuffer* pointer to **NULL** but do not set the DMO\_PROCESS\_OUTPUT\_DISCARD\_WHEN\_NO\_BUFFER flag, the DMO does not discard the data.</span></span> <span data-ttu-id="b90a6-118">在這種情況下，會在內部緩衝輸出，或只是 **ProcessOutput** 呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="b90a6-118">In that case, the DMO either buffers the output internally, or simply fails the **ProcessOutput** call.</span></span>

<span data-ttu-id="b90a6-119">SQL-DMO \_ 輸出 \_ STREAMF \_ 選用旗標和 Sql-dmo \_ output \_ STREAMF \_ DISCARDABLE 旗標之間唯一的功能差異如下：</span><span class="sxs-lookup"><span data-stu-id="b90a6-119">The only functional difference between the DMO\_OUTPUT\_STREAMF\_OPTIONAL flag and the DMO\_OUTPUT\_STREAMF\_DISCARDABLE flag is the following:</span></span>

-   <span data-ttu-id="b90a6-120">[SQL-DMO \_ 輸出 \_ STREAMF] \_ 選擇性旗標表示用戶端不需要在該資料流程上設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b90a6-120">The DMO\_OUTPUT\_STREAMF\_OPTIONAL flag indicates that the client does not have to set a media type on that stream.</span></span> <span data-ttu-id="b90a6-121">但是，如果用戶端在沒有設定該資料流程的媒體類型的情況下開始處理資料，則它必須在串流的整個持續期間捨棄該資料流程中的資料。</span><span class="sxs-lookup"><span data-stu-id="b90a6-121">However, if the client begins processing data without setting the media type for that stream, then it must discard the data from that stream for the entire duration of streaming.</span></span> <span data-ttu-id="b90a6-122">如果您想要選擇性地捨棄樣本，則必須設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b90a6-122">If you want to discard samples selectively, then you must set the media type.</span></span>
-   <span data-ttu-id="b90a6-123">[SQL-DMO \_ OUTPUT \_ STREAMF \_ DISCARDABLE] 旗標表示雖然資料流程是選擇性的，但它一律需要媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b90a6-123">The DMO\_OUTPUT\_STREAMF\_DISCARDABLE flag indicates that, although the stream is optional, it always requires a media type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b90a6-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="b90a6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b90a6-125">直接裝載</span><span class="sxs-lookup"><span data-stu-id="b90a6-125">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



