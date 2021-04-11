---
description: 指定 (I、P 或 B 的框架類型)  (已套用的) 的量化參數。
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: 'CODECAPI_AVEncVideoEncodeFrameTypeQP 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111860"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a><span data-ttu-id="d201f-103">CODECAPI \_ AVEncVideoEncodeFrameTypeQP 屬性</span><span class="sxs-lookup"><span data-stu-id="d201f-103">CODECAPI\_AVEncVideoEncodeFrameTypeQP property</span></span>

<span data-ttu-id="d201f-104">指定 (I、P 或 B 的框架類型)  (已套用的) 的量化參數。</span><span class="sxs-lookup"><span data-stu-id="d201f-104">Specifies the frame types (I, P, or B) that the quantization parameter (QP) is applied to.</span></span>

## <a name="data-type"></a><span data-ttu-id="d201f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d201f-105">Data type</span></span>

<span data-ttu-id="d201f-106">**ULONGULONG** (VT \_ UI8) </span><span class="sxs-lookup"><span data-stu-id="d201f-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d201f-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="d201f-107">Property GUID</span></span>

<span data-ttu-id="d201f-108">**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**</span><span class="sxs-lookup"><span data-stu-id="d201f-108">**CODECAPI\_AVEncVideoEncodeFrameTypeQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="d201f-109">備註</span><span class="sxs-lookup"><span data-stu-id="d201f-109">Remarks</span></span>

<span data-ttu-id="d201f-110">針對不同的框架類型，支援設定量化參數 (QP) 的編碼器 (I、P、B) ，除了 [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)之外，還應該公開此 API。</span><span class="sxs-lookup"><span data-stu-id="d201f-110">For encoders which support setting a quantization parameter (QP) for different frame types (I, P, B), they shall expose this API in addition to [CODECAPI\_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span></span> <span data-ttu-id="d201f-111">如果編碼器只針對所有框架類型支援單一的 QP，則只支援 CODECAPI \_ AVEncVideoEncodeQP。</span><span class="sxs-lookup"><span data-stu-id="d201f-111">If an encoder supports only a single QP for all frame types, they shall support only CODECAPI\_AVEncVideoEncodeQP.</span></span>

<span data-ttu-id="d201f-112">這是動態編碼屬性，表示可以在編碼會話期間隨時設定新的值。</span><span class="sxs-lookup"><span data-stu-id="d201f-112">This is a dynamic encoding property meaning that a new value can be set any time during the encoding session.</span></span>

<span data-ttu-id="d201f-113">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="d201f-113">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="d201f-114">編碼器應支援 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)、 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)和 [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="d201f-114">Encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="d201f-115">一組 4 16 位欄位是用來指定固定-QP 編碼的框架 QPs。</span><span class="sxs-lookup"><span data-stu-id="d201f-115">A set of four 16-bit fields are used to specify the frame QPs in fixed-QP encoding.</span></span> <span data-ttu-id="d201f-116">這些欄位包括：</span><span class="sxs-lookup"><span data-stu-id="d201f-116">The fields are:</span></span>

-   <span data-ttu-id="d201f-117">**Bits 0-15：** 用於 I 框架的 QP，有效範圍為 \[ 0，51 \] 。</span><span class="sxs-lookup"><span data-stu-id="d201f-117">**Bits 0-15:** QP used for I frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="d201f-118">**Bits 16-31：** 用於 P 框架的 QP，有效範圍為 \[ 0，51 \] 。</span><span class="sxs-lookup"><span data-stu-id="d201f-118">**Bits 16-31:** QP used for P frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="d201f-119">**Bits 32-47：** 用於 B 框架、有效範圍 \[ 0、51的 QP\]</span><span class="sxs-lookup"><span data-stu-id="d201f-119">**Bits 32-47:** QP used for B frames, valid range \[0, 51\]</span></span>
-   <span data-ttu-id="d201f-120">**Bits 48-63：** 已保留</span><span class="sxs-lookup"><span data-stu-id="d201f-120">**Bits 48-63:** reserved</span></span>

<span data-ttu-id="d201f-121">當支援此 CodecAPI 時，編碼器應支援 I、P 和 B 的框架類型上的 QP 設定。</span><span class="sxs-lookup"><span data-stu-id="d201f-121">When this CodecAPI is supported, encoders shall support QP setting on frame type of I, P, and B.</span></span>

<span data-ttu-id="d201f-122">預設值應該是0x0000001a001a001a。</span><span class="sxs-lookup"><span data-stu-id="d201f-122">Default value shall be 0x0000001a001a001a.</span></span> <span data-ttu-id="d201f-123">適用于 I、P 和 B 的 QP 等於26。</span><span class="sxs-lookup"><span data-stu-id="d201f-123">QP equal to 26 for I, P and B.</span></span>

<span data-ttu-id="d201f-124">當 [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) 選取特定的時態圖層時，CODECAPI AVEncVideoEncodeFrameTypeQP 的 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) \_ 應該在該時態圖層上為 I、P 和 B 框架設定 QP。</span><span class="sxs-lookup"><span data-stu-id="d201f-124">When [CODECAPI\_AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selects a specific temporal layer, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI\_AVEncVideoEncodeFrameTypeQP shall set QP for I, P, and B frames on that temporal layer.</span></span> <span data-ttu-id="d201f-125">根據預設，它會在基底時態層時態圖層0上為 I、P 和 B 框架設定 QP。</span><span class="sxs-lookup"><span data-stu-id="d201f-125">By default, it sets QP for I, P, and B frames on base temporal layer temporal layer 0.</span></span>

<span data-ttu-id="d201f-126">[CODECAPI \_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) 和 [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) 應該用來定義和限制所有圖片類型、I、P 和 B QPs 的 QP 範圍。</span><span class="sxs-lookup"><span data-stu-id="d201f-126">[CODECAPI\_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) and [CODECAPI\_AVEncVideoMinQP](codecapi-avencvideominqp.md) shall be used to define and limit the QP range for QPs of all picture types, I, P and B.</span></span>

## <a name="requirements"></a><span data-ttu-id="d201f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d201f-127">Requirements</span></span>



| <span data-ttu-id="d201f-128">需求</span><span class="sxs-lookup"><span data-stu-id="d201f-128">Requirement</span></span> | <span data-ttu-id="d201f-129">值</span><span class="sxs-lookup"><span data-stu-id="d201f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d201f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d201f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d201f-131">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d201f-131">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="d201f-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d201f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d201f-133">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d201f-133">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d201f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d201f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d201f-135"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d201f-135"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d201f-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d201f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d201f-137">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="d201f-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

