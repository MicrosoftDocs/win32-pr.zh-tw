---
description: 指定聲場 echo 取消 (AEC) 演算法可以處理的回應持續時間（以毫秒為單位）。
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: 'MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974570"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a><span data-ttu-id="65aa1-103">MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH 屬性</span><span class="sxs-lookup"><span data-stu-id="65aa1-103">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH Property</span></span>

<span data-ttu-id="65aa1-104">指定聲場 echo 取消 (AEC) 演算法可以處理的回應持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="65aa1-104">Specifies the duration of echo that the acoustic echo cancellation (AEC) algorithm can handle, in milliseconds.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="65aa1-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="65aa1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="65aa1-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="65aa1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="65aa1-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="65aa1-107">Data Type</span></span>

<span data-ttu-id="65aa1-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="65aa1-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="65aa1-109">預設值</span><span class="sxs-lookup"><span data-stu-id="65aa1-109">Default Value</span></span>

<span data-ttu-id="65aa1-110">256</span><span class="sxs-lookup"><span data-stu-id="65aa1-110">256</span></span>

## <a name="applies-to"></a><span data-ttu-id="65aa1-111">套用至</span><span class="sxs-lookup"><span data-stu-id="65aa1-111">Applies To</span></span>

-   [<span data-ttu-id="65aa1-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="65aa1-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="65aa1-113">備註</span><span class="sxs-lookup"><span data-stu-id="65aa1-113">Remarks</span></span>

<span data-ttu-id="65aa1-114">AEC 演算法會使用彈性篩選，其長度取決於回應的持續時間。</span><span class="sxs-lookup"><span data-stu-id="65aa1-114">The AEC algorithm uses an adaptive filter whose length is determined by the duration of the echo.</span></span> <span data-ttu-id="65aa1-115">建議應用程式使用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="65aa1-115">It is recommended that applications use one of the following values:</span></span>

-   <span data-ttu-id="65aa1-116">128</span><span class="sxs-lookup"><span data-stu-id="65aa1-116">128</span></span>
-   <span data-ttu-id="65aa1-117">256</span><span class="sxs-lookup"><span data-stu-id="65aa1-117">256</span></span>
-   <span data-ttu-id="65aa1-118">512</span><span class="sxs-lookup"><span data-stu-id="65aa1-118">512</span></span>
-   <span data-ttu-id="65aa1-119">1024</span><span class="sxs-lookup"><span data-stu-id="65aa1-119">1024</span></span>

<span data-ttu-id="65aa1-120">預設值為256毫秒，這對大部分的辦公室和家用環境都已足夠。</span><span class="sxs-lookup"><span data-stu-id="65aa1-120">The default value is 256 milliseconds, which is sufficient for most office and home environments.</span></span> <span data-ttu-id="65aa1-121">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="65aa1-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="65aa1-122">只有在啟用 AEC 處理時，DSP 才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="65aa1-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="65aa1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="65aa1-123">Requirements</span></span>



| <span data-ttu-id="65aa1-124">需求</span><span class="sxs-lookup"><span data-stu-id="65aa1-124">Requirement</span></span> | <span data-ttu-id="65aa1-125">值</span><span class="sxs-lookup"><span data-stu-id="65aa1-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65aa1-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65aa1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="65aa1-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65aa1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="65aa1-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65aa1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="65aa1-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65aa1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65aa1-130">標頭</span><span class="sxs-lookup"><span data-stu-id="65aa1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="65aa1-131"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="65aa1-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65aa1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65aa1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65aa1-133">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="65aa1-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="65aa1-134">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="65aa1-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
