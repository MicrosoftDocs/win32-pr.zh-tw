---
title: IMsTscAdvancedSettings IconFile 屬性
description: 指定檔案的名稱，這個檔案包含在全螢幕模式中顯示用戶端時，將會存取的圖示資料。
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- IconFile 屬性遠端桌面服務
- IconFile 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，IconFile 屬性
- IconFile 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，IconFile 屬性
- IconFile 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，IconFile 屬性
- IconFile 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，IconFile 屬性
- IconFile 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，IconFile 屬性
- IconFile 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，IconFile 屬性
- IconFile 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，IconFile 屬性
- IconFile 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，IconFile 屬性
- IconFile 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，IconFile 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f996e70873d5584bb80bbf4f40f71a7deae8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685909"
---
# <a name="imstscadvancedsettingsiconfile-property"></a><span data-ttu-id="7a840-122">IMsTscAdvancedSettings：： IconFile 屬性</span><span class="sxs-lookup"><span data-stu-id="7a840-122">IMsTscAdvancedSettings::IconFile property</span></span>

<span data-ttu-id="7a840-123">指定檔案的名稱，這個檔案包含在全螢幕模式中顯示用戶端時，將會存取的圖示資料。</span><span class="sxs-lookup"><span data-stu-id="7a840-123">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="7a840-124">ActiveX 控制項 (MsRdp) 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="7a840-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="7a840-125">標準用戶端 (MsTsc.exe) 中包含的 MsTscAx.dll 程式庫都支援此功能。</span><span class="sxs-lookup"><span data-stu-id="7a840-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="7a840-126">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="7a840-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a840-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a840-127">Syntax</span></span>


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a><span data-ttu-id="7a840-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="7a840-128">Property value</span></span>

<span data-ttu-id="7a840-129">圖示檔案的完整路徑，或包含圖示資料的檔案，例如 DLL。</span><span class="sxs-lookup"><span data-stu-id="7a840-129">The fully qualified path of icon file or a file containing icon data, such as a DLL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7a840-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7a840-130">Error codes</span></span>

<span data-ttu-id="7a840-131">傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7a840-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a840-132">備註</span><span class="sxs-lookup"><span data-stu-id="7a840-132">Remarks</span></span>

<span data-ttu-id="7a840-133">圖示檔的副檔名為 ".ico"。</span><span class="sxs-lookup"><span data-stu-id="7a840-133">The file name extension of an icon file is ".ico".</span></span>

<span data-ttu-id="7a840-134">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="7a840-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a840-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a840-135">Requirements</span></span>



| <span data-ttu-id="7a840-136">需求</span><span class="sxs-lookup"><span data-stu-id="7a840-136">Requirement</span></span> | <span data-ttu-id="7a840-137">值</span><span class="sxs-lookup"><span data-stu-id="7a840-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a840-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a840-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7a840-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a840-139">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="7a840-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a840-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7a840-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a840-141">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7a840-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7a840-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a840-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a840-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7a840-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7a840-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a840-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a840-145"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7a840-146">IID</span><span class="sxs-lookup"><span data-stu-id="7a840-146">IID</span></span><br/>                      | <span data-ttu-id="7a840-147">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="7a840-147">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a840-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a840-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a840-149">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7a840-149">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7a840-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7a840-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7a840-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7a840-151">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="7a840-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7a840-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7a840-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7a840-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7a840-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7a840-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7a840-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7a840-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7a840-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7a840-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7a840-157">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7a840-157">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





