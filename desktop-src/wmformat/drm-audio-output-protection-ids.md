---
title: 'DRM_AUDIO_OUTPUT_PROTECTION_IDS 結構 (Wmdrmsdk .h) '
description: DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼結構包含音訊輸出保護識別碼的清單。
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999490"
---
# <a name="drm_audio_output_protection_ids-structure"></a><span data-ttu-id="960a9-105">DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼結構</span><span class="sxs-lookup"><span data-stu-id="960a9-105">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="960a9-106">**DRM \_ 音訊 \_ 輸出 \_ 保護 \_** 識別碼結構包含音訊輸出保護識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="960a9-106">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** structure contains a list of audio output protection identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="960a9-107">語法</span><span class="sxs-lookup"><span data-stu-id="960a9-107">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="960a9-108">成員</span><span class="sxs-lookup"><span data-stu-id="960a9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="960a9-109">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="960a9-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="960a9-110">**RgAop** 陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="960a9-110">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="960a9-111">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="960a9-111">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="960a9-112">**DRM \_ 音訊 \_ 輸出 \_ 保護** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="960a9-112">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="960a9-113">**DRM \_音訊 \_ 輸出 \_ 保護** 是定義為 [**DRM \_ 輸出 \_ 保護**](drm-output-protection.md)的型別。</span><span class="sxs-lookup"><span data-stu-id="960a9-113">**DRM\_AUDIO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="960a9-114">備註</span><span class="sxs-lookup"><span data-stu-id="960a9-114">Remarks</span></span>

<span data-ttu-id="960a9-115">無。</span><span class="sxs-lookup"><span data-stu-id="960a9-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="960a9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="960a9-116">Requirements</span></span>



| <span data-ttu-id="960a9-117">需求</span><span class="sxs-lookup"><span data-stu-id="960a9-117">Requirement</span></span> | <span data-ttu-id="960a9-118">值</span><span class="sxs-lookup"><span data-stu-id="960a9-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="960a9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="960a9-119">Header</span></span><br/> | <dl> <span data-ttu-id="960a9-120"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="960a9-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="960a9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="960a9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960a9-122">**DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="960a9-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="960a9-123">**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="960a9-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="960a9-124">**結構**</span><span class="sxs-lookup"><span data-stu-id="960a9-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





