---
title: 'TS_SHIFT_ 常數 (Textstor) '
description: '\_ \_ IAnchor 介面會使用 TS Shift \ 常數來操作隱藏文字和字元計數。'
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384694"
---
# <a name="ts_shift_-constants"></a><span data-ttu-id="7fdb6-103">TS \_ 移位 \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="7fdb6-103">TS\_SHIFT\_\* Constants</span></span>

<span data-ttu-id="7fdb6-104">\_ \_ \* **IANCHOR** 介面會使用 TS 移位常數來操作隱藏文字和字元計數。</span><span class="sxs-lookup"><span data-stu-id="7fdb6-104">The TS\_Shift\_\* constants are used by the **IAnchor** interface for manipulation of hidden text and character counting.</span></span>



| <span data-ttu-id="7fdb6-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="7fdb6-105">Constant/value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="7fdb6-106">Description</span><span class="sxs-lookup"><span data-stu-id="7fdb6-106">Description</span></span>                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <span data-ttu-id="7fdb6-107"><dt>**TS \_SHIFT \_ COUNT \_ HIDDEN**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="7fdb6-107"><dt>**TS\_SHIFT\_COUNT\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="7fdb6-108">指定錨點將移至下一個區域界限，包括隱藏文字區域的界限。</span><span class="sxs-lookup"><span data-stu-id="7fdb6-108">Specifies that the anchor will be shifted to the next region boundary, including the boundary of a hidden text region.</span></span> <span data-ttu-id="7fdb6-109">如果未設定，則會將錨點移到任何連續的隱藏文字之前，直到找到可見文字的區域為止。</span><span class="sxs-lookup"><span data-stu-id="7fdb6-109">If not set, the anchor will be shifted past any adjacent hidden text until a region of visible text is found.</span></span><br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <span data-ttu-id="7fdb6-110"><dt>**TS \_SHIFT \_ 終止 \_ 隱藏**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="7fdb6-110"><dt>**TS\_SHIFT\_HALT\_HIDDEN**</dt> <dt>( 0x2 )</dt></span></span> </dl>    | <span data-ttu-id="7fdb6-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="7fdb6-111">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <span data-ttu-id="7fdb6-112"><dt>**TS \_SHIFT \_ 終止 \_ 可見**</dt> <dt> ( 0x4 )</dt></span><span class="sxs-lookup"><span data-stu-id="7fdb6-112"><dt>**TS\_SHIFT\_HALT\_VISIBLE**</dt> <dt>( 0x4 )</dt></span></span> </dl> | <span data-ttu-id="7fdb6-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="7fdb6-113">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <span data-ttu-id="7fdb6-114"><dt>**TS \_移位 \_ 計數 \_ 只**</dt> <dt> ( 0x8 )</dt></span><span class="sxs-lookup"><span data-stu-id="7fdb6-114"><dt>**TS\_SHIFT\_COUNT\_ONLY**</dt> <dt>( 0x8 )</dt></span></span> </dl>       | <span data-ttu-id="7fdb6-115">錨點不會移動。</span><span class="sxs-lookup"><span data-stu-id="7fdb6-115">The anchor is not shifted.</span></span><br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="7fdb6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fdb6-116">Requirements</span></span>



| <span data-ttu-id="7fdb6-117">需求</span><span class="sxs-lookup"><span data-stu-id="7fdb6-117">Requirement</span></span> | <span data-ttu-id="7fdb6-118">值</span><span class="sxs-lookup"><span data-stu-id="7fdb6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fdb6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fdb6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7fdb6-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fdb6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7fdb6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fdb6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7fdb6-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fdb6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7fdb6-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7fdb6-123">Redistributable</span></span><br/>          | <span data-ttu-id="7fdb6-124">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="7fdb6-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="7fdb6-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7fdb6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fdb6-126"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fdb6-126"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fdb6-127">Idl</span><span class="sxs-lookup"><span data-stu-id="7fdb6-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7fdb6-128"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fdb6-128"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fdb6-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fdb6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fdb6-130">IAnchor::ShiftRegion</span><span class="sxs-lookup"><span data-stu-id="7fdb6-130">IAnchor::ShiftRegion</span></span>](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





