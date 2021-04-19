---
description: TAPI \_ 串流設定 \_ \_ CAPS 結構包含影片或音訊串流設定資訊。
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: 'TAPI_STREAM_CONFIG_CAPS 結構 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977550"
---
# <a name="tapi_stream_config_caps-structure"></a><span data-ttu-id="4c317-103">TAPI \_ 串流 \_ 設定 \_ CAPS 結構</span><span class="sxs-lookup"><span data-stu-id="4c317-103">TAPI\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="4c317-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用此結構。</span><span class="sxs-lookup"><span data-stu-id="4c317-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4c317-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4c317-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4c317-106">**TAPI \_ 串流設定 \_ \_ CAPS** 結構包含影片或音訊串流設定資訊。</span><span class="sxs-lookup"><span data-stu-id="4c317-106">The **TAPI\_STREAM\_CONFIG\_CAPS** structure contains either video or audio stream configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c317-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c317-107">Syntax</span></span>


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="4c317-108">成員</span><span class="sxs-lookup"><span data-stu-id="4c317-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c317-109">**CapsType**</span><span class="sxs-lookup"><span data-stu-id="4c317-109">**CapsType**</span></span>
</dt> <dd>

<span data-ttu-id="4c317-110">定義聯集成員是否包含影片或音訊資訊。</span><span class="sxs-lookup"><span data-stu-id="4c317-110">Defines whether the union member contains video or audio information.</span></span>

</dd> <dt>

<span data-ttu-id="4c317-111">**VideoCap**</span><span class="sxs-lookup"><span data-stu-id="4c317-111">**VideoCap**</span></span>
</dt> <dd>

<span data-ttu-id="4c317-112">包含影片串流功能的 [**TAPI \_ 影片 \_ 串流設定 \_ \_ cap**](tapi-video-stream-config-caps.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="4c317-112">A [**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**](tapi-video-stream-config-caps.md) structure containing the video stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="4c317-113">**AudioCap**</span><span class="sxs-lookup"><span data-stu-id="4c317-113">**AudioCap**</span></span>
</dt> <dd>

<span data-ttu-id="4c317-114">包含音訊串流功能的 [**TAPI \_ 音訊 \_ 串流設定 \_ \_ cap**](tapi-audio-stream-config-caps.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="4c317-114">A [**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**](tapi-audio-stream-config-caps.md) structure containing the audio stream capabilities.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c317-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c317-115">Requirements</span></span>



| <span data-ttu-id="4c317-116">需求</span><span class="sxs-lookup"><span data-stu-id="4c317-116">Requirement</span></span> | <span data-ttu-id="4c317-117">值</span><span class="sxs-lookup"><span data-stu-id="4c317-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c317-118">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="4c317-118">TAPI version</span></span><br/> | <span data-ttu-id="4c317-119">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="4c317-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="4c317-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4c317-120">Header</span></span><br/>       | <dl> <span data-ttu-id="4c317-121"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c317-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c317-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c317-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c317-123">**ITFormatControl::GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="4c317-123">**ITFormatControl::GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[<span data-ttu-id="4c317-124">**StreamConfigCapsType**</span><span class="sxs-lookup"><span data-stu-id="4c317-124">**StreamConfigCapsType**</span></span>](streamconfigcapstype.md)
</dt> <dt>

[<span data-ttu-id="4c317-125">**TAPI \_ 影片 \_ 串流 \_ 設定 \_ 上限**</span><span class="sxs-lookup"><span data-stu-id="4c317-125">**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-video-stream-config-caps.md)
</dt> <dt>

[<span data-ttu-id="4c317-126">**TAPI \_ 音訊 \_ 串流 \_ 設定 \_ CAP**</span><span class="sxs-lookup"><span data-stu-id="4c317-126">**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




