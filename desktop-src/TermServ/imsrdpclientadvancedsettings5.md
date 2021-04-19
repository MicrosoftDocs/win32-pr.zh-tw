---
title: IMsRdpClientAdvancedSettings5 介面
description: 管理 advanced client 設定。 衍生自 IMsRdpClientAdvancedSettings4 介面。
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966502"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a><span data-ttu-id="a29d6-106">IMsRdpClientAdvancedSettings5 介面</span><span class="sxs-lookup"><span data-stu-id="a29d6-106">IMsRdpClientAdvancedSettings5 interface</span></span>

<span data-ttu-id="a29d6-107">管理 advanced client 設定。</span><span class="sxs-lookup"><span data-stu-id="a29d6-107">Manages advanced client settings.</span></span> <span data-ttu-id="a29d6-108">衍生自 [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="a29d6-108">Derives from the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="a29d6-109">若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="a29d6-109">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="a29d6-110">然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings5** 傳遞給 **QueryInterface**。</span><span class="sxs-lookup"><span data-stu-id="a29d6-110">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings5** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="a29d6-111">成員</span><span class="sxs-lookup"><span data-stu-id="a29d6-111">Members</span></span>

<span data-ttu-id="a29d6-112">**IMsRdpClientAdvancedSettings5** 介面繼承自 [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)。</span><span class="sxs-lookup"><span data-stu-id="a29d6-112">The **IMsRdpClientAdvancedSettings5** interface inherits from [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span></span> <span data-ttu-id="a29d6-113">**IMsRdpClientAdvancedSettings5** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a29d6-113">**IMsRdpClientAdvancedSettings5** also has these types of members:</span></span>

-   [<span data-ttu-id="a29d6-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a29d6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a29d6-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a29d6-115">Properties</span></span>

<span data-ttu-id="a29d6-116">**IMsRdpClientAdvancedSettings5** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a29d6-116">The **IMsRdpClientAdvancedSettings5** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a29d6-117">屬性</span><span class="sxs-lookup"><span data-stu-id="a29d6-117">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a29d6-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="a29d6-118">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a29d6-119">Description</span><span class="sxs-lookup"><span data-stu-id="a29d6-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a29d6-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29d6-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a29d6-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-122">音訊重新導向模式。</span><span class="sxs-lookup"><span data-stu-id="a29d6-122">The audio redirection mode.</span></span> <span data-ttu-id="a29d6-123"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a>屬性具有下列可能的值。</span><span class="sxs-lookup"><span data-stu-id="a29d6-123">The <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> property has the following possible values.</span></span><br/><span data-ttu-id="a29d6-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (已啟用音訊重新導向，而重新導向的選項會 &quot; 帶至此電腦 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="a29d6-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (Audio redirection is enabled and the option for redirection is &quot;Bring to this computer&quot;.</span></span> <span data-ttu-id="a29d6-125">這是預設模式。 ) </span><span class="sxs-lookup"><span data-stu-id="a29d6-125">This is the default mode.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="a29d6-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (已啟用音訊重新導向，且 [遠端電腦] 選項為 [ &quot; 離開] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="a29d6-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (Audio redirection is enabled and the option is &quot;Leave at remote computer&quot;.</span></span> <span data-ttu-id="a29d6-127">&quot; &quot; 只有在遠端連線到執行 Windows Vista 的主機電腦時，才支援 [離開遠端電腦] 選項。</span><span class="sxs-lookup"><span data-stu-id="a29d6-127">The &quot;Leave at remote computer&quot; option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="a29d6-128">如果連接到執行 Windows Server 2008 的主機電腦，則 [ &quot; 遠端電腦離開] 選項 &quot; 會變更為 [ &quot; 不播放] &quot; 。 ) </span><span class="sxs-lookup"><span data-stu-id="a29d6-128">If the connection is to a host computer that is running Windows Server 2008, the option &quot;Leave at remote computer&quot; is changed to &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="a29d6-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (已啟用音訊重新導向，且 &quot; 不播放模式 &quot; 。 ) </span><span class="sxs-lookup"><span data-stu-id="a29d6-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (Audio redirection is enabled and the mode is &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a29d6-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29d6-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a29d6-131">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-132">指定每圖元32位的虛擬快取檔案大小 (bpp) 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="a29d6-132">Specifies the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span> <span data-ttu-id="a29d6-133">最大值為 48 mb (MB) 。</span><span class="sxs-lookup"><span data-stu-id="a29d6-133">The maximum value is 48 megabytes (MB).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a29d6-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29d6-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a29d6-135">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-136">指定是否應該在連接列上顯示 [釘選] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a29d6-136">Specifies whether the pin button should be shown on the connection bar.</span></span> <span data-ttu-id="a29d6-137">依預設，此值為 <strong>TRUE</strong>。</span><span class="sxs-lookup"><span data-stu-id="a29d6-137">By default, the value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a29d6-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29d6-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-139">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a29d6-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-140">指定是否應啟用或停用公用模式。</span><span class="sxs-lookup"><span data-stu-id="a29d6-140">Specifies whether public mode should be enabled or disabled.</span></span> <span data-ttu-id="a29d6-141">Public 模式預設會設定為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="a29d6-141">By default, public mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a29d6-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29d6-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-143">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a29d6-143">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-144">指定是否應啟用或停用剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="a29d6-144">Specifies whether clipboard redirection should be enabled or disabled.</span></span> <span data-ttu-id="a29d6-145">根據預設，剪貼簿重新導向模式會設定為 <strong>TRUE</strong> (已啟用) 。</span><span class="sxs-lookup"><span data-stu-id="a29d6-145">By default, clipboard redirection mode is set to <strong>TRUE</strong> (enabled).</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a29d6-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29d6-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-147">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a29d6-147">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-148">指定是否應啟用或停用重新導向的裝置。</span><span class="sxs-lookup"><span data-stu-id="a29d6-148">Specifies whether redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="a29d6-149">根據預設，重新導向的裝置模式會設定為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="a29d6-149">By default, redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a29d6-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="a29d6-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a29d6-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a29d6-152">指定是否應啟用或停用服務重新導向裝置的點。</span><span class="sxs-lookup"><span data-stu-id="a29d6-152">Specifies whether Point of Service redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="a29d6-153">依預設，[服務重新導向裝置的時間點] 模式會設定為 [ <strong>FALSE</strong>]。</span><span class="sxs-lookup"><span data-stu-id="a29d6-153">By default, Point of Service redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a29d6-154">備註</span><span class="sxs-lookup"><span data-stu-id="a29d6-154">Remarks</span></span>

<span data-ttu-id="a29d6-155">此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：</span><span class="sxs-lookup"><span data-stu-id="a29d6-155">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="a29d6-156">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a29d6-156">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="a29d6-157">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a29d6-157">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="a29d6-158">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a29d6-158">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a><span data-ttu-id="a29d6-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="a29d6-159">Requirements</span></span>



| <span data-ttu-id="a29d6-160">需求</span><span class="sxs-lookup"><span data-stu-id="a29d6-160">Requirement</span></span> | <span data-ttu-id="a29d6-161">值</span><span class="sxs-lookup"><span data-stu-id="a29d6-161">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a29d6-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a29d6-162">Minimum supported client</span></span><br/> | <span data-ttu-id="a29d6-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a29d6-163">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a29d6-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a29d6-164">Minimum supported server</span></span><br/> | <span data-ttu-id="a29d6-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a29d6-165">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a29d6-166">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a29d6-166">Type library</span></span><br/>             | <dl> <span data-ttu-id="a29d6-167"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a29d6-167"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a29d6-168">DLL</span><span class="sxs-lookup"><span data-stu-id="a29d6-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a29d6-169"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a29d6-169"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a29d6-170">IID</span><span class="sxs-lookup"><span data-stu-id="a29d6-170">IID</span></span><br/>                      | <span data-ttu-id="a29d6-171">IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="a29d6-171">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a29d6-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a29d6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a29d6-173">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a29d6-173">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a29d6-174">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a29d6-174">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="a29d6-175">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a29d6-175">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a29d6-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a29d6-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a29d6-177">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a29d6-177">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a29d6-178">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="a29d6-178">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

