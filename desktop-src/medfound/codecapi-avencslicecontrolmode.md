---
description: 指定配量控制模式。 有效值為 0、1 和 2。
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: 'CODECAPI_AVEncSliceControlMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936563"
---
# <a name="codecapi_avencslicecontrolmode-property"></a><span data-ttu-id="25379-104">CODECAPI \_ AVEncSliceControlMode 屬性</span><span class="sxs-lookup"><span data-stu-id="25379-104">CODECAPI\_AVEncSliceControlMode property</span></span>

<span data-ttu-id="25379-105">指定配量控制模式。</span><span class="sxs-lookup"><span data-stu-id="25379-105">Specifies the slice control mode.</span></span> <span data-ttu-id="25379-106">有效值為 0、1 和 2。</span><span class="sxs-lookup"><span data-stu-id="25379-106">Valid values are 0, 1, and 2.</span></span>

## <a name="data-type"></a><span data-ttu-id="25379-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="25379-107">Data type</span></span>

<span data-ttu-id="25379-108">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="25379-108">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="25379-109">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="25379-109">Property GUID</span></span>

<span data-ttu-id="25379-110">**CODECAPI \_ AVEncSliceControlMode**</span><span class="sxs-lookup"><span data-stu-id="25379-110">**CODECAPI\_AVEncSliceControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="25379-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="25379-111">Property value</span></span>

<span data-ttu-id="25379-112">配量控制項模式值：</span><span class="sxs-lookup"><span data-stu-id="25379-112">Slice control mode values:</span></span>



| <span data-ttu-id="25379-113">值</span><span class="sxs-lookup"><span data-stu-id="25379-113">Value</span></span>                                                                        | <span data-ttu-id="25379-114">意義</span><span class="sxs-lookup"><span data-stu-id="25379-114">Meaning</span></span>                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25379-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="25379-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="25379-116">將此值設定為0，表示 [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) 屬性將會以每個配量的巨大區塊單位來指定配量大小。</span><span class="sxs-lookup"><span data-stu-id="25379-116">Setting this value to 0 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblocks per slice.</span></span><br/>     |
| <dl> <span data-ttu-id="25379-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="25379-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="25379-118">將此值設定為1，表示 [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) 屬性將會以每個配量的位數單位來指定配量大小。</span><span class="sxs-lookup"><span data-stu-id="25379-118">Setting this value to 1 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of bits per slice.</span></span><br/>            |
| <dl> <span data-ttu-id="25379-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="25379-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="25379-120">將此值設定為2表示 [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) 屬性將會以每個配量的巨大區塊資料列單位來指定配量大小。</span><span class="sxs-lookup"><span data-stu-id="25379-120">Setting this value to 2 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblock rows per slice.</span></span><br/> |



 

<span data-ttu-id="25379-121">編碼器會傳回它所支援的值。</span><span class="sxs-lookup"><span data-stu-id="25379-121">The encoder returns the values that it supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="25379-122">備註</span><span class="sxs-lookup"><span data-stu-id="25379-122">Remarks</span></span>

<span data-ttu-id="25379-123">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="25379-123">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="25379-124">建議編碼器支援 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)、 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)和 [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="25379-124">It is recommended that the encoder supports [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="25379-125">如果 [](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)未針對 CODECAPI AVEncSliceControlMode 呼叫 SetValue \_ ，則 CODECAPI AVEncSliceControlMode 的 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) \_ 可能會傳回 **VFW \_ E \_ CODECAPI \_ 沒有目前的 \_ \_ 值**。</span><span class="sxs-lookup"><span data-stu-id="25379-125">If [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) is not called for CODECAPI\_AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) for CODECAPI\_AVEncSliceControlMode can return **VFW\_E\_CODECAPI\_NO\_CURRENT\_VALUE**.</span></span> <span data-ttu-id="25379-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) 可能會傳回 **VFW \_ E CODECAPI NO CODECAPI AVEncSliceControlMode 的 \_ \_ \_ 預設值** \_ 。</span><span class="sxs-lookup"><span data-stu-id="25379-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) may return **VFW\_E\_CODECAPI\_NO\_DEFAULT** for CODECAPI\_AVEncSliceControlMode.</span></span>

<span data-ttu-id="25379-127">建議的預設值為 2 (每個配量) 的 MB 資料列大小。</span><span class="sxs-lookup"><span data-stu-id="25379-127">Recommended default value is 2 (size in MB row per slice).</span></span>

<span data-ttu-id="25379-128">這是靜態 API，這表示應用程式在編碼器執行時，會贏得變更。</span><span class="sxs-lookup"><span data-stu-id="25379-128">This is a static API, which means the application won t change this while the encoder is running.</span></span>

## <a name="examples"></a><span data-ttu-id="25379-129">範例</span><span class="sxs-lookup"><span data-stu-id="25379-129">Examples</span></span>


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a><span data-ttu-id="25379-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="25379-130">Requirements</span></span>



| <span data-ttu-id="25379-131">需求</span><span class="sxs-lookup"><span data-stu-id="25379-131">Requirement</span></span> | <span data-ttu-id="25379-132">值</span><span class="sxs-lookup"><span data-stu-id="25379-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25379-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25379-133">Minimum supported client</span></span><br/> | <span data-ttu-id="25379-134">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25379-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="25379-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25379-135">Minimum supported server</span></span><br/> | <span data-ttu-id="25379-136">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25379-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="25379-137">標頭</span><span class="sxs-lookup"><span data-stu-id="25379-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="25379-138"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="25379-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25379-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25379-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25379-140">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="25379-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

