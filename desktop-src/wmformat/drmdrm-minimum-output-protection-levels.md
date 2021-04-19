---
title: 'DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS 結構 (Wmdrmsdk .h) '
description: DRM 的 \_ 最小 \_ 輸出 \_ 保護 \_ 層級結構會保有最小輸出保護層級 (OPLs) 來播放各種類型的內容。 裝置必須支援一種資料類型的最小 OPL，才能從讀取器接收該類型的資料。
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986166"
---
# <a name="drm_minimum_output_protection_levels-structure"></a><span data-ttu-id="95e3c-106">DRM \_ 最小 \_ 輸出 \_ 保護 \_ 層級結構</span><span class="sxs-lookup"><span data-stu-id="95e3c-106">DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="95e3c-107">**DRM 的 \_ 最小 \_ 輸出 \_ 保護 \_ 層級** 結構會保有最小輸出保護層級 (OPLs) 來播放各種類型的內容。</span><span class="sxs-lookup"><span data-stu-id="95e3c-107">The **DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS** structure holds the minimum output protection levels (OPLs) for playback of various types of content.</span></span> <span data-ttu-id="95e3c-108">裝置必須支援一種資料類型的最小 OPL，才能從讀取器接收該類型的資料。</span><span class="sxs-lookup"><span data-stu-id="95e3c-108">A device must support the minimum OPL for a type of data to receive that type of data from the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e3c-109">語法</span><span class="sxs-lookup"><span data-stu-id="95e3c-109">Syntax</span></span>


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a><span data-ttu-id="95e3c-110">成員</span><span class="sxs-lookup"><span data-stu-id="95e3c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="95e3c-111">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="95e3c-111">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="95e3c-112">接收壓縮數位影片所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="95e3c-112">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="95e3c-113">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="95e3c-113">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="95e3c-114">接收未壓縮數位影片所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="95e3c-114">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="95e3c-115">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="95e3c-115">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="95e3c-116">接收類比影片所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="95e3c-116">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="95e3c-117">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="95e3c-117">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="95e3c-118">接收壓縮數位音訊所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="95e3c-118">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="95e3c-119">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="95e3c-119">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="95e3c-120">接收未壓縮數位音訊所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="95e3c-120">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95e3c-121">備註</span><span class="sxs-lookup"><span data-stu-id="95e3c-121">Remarks</span></span>

<span data-ttu-id="95e3c-122">此結構會當做 [**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md) 結構的成員使用。</span><span class="sxs-lookup"><span data-stu-id="95e3c-122">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e3c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="95e3c-123">Requirements</span></span>



| <span data-ttu-id="95e3c-124">需求</span><span class="sxs-lookup"><span data-stu-id="95e3c-124">Requirement</span></span> | <span data-ttu-id="95e3c-125">值</span><span class="sxs-lookup"><span data-stu-id="95e3c-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95e3c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="95e3c-126">Header</span></span><br/> | <dl> <span data-ttu-id="95e3c-127"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="95e3c-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e3c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95e3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e3c-129">**結構**</span><span class="sxs-lookup"><span data-stu-id="95e3c-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





