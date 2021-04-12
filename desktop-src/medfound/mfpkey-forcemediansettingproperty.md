---
description: 指定編解碼器是否應在編碼期間使用中位數篩選。
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: 'MFPKEY_FORCEMEDIANSETTING 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853439"
---
# <a name="mfpkey_forcemediansetting-property"></a><span data-ttu-id="fb9c6-103">MFPKEY \_ FORCEMEDIANSETTING 屬性</span><span class="sxs-lookup"><span data-stu-id="fb9c6-103">MFPKEY\_FORCEMEDIANSETTING Property</span></span>

<span data-ttu-id="fb9c6-104">指定編解碼器是否應在編碼期間使用中位數篩選。</span><span class="sxs-lookup"><span data-stu-id="fb9c6-104">Specifies whether the codec should use median filtering during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fb9c6-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="fb9c6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fb9c6-106">g \_ wszWMVCForceMedianSetting</span><span class="sxs-lookup"><span data-stu-id="fb9c6-106">g\_wszWMVCForceMedianSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="fb9c6-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="fb9c6-107">Data Type</span></span>

<span data-ttu-id="fb9c6-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="fb9c6-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="fb9c6-109">預設值</span><span class="sxs-lookup"><span data-stu-id="fb9c6-109">Default Value</span></span>

<span data-ttu-id="fb9c6-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="fb9c6-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="fb9c6-111">備註</span><span class="sxs-lookup"><span data-stu-id="fb9c6-111">Remarks</span></span>

<span data-ttu-id="fb9c6-112">中間值篩選會在計算畫面格之間的動作時，告訴編解碼器忽略雜訊和細微性。</span><span class="sxs-lookup"><span data-stu-id="fb9c6-112">Median filtering tells the codec to ignore noise and grain when calculating motion between frames.</span></span> <span data-ttu-id="fb9c6-113">這可以改善非常雜訊影片的品質，但可能會導致動作軌跡 (也稱為「尾端成品」，) 套用至「清理來源」影片時。</span><span class="sxs-lookup"><span data-stu-id="fb9c6-113">This can improve the quality of very noisy video, but can lead to motion trails (also known as trailing artifacts) when applied to clean source video.</span></span>

<span data-ttu-id="fb9c6-114">根據預設，編解碼器會使用內部邏輯來判斷是否應該使用中間值篩選。</span><span class="sxs-lookup"><span data-stu-id="fb9c6-114">By default, the codec uses internal logic to determine whether median filtering should be used.</span></span> <span data-ttu-id="fb9c6-115">如果設定此屬性，則會覆寫該邏輯。</span><span class="sxs-lookup"><span data-stu-id="fb9c6-115">If you set this property, that logic will be overridden.</span></span>

> [!Note]  
> <span data-ttu-id="fb9c6-116">此篩選與在許多影片編輯和後置處理應用程式中找到的中位數模糊篩選不同。</span><span class="sxs-lookup"><span data-stu-id="fb9c6-116">This filter is not the same as median blur filters found in many video editing and post-processing applications.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb9c6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb9c6-117">Requirements</span></span>



| <span data-ttu-id="fb9c6-118">需求</span><span class="sxs-lookup"><span data-stu-id="fb9c6-118">Requirement</span></span> | <span data-ttu-id="fb9c6-119">值</span><span class="sxs-lookup"><span data-stu-id="fb9c6-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c6-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb9c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fb9c6-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb9c6-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fb9c6-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb9c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fb9c6-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb9c6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb9c6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fb9c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb9c6-125"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb9c6-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb9c6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb9c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9c6-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="fb9c6-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




