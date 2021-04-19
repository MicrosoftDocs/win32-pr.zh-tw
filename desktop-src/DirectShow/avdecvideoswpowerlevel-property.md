---
description: 指定視頻解碼器的省電層級。
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: 'AVDecVideoSWPowerLevel 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991793"
---
# <a name="avdecvideoswpowerlevel-property"></a><span data-ttu-id="985fa-103">AVDecVideoSWPowerLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="985fa-103">AVDecVideoSWPowerLevel property</span></span>

<span data-ttu-id="985fa-104">指定視頻解碼器的省電層級。</span><span class="sxs-lookup"><span data-stu-id="985fa-104">Specifies the power-saving level of a video decoder.</span></span>

<span data-ttu-id="985fa-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="985fa-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="985fa-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="985fa-106">Data type</span></span>

<span data-ttu-id="985fa-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="985fa-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="985fa-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="985fa-108">Property GUID</span></span>

<span data-ttu-id="985fa-109">**CODECAPI \_ AVDecVideoSWPowerLevel**</span><span class="sxs-lookup"><span data-stu-id="985fa-109">**CODECAPI\_AVDecVideoSWPowerLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="985fa-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="985fa-110">Property value</span></span>

<span data-ttu-id="985fa-111">可能值的範圍為 \[ 0 和 100 \] （含），具有下列意義。</span><span class="sxs-lookup"><span data-stu-id="985fa-111">The range of possible values is \[0..100\], inclusive, with the following meaning.</span></span>



| <span data-ttu-id="985fa-112">值</span><span class="sxs-lookup"><span data-stu-id="985fa-112">Value</span></span> | <span data-ttu-id="985fa-113">描述</span><span class="sxs-lookup"><span data-stu-id="985fa-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="985fa-114">0</span><span class="sxs-lookup"><span data-stu-id="985fa-114">0</span></span>     | <span data-ttu-id="985fa-115">針對電池壽命進行優化。</span><span class="sxs-lookup"><span data-stu-id="985fa-115">Optimize for battery life.</span></span>  |
| <span data-ttu-id="985fa-116">100</span><span class="sxs-lookup"><span data-stu-id="985fa-116">100</span></span>   | <span data-ttu-id="985fa-117">針對影片品質進行優化。</span><span class="sxs-lookup"><span data-stu-id="985fa-117">Optimize for video quality.</span></span> |



 

<span data-ttu-id="985fa-118">[**EAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)列舉會定義此範圍內的某些特定常數。</span><span class="sxs-lookup"><span data-stu-id="985fa-118">The [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) enumeration defines some specific constants within this range.</span></span>

## <a name="remarks"></a><span data-ttu-id="985fa-119">備註</span><span class="sxs-lookup"><span data-stu-id="985fa-119">Remarks</span></span>

<span data-ttu-id="985fa-120">您可以在播放期間設定此屬性，以變更省電層級。</span><span class="sxs-lookup"><span data-stu-id="985fa-120">You can set this property during playback to change the pwoer-saving level.</span></span>

## <a name="requirements"></a><span data-ttu-id="985fa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="985fa-121">Requirements</span></span>



| <span data-ttu-id="985fa-122">需求</span><span class="sxs-lookup"><span data-stu-id="985fa-122">Requirement</span></span> | <span data-ttu-id="985fa-123">值</span><span class="sxs-lookup"><span data-stu-id="985fa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="985fa-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="985fa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="985fa-125">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="985fa-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="985fa-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="985fa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="985fa-127">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="985fa-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="985fa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="985fa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="985fa-129"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="985fa-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985fa-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="985fa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985fa-131">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="985fa-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="985fa-132">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="985fa-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




