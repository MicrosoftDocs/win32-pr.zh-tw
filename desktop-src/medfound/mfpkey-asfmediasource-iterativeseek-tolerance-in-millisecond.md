---
description: 設定當 ASF 媒體來源執行反復搜尋時，所使用的容錯（以毫秒為單位）。
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: 'MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981932"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a><span data-ttu-id="09013-103">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ 容錯 \_ In \_ 毫秒屬性</span><span class="sxs-lookup"><span data-stu-id="09013-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond property</span></span>

<span data-ttu-id="09013-104">設定當 ASF 媒體來源執行反復搜尋時，所使用的容錯（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="09013-104">Sets the tolerance, in milliseconds, that is used when the ASF media source performs iterative seeking.</span></span>



<span data-ttu-id="09013-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="09013-105">Data type</span></span>

<span data-ttu-id="09013-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="09013-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="09013-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="09013-107">PROPVARIANT member</span></span>

<span data-ttu-id="09013-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="09013-108">**ULONG**</span></span>

<span data-ttu-id="09013-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="09013-109">VT\_UI4</span></span>

<span data-ttu-id="09013-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="09013-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="09013-111">備註</span><span class="sxs-lookup"><span data-stu-id="09013-111">Remarks</span></span>

<span data-ttu-id="09013-112">使用這個屬性來設定 ASF 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="09013-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="09013-113">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="09013-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="09013-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="09013-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="09013-115">只有在已啟用反復搜尋時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="09013-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="09013-116">如需詳細資訊，請參閱 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md)。</span><span class="sxs-lookup"><span data-stu-id="09013-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="09013-117">如果找到的封包與搜尋時間的距離在指定的容錯範圍內，則反復搜尋演算法會中止。</span><span class="sxs-lookup"><span data-stu-id="09013-117">The iterative seeking algorithm halts if it finds a packet whose distance from the seek time is within the specified tolerance.</span></span> <span data-ttu-id="09013-118">預設值為8000毫秒。</span><span class="sxs-lookup"><span data-stu-id="09013-118">The default value is 8000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="09013-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="09013-119">Requirements</span></span>



| <span data-ttu-id="09013-120">需求</span><span class="sxs-lookup"><span data-stu-id="09013-120">Requirement</span></span> | <span data-ttu-id="09013-121">值</span><span class="sxs-lookup"><span data-stu-id="09013-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09013-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09013-122">Minimum supported client</span></span><br/> | <span data-ttu-id="09013-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09013-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="09013-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09013-124">Minimum supported server</span></span><br/> | <span data-ttu-id="09013-125">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09013-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="09013-126">標頭</span><span class="sxs-lookup"><span data-stu-id="09013-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="09013-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="09013-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09013-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09013-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09013-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="09013-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




