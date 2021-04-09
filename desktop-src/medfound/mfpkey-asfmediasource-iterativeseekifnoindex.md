---
description: 設定 ASF 媒體來源，以在原始程式檔沒有索引時使用反復搜尋。
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: 'MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696254"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a><span data-ttu-id="0b9ea-103">MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex 屬性</span><span class="sxs-lookup"><span data-stu-id="0b9ea-103">MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex property</span></span>

<span data-ttu-id="0b9ea-104">設定 ASF 媒體來源，以在原始程式檔沒有索引時使用反復搜尋。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-104">Configures the ASF media source to use iterative seeking if the source file has no index.</span></span>



<span data-ttu-id="0b9ea-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0b9ea-105">Data type</span></span>

<span data-ttu-id="0b9ea-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="0b9ea-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0b9ea-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="0b9ea-107">PROPVARIANT member</span></span>

<span data-ttu-id="0b9ea-108">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="0b9ea-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="0b9ea-109">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="0b9ea-109">VT\_BOOL</span></span>

<span data-ttu-id="0b9ea-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="0b9ea-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="0b9ea-111">備註</span><span class="sxs-lookup"><span data-stu-id="0b9ea-111">Remarks</span></span>

<span data-ttu-id="0b9ea-112">使用這個屬性來設定 ASF 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="0b9ea-113">若要設定屬性，請將 **IPropertyStore** 指標傳遞至 *來源解析程式*。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-113">To set the property, pass an **IPropertyStore** pointer to the *source resolver*.</span></span> <span data-ttu-id="0b9ea-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="0b9ea-115">*反復搜尋* 是一種演算法，可在沒有索引的 ASF 檔案中尋找位置。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-115">*Iterative seeking* is an algorithm to find a position in an ASF file with no index.</span></span> <span data-ttu-id="0b9ea-116">它會根據平均位元速率來使用一連串的近似值，以逐漸接近目標搜尋時間。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-116">It uses a series of approximations, based on the average bit rate, to get progressively closer to the target seek time.</span></span> <span data-ttu-id="0b9ea-117"> (演算法類似于二進位搜尋。 ) 反復的搜尋可能需要比依索引搜尋更長的時間，因此預設為停用。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-117">(The algorithm is similar to a binary search.) Iterative seeking can take longer than seeking by index, so it is disabled by default.</span></span>

<span data-ttu-id="0b9ea-118">如果設定此屬性，請使用下列屬性來設定搜尋參數：</span><span class="sxs-lookup"><span data-stu-id="0b9ea-118">If you set this property, use the following properties to set the search parameters:</span></span>

-   [<span data-ttu-id="0b9ea-119">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ 最大 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="0b9ea-119">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count</span></span>](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [<span data-ttu-id="0b9ea-120">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ 容錯 \_ （ \_ 毫秒）</span><span class="sxs-lookup"><span data-stu-id="0b9ea-120">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond</span></span>](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

<span data-ttu-id="0b9ea-121">這些屬性會分別設定反覆運算次數和容錯值的最大數目。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-121">These properties set the maximum number of iterations and the tolerance, respectively.</span></span> <span data-ttu-id="0b9ea-122">當演算法達到反覆運算次數上限時，或當它找到的封包與搜尋時間的距離在指定的容錯範圍內時，就會中止。</span><span class="sxs-lookup"><span data-stu-id="0b9ea-122">The algorithm halts when it reaches the maximum number of iterations, or when it finds a packet whose distance from the seek time is within the specified tolerance.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b9ea-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b9ea-123">Requirements</span></span>



| <span data-ttu-id="0b9ea-124">需求</span><span class="sxs-lookup"><span data-stu-id="0b9ea-124">Requirement</span></span> | <span data-ttu-id="0b9ea-125">值</span><span class="sxs-lookup"><span data-stu-id="0b9ea-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9ea-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b9ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9ea-127">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b9ea-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0b9ea-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b9ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9ea-129">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b9ea-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0b9ea-130">標頭</span><span class="sxs-lookup"><span data-stu-id="0b9ea-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b9ea-131"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b9ea-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b9ea-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b9ea-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9ea-133">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="0b9ea-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




