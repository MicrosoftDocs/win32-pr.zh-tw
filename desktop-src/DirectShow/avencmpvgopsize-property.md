---
description: 指定從一組圖片 (GOP) 標頭到下一個 GOP 標頭的圖片數目上限。
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: 'AVEncMPVGOPSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025754"
---
# <a name="avencmpvgopsize-property"></a><span data-ttu-id="5d3b9-103">AVEncMPVGOPSize 屬性</span><span class="sxs-lookup"><span data-stu-id="5d3b9-103">AVEncMPVGOPSize property</span></span>

<span data-ttu-id="5d3b9-104">指定從一組圖片 (GOP) 標頭到下一個 GOP 標頭的圖片數目上限。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-104">Specifies the maximum number of pictures from one group-of-pictures (GOP) header to the next GOP header.</span></span>

<span data-ttu-id="5d3b9-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5d3b9-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="5d3b9-106">Data type</span></span>

<span data-ttu-id="5d3b9-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="5d3b9-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5d3b9-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="5d3b9-108">Property GUID</span></span>

<span data-ttu-id="5d3b9-109">**CODECAPI \_ AVEncMPVGOPSize**</span><span class="sxs-lookup"><span data-stu-id="5d3b9-109">**CODECAPI\_AVEncMPVGOPSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="5d3b9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5d3b9-110">Property value</span></span>

<span data-ttu-id="5d3b9-111">編碼器可以將此屬性實作為列舉集或線性範圍。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-111">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d3b9-112">備註</span><span class="sxs-lookup"><span data-stu-id="5d3b9-112">Remarks</span></span>

<span data-ttu-id="5d3b9-113">開始錄製之前，請先設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-113">Set this property before starting a recording.</span></span>

<span data-ttu-id="5d3b9-114">**適用于 Windows 8：** 編碼的 GOP 大小應透過這個屬性小於或等於指定的數位，以保持在 GOP 中 [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) 所設定的相同 B 框架模式，或因場景變更。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-114">**Applies to Windows 8:** The encoded GOP size shall be smaller than or equal to the specified number through this property, in order to keep the same B frame pattern set by [CODECAPI\_AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) throughout the GOP or due to scene change.</span></span> <span data-ttu-id="5d3b9-115">例如，當 GOP 中的 B 框架數目指定為2，而 GOP 大小為11時，則編碼器應產生10個框架以內的 GOP 大小。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-115">For example, when the number of B frames in a GOP is specified to be 2, and GOP size is 11, then encoder shall produce GOP size of 10 frames or less.</span></span> <span data-ttu-id="5d3b9-116">當 GOP 中間發生場景變更時，編碼器可能也會插入主要畫面格，並產生較小的 GOP。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-116">When scene change happens in the middle of a GOP, encoder might also insert key frame and produce smaller GOP.</span></span>

<span data-ttu-id="5d3b9-117">GOP 大小0是編碼器相依的，且編碼器可以根據其執行/品質/效能選擇不同的 GOP 大小。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-117">GOP size 0 is encoder dependent and encoders can choose different GOP sizes based on their implementation/quality/performance.</span></span> <span data-ttu-id="5d3b9-118">在此情況下，編碼器應接受 GOP 大小並截斷 B 框架。</span><span class="sxs-lookup"><span data-stu-id="5d3b9-118">Encoders should honor the GOP size and truncate B frames in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d3b9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d3b9-119">Requirements</span></span>



| <span data-ttu-id="5d3b9-120">需求</span><span class="sxs-lookup"><span data-stu-id="5d3b9-120">Requirement</span></span> | <span data-ttu-id="5d3b9-121">值</span><span class="sxs-lookup"><span data-stu-id="5d3b9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d3b9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d3b9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5d3b9-123">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d3b9-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5d3b9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d3b9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5d3b9-125">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d3b9-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5d3b9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="5d3b9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d3b9-127"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d3b9-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d3b9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d3b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d3b9-129">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="5d3b9-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5d3b9-130">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="5d3b9-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




