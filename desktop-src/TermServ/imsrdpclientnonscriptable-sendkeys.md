---
title: IMsRdpClientNonScriptable SendKeys 方法
description: 將一連串的按鍵傳送到控制項。 按鍵是掃描程式碼形式，也就是實際實體索引鍵的鍵盤資料。
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- SendKeys 方法遠端桌面服務
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，SendKeys 方法
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，SendKeys 方法
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，SendKeys 方法
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，SendKeys 方法
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，SendKeys 方法
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466008"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a><span data-ttu-id="4d2e8-115">IMsRdpClientNonScriptable：： SendKeys 方法</span><span class="sxs-lookup"><span data-stu-id="4d2e8-115">IMsRdpClientNonScriptable::SendKeys method</span></span>

<span data-ttu-id="4d2e8-116">將一連串的按鍵傳送到控制項。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-116">Sends a series of keystrokes to the control.</span></span> <span data-ttu-id="4d2e8-117">按鍵是掃描程式碼形式，也就是實際實體索引鍵的鍵盤資料。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-117">The keystrokes are in scan code form, which is the keyboard data from the actual physical keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d2e8-118">語法</span><span class="sxs-lookup"><span data-stu-id="4d2e8-118">Syntax</span></span>


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="4d2e8-119">參數</span><span class="sxs-lookup"><span data-stu-id="4d2e8-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d2e8-120">*numKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d2e8-120">*numKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2e8-121">要傳送的按鍵數目。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-121">The number of keystrokes to send.</span></span> <span data-ttu-id="4d2e8-122">可以在一個作業中傳送的最大索引鍵數目是20。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-122">The maximum number of keys that can be sent in one operation is 20.</span></span> <span data-ttu-id="4d2e8-123">如果此參數大於20，則方法會傳回 **E \_ INVALIDARG** 。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-123">The method returns **E\_INVALIDARG** if this parameter is greater than 20.</span></span> <span data-ttu-id="4d2e8-124">如需詳細資訊，請參閱接下來的＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-124">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="4d2e8-125">*pbArrayKeyUp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d2e8-125">*pbArrayKeyUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2e8-126">大小等於 *numKeys* 的陣列。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-126">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="4d2e8-127">如果對應的索引鍵為 UP，元素就是 **TRUE** ，如果對應的索引鍵已關閉，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-127">An element is **TRUE** if the corresponding key is UP and **FALSE** if the corresponding key is DOWN.</span></span>

</dd> <dt>

<span data-ttu-id="4d2e8-128">*plKeyData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d2e8-128">*plKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2e8-129">大小等於 *numKeys* 的陣列。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-129">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="4d2e8-130">陣列包含擊鍵資料，並且對應至 [WM \_ KEYDOWN](../inputdev/wm-keydown.md)訊息的 *lParam* 參數值。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-130">The array contains keystroke data and corresponds to the value of the *lParam* parameter of the [WM\_KEYDOWN](../inputdev/wm-keydown.md) message.</span></span> <span data-ttu-id="4d2e8-131">資料會指定重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的索引鍵狀態旗標，以及轉換狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-131">The data specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span> <span data-ttu-id="4d2e8-132">如需此陣列中位的描述，請參閱 [WM \_ KEYDOWN](../inputdev/wm-keydown.md)。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-132">For a description of the bits in this array, see [WM\_KEYDOWN](../inputdev/wm-keydown.md).</span></span>

<span data-ttu-id="4d2e8-133">*PbArrayKeyUp* 中的對應元素會指出金鑰是否為向上或向下。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-133">The corresponding element in *pbArrayKeyUp* indicates if the key is UP or DOWN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d2e8-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d2e8-134">Return value</span></span>

<span data-ttu-id="4d2e8-135">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-135">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d2e8-136">備註</span><span class="sxs-lookup"><span data-stu-id="4d2e8-136">Remarks</span></span>

<span data-ttu-id="4d2e8-137">**SendKeys** 方法不會混合由本機使用者進行的按鍵，以及方法所傳送的按鍵。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-137">The **SendKeys** method does not mix keystrokes made by the local user with keystrokes that the method is sending.</span></span> <span data-ttu-id="4d2e8-138">傳遞至方法的所有按鍵都會以單一不可部分完成的順序傳送至遠端會話。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-138">All keystrokes passed to the method are sent to the remote session in a single atomic sequence.</span></span>

<span data-ttu-id="4d2e8-139">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="4d2e8-139">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d2e8-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d2e8-140">Requirements</span></span>



| <span data-ttu-id="4d2e8-141">需求</span><span class="sxs-lookup"><span data-stu-id="4d2e8-141">Requirement</span></span> | <span data-ttu-id="4d2e8-142">值</span><span class="sxs-lookup"><span data-stu-id="4d2e8-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2e8-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d2e8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4d2e8-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d2e8-144">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="4d2e8-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d2e8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4d2e8-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d2e8-146">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="4d2e8-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4d2e8-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d2e8-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d2e8-148"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="4d2e8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4d2e8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d2e8-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d2e8-150"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="4d2e8-151">IID</span><span class="sxs-lookup"><span data-stu-id="4d2e8-151">IID</span></span><br/>                      | <span data-ttu-id="4d2e8-152">IID \_ IMsRdpClientNonScriptable 定義為2f079c4c-87b2-4afd-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="4d2e8-152">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d2e8-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d2e8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2e8-154">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="4d2e8-154">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="4d2e8-155">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="4d2e8-155">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="4d2e8-156">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="4d2e8-156">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="4d2e8-157">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="4d2e8-157">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="4d2e8-158">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="4d2e8-158">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="4d2e8-159">WM \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="4d2e8-159">WM\_KEYDOWN</span></span>](../inputdev/wm-keydown.md)
</dt> </dl>

 

