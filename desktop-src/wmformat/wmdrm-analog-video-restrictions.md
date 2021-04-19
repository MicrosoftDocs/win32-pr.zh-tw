---
title: 'WMDRM_ANALOG_VIDEO_RESTRICTIONS 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 類比 \_ 影片 \_ 限制結構會保存將內容播放為類比影片之限制的相關資訊。
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981279"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a><span data-ttu-id="25e3d-105">WMDRM \_ 類比 \_ 影片 \_ 限制結構</span><span class="sxs-lookup"><span data-stu-id="25e3d-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS structure</span></span>

<span data-ttu-id="25e3d-106">**WMDRM \_ 類比 \_ 影片 \_ 限制** 結構會保存將內容播放為類比影片之限制的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="25e3d-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS** structure holds information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="25e3d-107">語法</span><span class="sxs-lookup"><span data-stu-id="25e3d-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="25e3d-108">成員</span><span class="sxs-lookup"><span data-stu-id="25e3d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="25e3d-109">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="25e3d-109">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="25e3d-110">限制識別碼。</span><span class="sxs-lookup"><span data-stu-id="25e3d-110">Restriction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="25e3d-111">**dwRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="25e3d-111">**dwRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="25e3d-112">限制資料。</span><span class="sxs-lookup"><span data-stu-id="25e3d-112">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25e3d-113">備註</span><span class="sxs-lookup"><span data-stu-id="25e3d-113">Remarks</span></span>

<span data-ttu-id="25e3d-114">當您呼叫 [**IWMDRMLicense：： GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md)時，會收到此結構。</span><span class="sxs-lookup"><span data-stu-id="25e3d-114">This structure is received when you call [**IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25e3d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="25e3d-115">Requirements</span></span>



| <span data-ttu-id="25e3d-116">需求</span><span class="sxs-lookup"><span data-stu-id="25e3d-116">Requirement</span></span> | <span data-ttu-id="25e3d-117">值</span><span class="sxs-lookup"><span data-stu-id="25e3d-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25e3d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="25e3d-118">Header</span></span><br/> | <dl> <span data-ttu-id="25e3d-119"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="25e3d-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e3d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25e3d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e3d-121">**結構**</span><span class="sxs-lookup"><span data-stu-id="25e3d-121">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="25e3d-122">**WMDRM \_ 類比 \_ 影片 \_ 限制， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="25e3d-122">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX**</span></span>](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





