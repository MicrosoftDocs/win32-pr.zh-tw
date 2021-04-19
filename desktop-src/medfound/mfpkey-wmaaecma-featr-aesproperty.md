---
description: 指定「語音捕獲」 DSP 對剩餘信號的 (AES) 執行聲場 DSP 抑制的次數。
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: 'MFPKEY_WMAAECMA_FEATR_AES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980737"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a><span data-ttu-id="dff9e-103">MFPKEY \_ WMAAECMA \_ FEATR \_ AES 屬性</span><span class="sxs-lookup"><span data-stu-id="dff9e-103">MFPKEY\_WMAAECMA\_FEATR\_AES Property</span></span>

<span data-ttu-id="dff9e-104">指定「語音捕獲」 DSP 對剩餘信號的 (AES) 執行聲場 DSP 抑制的次數。</span><span class="sxs-lookup"><span data-stu-id="dff9e-104">Specifies how many times the Voice Capture DSP performs acoustic echo suppression (AES) on the residual signal.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="dff9e-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="dff9e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="dff9e-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="dff9e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="dff9e-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="dff9e-107">Data Type</span></span>

<span data-ttu-id="dff9e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="dff9e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="dff9e-109">預設值</span><span class="sxs-lookup"><span data-stu-id="dff9e-109">Default Value</span></span>

<span data-ttu-id="dff9e-110">0</span><span class="sxs-lookup"><span data-stu-id="dff9e-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="dff9e-111">套用至</span><span class="sxs-lookup"><span data-stu-id="dff9e-111">Applies To</span></span>

-   [<span data-ttu-id="dff9e-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="dff9e-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="dff9e-113">備註</span><span class="sxs-lookup"><span data-stu-id="dff9e-113">Remarks</span></span>

<span data-ttu-id="dff9e-114">語音捕獲 DSP 可在回應取消之後，對剩餘的信號執行 AES。</span><span class="sxs-lookup"><span data-stu-id="dff9e-114">The Voice Capture DSP can perform AES on the residual signal after echo cancellation.</span></span> <span data-ttu-id="dff9e-115">這個屬性的值可以是0、1或2。</span><span class="sxs-lookup"><span data-stu-id="dff9e-115">This property can have the value 0, 1, or 2.</span></span> <span data-ttu-id="dff9e-116">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="dff9e-116">The default value is 0.</span></span> <span data-ttu-id="dff9e-117">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="dff9e-117">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="dff9e-118">只有在啟用 AEC 處理時，DSP 才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="dff9e-118">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="dff9e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dff9e-119">Requirements</span></span>



| <span data-ttu-id="dff9e-120">需求</span><span class="sxs-lookup"><span data-stu-id="dff9e-120">Requirement</span></span> | <span data-ttu-id="dff9e-121">值</span><span class="sxs-lookup"><span data-stu-id="dff9e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dff9e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dff9e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dff9e-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dff9e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dff9e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dff9e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dff9e-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dff9e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dff9e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="dff9e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff9e-127"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="dff9e-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff9e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dff9e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff9e-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="dff9e-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="dff9e-130">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="dff9e-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
