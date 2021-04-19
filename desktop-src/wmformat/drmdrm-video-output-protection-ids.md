---
title: 'DRM_VIDEO_OUTPUT_PROTECTION_IDS 結構 (Wmdrmsdk .h) '
description: DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼結構會保存 drm \_ 影片 \_ 輸出 \_ 保護結構的陣列。
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981266"
---
# <a name="drm_video_output_protection_ids-structure"></a><span data-ttu-id="c1008-105">DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼結構</span><span class="sxs-lookup"><span data-stu-id="c1008-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="c1008-106">**Drm \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼** 結構會保存 **drm \_ 影片 \_ 輸出 \_ 保護** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="c1008-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1008-107">語法</span><span class="sxs-lookup"><span data-stu-id="c1008-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="c1008-108">成員</span><span class="sxs-lookup"><span data-stu-id="c1008-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1008-109">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="c1008-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c1008-110">**RgVop** 所參考之陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c1008-110">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="c1008-111">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="c1008-111">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="c1008-112">**DRM \_ 影片 \_ 輸出 \_ 保護** 結構陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="c1008-112">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="c1008-113">**DRM \_影片 \_ 輸出 \_ 保護** 是定義為 [**DRM \_ 輸出 \_ 保護**](drm-output-protection.md)的類型。</span><span class="sxs-lookup"><span data-stu-id="c1008-113">**DRM\_VIDEO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1008-114">備註</span><span class="sxs-lookup"><span data-stu-id="c1008-114">Remarks</span></span>

<span data-ttu-id="c1008-115">此結構會當做 [**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md) 結構的成員使用。</span><span class="sxs-lookup"><span data-stu-id="c1008-115">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1008-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1008-116">Requirements</span></span>



| <span data-ttu-id="c1008-117">需求</span><span class="sxs-lookup"><span data-stu-id="c1008-117">Requirement</span></span> | <span data-ttu-id="c1008-118">值</span><span class="sxs-lookup"><span data-stu-id="c1008-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1008-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c1008-119">Header</span></span><br/> | <dl> <span data-ttu-id="c1008-120"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1008-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1008-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1008-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1008-122">**DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="c1008-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="c1008-123">**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="c1008-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="c1008-124">**結構**</span><span class="sxs-lookup"><span data-stu-id="c1008-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





