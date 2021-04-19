---
description: 指定感興趣區域的界限，指出需要不同品質的框架區域。
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: 'MFSampleExtension_ROIRectangle 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976822"
---
# <a name="mfsampleextension_roirectangle-attribute"></a><span data-ttu-id="7d855-103">MFSampleExtension \_ ROIRectangle 屬性</span><span class="sxs-lookup"><span data-stu-id="7d855-103">MFSampleExtension\_ROIRectangle attribute</span></span>

<span data-ttu-id="7d855-104">指定感興趣區域的界限，指出需要不同品質的框架區域。</span><span class="sxs-lookup"><span data-stu-id="7d855-104">Specifies the bounds of the region of interest which indicates the region of the frame that requires different quality.</span></span>

## <a name="data-type"></a><span data-ttu-id="7d855-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7d855-105">Data type</span></span>

<span data-ttu-id="7d855-106">**[**ROI \_**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** 儲存為 **BLOB** 的區域</span><span class="sxs-lookup"><span data-stu-id="7d855-106">**[**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stored as **BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="7d855-107">備註</span><span class="sxs-lookup"><span data-stu-id="7d855-107">Remarks</span></span>

<span data-ttu-id="7d855-108">將 [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) 成功設定為編碼器 MFT 上的非零值之後，應用程式可以在輸入範例上設定此屬性，並預期它會被接受。</span><span class="sxs-lookup"><span data-stu-id="7d855-108">After successfully setting [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) to a non-zero value on an encoder MFT, the application can set this attribute on input samples and expect it to be honored.</span></span>

<span data-ttu-id="7d855-109">如果 [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) 未設定為非零值，則在 \_ 輸入範例上會忽略 MFSampleExtension ROIRectangle 屬性。</span><span class="sxs-lookup"><span data-stu-id="7d855-109">If [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) is not set to a non-zero value, the MFSampleExtension\_ROIRectangle attribute is ignored on input samples.</span></span>

<span data-ttu-id="7d855-110">MFSampleExtension \_ ROIRectangle 是在輸入範例上設定的，而且只會套用至目前的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="7d855-110">MFSampleExtension\_ROIRectangle is set on an input sample and is only applied to the current input sample.</span></span>

<span data-ttu-id="7d855-111">[**ROI \_ 區域**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)結構上的 [ **QPDelta** ] 欄位會從框架的其餘部分，指定指定區域的量化參數差異。</span><span class="sxs-lookup"><span data-stu-id="7d855-111">The **QPDelta** field on the [**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) structure specifies the quantization parameter delta for the specified region from the rest of the frame.</span></span> <span data-ttu-id="7d855-112">如果 **QPDelta** 是正數，則表示應用程式希望矩形的品質比框架的其餘部分低。</span><span class="sxs-lookup"><span data-stu-id="7d855-112">If **QPDelta** is positive, this indicates the application wants the rectangle to have lower quality than the rest of the frame.</span></span>

<span data-ttu-id="7d855-113">H.264 **/AVC 編碼器：** **QPDelta** 應介於 \[ -25、+ 25 之間 \] 。</span><span class="sxs-lookup"><span data-stu-id="7d855-113">**H.264/AVC encoders:** **QPDelta** shall be between \[-25, +25\].</span></span> <span data-ttu-id="7d855-114">編碼器應確定最終的 QP 位於適用于影片標準的有效範圍內。</span><span class="sxs-lookup"><span data-stu-id="7d855-114">The encoder shall ensure that the final QP is in a valid range for the video standard.</span></span>

<span data-ttu-id="7d855-115">指定的區域不需要 MB 對齊。</span><span class="sxs-lookup"><span data-stu-id="7d855-115">The specified region is not required to be MB aligned.</span></span> <span data-ttu-id="7d855-116">編碼器具有決定實際界限的彈性。</span><span class="sxs-lookup"><span data-stu-id="7d855-116">Encoders have flexibility to decide the actual boundary.</span></span> <span data-ttu-id="7d855-117">建議您涵蓋整個指定的區域。</span><span class="sxs-lookup"><span data-stu-id="7d855-117">It is recommended to cover the entire specified region.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d855-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d855-118">Requirements</span></span>



| <span data-ttu-id="7d855-119">需求</span><span class="sxs-lookup"><span data-stu-id="7d855-119">Requirement</span></span> | <span data-ttu-id="7d855-120">值</span><span class="sxs-lookup"><span data-stu-id="7d855-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d855-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d855-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d855-122">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d855-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="7d855-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d855-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d855-124">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d855-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7d855-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7d855-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d855-126"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d855-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d855-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d855-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d855-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7d855-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




