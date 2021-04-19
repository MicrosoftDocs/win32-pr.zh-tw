---
title: 'DRM_COPY_OPL 結構 (Wmdrmsdk .h) '
description: DRM \_ 複製 \_ OPL 結構會保存輸出保護層級的相關資訊， (OPLs 在複製動作的授權中指定的) 。
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980146"
---
# <a name="drm_copy_opl-structure"></a><span data-ttu-id="770b5-105">DRM \_ 複製 \_ OPL 結構</span><span class="sxs-lookup"><span data-stu-id="770b5-105">DRM\_COPY\_OPL structure</span></span>

<span data-ttu-id="770b5-106">**DRM \_ 複製 \_ OPL** 結構會保存輸出保護層級的相關資訊， (OPLs 在複製動作的授權中指定的) 。</span><span class="sxs-lookup"><span data-stu-id="770b5-106">The **DRM\_COPY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for copy actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="770b5-107">語法</span><span class="sxs-lookup"><span data-stu-id="770b5-107">Syntax</span></span>


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a><span data-ttu-id="770b5-108">成員</span><span class="sxs-lookup"><span data-stu-id="770b5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="770b5-109">**wMinimumCopyLevel**</span><span class="sxs-lookup"><span data-stu-id="770b5-109">**wMinimumCopyLevel**</span></span>
</dt> <dd>

<span data-ttu-id="770b5-110">複製動作的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="770b5-110">Minimum OPL for copy actions.</span></span>

</dd> <dt>

<span data-ttu-id="770b5-111">**oplIdIncludes**</span><span class="sxs-lookup"><span data-stu-id="770b5-111">**oplIdIncludes**</span></span>
</dt> <dd>

<span data-ttu-id="770b5-112">[**DRM \_OPL \_ 輸出 \_**](drmdrm-opl-output-ids.md) 識別碼結構，其中包含要允許的技術識別碼。</span><span class="sxs-lookup"><span data-stu-id="770b5-112">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the identifiers of technologies to allow.</span></span> <span data-ttu-id="770b5-113">此成員用於指派的 OPLs 低於最小複製層級的輸出技術，但可將內容複寫到其中。</span><span class="sxs-lookup"><span data-stu-id="770b5-113">This member is used for output technologies that are assigned OPLs lower than the minimum copy level, but to which the content may be copied.</span></span>

</dd> <dt>

<span data-ttu-id="770b5-114">**oplIdExcludes**</span><span class="sxs-lookup"><span data-stu-id="770b5-114">**oplIdExcludes**</span></span>
</dt> <dd>

<span data-ttu-id="770b5-115">[**DRM \_OPL \_ 輸出 \_**](drmdrm-opl-output-ids.md) 識別碼結構，其中包含要限制之技術的輸出識別碼。</span><span class="sxs-lookup"><span data-stu-id="770b5-115">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the output identifiers of technologies to restrict.</span></span> <span data-ttu-id="770b5-116">此成員用於指派的 OPLs 超過最小複製層級的輸出技術，但授權簽發者不會授與複製的許可權。</span><span class="sxs-lookup"><span data-stu-id="770b5-116">This member is used for output technologies that are assigned OPLs that exceed the minimum copy level, but that the license issuer does not grant rights for copying to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="770b5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="770b5-117">Requirements</span></span>



| <span data-ttu-id="770b5-118">需求</span><span class="sxs-lookup"><span data-stu-id="770b5-118">Requirement</span></span> | <span data-ttu-id="770b5-119">值</span><span class="sxs-lookup"><span data-stu-id="770b5-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="770b5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="770b5-120">Header</span></span><br/> | <dl> <span data-ttu-id="770b5-121"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="770b5-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="770b5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="770b5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="770b5-123">**DRM \_ PLAY \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="770b5-123">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="770b5-124">**結構**</span><span class="sxs-lookup"><span data-stu-id="770b5-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





