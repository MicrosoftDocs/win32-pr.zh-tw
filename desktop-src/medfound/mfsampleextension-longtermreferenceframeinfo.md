---
description: 指定長期參考 (LTR) 框架資訊，並且在輸出範例上傳回。
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: 'MFSampleExtension_LongTermReferenceFrameInfo 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992237"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a><span data-ttu-id="0443a-103">MFSampleExtension \_ LongTermReferenceFrameInfo 屬性</span><span class="sxs-lookup"><span data-stu-id="0443a-103">MFSampleExtension\_LongTermReferenceFrameInfo attribute</span></span>

<span data-ttu-id="0443a-104">指定長期參考 (LTR) 框架資訊，並且在輸出範例上傳回。</span><span class="sxs-lookup"><span data-stu-id="0443a-104">Specifies Long Term Reference (LTR) frame info and is returned on the output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="0443a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0443a-105">Data type</span></span>

<span data-ttu-id="0443a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0443a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0443a-107">備註</span><span class="sxs-lookup"><span data-stu-id="0443a-107">Remarks</span></span>

<span data-ttu-id="0443a-108">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="0443a-108">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="0443a-109">當應用程式控制 LTR 框架（由 [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)指定）時，編碼器應該會在輸出範例上傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0443a-109">Encoders shall return this attribute on the output sample when the application controls LTR frames, which is specified by [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

<span data-ttu-id="0443a-110">MFSampleExtension \_ LongTermReferenceFrameInfo 會傳回最多兩個欄位。</span><span class="sxs-lookup"><span data-stu-id="0443a-110">MFSampleExtension\_LongTermReferenceFrameInfo returns up to two fields.</span></span>

<span data-ttu-id="0443a-111">第一個欄位（位 \[ 0.. 15 \] ） *LongTermFrameIdx* 與輸出框架相關聯（如果它標示為 LTR 框架）。</span><span class="sxs-lookup"><span data-stu-id="0443a-111">The first field, bits\[0..15\], is *LongTermFrameIdx* associated with the output frame if it is marked as a LTR frame.</span></span> <span data-ttu-id="0443a-112">如果這個輸出框架是短期參考框架或非參考框架，則第一個值是0xffff。</span><span class="sxs-lookup"><span data-stu-id="0443a-112">The first value is 0xffff, if this output frame is a short term reference frame or a non-reference frame.</span></span>

<span data-ttu-id="0443a-113">第二個欄位（位 \[ 16.. 31 \] ）是由 *MaxNumLTRFrames* 多個位所組成的點陣圖，表示用來編碼此輸出框架的 (s) ，從位16開始。</span><span class="sxs-lookup"><span data-stu-id="0443a-113">The second field, bits\[16..31\], is a bitmap consisting of *MaxNumLTRFrames* many bits that indicate which LTR frame(s) were used for encoding this output frame, starting from bit 16.</span></span> <span data-ttu-id="0443a-114">其餘的位應設定為0。</span><span class="sxs-lookup"><span data-stu-id="0443a-114">The rest of bits shall be set to 0.</span></span> <span data-ttu-id="0443a-115">如果這個輸出框架未使用任何 LTR 框架編碼，則第二個值是0。</span><span class="sxs-lookup"><span data-stu-id="0443a-115">The second value is 0 if this output frame is not encoded using any LTR frames.</span></span> <span data-ttu-id="0443a-116">*MaxNumLTRFrames* 是透過 [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)設定之 LTR 框架的最大數目。</span><span class="sxs-lookup"><span data-stu-id="0443a-116">*MaxNumLTRFrames* is the maximum number of LTR frames set through [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0443a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0443a-117">Requirements</span></span>



| <span data-ttu-id="0443a-118">需求</span><span class="sxs-lookup"><span data-stu-id="0443a-118">Requirement</span></span> | <span data-ttu-id="0443a-119">值</span><span class="sxs-lookup"><span data-stu-id="0443a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0443a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0443a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0443a-121">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0443a-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="0443a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0443a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0443a-123">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0443a-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0443a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0443a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0443a-125"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="0443a-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0443a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0443a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0443a-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0443a-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




