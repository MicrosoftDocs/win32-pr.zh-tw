---
title: 'WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 類比 \_ 影片 \_ 限制 \_ EX 結構會保存有關將內容播放為類比影片之限制的延伸資訊。
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995255"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a><span data-ttu-id="38a46-105">WMDRM \_ 類比 \_ 影片 \_ 限制 \_ EX 結構</span><span class="sxs-lookup"><span data-stu-id="38a46-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX structure</span></span>

<span data-ttu-id="38a46-106">**WMDRM \_ 類比 \_ 影片 \_ 限制 \_ EX** 結構會保存有關將內容播放為類比影片之限制的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="38a46-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX** structure holds extended information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a46-107">語法</span><span class="sxs-lookup"><span data-stu-id="38a46-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="38a46-108">成員</span><span class="sxs-lookup"><span data-stu-id="38a46-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="38a46-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="38a46-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="38a46-110">版本號碼。</span><span class="sxs-lookup"><span data-stu-id="38a46-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="38a46-111">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="38a46-111">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="38a46-112">限制識別碼。</span><span class="sxs-lookup"><span data-stu-id="38a46-112">Restriction ID.</span></span>

</dd> <dt>

<span data-ttu-id="38a46-113">**cbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="38a46-113">**cbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="38a46-114">限制資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="38a46-114">Size of restriction data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="38a46-115">**pbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="38a46-115">**pbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="38a46-116">限制資料。</span><span class="sxs-lookup"><span data-stu-id="38a46-116">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38a46-117">備註</span><span class="sxs-lookup"><span data-stu-id="38a46-117">Remarks</span></span>

<span data-ttu-id="38a46-118">無。</span><span class="sxs-lookup"><span data-stu-id="38a46-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="38a46-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="38a46-119">Requirements</span></span>



| <span data-ttu-id="38a46-120">需求</span><span class="sxs-lookup"><span data-stu-id="38a46-120">Requirement</span></span> | <span data-ttu-id="38a46-121">值</span><span class="sxs-lookup"><span data-stu-id="38a46-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38a46-122">標頭</span><span class="sxs-lookup"><span data-stu-id="38a46-122">Header</span></span><br/> | <dl> <span data-ttu-id="38a46-123"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="38a46-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a46-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38a46-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a46-125">**結構**</span><span class="sxs-lookup"><span data-stu-id="38a46-125">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="38a46-126">**WMDRM \_ 類比 \_ 影片 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="38a46-126">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**</span></span>](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





