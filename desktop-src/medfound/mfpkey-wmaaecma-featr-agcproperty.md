---
description: 指定語音捕獲 DSP 是否執行自動增益控制。
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: 'MFPKEY_WMAAECMA_FEATR_AGC 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991839"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a><span data-ttu-id="a31e1-103">MFPKEY \_ WMAAECMA \_ FEATR \_ AGC 屬性</span><span class="sxs-lookup"><span data-stu-id="a31e1-103">MFPKEY\_WMAAECMA\_FEATR\_AGC Property</span></span>

<span data-ttu-id="a31e1-104">指定語音捕獲 DSP 是否執行自動增益控制。</span><span class="sxs-lookup"><span data-stu-id="a31e1-104">Specifies whether the Voice Capture DSP performs automatic gain control.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a31e1-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="a31e1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a31e1-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="a31e1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="a31e1-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="a31e1-107">Data Type</span></span>

<span data-ttu-id="a31e1-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="a31e1-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="a31e1-109">預設值</span><span class="sxs-lookup"><span data-stu-id="a31e1-109">Default Value</span></span>

<span data-ttu-id="a31e1-110">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="a31e1-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="a31e1-111">套用至</span><span class="sxs-lookup"><span data-stu-id="a31e1-111">Applies To</span></span>

-   [<span data-ttu-id="a31e1-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="a31e1-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="a31e1-113">備註</span><span class="sxs-lookup"><span data-stu-id="a31e1-113">Remarks</span></span>

<span data-ttu-id="a31e1-114">自動增益控制是數位信號處理 (DSP) 元件，可調整增益，讓信號的輸出層級維持在相同的大約範圍內。</span><span class="sxs-lookup"><span data-stu-id="a31e1-114">Automatic gain control is a digital signal processing (DSP) component that adjusts the gain so that the output level of the signal remains within the same approximate range.</span></span>

<span data-ttu-id="a31e1-115">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="a31e1-115">This property can have the following values.</span></span>



| <span data-ttu-id="a31e1-116">值</span><span class="sxs-lookup"><span data-stu-id="a31e1-116">Value</span></span>          | <span data-ttu-id="a31e1-117">描述</span><span class="sxs-lookup"><span data-stu-id="a31e1-117">Description</span></span>                     |
|----------------|---------------------------------|
| <span data-ttu-id="a31e1-118">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="a31e1-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="a31e1-119">停用自動增益控制。</span><span class="sxs-lookup"><span data-stu-id="a31e1-119">Disable automatic gain control.</span></span> |
| <span data-ttu-id="a31e1-120">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="a31e1-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="a31e1-121">啟用自動增益控制。</span><span class="sxs-lookup"><span data-stu-id="a31e1-121">Enable automatic gain control.</span></span>  |



 

<span data-ttu-id="a31e1-122">這個屬性的預設值為 VARIANT \_ FALSE (disabled) 。</span><span class="sxs-lookup"><span data-stu-id="a31e1-122">The default value of this property is VARIANT\_FALSE (disabled).</span></span> <span data-ttu-id="a31e1-123">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="a31e1-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a31e1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a31e1-124">Requirements</span></span>



| <span data-ttu-id="a31e1-125">需求</span><span class="sxs-lookup"><span data-stu-id="a31e1-125">Requirement</span></span> | <span data-ttu-id="a31e1-126">值</span><span class="sxs-lookup"><span data-stu-id="a31e1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a31e1-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a31e1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a31e1-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31e1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a31e1-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a31e1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a31e1-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31e1-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a31e1-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a31e1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a31e1-132"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a31e1-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a31e1-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a31e1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a31e1-134">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a31e1-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a31e1-135">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="a31e1-135">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
