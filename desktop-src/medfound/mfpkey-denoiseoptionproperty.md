---
description: 指定編解碼器是否會在編碼時使用雜訊篩選器。
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: 'MFPKEY_DENOISEOPTION 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974634"
---
# <a name="mfpkey_denoiseoption-property"></a><span data-ttu-id="900a8-103">MFPKEY \_ DENOISEOPTION 屬性</span><span class="sxs-lookup"><span data-stu-id="900a8-103">MFPKEY\_DENOISEOPTION Property</span></span>

<span data-ttu-id="900a8-104">指定編解碼器是否會在編碼時使用雜訊篩選器。</span><span class="sxs-lookup"><span data-stu-id="900a8-104">Specifies whether the codec will use the noise filter when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="900a8-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="900a8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="900a8-106">g \_ wszWMVCDenoiseOption</span><span class="sxs-lookup"><span data-stu-id="900a8-106">g\_wszWMVCDenoiseOption</span></span>

## <a name="data-type"></a><span data-ttu-id="900a8-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="900a8-107">Data Type</span></span>

<span data-ttu-id="900a8-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="900a8-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="900a8-109">預設值</span><span class="sxs-lookup"><span data-stu-id="900a8-109">Default Value</span></span>

<span data-ttu-id="900a8-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="900a8-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="900a8-111">備註</span><span class="sxs-lookup"><span data-stu-id="900a8-111">Remarks</span></span>

<span data-ttu-id="900a8-112">雜訊篩選器可以改善雜訊影片來源的品質，例如包含很多細微性或影片的電影。</span><span class="sxs-lookup"><span data-stu-id="900a8-112">The noise filter can improve the quality of noisy video sources, such as film containing lots of grain or video shot in low light.</span></span> <span data-ttu-id="900a8-113">此篩選準則可用於無法選擇外部前置處理的即時編碼案例中。</span><span class="sxs-lookup"><span data-stu-id="900a8-113">This filter can be used in live encoding scenarios where external preprocessing is not an option.</span></span>

<span data-ttu-id="900a8-114">這項篩選器應該針對乾淨的影片來源停用，因為它可以在品質適合開始時降低影像品質。</span><span class="sxs-lookup"><span data-stu-id="900a8-114">This filter should be disabled for clean video sources since it can reduce image quality when the quality is good to start with.</span></span>

## <a name="requirements"></a><span data-ttu-id="900a8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="900a8-115">Requirements</span></span>



| <span data-ttu-id="900a8-116">需求</span><span class="sxs-lookup"><span data-stu-id="900a8-116">Requirement</span></span> | <span data-ttu-id="900a8-117">值</span><span class="sxs-lookup"><span data-stu-id="900a8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="900a8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="900a8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="900a8-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="900a8-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="900a8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="900a8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="900a8-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="900a8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="900a8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="900a8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="900a8-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="900a8-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="900a8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="900a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900a8-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="900a8-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




