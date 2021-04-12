---
title: 'GXFPF_ 常數 (Textstor) '
description: GXFPF \_ \ 常數會根據相對於字元周框方塊的點螢幕座標，來指定要傳回的字元位置。
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464705"
---
# <a name="gxfpf_-constants"></a><span data-ttu-id="9189f-103">GXFPF \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="9189f-103">GXFPF\_\* Constants</span></span>

<span data-ttu-id="9189f-104">GXFPF \_ \* 常數會根據相對於字元周框方塊的點螢幕座標，來指定要傳回的字元位置。</span><span class="sxs-lookup"><span data-stu-id="9189f-104">GXFPF\_\* constants specify the character position to return based on the screen coordinates of the point relative to a character bounding box.</span></span>



| <span data-ttu-id="9189f-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="9189f-105">Constant/value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="9189f-106">Description</span><span class="sxs-lookup"><span data-stu-id="9189f-106">Description</span></span>                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <span data-ttu-id="9189f-107"><dt>**GXFPF \_四捨五入 \_ 最接近**</dt>的 <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="9189f-107"><dt>**GXFPF\_ROUND\_NEAREST**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="9189f-108">如果點的螢幕座標包含在字元周框方塊中，則傳回的字元位置是最接近該點螢幕座標的周框邊緣。</span><span class="sxs-lookup"><span data-stu-id="9189f-108">If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.</span></span><br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <span data-ttu-id="9189f-109"><dt>**GXFPF \_最接近**</dt>的 <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="9189f-109"><dt>**GXFPF\_NEAREST**</dt> <dt>( 0x2 )</dt></span></span> </dl>                    | <span data-ttu-id="9189f-110">如果點的螢幕座標未包含在字元周框方塊中，則會傳回最接近的字元位置。</span><span class="sxs-lookup"><span data-stu-id="9189f-110">If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.</span></span><br/>                                                      |



## <a name="remarks"></a><span data-ttu-id="9189f-111">備註</span><span class="sxs-lookup"><span data-stu-id="9189f-111">Remarks</span></span>

<span data-ttu-id="9189f-112">[ITextStoreACP：： GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)和 [ITfCoNtextOwner：： GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)方法的 *dwflags* 參數會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="9189f-112">The *dwflags* parameters of the [ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) and [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) methods use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="9189f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9189f-113">Requirements</span></span>



| <span data-ttu-id="9189f-114">需求</span><span class="sxs-lookup"><span data-stu-id="9189f-114">Requirement</span></span> | <span data-ttu-id="9189f-115">值</span><span class="sxs-lookup"><span data-stu-id="9189f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9189f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9189f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9189f-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9189f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9189f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9189f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9189f-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9189f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9189f-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9189f-120">Redistributable</span></span><br/>          | <span data-ttu-id="9189f-121">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="9189f-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="9189f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9189f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9189f-123"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="9189f-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="9189f-124">Idl</span><span class="sxs-lookup"><span data-stu-id="9189f-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9189f-125"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9189f-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9189f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9189f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9189f-127">ITextStoreACP：： GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="9189f-127">ITextStoreACP::GetACPFromPoint</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[<span data-ttu-id="9189f-128">ITfCoNtextOwner::GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="9189f-128">ITfContextOwner::GetACPFromPoint</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





