---
title: IMsRdpClient2 ConnectedStatusText 屬性
description: 包含控制項處於連接狀態時，在控制項的工作區中顯示的文字。
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- ConnectedStatusText 屬性遠端桌面服務
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，ConnectedStatusText 屬性
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，ConnectedStatusText 屬性
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，ConnectedStatusText 屬性
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，ConnectedStatusText 屬性
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，ConnectedStatusText 屬性
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，ConnectedStatusText 屬性
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，ConnectedStatusText 屬性
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，ConnectedStatusText 屬性
- ConnectedStatusText 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，ConnectedStatusText 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106988034"
---
# <a name="imsrdpclient2connectedstatustext-property"></a><span data-ttu-id="87d6f-122">IMsRdpClient2：： ConnectedStatusText 屬性</span><span class="sxs-lookup"><span data-stu-id="87d6f-122">IMsRdpClient2::ConnectedStatusText property</span></span>

<span data-ttu-id="87d6f-123">包含控制項處於連接狀態時，在控制項的工作區中顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="87d6f-123">Contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

<span data-ttu-id="87d6f-124">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="87d6f-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d6f-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="87d6f-125">Syntax</span></span>


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a><span data-ttu-id="87d6f-126">屬性值</span><span class="sxs-lookup"><span data-stu-id="87d6f-126">Property value</span></span>

<span data-ttu-id="87d6f-127">**ConnectedStatusText** 屬性包含當控制項處於連接狀態時，在控制項的工作區中顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="87d6f-127">The **ConnectedStatusText** property contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

## <a name="error-codes"></a><span data-ttu-id="87d6f-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="87d6f-128">Error codes</span></span>

<span data-ttu-id="87d6f-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="87d6f-129">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d6f-130">備註</span><span class="sxs-lookup"><span data-stu-id="87d6f-130">Remarks</span></span>

<span data-ttu-id="87d6f-131">控制項處於連接狀態時，要在控制項的工作區中顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="87d6f-131">Text to display in the client area of the control while the control is in the connected state.</span></span> <span data-ttu-id="87d6f-132">這是可見的文字，例如，當使用者在網頁瀏覽器中將控制項切換至全螢幕模式時，會有一個在瀏覽器中裝載的控制項部分的情節。</span><span class="sxs-lookup"><span data-stu-id="87d6f-132">This is the text that is visible, for example, when the user switches the control to the full-screen mode in a web browser, a scenario that leaves a portion of the control hosted in the browser.</span></span>

<span data-ttu-id="87d6f-133">**Get \_ ConnectedStatusText** 方法會配置 *pConnectedStatusText* 參數所指向之緩衝區所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="87d6f-133">The **get\_ConnectedStatusText** method allocates the memory required for the buffer pointed to by the *pConnectedStatusText* parameter.</span></span> <span data-ttu-id="87d6f-134">呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="87d6f-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="87d6f-135">Visual Basic 和腳本用戶端都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="87d6f-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="87d6f-136">連接控制項時，無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="87d6f-136">This property cannot be set when the control is connected.</span></span> <span data-ttu-id="87d6f-137">您可以藉由呼叫 [**IMsTscAx：： get \_ connected**](imstscax-connected.md) 方法來檢查控制項是否已連接。</span><span class="sxs-lookup"><span data-stu-id="87d6f-137">You can check if the control is connected by calling the [**IMsTscAx::get\_Connected**](imstscax-connected.md) method.</span></span>

<span data-ttu-id="87d6f-138">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="87d6f-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87d6f-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="87d6f-139">Requirements</span></span>



| <span data-ttu-id="87d6f-140">需求</span><span class="sxs-lookup"><span data-stu-id="87d6f-140">Requirement</span></span> | <span data-ttu-id="87d6f-141">值</span><span class="sxs-lookup"><span data-stu-id="87d6f-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87d6f-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87d6f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="87d6f-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87d6f-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="87d6f-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87d6f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="87d6f-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87d6f-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="87d6f-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="87d6f-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="87d6f-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d6f-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="87d6f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="87d6f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87d6f-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d6f-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="87d6f-150">IID</span><span class="sxs-lookup"><span data-stu-id="87d6f-150">IID</span></span><br/>                      | <span data-ttu-id="87d6f-151">IID \_ IMsRdpClient2 定義為 e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="87d6f-151">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="87d6f-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87d6f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d6f-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="87d6f-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="87d6f-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="87d6f-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="87d6f-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="87d6f-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="87d6f-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="87d6f-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="87d6f-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="87d6f-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="87d6f-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="87d6f-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="87d6f-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="87d6f-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="87d6f-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="87d6f-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="87d6f-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="87d6f-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

