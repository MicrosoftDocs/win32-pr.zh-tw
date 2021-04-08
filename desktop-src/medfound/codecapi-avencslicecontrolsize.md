---
description: 以 mb 為單位指定配量的大小 (MB) 、位或 MB 的資料列。
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: 'CODECAPI_AVEncSliceControlSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111861"
---
# <a name="codecapi_avencslicecontrolsize-property"></a><span data-ttu-id="f0319-103">CODECAPI \_ AVEncSliceControlSize 屬性</span><span class="sxs-lookup"><span data-stu-id="f0319-103">CODECAPI\_AVEncSliceControlSize property</span></span>

<span data-ttu-id="f0319-104">以 mb 為單位指定配量的大小 (MB) 、位或 MB 的資料列。</span><span class="sxs-lookup"><span data-stu-id="f0319-104">Specifies the size of the slice in units of megabyte (MB), bits, or MB row.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0319-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f0319-105">Data type</span></span>

<span data-ttu-id="f0319-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="f0319-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f0319-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="f0319-107">Property GUID</span></span>

<span data-ttu-id="f0319-108">**CODECAPI \_ AVEncSliceControlSize**</span><span class="sxs-lookup"><span data-stu-id="f0319-108">**CODECAPI\_AVEncSliceControlSize**</span></span>

## <a name="remarks"></a><span data-ttu-id="f0319-109">備註</span><span class="sxs-lookup"><span data-stu-id="f0319-109">Remarks</span></span>

<span data-ttu-id="f0319-110">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="f0319-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="f0319-111">CODECAPI AVEncSliceControlSize 值的意義 \_ 是由 [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="f0319-111">The meaning of the value of CODECAPI\_AVEncSliceControlSize is controlled by the [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) property.</span></span> <span data-ttu-id="f0319-112">下表說明 CODECAPI \_ AVEncSliceControlSize 和 CODECAPI \_ AVEncSliceControlMode 屬性如何控制框架中的磁區大小和數目。</span><span class="sxs-lookup"><span data-stu-id="f0319-112">The following table illustrates how the CODECAPI\_AVEncSliceControlSize and CODECAPI\_AVEncSliceControlMode properties control the size and number of slices in a frame.</span></span>



| <span data-ttu-id="f0319-113">CODECAPI \_ AVEncSliceControlMode 設定</span><span class="sxs-lookup"><span data-stu-id="f0319-113">CODECAPI\_AVEncSliceControlMode setting</span></span> | <span data-ttu-id="f0319-114">值的意義</span><span class="sxs-lookup"><span data-stu-id="f0319-114">Meaning of value</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0319-115">0</span><span class="sxs-lookup"><span data-stu-id="f0319-115">0</span></span>                                       | <span data-ttu-id="f0319-116">這是一個整數，指出框架中每個配量的大小（以巨大區塊為單位）。</span><span class="sxs-lookup"><span data-stu-id="f0319-116">This is an integer that indicates the size of each slice in the frame in units of macroblocks.</span></span> <br/> <span data-ttu-id="f0319-117">當值大於框架中的巨大區塊數目時，編碼器應該拒絕設定。</span><span class="sxs-lookup"><span data-stu-id="f0319-117">The encoder should reject the setting when the value is greater than the number of macroblocks in the frame.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="f0319-118">1</span><span class="sxs-lookup"><span data-stu-id="f0319-118">1</span></span>                                       | <span data-ttu-id="f0319-119">這是一個整數，指出框架中每個磁區的大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="f0319-119">This is an integer that indicates the size of each slice in the frame in units of bits.</span></span> <br/> <span data-ttu-id="f0319-120">編碼器應該會在巨大區塊上啟動新的配量，此配量會導致配量中的位數超過此值 (因此，每個配量的大小一律會小於或等於此值) 。</span><span class="sxs-lookup"><span data-stu-id="f0319-120">The encoder should start a new slice at the macroblock that causes the number of bits in the slice to exceed this value (so the size of each slice will always be less than or equal than this value).</span></span> <span data-ttu-id="f0319-121">這表示最後一個配量大小可能明顯小於此值。</span><span class="sxs-lookup"><span data-stu-id="f0319-121">This means that the last slice size could be significantly smaller than this value.</span></span> <br/> |
| <span data-ttu-id="f0319-122">2</span><span class="sxs-lookup"><span data-stu-id="f0319-122">2</span></span>                                       | <span data-ttu-id="f0319-123">這是一個整數，以巨大區塊資料列的單位表示框架中每個配量的大小。</span><span class="sxs-lookup"><span data-stu-id="f0319-123">This is an integer that indicates the size of each slice in the frame in units of macroblock rows.</span></span> <br/> <span data-ttu-id="f0319-124">當值大於框架中的巨大區塊資料列數目時，編碼器應該拒絕設定。</span><span class="sxs-lookup"><span data-stu-id="f0319-124">The encoder should reject the setting when the value is greater than the number of macroblock rows in the frame.</span></span><br/>                                                                                                                                                                 |



 

<span data-ttu-id="f0319-125">如果應用程式未設定 [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)的值，則編碼器應該會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f0319-125">If the application does not set a value for [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), the encoder should return an error.</span></span>

<span data-ttu-id="f0319-126">建議的預設值是針對整個框架具有單一配量。</span><span class="sxs-lookup"><span data-stu-id="f0319-126">The recommended default is to have a single slice for whole frame.</span></span>

<span data-ttu-id="f0319-127">某些編碼器可能會以平行方式編碼配量，因此效能可能會受到影響，取決於配量控制項設定。</span><span class="sxs-lookup"><span data-stu-id="f0319-127">Some encoders might encode slices in parallel and so performance could be affected depending on the slice control settings.</span></span> <span data-ttu-id="f0319-128">例如，將框架編碼成單一配量可能會比框架編碼為多個配量更慢。</span><span class="sxs-lookup"><span data-stu-id="f0319-128">For example, encoding a frame as a single slice might be slower than if the frame was encoded as multiple slices.</span></span>

<span data-ttu-id="f0319-129">配量控制項設定為動態，而且可以在編碼會話期間變更。</span><span class="sxs-lookup"><span data-stu-id="f0319-129">The slice control settings are dynamic and can be changed during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0319-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0319-130">Requirements</span></span>



| <span data-ttu-id="f0319-131">需求</span><span class="sxs-lookup"><span data-stu-id="f0319-131">Requirement</span></span> | <span data-ttu-id="f0319-132">值</span><span class="sxs-lookup"><span data-stu-id="f0319-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0319-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0319-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f0319-134">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0319-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="f0319-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0319-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f0319-136">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0319-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f0319-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f0319-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0319-138"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0319-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0319-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0319-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0319-140">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="f0319-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




