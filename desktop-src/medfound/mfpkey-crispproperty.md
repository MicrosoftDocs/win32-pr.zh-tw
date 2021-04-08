---
description: 指定以數位表示的方式來表示動畫平滑與影像品質的編解碼器輸出之間的取捨。
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: 'MFPKEY_CRISP 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692420"
---
# <a name="mfpkey_crisp-property"></a><span data-ttu-id="b563c-103">MFPKEY \_ 清晰屬性</span><span class="sxs-lookup"><span data-stu-id="b563c-103">MFPKEY\_CRISP Property</span></span>

<span data-ttu-id="b563c-104">指定以數位表示的方式來表示動畫平滑與影像品質的編解碼器輸出之間的取捨。</span><span class="sxs-lookup"><span data-stu-id="b563c-104">Specifies a numeric representation of the tradeoff between motion smoothness and image quality of codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b563c-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="b563c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b563c-106">g \_ wszWMVCCrisp</span><span class="sxs-lookup"><span data-stu-id="b563c-106">g\_wszWMVCCrisp</span></span>

## <a name="data-type"></a><span data-ttu-id="b563c-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="b563c-107">Data Type</span></span>

<span data-ttu-id="b563c-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b563c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b563c-109">預設值</span><span class="sxs-lookup"><span data-stu-id="b563c-109">Default Value</span></span>

<span data-ttu-id="b563c-110">75</span><span class="sxs-lookup"><span data-stu-id="b563c-110">75</span></span>

## <a name="remarks"></a><span data-ttu-id="b563c-111">備註</span><span class="sxs-lookup"><span data-stu-id="b563c-111">Remarks</span></span>

<span data-ttu-id="b563c-112">這個整數值的範圍可以從0到100。</span><span class="sxs-lookup"><span data-stu-id="b563c-112">This integer value can range from 0 to 100.</span></span> <span data-ttu-id="b563c-113">值愈高，編解碼器將會針對個別畫面格的影像品質優化編碼，這通常會減少動畫平滑。</span><span class="sxs-lookup"><span data-stu-id="b563c-113">The higher the value, the more the codec will optimize encoding for the image quality of individual frames, which usually reduces motion smoothness.</span></span>

<span data-ttu-id="b563c-114">這個屬性應該只針對常數位速率 (CBR) 編碼進行設定。</span><span class="sxs-lookup"><span data-stu-id="b563c-114">This property should be set only for constant-bit-rate (CBR) encoding.</span></span> <span data-ttu-id="b563c-115">變數位元速率 (VBR) 編碼的優化會以不同的方式運作。</span><span class="sxs-lookup"><span data-stu-id="b563c-115">The optimizations for variable-bit-rate (VBR) encoding work differently.</span></span>

## <a name="requirements"></a><span data-ttu-id="b563c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b563c-116">Requirements</span></span>



| <span data-ttu-id="b563c-117">需求</span><span class="sxs-lookup"><span data-stu-id="b563c-117">Requirement</span></span> | <span data-ttu-id="b563c-118">值</span><span class="sxs-lookup"><span data-stu-id="b563c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b563c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b563c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b563c-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b563c-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b563c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b563c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b563c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b563c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b563c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b563c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b563c-124"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b563c-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b563c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b563c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b563c-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="b563c-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




