---
description: 設定語音捕獲 DSP 的處理模式。
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: 'MFPKEY_WMAAECMA_SYSTEM_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974210"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a><span data-ttu-id="f940b-103">MFPKEY \_ WMAAECMA \_ 系統 \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="f940b-103">MFPKEY\_WMAAECMA\_SYSTEM\_MODE Property</span></span>

<span data-ttu-id="f940b-104">設定語音捕獲 DSP 的處理模式。</span><span class="sxs-lookup"><span data-stu-id="f940b-104">Sets the processing mode for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f940b-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="f940b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f940b-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="f940b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f940b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="f940b-107">Data Type</span></span>

<span data-ttu-id="f940b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f940b-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="f940b-109">套用至</span><span class="sxs-lookup"><span data-stu-id="f940b-109">Applies To</span></span>

-   [<span data-ttu-id="f940b-110">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="f940b-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="f940b-111">備註</span><span class="sxs-lookup"><span data-stu-id="f940b-111">Remarks</span></span>

<span data-ttu-id="f940b-112">這個屬性的值是 [AEC \_ 系統 \_ 模式](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="f940b-112">The value of this property is a member of the [AEC\_SYSTEM\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) enumeration.</span></span>

<span data-ttu-id="f940b-113">屬性必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f940b-113">The property must be one of the following values.</span></span>



| <span data-ttu-id="f940b-114">值</span><span class="sxs-lookup"><span data-stu-id="f940b-114">Value</span></span> | <span data-ttu-id="f940b-115">描述</span><span class="sxs-lookup"><span data-stu-id="f940b-115">Description</span></span>                                 |
|-------|---------------------------------------------|
| <span data-ttu-id="f940b-116">0</span><span class="sxs-lookup"><span data-stu-id="f940b-116">0</span></span>     | <span data-ttu-id="f940b-117">音訊 echo 取消 (AEC 只) 模式</span><span class="sxs-lookup"><span data-stu-id="f940b-117">Audio echo cancellation (AEC) only mode</span></span>     |
| <span data-ttu-id="f940b-118">2</span><span class="sxs-lookup"><span data-stu-id="f940b-118">2</span></span>     | <span data-ttu-id="f940b-119">麥克風陣列處理 (MAP) 模式</span><span class="sxs-lookup"><span data-stu-id="f940b-119">Microphone array processing (MAP) only mode</span></span> |
| <span data-ttu-id="f940b-120">4</span><span class="sxs-lookup"><span data-stu-id="f940b-120">4</span></span>     | <span data-ttu-id="f940b-121">AEC 和對應模式</span><span class="sxs-lookup"><span data-stu-id="f940b-121">AEC and MAP mode</span></span>                            |
| <span data-ttu-id="f940b-122">5</span><span class="sxs-lookup"><span data-stu-id="f940b-122">5</span></span>     | <span data-ttu-id="f940b-123">AEC 或對應模式皆非</span><span class="sxs-lookup"><span data-stu-id="f940b-123">Neither AEC nor MAP mode</span></span>                    |



 

<span data-ttu-id="f940b-124">您必須先設定這個屬性，才能使用語音捕獲 DSP。</span><span class="sxs-lookup"><span data-stu-id="f940b-124">You must set this property before using the Voice Capture DSP.</span></span> <span data-ttu-id="f940b-125">設定這個屬性之後，您可以使用 DSP 的預設設定，或設定其他屬性。</span><span class="sxs-lookup"><span data-stu-id="f940b-125">After you set this property, you can use the DSP with its default settings, or set additional properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="f940b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f940b-126">Requirements</span></span>



| <span data-ttu-id="f940b-127">需求</span><span class="sxs-lookup"><span data-stu-id="f940b-127">Requirement</span></span> | <span data-ttu-id="f940b-128">值</span><span class="sxs-lookup"><span data-stu-id="f940b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f940b-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f940b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f940b-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f940b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f940b-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f940b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f940b-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f940b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f940b-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f940b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f940b-134"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f940b-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f940b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f940b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f940b-136">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="f940b-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f940b-137">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="f940b-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
