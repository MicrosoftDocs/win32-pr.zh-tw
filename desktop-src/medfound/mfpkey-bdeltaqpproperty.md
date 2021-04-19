---
description: 指定在錨點框架的圖片 quantizer 與 B 型框架的圖片 quantizer 之間的差異增加。
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: 'MFPKEY_BDELTAQP 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986916"
---
# <a name="mfpkey_bdeltaqp-property"></a><span data-ttu-id="0b5bb-103">MFPKEY \_ BDELTAQP 屬性</span><span class="sxs-lookup"><span data-stu-id="0b5bb-103">MFPKEY\_BDELTAQP Property</span></span>

<span data-ttu-id="0b5bb-104">指定在錨點框架的圖片 quantizer 與 B 型框架的圖片 quantizer 之間的差異增加。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-104">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0b5bb-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="0b5bb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0b5bb-106">g \_ wszWMVCBDeltaQP</span><span class="sxs-lookup"><span data-stu-id="0b5bb-106">g\_wszWMVCBDeltaQP</span></span>

## <a name="data-type"></a><span data-ttu-id="0b5bb-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="0b5bb-107">Data Type</span></span>

<span data-ttu-id="0b5bb-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0b5bb-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="0b5bb-109">預設值</span><span class="sxs-lookup"><span data-stu-id="0b5bb-109">Default Value</span></span>

<span data-ttu-id="0b5bb-110">0</span><span class="sxs-lookup"><span data-stu-id="0b5bb-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="0b5bb-111">備註</span><span class="sxs-lookup"><span data-stu-id="0b5bb-111">Remarks</span></span>

<span data-ttu-id="0b5bb-112">Picture quantizer (QP) 是一種測量框架壓縮方式的度量。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-112">Picture quantizer (QP) is a measurement of how compressed a frame is.</span></span> <span data-ttu-id="0b5bb-113">較高的值表示較高的壓縮比率。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-113">Higher values represent higher compression ratios.</span></span> <span data-ttu-id="0b5bb-114">您可以設定以半點遞增的方式設定 QP。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-114">The QP can be set in half-point increments.</span></span> <span data-ttu-id="0b5bb-115">B 型框架通常會在與錨點框架的 QP 相同或高於0.5 的 QP 上進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-115">A B-frame is typically compressed at a QP the same as or 0.5 higher than the anchor frame's QP.</span></span> <span data-ttu-id="0b5bb-116">您可以藉由指定大於0的 B 型框架 QP 差異，以更高的壓縮比例壓縮 B 框架。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-116">By specifying a B-frame QP delta higher than 0, it is possible to compress B-frames at an even higher compression ratio.</span></span>

<span data-ttu-id="0b5bb-117">B 型框架 delta QP 只能以整數遞增的方式設定。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-117">The B-frame delta QP can be set only in whole-point increments.</span></span> <span data-ttu-id="0b5bb-118">這個屬性必須設定為介於0到31之間的整數值。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-118">This property must be set to an integer value from 0 to 31.</span></span> <span data-ttu-id="0b5bb-119">建議值為1。</span><span class="sxs-lookup"><span data-stu-id="0b5bb-119">The recommended value is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b5bb-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b5bb-120">Requirements</span></span>



| <span data-ttu-id="0b5bb-121">需求</span><span class="sxs-lookup"><span data-stu-id="0b5bb-121">Requirement</span></span> | <span data-ttu-id="0b5bb-122">值</span><span class="sxs-lookup"><span data-stu-id="0b5bb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b5bb-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b5bb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0b5bb-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b5bb-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0b5bb-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b5bb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0b5bb-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b5bb-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0b5bb-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0b5bb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b5bb-128"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b5bb-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b5bb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b5bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b5bb-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="0b5bb-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




