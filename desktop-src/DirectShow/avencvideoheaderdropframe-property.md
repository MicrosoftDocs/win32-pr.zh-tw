---
description: 在圖片群組 (GOP) 標頭中指定放置框架旗標的值。
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: 'AVEncVideoHeaderDropFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846739"
---
# <a name="avencvideoheaderdropframe-property"></a><span data-ttu-id="36cc6-103">AVEncVideoHeaderDropFrame 屬性</span><span class="sxs-lookup"><span data-stu-id="36cc6-103">AVEncVideoHeaderDropFrame property</span></span>

<span data-ttu-id="36cc6-104">在圖片群組 (GOP) 標頭中指定放置框架旗標的值。</span><span class="sxs-lookup"><span data-stu-id="36cc6-104">Specifies the value of drop-frame flag in the group of pictures (GOP) header.</span></span>

<span data-ttu-id="36cc6-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="36cc6-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="36cc6-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="36cc6-106">Data type</span></span>

<span data-ttu-id="36cc6-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="36cc6-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="36cc6-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="36cc6-108">Property GUID</span></span>

<span data-ttu-id="36cc6-109">**CODECAPI \_ AVEncVideoHeaderDropFrame**</span><span class="sxs-lookup"><span data-stu-id="36cc6-109">**CODECAPI\_AVEncVideoHeaderDropFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="36cc6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="36cc6-110">Property value</span></span>

<span data-ttu-id="36cc6-111">這個屬性的值可以是0或1。</span><span class="sxs-lookup"><span data-stu-id="36cc6-111">The value of this property can be 0 or 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="36cc6-112">備註</span><span class="sxs-lookup"><span data-stu-id="36cc6-112">Remarks</span></span>

<span data-ttu-id="36cc6-113">NTSC 影片中會使用放置畫面格模式來修正影片之間的差異，也就是每秒29.97 個畫面格，以及時間代碼顯示，也就是每秒30個畫面格。</span><span class="sxs-lookup"><span data-stu-id="36cc6-113">Drop-frame mode is used in NTSC video to correct the discrepancy between the video, which is 29.97 frames per second, and the time code display, which is 30 frames per second.</span></span> <span data-ttu-id="36cc6-114">在拖放框架模式中，會在每分鐘的開頭略過畫面格數位00和01，但大約是 10 (00、10、20等等) 的倍數。</span><span class="sxs-lookup"><span data-stu-id="36cc6-114">In drop-frame mode, frame numbers 00 and 01 are skipped at the start of each minute, except for minutes that are even multiples of ten (00, 10, 20, and so forth).</span></span> <span data-ttu-id="36cc6-115">只有時間碼中的框架號碼會被捨棄;不會卸載任何實際的畫面格。</span><span class="sxs-lookup"><span data-stu-id="36cc6-115">Only the frame numbers in the time code are dropped; no actual frames are dropped.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cc6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="36cc6-116">Requirements</span></span>



| <span data-ttu-id="36cc6-117">需求</span><span class="sxs-lookup"><span data-stu-id="36cc6-117">Requirement</span></span> | <span data-ttu-id="36cc6-118">值</span><span class="sxs-lookup"><span data-stu-id="36cc6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36cc6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36cc6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36cc6-120">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36cc6-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="36cc6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36cc6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36cc6-122">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36cc6-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="36cc6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="36cc6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cc6-124"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="36cc6-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cc6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36cc6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cc6-126">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="36cc6-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="36cc6-127">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="36cc6-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




