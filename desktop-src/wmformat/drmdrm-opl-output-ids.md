---
title: 'DRM_OPL_OUTPUT_IDS 結構 (Wmdrmsdk .h) '
description: DRM \_ OPL \_ 輸出 \_ 識別碼結構會保存多個輸出保護層級 (OPL) 輸出識別碼。
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983114"
---
# <a name="drm_opl_output_ids-structure"></a><span data-ttu-id="7ff7d-105">DRM \_ OPL \_ 輸出 \_ 識別碼結構</span><span class="sxs-lookup"><span data-stu-id="7ff7d-105">DRM\_OPL\_OUTPUT\_IDS structure</span></span>

<span data-ttu-id="7ff7d-106">**DRM \_ OPL \_ 輸出 \_** 識別碼結構會保存多個輸出保護層級 (OPL) 輸出識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ff7d-106">The **DRM\_OPL\_OUTPUT\_IDS** structure holds a number of output protection level (OPL) output identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="7ff7d-107">Syntax</span></span>


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a><span data-ttu-id="7ff7d-108">成員</span><span class="sxs-lookup"><span data-stu-id="7ff7d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ff7d-109">**Cid**</span><span class="sxs-lookup"><span data-stu-id="7ff7d-109">**cIds**</span></span>
</dt> <dd>

<span data-ttu-id="7ff7d-110">**RgIds** 所參考之陣列中的識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="7ff7d-110">Number of identifiers in the array referenced by **rgIds**.</span></span>

</dd> <dt>

<span data-ttu-id="7ff7d-111">**rgIds**</span><span class="sxs-lookup"><span data-stu-id="7ff7d-111">**rgIds**</span></span>
</dt> <dd>

<span data-ttu-id="7ff7d-112">Guid 陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="7ff7d-112">Address of an array of GUIDs.</span></span> <span data-ttu-id="7ff7d-113">陣列的每個成員都包含 OPL 輸出識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ff7d-113">Each member of the array contains an OPL output identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ff7d-114">備註</span><span class="sxs-lookup"><span data-stu-id="7ff7d-114">Remarks</span></span>

<span data-ttu-id="7ff7d-115">此結構會當做 [**drm \_ 複製 \_ OPL**](drmdrm-copy-opl.md) 和 [**drm \_ PLAY \_ OPL**](drmdrm-play-opl.md) 結構的成員使用，以識別輸出識別碼的群組。</span><span class="sxs-lookup"><span data-stu-id="7ff7d-115">This structure is used as a member of the [**DRM\_COPY\_OPL**](drmdrm-copy-opl.md) and [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structures to identify groups of output identifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff7d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ff7d-116">Requirements</span></span>



| <span data-ttu-id="7ff7d-117">需求</span><span class="sxs-lookup"><span data-stu-id="7ff7d-117">Requirement</span></span> | <span data-ttu-id="7ff7d-118">值</span><span class="sxs-lookup"><span data-stu-id="7ff7d-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff7d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7ff7d-119">Header</span></span><br/> | <dl> <span data-ttu-id="7ff7d-120"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff7d-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff7d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ff7d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff7d-122">**結構**</span><span class="sxs-lookup"><span data-stu-id="7ff7d-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





