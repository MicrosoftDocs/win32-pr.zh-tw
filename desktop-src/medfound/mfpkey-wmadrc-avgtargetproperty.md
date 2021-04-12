---
description: 指定輸出音訊內容所需的平均音量層級。
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: 'MFPKEY_WMADRC_AVGTARGET 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192166"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a><span data-ttu-id="db650-103">MFPKEY \_ WMADRC \_ AVGTARGET 屬性</span><span class="sxs-lookup"><span data-stu-id="db650-103">MFPKEY\_WMADRC\_AVGTARGET Property</span></span>

<span data-ttu-id="db650-104">指定輸出音訊內容所需的平均音量層級。</span><span class="sxs-lookup"><span data-stu-id="db650-104">Specifies the desired average volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="db650-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="db650-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="db650-106">g \_ wszWMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="db650-106">g\_wszWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="db650-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="db650-107">Data Type</span></span>

<span data-ttu-id="db650-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="db650-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="db650-109">預設值</span><span class="sxs-lookup"><span data-stu-id="db650-109">Default Value</span></span>

<span data-ttu-id="db650-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="db650-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="db650-111">備註</span><span class="sxs-lookup"><span data-stu-id="db650-111">Remarks</span></span>

<span data-ttu-id="db650-112">您可以針對動態範圍控制項的目的，在解碼器上設定此值，但只有在已設定 [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) 屬性時，才會有作用。</span><span class="sxs-lookup"><span data-stu-id="db650-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

> [!Note]  
> <span data-ttu-id="db650-113">不建議設定平均目標值。</span><span class="sxs-lookup"><span data-stu-id="db650-113">Setting the average target value is not recommended.</span></span> <span data-ttu-id="db650-114">調整平均值不會影響高音和音效之間的差異。</span><span class="sxs-lookup"><span data-stu-id="db650-114">Adjusting the average value does not affect the difference between loud and soft sounds.</span></span> <span data-ttu-id="db650-115">相反地，它會剪下或提高整體平均量，而這可能會在播放期間造成不適當的失真。</span><span class="sxs-lookup"><span data-stu-id="db650-115">Instead, it cuts or boosts the overall average volume which may cause undesirable distortion during playback.</span></span>

 

<span data-ttu-id="db650-116">如果您在未設定此屬性時，從編碼器要求動態範圍控制，則編解碼器會計算預設值。</span><span class="sxs-lookup"><span data-stu-id="db650-116">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="db650-117">您可以使用 [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) 和 [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) 屬性來計算這個屬性的適當值。</span><span class="sxs-lookup"><span data-stu-id="db650-117">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="db650-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="db650-118">Requirements</span></span>



| <span data-ttu-id="db650-119">需求</span><span class="sxs-lookup"><span data-stu-id="db650-119">Requirement</span></span> | <span data-ttu-id="db650-120">值</span><span class="sxs-lookup"><span data-stu-id="db650-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db650-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db650-121">Minimum supported client</span></span><br/> | <span data-ttu-id="db650-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db650-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db650-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db650-123">Minimum supported server</span></span><br/> | <span data-ttu-id="db650-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db650-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db650-125">標頭</span><span class="sxs-lookup"><span data-stu-id="db650-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="db650-126"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="db650-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db650-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db650-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db650-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="db650-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




