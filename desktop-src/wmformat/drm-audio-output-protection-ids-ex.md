---
title: 'DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX 結構 (Wmdrmsdk .h) '
description: DRM \_ 音訊 \_ 輸出 \_ 保護 \_ \_ 識別碼 EX 結構包含音訊輸出保護識別碼的清單。 此結構會藉 \_ \_ \_ \_ 由新增版本號碼來擴充 DRM 音訊輸出保護識別碼。
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991346"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a><span data-ttu-id="beaca-106">DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼 \_ EX 結構</span><span class="sxs-lookup"><span data-stu-id="beaca-106">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="beaca-107">**DRM \_ 音訊 \_ 輸出保護識別碼 \_ \_ \_ EX** 結構包含音訊輸出保護識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="beaca-107">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX** structure contains a list of audio output protection identifiers.</span></span> <span data-ttu-id="beaca-108">此結構會藉由新增版本號碼來擴充 **DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼** 。</span><span class="sxs-lookup"><span data-stu-id="beaca-108">This structure extends **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="beaca-109">語法</span><span class="sxs-lookup"><span data-stu-id="beaca-109">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="beaca-110">成員</span><span class="sxs-lookup"><span data-stu-id="beaca-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="beaca-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="beaca-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="beaca-112">版本號碼。</span><span class="sxs-lookup"><span data-stu-id="beaca-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="beaca-113">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="beaca-113">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="beaca-114">**RgAop** 陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="beaca-114">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="beaca-115">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="beaca-115">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="beaca-116">**DRM \_ 音訊 \_ 輸出保護（ \_ \_ 例如** 結構）的陣列。</span><span class="sxs-lookup"><span data-stu-id="beaca-116">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="beaca-117">**DRM \_音訊 \_ 輸出 \_ 保護 \_** （例如）是定義為 [**DRM \_ 輸出 \_ 保護 \_**](drm-output-protection-ex.md)的類型，例如</span><span class="sxs-lookup"><span data-stu-id="beaca-117">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="beaca-118">備註</span><span class="sxs-lookup"><span data-stu-id="beaca-118">Remarks</span></span>

<span data-ttu-id="beaca-119">無。</span><span class="sxs-lookup"><span data-stu-id="beaca-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="beaca-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="beaca-120">Requirements</span></span>



| <span data-ttu-id="beaca-121">需求</span><span class="sxs-lookup"><span data-stu-id="beaca-121">Requirement</span></span> | <span data-ttu-id="beaca-122">值</span><span class="sxs-lookup"><span data-stu-id="beaca-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="beaca-123">標頭</span><span class="sxs-lookup"><span data-stu-id="beaca-123">Header</span></span><br/> | <dl> <span data-ttu-id="beaca-124"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="beaca-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beaca-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="beaca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beaca-126">**DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="beaca-126">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="beaca-127">**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="beaca-127">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="beaca-128">**結構**</span><span class="sxs-lookup"><span data-stu-id="beaca-128">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





