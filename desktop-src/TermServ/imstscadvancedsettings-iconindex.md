---
title: IMsTscAdvancedSettings >iconindex 屬性
description: 指定目前圖示檔中的圖示索引。
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- '>iconindex 屬性遠端桌面服務'
- '>iconindex 屬性遠端桌面服務，IMsTscAdvancedSettings 介面'
- IMsTscAdvancedSettings 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面'
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面'
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面'
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面'
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面'
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面'
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面'
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面'
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，>iconindex 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be56eab5dbe7f03155c6082e4e70fc4bd439253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508556"
---
# <a name="imstscadvancedsettingsiconindex-property"></a><span data-ttu-id="2ec47-122">IMsTscAdvancedSettings：： >iconindex 屬性</span><span class="sxs-lookup"><span data-stu-id="2ec47-122">IMsTscAdvancedSettings::IconIndex property</span></span>

<span data-ttu-id="2ec47-123">指定目前圖示檔中的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="2ec47-123">Specifies the index of the icon within the current icon file.</span></span>

> [!Note]  
> <span data-ttu-id="2ec47-124">ActiveX 控制項 (MsRdp) 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2ec47-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="2ec47-125">標準用戶端 (MsTsc.exe) 中包含的 MsTscAx.dll 程式庫都支援此功能。</span><span class="sxs-lookup"><span data-stu-id="2ec47-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="2ec47-126">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="2ec47-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ec47-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ec47-127">Syntax</span></span>


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a><span data-ttu-id="2ec47-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="2ec47-128">Property value</span></span>

<span data-ttu-id="2ec47-129">圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="2ec47-129">The index of the icon.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ec47-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2ec47-130">Error codes</span></span>

<span data-ttu-id="2ec47-131">傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2ec47-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ec47-132">備註</span><span class="sxs-lookup"><span data-stu-id="2ec47-132">Remarks</span></span>

<span data-ttu-id="2ec47-133">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="2ec47-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ec47-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ec47-134">Requirements</span></span>



| <span data-ttu-id="2ec47-135">需求</span><span class="sxs-lookup"><span data-stu-id="2ec47-135">Requirement</span></span> | <span data-ttu-id="2ec47-136">值</span><span class="sxs-lookup"><span data-stu-id="2ec47-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec47-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ec47-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2ec47-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ec47-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="2ec47-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ec47-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2ec47-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ec47-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2ec47-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2ec47-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ec47-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ec47-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="2ec47-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2ec47-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ec47-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ec47-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="2ec47-145">IID</span><span class="sxs-lookup"><span data-stu-id="2ec47-145">IID</span></span><br/>                      | <span data-ttu-id="2ec47-146">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="2ec47-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ec47-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ec47-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ec47-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="2ec47-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2ec47-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2ec47-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2ec47-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2ec47-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="2ec47-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2ec47-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2ec47-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2ec47-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2ec47-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2ec47-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2ec47-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2ec47-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2ec47-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2ec47-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2ec47-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="2ec47-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





