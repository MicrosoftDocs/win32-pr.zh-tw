---
description: 指定編碼器支援的最大 QP。
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: 'CODECAPI_AVEncVideoMaxQP 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972359"
---
# <a name="codecapi_avencvideomaxqp-property"></a><span data-ttu-id="c78ed-103">CODECAPI \_ AVEncVideoMaxQP 屬性</span><span class="sxs-lookup"><span data-stu-id="c78ed-103">CODECAPI\_AVEncVideoMaxQP property</span></span>

<span data-ttu-id="c78ed-104">指定編碼器支援的最大 QP。</span><span class="sxs-lookup"><span data-stu-id="c78ed-104">Specifies the maximum QP supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="c78ed-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c78ed-105">Data type</span></span>

<span data-ttu-id="c78ed-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="c78ed-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c78ed-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="c78ed-107">Property GUID</span></span>

<span data-ttu-id="c78ed-108">**CODECAPI \_ AVEncVideoMaxQP**</span><span class="sxs-lookup"><span data-stu-id="c78ed-108">**CODECAPI\_AVEncVideoMaxQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="c78ed-109">備註</span><span class="sxs-lookup"><span data-stu-id="c78ed-109">Remarks</span></span>

<span data-ttu-id="c78ed-110">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="c78ed-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="c78ed-111">編碼器應支援 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)、 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)和 [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="c78ed-111">The encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="c78ed-112">這是靜態屬性，表示只能在編碼會話開始之前設定。</span><span class="sxs-lookup"><span data-stu-id="c78ed-112">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="c78ed-113">預設值必須是相對應的編碼標準所允許的最大 QP。</span><span class="sxs-lookup"><span data-stu-id="c78ed-113">Default value shall be the max QP allowed by the corresponding coding standard.</span></span> <span data-ttu-id="c78ed-114">例如，h.264 編碼器的預設值應為51。</span><span class="sxs-lookup"><span data-stu-id="c78ed-114">For example, H.264 encoders shall have a default value of 51.</span></span>

## <a name="requirements"></a><span data-ttu-id="c78ed-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c78ed-115">Requirements</span></span>



| <span data-ttu-id="c78ed-116">需求</span><span class="sxs-lookup"><span data-stu-id="c78ed-116">Requirement</span></span> | <span data-ttu-id="c78ed-117">值</span><span class="sxs-lookup"><span data-stu-id="c78ed-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c78ed-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c78ed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c78ed-119">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c78ed-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="c78ed-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c78ed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c78ed-121">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c78ed-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c78ed-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c78ed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c78ed-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c78ed-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c78ed-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c78ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c78ed-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c78ed-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c78ed-126">CODECAPI \_ AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="c78ed-126">CODECAPI\_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
</dt> </dl>

 

