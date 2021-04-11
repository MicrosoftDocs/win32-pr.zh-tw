---
title: IMsRdpClientNonScriptable3 介面
description: 提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 IMsRdpClientNonScriptable2 介面。
ms.assetid: 40cfcd8e-5dd7-497d-8c57-da1f542136b8
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable3 介面遠端桌面服務
- IMsRdpClientNonScriptable3 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c456393ee00c06bcd16135a7fbc73b0f1686259f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934581"
---
# <a name="imsrdpclientnonscriptable3-interface"></a><span data-ttu-id="a639a-106">IMsRdpClientNonScriptable3 介面</span><span class="sxs-lookup"><span data-stu-id="a639a-106">IMsRdpClientNonScriptable3 interface</span></span>

<span data-ttu-id="a639a-107">提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。</span><span class="sxs-lookup"><span data-stu-id="a639a-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="a639a-108">衍生自 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="a639a-108">Derives from the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface.</span></span> <span data-ttu-id="a639a-109">這個介面的方法只能透過 vtable 存取;它們無法用於可編寫腳本的用戶端。</span><span class="sxs-lookup"><span data-stu-id="a639a-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

## <a name="members"></a><span data-ttu-id="a639a-110">成員</span><span class="sxs-lookup"><span data-stu-id="a639a-110">Members</span></span>

<span data-ttu-id="a639a-111">**IMsRdpClientNonScriptable3** 介面繼承自 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)。</span><span class="sxs-lookup"><span data-stu-id="a639a-111">The **IMsRdpClientNonScriptable3** interface inherits from [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md).</span></span> <span data-ttu-id="a639a-112">**IMsRdpClientNonScriptable3** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a639a-112">**IMsRdpClientNonScriptable3** also has these types of members:</span></span>

-   [<span data-ttu-id="a639a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a639a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a639a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a639a-114">Properties</span></span>

<span data-ttu-id="a639a-115">**IMsRdpClientNonScriptable3** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a639a-115">The **IMsRdpClientNonScriptable3** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a639a-116">屬性</span><span class="sxs-lookup"><span data-stu-id="a639a-116">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a639a-117">存取類型</span><span class="sxs-lookup"><span data-stu-id="a639a-117">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a639a-118">Description</span><span class="sxs-lookup"><span data-stu-id="a639a-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a639a-119"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-119"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-120">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-121">要為連接列顯示的文字字串。</span><span class="sxs-lookup"><span data-stu-id="a639a-121">The text string to display for the connection bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a639a-122"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-122"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="a639a-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-124">可用於重新導向的 PnP 裝置集合。</span><span class="sxs-lookup"><span data-stu-id="a639a-124">The collection of PnP devices that are available for redirection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a639a-125"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-125"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="a639a-126">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-127">可用於重新導向的磁片磁碟機集合。</span><span class="sxs-lookup"><span data-stu-id="a639a-127">The collection of disk drives that is available for redirection.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a639a-128"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-128"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-130">指定是否啟用此連接的 CredSSP。</span><span class="sxs-lookup"><span data-stu-id="a639a-130">Specifies whether CredSSP is enabled for this connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a639a-131"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-131"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-133">指定此連接是否支援 NegotiateSecurityLayer 設定。</span><span class="sxs-lookup"><span data-stu-id="a639a-133">Specifies whether the NegotiateSecurityLayer setting is supported for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a639a-134">當 <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> 已啟用並存在於用戶端上，或當安全通訊端層 (SSL) 啟用使用者驗證時，會忽略 NegotiateSecurityLayer。</span><span class="sxs-lookup"><span data-stu-id="a639a-134">When <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> is enabled and present on the client, or when Secure Sockets Layer (SSL) is enabled with user authentication, NegotiateSecurityLayer is ignored.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a639a-135"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-135"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-136">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-137">指定是否應顯示 [提示輸入認證] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a639a-137">Specifies whether the prompt for credentials dialog box should be shown.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a639a-138"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-138"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-139">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-140">指定是否可重新導向會話中所列舉的動態連接 PnP 裝置。</span><span class="sxs-lookup"><span data-stu-id="a639a-140">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a639a-141"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-141"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-142">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-143">指定在會話中列舉的動態連接 PnP 磁片磁碟機是否可用於重新導向。</span><span class="sxs-lookup"><span data-stu-id="a639a-143">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a639a-144"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-144"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-145">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-145">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-146">指定在啟動會話之前，是否應該顯示重新導向安全性警告對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a639a-146">Specifies whether the redirection security warning dialog box should be shown before starting a session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a639a-147"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-147"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-148">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-148">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-149">指定在啟動會話之前，安全性警告對話方塊是否應包含關於剪貼簿重新導向的警告。</span><span class="sxs-lookup"><span data-stu-id="a639a-149">Specifies whether the security warning dialog box should include a warning about clipboard redirection before starting a session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a639a-150"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a></span><span class="sxs-lookup"><span data-stu-id="a639a-150"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a639a-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="a639a-152">指定在啟動會話之前，安全性警告是否應包含有關將認證傳送至遠端伺服器的警告。</span><span class="sxs-lookup"><span data-stu-id="a639a-152">Specifies whether the security warning should include a warning about sending credentials to the remote server before starting a session.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a639a-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="a639a-153">Requirements</span></span>



| <span data-ttu-id="a639a-154">需求</span><span class="sxs-lookup"><span data-stu-id="a639a-154">Requirement</span></span> | <span data-ttu-id="a639a-155">值</span><span class="sxs-lookup"><span data-stu-id="a639a-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a639a-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a639a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="a639a-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a639a-157">Windows Vista</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a639a-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a639a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="a639a-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a639a-159">Windows Server 2008</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a639a-160">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a639a-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="a639a-161"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a639a-161"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a639a-162">DLL</span><span class="sxs-lookup"><span data-stu-id="a639a-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a639a-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a639a-163"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a639a-164">CLSID</span><span class="sxs-lookup"><span data-stu-id="a639a-164">CLSID</span></span><br/>                    | <span data-ttu-id="a639a-165">CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span><span class="sxs-lookup"><span data-stu-id="a639a-165">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="a639a-166">CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D</span><span class="sxs-lookup"><span data-stu-id="a639a-166">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="a639a-167">CLSID \_ MsRdpClient5 定義為4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span><span class="sxs-lookup"><span data-stu-id="a639a-167">CLSID\_MsRdpClient5 is defined as 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span><br/> <span data-ttu-id="a639a-168">CLSID \_ MsRdpClient5NotSafeForScripting 定義為4EB2F086-C818-447E-B32C-C51CE2B30D31</span><span class="sxs-lookup"><span data-stu-id="a639a-168">CLSID\_MsRdpClient5NotSafeForScripting is defined as 4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span><br/> <span data-ttu-id="a639a-169">CLSID \_ MsRdpClient6 定義為7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span><span class="sxs-lookup"><span data-stu-id="a639a-169">CLSID\_MsRdpClient6 is defined as 7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span><br/> <span data-ttu-id="a639a-170">CLSID \_ MsRdpClient6NotSafeForScripting 定義為 D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="a639a-170">CLSID\_MsRdpClient6NotSafeForScripting is defined as D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span><br/> <span data-ttu-id="a639a-171">CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="a639a-171">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="a639a-172">CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="a639a-172">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="a639a-173">CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="a639a-173">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="a639a-174">CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="a639a-174">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="a639a-175">CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="a639a-175">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="a639a-176">CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="a639a-176">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="a639a-177">IID</span><span class="sxs-lookup"><span data-stu-id="a639a-177">IID</span></span><br/>                      | <span data-ttu-id="a639a-178">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="a639a-178">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



## <a name="see-also"></a><span data-ttu-id="a639a-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a639a-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a639a-180">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="a639a-180">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="a639a-181">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a639a-181">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="a639a-182">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a639a-182">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="a639a-183">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="a639a-183">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





