---
title: IMsTscAdvancedSettings 介面
description: 包含取得和設定屬性的方法，這些屬性可啟用點陣圖快取、壓縮和印表機和剪貼簿重新導向。
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- IMsTscAdvancedSettings 介面遠端桌面服務
- IMsTscAdvancedSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968162"
---
# <a name="imstscadvancedsettings-interface"></a><span data-ttu-id="a8982-105">IMsTscAdvancedSettings 介面</span><span class="sxs-lookup"><span data-stu-id="a8982-105">IMsTscAdvancedSettings interface</span></span>

<span data-ttu-id="a8982-106">包含取得和設定屬性的方法，這些屬性可啟用點陣圖快取、壓縮和印表機和剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="a8982-106">Includes methods to retrieve and set properties that enable bitmap caching, compression, and printer and clipboard redirection.</span></span> <span data-ttu-id="a8982-107">您也可以指定虛擬通道用戶端 Dll 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8982-107">You can also specify names of virtual channel client DLLs.</span></span>

<span data-ttu-id="a8982-108">您可以使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得這個介面的實例。</span><span class="sxs-lookup"><span data-stu-id="a8982-108">You obtain an instance of this interface by using the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="a8982-109">成員</span><span class="sxs-lookup"><span data-stu-id="a8982-109">Members</span></span>

<span data-ttu-id="a8982-110">**IMsTscAdvancedSettings** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="a8982-110">The **IMsTscAdvancedSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a8982-111">**IMsTscAdvancedSettings** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a8982-111">**IMsTscAdvancedSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="a8982-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a8982-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8982-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a8982-113">Properties</span></span>

<span data-ttu-id="a8982-114">**IMsTscAdvancedSettings** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a8982-114">The **IMsTscAdvancedSettings** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a8982-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a8982-115">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a8982-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="a8982-116">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a8982-117">Description</span><span class="sxs-lookup"><span data-stu-id="a8982-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a8982-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8982-119">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-120">指定是否啟用背景輸入模式。</span><span class="sxs-lookup"><span data-stu-id="a8982-120">Specifies whether background input mode is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a8982-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8982-122">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-123">指定是否啟用點陣圖快取。</span><span class="sxs-lookup"><span data-stu-id="a8982-123">Specifies whether bitmap caching is enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a8982-124">屬性名稱中的拼寫錯誤是在控制項的發行版本中。</span><span class="sxs-lookup"><span data-stu-id="a8982-124">The spelling error in the name of the property is in the released version of the control.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a8982-125"><a href="imstscadvancedsettings-compress.md"><strong>壓縮</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-125"><a href="imstscadvancedsettings-compress.md"><strong>Compress</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8982-126">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-127">指定是否啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="a8982-127">Specifies whether compression is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a8982-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8982-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-130">指定是否啟用容器處理的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="a8982-130">Specifies whether the container-handled full-screen mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a8982-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8982-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-133">指定是否啟用印表機和剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="a8982-133">Specifies whether printer and clipboard redirection is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a8982-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-135">唯寫</span><span class="sxs-lookup"><span data-stu-id="a8982-135">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-136">指定檔案的名稱，這個檔案包含在全螢幕模式中顯示用戶端時，將會存取的圖示資料。</span><span class="sxs-lookup"><span data-stu-id="a8982-136">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a8982-137"><a href="imstscadvancedsettings-iconindex.md"><strong>>iconindex</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-138">唯寫</span><span class="sxs-lookup"><span data-stu-id="a8982-138">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-139">指定目前圖示檔中的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="a8982-139">Specifies the index of the icon within the current icon file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a8982-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-141">唯寫</span><span class="sxs-lookup"><span data-stu-id="a8982-141">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-142">指定使用中輸入地區設定識別碼的名稱 (先前稱為用於連接的鍵盤配置) 。</span><span class="sxs-lookup"><span data-stu-id="a8982-142">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a8982-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8982-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-144">唯寫</span><span class="sxs-lookup"><span data-stu-id="a8982-144">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a8982-145">指定要載入的虛擬通道用戶端 Dll 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8982-145">Specifies the names of virtual channel client DLLs to be loaded.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a8982-146">備註</span><span class="sxs-lookup"><span data-stu-id="a8982-146">Remarks</span></span>

<span data-ttu-id="a8982-147">此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：</span><span class="sxs-lookup"><span data-stu-id="a8982-147">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="a8982-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a8982-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
-   [<span data-ttu-id="a8982-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a8982-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
-   [<span data-ttu-id="a8982-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a8982-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
-   [<span data-ttu-id="a8982-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a8982-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="a8982-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a8982-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="a8982-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a8982-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="a8982-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a8982-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="a8982-155">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="a8982-155">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8982-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8982-156">Requirements</span></span>



| <span data-ttu-id="a8982-157">需求</span><span class="sxs-lookup"><span data-stu-id="a8982-157">Requirement</span></span> | <span data-ttu-id="a8982-158">值</span><span class="sxs-lookup"><span data-stu-id="a8982-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8982-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8982-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a8982-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8982-160">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="a8982-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8982-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a8982-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8982-162">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a8982-163">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a8982-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8982-164"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8982-164"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="a8982-165">DLL</span><span class="sxs-lookup"><span data-stu-id="a8982-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8982-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8982-166"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="a8982-167">IID</span><span class="sxs-lookup"><span data-stu-id="a8982-167">IID</span></span><br/>                      | <span data-ttu-id="a8982-168">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="a8982-168">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8982-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8982-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8982-170">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a8982-170">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="a8982-171">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="a8982-171">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

