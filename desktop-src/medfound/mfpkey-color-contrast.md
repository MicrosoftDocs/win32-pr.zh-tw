---
description: 調整對比。
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: 'MFPKEY_COLOR_CONTRAST 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988744"
---
# <a name="mfpkey_color_contrast-property"></a><span data-ttu-id="e6ac6-103">MFPKEY \_ 色彩 \_ 對比屬性</span><span class="sxs-lookup"><span data-stu-id="e6ac6-103">MFPKEY\_COLOR\_CONTRAST Property</span></span>

<span data-ttu-id="e6ac6-104">調整對比。</span><span class="sxs-lookup"><span data-stu-id="e6ac6-104">Adjusts the contrast.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e6ac6-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="e6ac6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e6ac6-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="e6ac6-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e6ac6-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="e6ac6-107">Data Type</span></span>

<span data-ttu-id="e6ac6-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e6ac6-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e6ac6-109">預設值</span><span class="sxs-lookup"><span data-stu-id="e6ac6-109">Default Value</span></span>

<span data-ttu-id="e6ac6-110">0</span><span class="sxs-lookup"><span data-stu-id="e6ac6-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="e6ac6-111">套用至</span><span class="sxs-lookup"><span data-stu-id="e6ac6-111">Applies To</span></span>

-   [<span data-ttu-id="e6ac6-112">色彩控制轉換 DSP</span><span class="sxs-lookup"><span data-stu-id="e6ac6-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="e6ac6-113">備註</span><span class="sxs-lookup"><span data-stu-id="e6ac6-113">Remarks</span></span>

<span data-ttu-id="e6ac6-114">對比調整是藉由將 YCbCr 值乘以縮放因數來執行。</span><span class="sxs-lookup"><span data-stu-id="e6ac6-114">Contrast adjustment is performed by multiplying the YCbCr values by a scaling factor.</span></span>

<span data-ttu-id="e6ac6-115">這個屬性的範圍為-127 到127。</span><span class="sxs-lookup"><span data-stu-id="e6ac6-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="e6ac6-116">零表示對比沒有變更。</span><span class="sxs-lookup"><span data-stu-id="e6ac6-116">Zero indicates no change in contrast.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ac6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6ac6-117">Requirements</span></span>



| <span data-ttu-id="e6ac6-118">需求</span><span class="sxs-lookup"><span data-stu-id="e6ac6-118">Requirement</span></span> | <span data-ttu-id="e6ac6-119">值</span><span class="sxs-lookup"><span data-stu-id="e6ac6-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ac6-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6ac6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ac6-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6ac6-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e6ac6-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6ac6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ac6-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6ac6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6ac6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e6ac6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6ac6-125"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6ac6-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ac6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6ac6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ac6-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e6ac6-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
