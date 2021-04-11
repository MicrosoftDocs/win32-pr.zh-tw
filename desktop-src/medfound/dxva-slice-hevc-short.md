---
description: 指定配量控制項資料。
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: 'DXVA_Slice_HEVC_Short 結構 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026039"
---
# <a name="dxva_slice_hevc_short-structure"></a><span data-ttu-id="bc2d0-103">DXVA 配量 \_ \_ HEVC \_ 簡略結構</span><span class="sxs-lookup"><span data-stu-id="bc2d0-103">DXVA\_Slice\_HEVC\_Short structure</span></span>

<span data-ttu-id="bc2d0-104">指定配量控制項資料。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-104">Specifies slice control data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc2d0-105">Syntax</span></span>


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a><span data-ttu-id="bc2d0-106">成員</span><span class="sxs-lookup"><span data-stu-id="bc2d0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc2d0-107">**BSNALunitDataLocation**</span><span class="sxs-lookup"><span data-stu-id="bc2d0-107">**BSNALunitDataLocation**</span></span>
</dt> <dd>

<span data-ttu-id="bc2d0-108">指定 NAL 單位的位置。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-108">Specifies the location of the NAL unit.</span></span>

</dd> <dt>

<span data-ttu-id="bc2d0-109">**SliceBytesInBuffer**</span><span class="sxs-lookup"><span data-stu-id="bc2d0-109">**SliceBytesInBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="bc2d0-110">位流資料緩衝區中與這個配量控制項資料結構相關聯的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-110">The number of bytes in the bitstream data buffer that are associated with this slice control data structure.</span></span>

</dd> <dt>

<span data-ttu-id="bc2d0-111">**wBadSliceChopping**</span><span class="sxs-lookup"><span data-stu-id="bc2d0-111">**wBadSliceChopping**</span></span>
</dt> <dd>

<span data-ttu-id="bc2d0-112">如果使用了非主機位流剖析，此值會指出錯誤的配量將切分成，並包含下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="bc2d0-112">If off-host bitstream parsing is used, this value indicates the bad slice chopping and contains one of the following values:</span></span>



| <span data-ttu-id="bc2d0-113">需求</span><span class="sxs-lookup"><span data-stu-id="bc2d0-113">Requirement</span></span> | <span data-ttu-id="bc2d0-114">值</span><span class="sxs-lookup"><span data-stu-id="bc2d0-114">Value</span></span> |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2d0-115">值</span><span class="sxs-lookup"><span data-stu-id="bc2d0-115">Value</span></span> | <span data-ttu-id="bc2d0-116">描述</span><span class="sxs-lookup"><span data-stu-id="bc2d0-116">Description</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="bc2d0-117">0</span><span class="sxs-lookup"><span data-stu-id="bc2d0-117">0</span></span>     | <span data-ttu-id="bc2d0-118">配量的所有位都位於對應的位流資料緩衝區內。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-118">All bits for the slice are located within the corresponding bitstream data buffer.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="bc2d0-119">1</span><span class="sxs-lookup"><span data-stu-id="bc2d0-119">1</span></span>     | <span data-ttu-id="bc2d0-120">位流資料緩衝區包含配量的開頭，而不是整個磁區，因為緩衝區已滿。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-120">The bitstream data buffer contains the start of the slice, but not the entire slice, because the buffer is full.</span></span>                                                                                                                                        |
| <span data-ttu-id="bc2d0-121">2</span><span class="sxs-lookup"><span data-stu-id="bc2d0-121">2</span></span>     | <span data-ttu-id="bc2d0-122">位流資料緩衝區包含配量的結尾。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-122">The bitstream data buffer contains the end of the slice.</span></span> <span data-ttu-id="bc2d0-123">它不會包含配量的起點，因為配量開頭是位於先前的位流資料緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-123">It does not contain the start of the slice, because the start of the slice was located in the previous bitstream data buffer.</span></span>                                                                  |
| <span data-ttu-id="bc2d0-124">3</span><span class="sxs-lookup"><span data-stu-id="bc2d0-124">3</span></span>     | <span data-ttu-id="bc2d0-125">位流資料緩衝區不包含配量的開頭，因為配量的開頭位於先前的位流資料緩衝區，而且不包含配量的結尾，因為目前的位流資料緩衝區也已滿。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-125">The bitstream data buffer does not contain the start of the slice because the start of the slice was located in the previous bitstream data buffer and it does not contain the end of the slice becuase the current bitstream data buffer is also full.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc2d0-126">備註</span><span class="sxs-lookup"><span data-stu-id="bc2d0-126">Remarks</span></span>

<span data-ttu-id="bc2d0-127">**DXVA \_配量 \_ HEVC \_ Short** 包含配量控制項資料，此資料會從主機軟體解碼器傳遞給硬體加速器。</span><span class="sxs-lookup"><span data-stu-id="bc2d0-127">**DXVA\_Slice\_HEVC\_Short** contains slice control data which is passed to the hardware accelerator from the host software decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc2d0-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc2d0-128">Requirements</span></span>



| <span data-ttu-id="bc2d0-129">需求</span><span class="sxs-lookup"><span data-stu-id="bc2d0-129">Requirement</span></span> | <span data-ttu-id="bc2d0-130">值</span><span class="sxs-lookup"><span data-stu-id="bc2d0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bc2d0-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc2d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bc2d0-132">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc2d0-132">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bc2d0-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc2d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bc2d0-134">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc2d0-134">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bc2d0-135">標頭</span><span class="sxs-lookup"><span data-stu-id="bc2d0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc2d0-136"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc2d0-136"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc2d0-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc2d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2d0-138">媒體基礎結構</span><span class="sxs-lookup"><span data-stu-id="bc2d0-138">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




