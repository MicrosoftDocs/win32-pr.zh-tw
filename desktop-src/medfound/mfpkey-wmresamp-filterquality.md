---
description: 指定輸出的品質。
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: 'MFPKEY_WMRESAMP_FILTERQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191785"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a><span data-ttu-id="f893b-103">MFPKEY \_ WMRESAMP \_ FILTERQUALITY 屬性</span><span class="sxs-lookup"><span data-stu-id="f893b-103">MFPKEY\_WMRESAMP\_FILTERQUALITY Property</span></span>

<span data-ttu-id="f893b-104">指定輸出的品質。</span><span class="sxs-lookup"><span data-stu-id="f893b-104">Specifies the quality of the output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f893b-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="f893b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f893b-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="f893b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f893b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="f893b-107">Data Type</span></span>

<span data-ttu-id="f893b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f893b-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="f893b-109">套用至</span><span class="sxs-lookup"><span data-stu-id="f893b-109">Applies To</span></span>

-   [<span data-ttu-id="f893b-110">音訊 Resampler DSP</span><span class="sxs-lookup"><span data-stu-id="f893b-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="f893b-111">備註</span><span class="sxs-lookup"><span data-stu-id="f893b-111">Remarks</span></span>

<span data-ttu-id="f893b-112">這個屬性的有效範圍是1到60（含）。</span><span class="sxs-lookup"><span data-stu-id="f893b-112">The valid range of this property is 1 to 60, inclusive.</span></span> <span data-ttu-id="f893b-113">較高的值會產生較高品質的輸出，但會導致更多延遲。</span><span class="sxs-lookup"><span data-stu-id="f893b-113">Higher values produce higher-quality output, but introduce more latency.</span></span> <span data-ttu-id="f893b-114">1的值基本上與線性插補相同。</span><span class="sxs-lookup"><span data-stu-id="f893b-114">A value of 1 is essentially the same as linear interpolation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f893b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f893b-115">Requirements</span></span>



| <span data-ttu-id="f893b-116">需求</span><span class="sxs-lookup"><span data-stu-id="f893b-116">Requirement</span></span> | <span data-ttu-id="f893b-117">值</span><span class="sxs-lookup"><span data-stu-id="f893b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f893b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f893b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f893b-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f893b-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f893b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f893b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f893b-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f893b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f893b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f893b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f893b-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f893b-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f893b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f893b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f893b-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="f893b-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
