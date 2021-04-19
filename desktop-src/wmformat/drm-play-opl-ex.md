---
title: 'DRM_PLAY_OPL_EX 結構 (Wmdrmsdk .h) '
description: DRM \_ play \_ OPL \_ EX 結構會保存輸出保護層級的相關資訊， (OPLs) 在播放動作的授權中指定。
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998411"
---
# <a name="drm_play_opl_ex-structure"></a><span data-ttu-id="82ac8-105">DRM \_ PLAY \_ OPL \_ EX 結構</span><span class="sxs-lookup"><span data-stu-id="82ac8-105">DRM\_PLAY\_OPL\_EX structure</span></span>

<span data-ttu-id="82ac8-106">**DRM \_ play \_ OPL \_ EX** 結構會保存輸出保護層級的相關資訊， (OPLs) 在播放動作的授權中指定。</span><span class="sxs-lookup"><span data-stu-id="82ac8-106">The **DRM\_PLAY\_OPL\_EX** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ac8-107">語法</span><span class="sxs-lookup"><span data-stu-id="82ac8-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="82ac8-108">成員</span><span class="sxs-lookup"><span data-stu-id="82ac8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="82ac8-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="82ac8-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="82ac8-110">版本號碼。</span><span class="sxs-lookup"><span data-stu-id="82ac8-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="82ac8-111">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="82ac8-111">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="82ac8-112">[**DRM \_最小 \_ 輸出 \_ 保護 \_ 層級**](drmdrm-minimum-output-protection-levels.md) 結構，包含以不同格式播放內容所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="82ac8-112">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="82ac8-113">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="82ac8-113">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="82ac8-114">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="82ac8-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="82ac8-115">**vopi**</span><span class="sxs-lookup"><span data-stu-id="82ac8-115">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="82ac8-116">[**DRM \_影片 \_ 輸出 \_ 保護 \_**](drmdrm-video-output-protection-ids.md) 識別碼結構，其中包含適用于播放內容的影片輸出保護識別碼。</span><span class="sxs-lookup"><span data-stu-id="82ac8-116">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82ac8-117">備註</span><span class="sxs-lookup"><span data-stu-id="82ac8-117">Remarks</span></span>

<span data-ttu-id="82ac8-118">此結構與 **DRM \_ PLAY \_ OPL** 結構相同，不同之處在于它包含版本號碼。</span><span class="sxs-lookup"><span data-stu-id="82ac8-118">This structure is identical to the **DRM\_PLAY\_OPL** structure, except that it includes a version number.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ac8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="82ac8-119">Requirements</span></span>



| <span data-ttu-id="82ac8-120">需求</span><span class="sxs-lookup"><span data-stu-id="82ac8-120">Requirement</span></span> | <span data-ttu-id="82ac8-121">值</span><span class="sxs-lookup"><span data-stu-id="82ac8-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82ac8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="82ac8-122">Header</span></span><br/> | <dl> <span data-ttu-id="82ac8-123"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="82ac8-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ac8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82ac8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ac8-125">**DRM \_ PLAY \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="82ac8-125">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="82ac8-126">**結構**</span><span class="sxs-lookup"><span data-stu-id="82ac8-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





