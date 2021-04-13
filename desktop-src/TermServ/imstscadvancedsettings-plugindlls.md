---
title: IMsTscAdvancedSettings PluginDlls 屬性
description: 指定要載入的虛擬通道用戶端 Dll 的名稱。
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- PluginDlls 屬性遠端桌面服務
- PluginDlls 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，PluginDlls 屬性
- PluginDlls 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，PluginDlls 屬性
- PluginDlls 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，PluginDlls 屬性
- PluginDlls 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，PluginDlls 屬性
- PluginDlls 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，PluginDlls 屬性
- PluginDlls 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，PluginDlls 屬性
- PluginDlls 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，PluginDlls 屬性
- PluginDlls 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，PluginDlls 屬性
- PluginDlls 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，PluginDlls 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.PluginDlls
- IMsTscAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings.PluginDlls
- IMsRdpClientAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings2.PluginDlls
- IMsRdpClientAdvancedSettings2.put_PluginDlls
- IMsRdpClientAdvancedSettings3.PluginDlls
- IMsRdpClientAdvancedSettings3.put_PluginDlls
- IMsRdpClientAdvancedSettings4.PluginDlls
- IMsRdpClientAdvancedSettings4.put_PluginDlls
- IMsRdpClientAdvancedSettings5.PluginDlls
- IMsRdpClientAdvancedSettings5.put_PluginDlls
- IMsRdpClientAdvancedSettings6.PluginDlls
- IMsRdpClientAdvancedSettings6.put_PluginDlls
- IMsRdpClientAdvancedSettings7.PluginDlls
- IMsRdpClientAdvancedSettings7.put_PluginDlls
- IMsRdpClientAdvancedSettings8.PluginDlls
- IMsRdpClientAdvancedSettings8.put_PluginDlls
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ef2e518145ae34533477bcbefb92e15d9c8d94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465325"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a><span data-ttu-id="e0d3d-122">IMsTscAdvancedSettings：:P luginDlls 屬性</span><span class="sxs-lookup"><span data-stu-id="e0d3d-122">IMsTscAdvancedSettings::PluginDlls property</span></span>

<span data-ttu-id="e0d3d-123">指定要載入的虛擬通道用戶端 Dll 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-123">Specifies the names of virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="e0d3d-124">虛擬通道用戶端 Dll 也稱為外掛程式 Dll。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-124">Virtual channel client DLLs are also referred to as Plug-in DLLs.</span></span>

<span data-ttu-id="e0d3d-125">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d3d-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0d3d-126">Syntax</span></span>


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a><span data-ttu-id="e0d3d-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="e0d3d-127">Property value</span></span>

<span data-ttu-id="e0d3d-128">要載入之虛擬通道用戶端 Dll 名稱的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-128">Comma-separated list of the names of the virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="e0d3d-129">DLL 名稱必須只包含英數位元。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-129">The DLL names must contain only alphanumeric characters.</span></span> <span data-ttu-id="e0d3d-130">如需這些名稱格式的詳細資訊，請參閱 [DVC 外掛程式註冊](dvc-plug-in-registration.md)。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-130">For more information about the format of these names, see [DVC plug-in registration](dvc-plug-in-registration.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0d3d-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e0d3d-131">Error codes</span></span>

<span data-ttu-id="e0d3d-132">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d3d-133">備註</span><span class="sxs-lookup"><span data-stu-id="e0d3d-133">Remarks</span></span>

<span data-ttu-id="e0d3d-134">基於安全性理由，如果控制項裝載在網頁中， **PluginDlls** 屬性只接受虛擬通道用戶端 dll 的命名清單。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-134">For security reasons, if the control is hosted in a webpage the **PluginDlls** property only accepts a named list of virtual channel client DLLs.</span></span> <span data-ttu-id="e0d3d-135">如果指定了檔案系統或 UNC 路徑，控制項就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-135">The control returns an error if a file system or UNC path is specified.</span></span>

<span data-ttu-id="e0d3d-136">將從網頁存取的虛擬通道用戶端 Dll 必須安裝在 "% WinDir% \\ system32" 目錄中，因為遠端桌面 ActiveX 控制項只會存取該位置中的 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-136">Virtual channel client DLLs that will be accessed from a webpage must be installed in the "%WinDir%\\system32" directory because the Remote Desktop ActiveX control only accesses DLL files in that location.</span></span> <span data-ttu-id="e0d3d-137">如果控制項未裝載在網頁中，此安全性限制並不存在，而且可以使用完整路徑來存取和載入位於檔案系統任何位置的虛擬通道用戶端 Dll。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-137">If the control is not hosted in a webpage, this security restriction does not exist and full paths may be used to access and load virtual channel client DLLs located anywhere on the file system.</span></span>

<span data-ttu-id="e0d3d-138">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="e0d3d-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d3d-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0d3d-139">Requirements</span></span>



| <span data-ttu-id="e0d3d-140">需求</span><span class="sxs-lookup"><span data-stu-id="e0d3d-140">Requirement</span></span> | <span data-ttu-id="e0d3d-141">值</span><span class="sxs-lookup"><span data-stu-id="e0d3d-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d3d-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0d3d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d3d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0d3d-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="e0d3d-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0d3d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d3d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0d3d-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e0d3d-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e0d3d-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0d3d-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0d3d-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e0d3d-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e0d3d-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0d3d-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0d3d-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e0d3d-150">IID</span><span class="sxs-lookup"><span data-stu-id="e0d3d-150">IID</span></span><br/>                      | <span data-ttu-id="e0d3d-151">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="e0d3d-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0d3d-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0d3d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d3d-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e0d3d-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e0d3d-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="e0d3d-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e0d3d-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e0d3d-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e0d3d-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e0d3d-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e0d3d-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e0d3d-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





