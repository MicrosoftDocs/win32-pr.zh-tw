---
description: 取得音訊位串流中音訊頻道的喇叭設定。
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: 'AVAudioChannelConfig 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025676"
---
# <a name="avaudiochannelconfig-property"></a><span data-ttu-id="67586-103">AVAudioChannelConfig 屬性</span><span class="sxs-lookup"><span data-stu-id="67586-103">AVAudioChannelConfig property</span></span>

<span data-ttu-id="67586-104">取得音訊位串流中音訊頻道的喇叭設定。</span><span class="sxs-lookup"><span data-stu-id="67586-104">Gets the speaker configuration for the audio channels in the audio bit stream.</span></span>

<span data-ttu-id="67586-105">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="67586-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="67586-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="67586-106">Data type</span></span>

<span data-ttu-id="67586-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="67586-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="67586-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="67586-108">Property GUID</span></span>

<span data-ttu-id="67586-109">**CODECAPI \_ AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="67586-109">**CODECAPI\_AVAudioChannelConfig**</span></span>

## <a name="property-value"></a><span data-ttu-id="67586-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="67586-110">Property value</span></span>

<span data-ttu-id="67586-111">這個屬性的值是 [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) 列舉之成員的位 or。</span><span class="sxs-lookup"><span data-stu-id="67586-111">The value of this property is a bitwise OR of members of the [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="67586-112">備註</span><span class="sxs-lookup"><span data-stu-id="67586-112">Remarks</span></span>

<span data-ttu-id="67586-113">通道數目包含 (LFE) 通道的低頻率效果（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="67586-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="67586-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="67586-114">Requirements</span></span>



| <span data-ttu-id="67586-115">需求</span><span class="sxs-lookup"><span data-stu-id="67586-115">Requirement</span></span> | <span data-ttu-id="67586-116">值</span><span class="sxs-lookup"><span data-stu-id="67586-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67586-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67586-117">Minimum supported client</span></span><br/> | <span data-ttu-id="67586-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67586-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="67586-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67586-119">Minimum supported server</span></span><br/> | <span data-ttu-id="67586-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67586-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="67586-121">標頭</span><span class="sxs-lookup"><span data-stu-id="67586-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="67586-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="67586-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67586-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67586-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67586-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="67586-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="67586-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="67586-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




