---
title: IMsTscAx StartConnected 屬性
description: 指出控制項是否會在啟動時立即建立遠端桌面工作階段主機 (RD 工作階段主機) server 連接。
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- StartConnected 屬性遠端桌面服務
- StartConnected 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，StartConnected 屬性
- StartConnected 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，StartConnected 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965699"
---
# <a name="imstscaxstartconnected-property"></a><span data-ttu-id="845b7-124">IMsTscAx：： StartConnected 屬性</span><span class="sxs-lookup"><span data-stu-id="845b7-124">IMsTscAx::StartConnected property</span></span>

<span data-ttu-id="845b7-125">指出控制項是否會在啟動時立即建立遠端桌面工作階段主機 (RD 工作階段主機) server 連接。</span><span class="sxs-lookup"><span data-stu-id="845b7-125">Indicates whether the control will establish the Remote Desktop Session Host (RD Session Host) server connection immediately upon startup.</span></span>

<span data-ttu-id="845b7-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="845b7-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="845b7-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="845b7-127">Syntax</span></span>


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a><span data-ttu-id="845b7-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="845b7-128">Property value</span></span>

<span data-ttu-id="845b7-129">如果控制項應該在啟動時立即連接，則將此參數設定為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="845b7-129">Set this parameter to **TRUE** if the control should connect immediately on startup, or **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="845b7-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="845b7-130">Error codes</span></span>

<span data-ttu-id="845b7-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="845b7-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="845b7-132">備註</span><span class="sxs-lookup"><span data-stu-id="845b7-132">Remarks</span></span>

<span data-ttu-id="845b7-133">當控制項屬性是在標記的參數清單中設定 <OBJECT> ，而不是透過腳本呼叫時，這個屬性最有用。</span><span class="sxs-lookup"><span data-stu-id="845b7-133">This property is most useful when the control properties are set in the parameter list of an <OBJECT> tag, rather than through script calls.</span></span>

<span data-ttu-id="845b7-134">只有當伺服器名稱也使用 server 屬性指定時，才能使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="845b7-134">This property can be used only if the server name is also specified using the server property.</span></span> <span data-ttu-id="845b7-135">此參數必須在控制項啟動之前設定，例如，在使用網頁的控制項時，將它包含在標記的參數清單中 <OBJECT> 。</span><span class="sxs-lookup"><span data-stu-id="845b7-135">This parameter has to be set before the control starts up for example, by including it in the parameter list of an <OBJECT> tag when using the control from a webpage.</span></span>

<span data-ttu-id="845b7-136">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="845b7-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="845b7-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="845b7-137">Requirements</span></span>



| <span data-ttu-id="845b7-138">需求</span><span class="sxs-lookup"><span data-stu-id="845b7-138">Requirement</span></span> | <span data-ttu-id="845b7-139">值</span><span class="sxs-lookup"><span data-stu-id="845b7-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="845b7-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="845b7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="845b7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="845b7-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="845b7-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="845b7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="845b7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="845b7-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="845b7-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="845b7-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="845b7-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="845b7-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="845b7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="845b7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="845b7-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="845b7-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="845b7-148">IID</span><span class="sxs-lookup"><span data-stu-id="845b7-148">IID</span></span><br/>                      | <span data-ttu-id="845b7-149">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="845b7-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="845b7-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="845b7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="845b7-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="845b7-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="845b7-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="845b7-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="845b7-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="845b7-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="845b7-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="845b7-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="845b7-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="845b7-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="845b7-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="845b7-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="845b7-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="845b7-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="845b7-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="845b7-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="845b7-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="845b7-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="845b7-160">在網頁中內嵌遠端桌面 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="845b7-160">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[<span data-ttu-id="845b7-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="845b7-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





