---
title: 'DRM_PLAY_OPL 結構 (Wmdrmsdk .h) '
description: DRM \_ play \_ OPL 結構會保存輸出保護層級的相關資訊， (OPLs) 在播放動作的授權中指定。
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995100"
---
# <a name="drm_play_opl-structure"></a><span data-ttu-id="96128-105">DRM \_ PLAY \_ OPL 結構</span><span class="sxs-lookup"><span data-stu-id="96128-105">DRM\_PLAY\_OPL structure</span></span>

<span data-ttu-id="96128-106">**DRM \_ play \_ OPL** 結構會保存輸出保護層級的相關資訊， (OPLs) 在播放動作的授權中指定。</span><span class="sxs-lookup"><span data-stu-id="96128-106">The **DRM\_PLAY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="96128-107">語法</span><span class="sxs-lookup"><span data-stu-id="96128-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="96128-108">成員</span><span class="sxs-lookup"><span data-stu-id="96128-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="96128-109">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="96128-109">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="96128-110">[**DRM \_最小 \_ 輸出 \_ 保護 \_ 層級**](drmdrm-minimum-output-protection-levels.md) 結構，包含以不同格式播放內容所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="96128-110">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="96128-111">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="96128-111">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="96128-112">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="96128-112">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="96128-113">**vopi**</span><span class="sxs-lookup"><span data-stu-id="96128-113">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="96128-114">[**DRM \_影片 \_ 輸出 \_ 保護 \_**](drmdrm-video-output-protection-ids.md) 識別碼結構，其中包含適用于播放內容的影片輸出保護識別碼。</span><span class="sxs-lookup"><span data-stu-id="96128-114">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96128-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="96128-115">Requirements</span></span>



| <span data-ttu-id="96128-116">需求</span><span class="sxs-lookup"><span data-stu-id="96128-116">Requirement</span></span> | <span data-ttu-id="96128-117">值</span><span class="sxs-lookup"><span data-stu-id="96128-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96128-118">標頭</span><span class="sxs-lookup"><span data-stu-id="96128-118">Header</span></span><br/> | <dl> <span data-ttu-id="96128-119"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="96128-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96128-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96128-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96128-121">**DRM \_ 複製 \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="96128-121">**DRM\_COPY\_OPL**</span></span>](drmdrm-copy-opl.md)
</dt> <dt>

[<span data-ttu-id="96128-122">**DRM \_ PLAY \_ OPL \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="96128-122">**DRM\_PLAY\_OPL\_EX**</span></span>](drm-play-opl-ex.md)
</dt> <dt>

[<span data-ttu-id="96128-123">**結構**</span><span class="sxs-lookup"><span data-stu-id="96128-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





