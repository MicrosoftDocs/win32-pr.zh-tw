---
description: 指定是否使用產生更高品質影片或更快速演算法的演算法。
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: 'MFPKEY_RESIZE_QUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969316"
---
# <a name="mfpkey_resize_quality-property"></a><span data-ttu-id="691b5-103">MFPKEY \_ 調整 \_ 品質屬性</span><span class="sxs-lookup"><span data-stu-id="691b5-103">MFPKEY\_RESIZE\_QUALITY Property</span></span>

<span data-ttu-id="691b5-104">指定是否使用產生更高品質影片或更快速演算法的演算法。</span><span class="sxs-lookup"><span data-stu-id="691b5-104">Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="691b5-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="691b5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="691b5-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="691b5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="691b5-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="691b5-107">Data Type</span></span>

<span data-ttu-id="691b5-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="691b5-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="691b5-109">套用至</span><span class="sxs-lookup"><span data-stu-id="691b5-109">Applies To</span></span>

-   [<span data-ttu-id="691b5-110">影片尺寸調整 DSP</span><span class="sxs-lookup"><span data-stu-id="691b5-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="691b5-111">備註</span><span class="sxs-lookup"><span data-stu-id="691b5-111">Remarks</span></span>

<span data-ttu-id="691b5-112">請使用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="691b5-112">Use one of the following values:</span></span>



| <span data-ttu-id="691b5-113">值</span><span class="sxs-lookup"><span data-stu-id="691b5-113">Value</span></span>     | <span data-ttu-id="691b5-114">描述</span><span class="sxs-lookup"><span data-stu-id="691b5-114">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="691b5-115">VT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="691b5-115">VT\_FALSE</span></span> | <span data-ttu-id="691b5-116">更快速的演算法</span><span class="sxs-lookup"><span data-stu-id="691b5-116">Faster algorithm</span></span>     |
| <span data-ttu-id="691b5-117">VT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="691b5-117">VT\_TRUE</span></span>  | <span data-ttu-id="691b5-118">品質較高的影片</span><span class="sxs-lookup"><span data-stu-id="691b5-118">Higher-quality video</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="691b5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="691b5-119">Requirements</span></span>



| <span data-ttu-id="691b5-120">需求</span><span class="sxs-lookup"><span data-stu-id="691b5-120">Requirement</span></span> | <span data-ttu-id="691b5-121">值</span><span class="sxs-lookup"><span data-stu-id="691b5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="691b5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="691b5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="691b5-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="691b5-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="691b5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="691b5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="691b5-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="691b5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="691b5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="691b5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="691b5-127"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="691b5-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="691b5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="691b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="691b5-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="691b5-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
