---
title: 'DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX 結構 (Wmdrmsdk .h) '
description: DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼 \_ EX 結構包含 drm \_ 影片 \_ 輸出保護結構的陣列 \_ 。
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985536"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a><span data-ttu-id="5e98d-105">DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼 \_ EX 結構</span><span class="sxs-lookup"><span data-stu-id="5e98d-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="5e98d-106">**Drm \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼 \_ EX** 結構包含 **drm \_ 影片 \_ 輸出 \_ 保護** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="5e98d-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e98d-107">語法</span><span class="sxs-lookup"><span data-stu-id="5e98d-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="5e98d-108">成員</span><span class="sxs-lookup"><span data-stu-id="5e98d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5e98d-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="5e98d-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5e98d-110">版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5e98d-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="5e98d-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="5e98d-111">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="5e98d-112">**RgVop** 所參考之陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="5e98d-112">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="5e98d-113">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="5e98d-113">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="5e98d-114">**DRM \_ 影片 \_ 輸出 \_ 保護 \_** 的陣列位址，例如結構。</span><span class="sxs-lookup"><span data-stu-id="5e98d-114">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="5e98d-115">**DRM \_影片 \_ 輸出 \_ 保護 \_** 範例是定義為 [**DRM \_ 輸出 \_ 保護 \_**](drm-output-protection-ex.md)的類型，例如</span><span class="sxs-lookup"><span data-stu-id="5e98d-115">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e98d-116">備註</span><span class="sxs-lookup"><span data-stu-id="5e98d-116">Remarks</span></span>

<span data-ttu-id="5e98d-117">無。</span><span class="sxs-lookup"><span data-stu-id="5e98d-117">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e98d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e98d-118">Requirements</span></span>



| <span data-ttu-id="5e98d-119">需求</span><span class="sxs-lookup"><span data-stu-id="5e98d-119">Requirement</span></span> | <span data-ttu-id="5e98d-120">值</span><span class="sxs-lookup"><span data-stu-id="5e98d-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e98d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5e98d-121">Header</span></span><br/> | <dl> <span data-ttu-id="5e98d-122"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e98d-122"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e98d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e98d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e98d-124">**DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="5e98d-124">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="5e98d-125">**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="5e98d-125">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="5e98d-126">**結構**</span><span class="sxs-lookup"><span data-stu-id="5e98d-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





