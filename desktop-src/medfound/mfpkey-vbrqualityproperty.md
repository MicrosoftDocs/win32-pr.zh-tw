---
description: 指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: 'MFPKEY_VBRQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943906"
---
# <a name="mfpkey_vbrquality-property"></a><span data-ttu-id="3c862-103">MFPKEY \_ VBRQUALITY 屬性</span><span class="sxs-lookup"><span data-stu-id="3c862-103">MFPKEY\_VBRQUALITY Property</span></span>

<span data-ttu-id="3c862-104">指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="3c862-104">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3c862-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="3c862-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3c862-106">g \_ wszWMVCVBRQuality、g \_ wszWMCPAudioVBRQuality</span><span class="sxs-lookup"><span data-stu-id="3c862-106">g\_wszWMVCVBRQuality, g\_wszWMCPAudioVBRQuality</span></span>

## <a name="data-type"></a><span data-ttu-id="3c862-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="3c862-107">Data Type</span></span>

<span data-ttu-id="3c862-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3c862-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="3c862-109">備註</span><span class="sxs-lookup"><span data-stu-id="3c862-109">Remarks</span></span>

<span data-ttu-id="3c862-110">並非範圍內的所有值都有唯一的意義。</span><span class="sxs-lookup"><span data-stu-id="3c862-110">Not all of the values in the range have a unique meaning.</span></span> <span data-ttu-id="3c862-111">代表上一層級之品質上階的值為：1、4、8、11、15、18、22、25、29、33、36、40、43、47、50、54、58、61、65、68、72、75、79、83、86、90、93和97。</span><span class="sxs-lookup"><span data-stu-id="3c862-111">The values that represent a step up in quality from the previous level are: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, and 100.</span></span>

<span data-ttu-id="3c862-112">若為音訊編碼器物件，則會在您使用 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)取出的輸出類型 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構中提供品質模式。</span><span class="sxs-lookup"><span data-stu-id="3c862-112">For audio encoder objects, the quality modes are provided in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the output types that you retrieve using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c862-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c862-113">Requirements</span></span>



| <span data-ttu-id="3c862-114">需求</span><span class="sxs-lookup"><span data-stu-id="3c862-114">Requirement</span></span> | <span data-ttu-id="3c862-115">值</span><span class="sxs-lookup"><span data-stu-id="3c862-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c862-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c862-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c862-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c862-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3c862-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c862-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c862-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c862-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c862-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3c862-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c862-121"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c862-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c862-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c862-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c862-123">列舉特定編碼模式的音訊類型</span><span class="sxs-lookup"><span data-stu-id="3c862-123">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[<span data-ttu-id="3c862-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3c862-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
