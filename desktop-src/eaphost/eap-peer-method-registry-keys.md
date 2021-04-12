---
title: EAP 對等方法登錄值
description: 瞭解 EAP 對等方法所需的特定登錄值。 查看登錄值的清單，並查看其他可用的資源。
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316492"
---
# <a name="eap-peer-method-registry-values"></a><span data-ttu-id="399fe-104">EAP 對等方法登錄值</span><span class="sxs-lookup"><span data-stu-id="399fe-104">EAP Peer Method Registry Values</span></span>

<span data-ttu-id="399fe-105">EAP 對等方法需要特定的登錄值。</span><span class="sxs-lookup"><span data-stu-id="399fe-105">Specific registry values are required for EAP peer methods.</span></span>

## <a name="eap-peer-method-dll-paths"></a><span data-ttu-id="399fe-106">EAP 對等方法 DLL 路徑</span><span class="sxs-lookup"><span data-stu-id="399fe-106">EAP Peer Method DLL Paths</span></span>

<span data-ttu-id="399fe-107">下列路徑指定一般 EAP 對等方法 Dll 的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="399fe-107">The following path specifies the registry location for regular EAP peer method DLLs.</span></span>

<span data-ttu-id="399fe-108">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ *&lt; 作者 &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="399fe-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="399fe-109">例如，假設 "311" 的 **作者為 "** " 的 EAP 方法安裝註冊路徑 (表示 "Microsoft" 是作者) ，而 **EapTypeId** "40"，則會顯示如下。</span><span class="sxs-lookup"><span data-stu-id="399fe-109">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="399fe-110">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="399fe-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="399fe-111">下列路徑指定擴充的 EAP 方法 Dll 的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="399fe-111">The following path specifies the registry location for extended EAP method DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="399fe-112">Windows Vista Service Pack 1 (SP1) 或更新版本支援擴充的 EAP 方法 Dll。</span><span class="sxs-lookup"><span data-stu-id="399fe-112">Extended EAP method DLLs are supported in Windows Vista with Service Pack 1 (SP1) or later.</span></span>

 

<span data-ttu-id="399fe-113">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ *&lt; 作者 &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="399fe-113">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="399fe-114">例如，假設 "311" 的 **作者為 "** " 的 EAP 方法安裝註冊路徑 (表示 "Microsoft" 是作者) 、"311" 的 **VendorId** 和 "40" 的 **EapTypeId** ，如下所示。</span><span class="sxs-lookup"><span data-stu-id="399fe-114">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="399fe-115">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="399fe-115">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="399fe-116">如需 EAP 方法類型配置的詳細資訊，請參閱 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)的6.2 節。</span><span class="sxs-lookup"><span data-stu-id="399fe-116">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="399fe-117">登錄值</span><span class="sxs-lookup"><span data-stu-id="399fe-117">Registry Values</span></span>

<span data-ttu-id="399fe-118">需要下列 EAPHost 對等方法登錄值。</span><span class="sxs-lookup"><span data-stu-id="399fe-118">The following EAPHost peer method registry values are required.</span></span>

-   [<span data-ttu-id="399fe-119">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="399fe-119">PeerDllPath</span></span>](#peerdllpath)
-   [<span data-ttu-id="399fe-120">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="399fe-120">PeerFriendlyName</span></span>](#peerfriendlyname)
-   [<span data-ttu-id="399fe-121">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="399fe-121">PeerInvokePasswordDialog</span></span>](#peerinvokepassworddialog)
-   [<span data-ttu-id="399fe-122">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="399fe-122">PeerInvokeUsernameDialog</span></span>](#peerinvokeusernamedialog)

<span data-ttu-id="399fe-123">建議使用下列 AP 對等方法登錄值。</span><span class="sxs-lookup"><span data-stu-id="399fe-123">The following AP peer method registry values are recommended.</span></span>

-   [<span data-ttu-id="399fe-124">屬性</span><span class="sxs-lookup"><span data-stu-id="399fe-124">Properties</span></span>](#properties)

<span data-ttu-id="399fe-125">下列 AP 對等方法登錄值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="399fe-125">The following AP peer method registry values are optional.</span></span>

-   [<span data-ttu-id="399fe-126">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="399fe-126">PeerConfigUIPath</span></span>](#peerconfiguipath)
-   [<span data-ttu-id="399fe-127">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="399fe-127">PeerIdentityPath</span></span>](#peeridentitypath)
-   [<span data-ttu-id="399fe-128">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="399fe-128">PeerInteractiveUIPath</span></span>](#peerinteractiveuipath)
-   [<span data-ttu-id="399fe-129">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="399fe-129">PeerRequireConfigUI</span></span>](#peerrequireconfigui)

### <a name="peerconfiguipath"></a><span data-ttu-id="399fe-130">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="399fe-130">PeerConfigUIPath</span></span>



| <span data-ttu-id="399fe-131">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-131">Constant Value</span></span> | <span data-ttu-id="399fe-132">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="399fe-132">PeerConfigUIPath</span></span>                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399fe-133">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-133">Type</span></span>           | <span data-ttu-id="399fe-134">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="399fe-134">REG\_EXPAND\_SZ</span></span>                                                                                                                                        |
| <span data-ttu-id="399fe-135">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-135">Description</span></span>    | <span data-ttu-id="399fe-136">包含 [使用者設定] 對話方塊之 [執行] 的 DLL 路徑。</span><span class="sxs-lookup"><span data-stu-id="399fe-136">The path to the DLL that contains the implementation of the user configuration dialog.</span></span> <span data-ttu-id="399fe-137">例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。</span><span class="sxs-lookup"><span data-stu-id="399fe-137">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerdllpath"></a><span data-ttu-id="399fe-138">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="399fe-138">PeerDllPath</span></span>



| <span data-ttu-id="399fe-139">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-139">Constant Value</span></span> | <span data-ttu-id="399fe-140">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="399fe-140">PeerDllPath</span></span>                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399fe-141">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-141">Type</span></span>           | <span data-ttu-id="399fe-142">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="399fe-142">REG\_EXPAND\_SZ</span></span>                                                                                 |
| <span data-ttu-id="399fe-143">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-143">Description</span></span>    | <span data-ttu-id="399fe-144">EAP 方法 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="399fe-144">The path to the EAP method DLL.</span></span> <span data-ttu-id="399fe-145">例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。</span><span class="sxs-lookup"><span data-stu-id="399fe-145">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerfriendlyname"></a><span data-ttu-id="399fe-146">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="399fe-146">PeerFriendlyName</span></span>



| <span data-ttu-id="399fe-147">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-147">Constant Value</span></span> | <span data-ttu-id="399fe-148">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="399fe-148">PeerFriendlyName</span></span>                                                     |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="399fe-149">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-149">Type</span></span>           | <span data-ttu-id="399fe-150">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="399fe-150">REG\_SZ</span></span>                                                              |
| <span data-ttu-id="399fe-151">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-151">Description</span></span>    | <span data-ttu-id="399fe-152">包含易記 (顯示 EAP 方法) 名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="399fe-152">String that contains the friendly (display) name for the EAP method.</span></span> |



 

### <a name="peeridentitypath"></a><span data-ttu-id="399fe-153">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="399fe-153">PeerIdentityPath</span></span>



| <span data-ttu-id="399fe-154">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-154">Constant Value</span></span> | <span data-ttu-id="399fe-155">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="399fe-155">PeerIdentityPath</span></span>                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399fe-156">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-156">Type</span></span>           | <span data-ttu-id="399fe-157">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="399fe-157">REG\_EXPAND\_SZ</span></span>                                                                                                                                      |
| <span data-ttu-id="399fe-158">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-158">Description</span></span>    | <span data-ttu-id="399fe-159">DLL 的路徑，其中包含使用者識別函式的執行。</span><span class="sxs-lookup"><span data-stu-id="399fe-159">The path to the DLL that contains the implementation of the user identity functions.</span></span> <span data-ttu-id="399fe-160">例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。</span><span class="sxs-lookup"><span data-stu-id="399fe-160">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinteractiveuipath"></a><span data-ttu-id="399fe-161">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="399fe-161">PeerInteractiveUIPath</span></span>



| <span data-ttu-id="399fe-162">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-162">Constant Value</span></span> | <span data-ttu-id="399fe-163">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="399fe-163">PeerInteractiveUIPath</span></span>                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399fe-164">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-164">Type</span></span>           | <span data-ttu-id="399fe-165">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="399fe-165">REG\_EXPAND\_SZ</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="399fe-166">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-166">Description</span></span>    | <span data-ttu-id="399fe-167">DLL 的路徑，其中包含在執行 EAP 方法期間用來取得使用者資訊的互動式使用者介面。</span><span class="sxs-lookup"><span data-stu-id="399fe-167">The path to the DLL that contains the implementation of the interactive user interface used to obtain user information during execution of the EAP method.</span></span> <span data-ttu-id="399fe-168">例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。</span><span class="sxs-lookup"><span data-stu-id="399fe-168">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinvokepassworddialog"></a><span data-ttu-id="399fe-169">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="399fe-169">PeerInvokePasswordDialog</span></span>



| <span data-ttu-id="399fe-170">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-170">Constant Value</span></span> | <span data-ttu-id="399fe-171">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="399fe-171">PeerInvokePasswordDialog</span></span>                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399fe-172">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-172">Type</span></span>           | <span data-ttu-id="399fe-173">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="399fe-173">REG\_DWORD</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="399fe-174">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-174">Description</span></span>    | <span data-ttu-id="399fe-175">1-使用一般 EAPHost 密碼和網域對話方塊取得認證。</span><span class="sxs-lookup"><span data-stu-id="399fe-175">1- to get credentials using the generic EAPHost password and domain dialog box.</span></span> <span data-ttu-id="399fe-176">0-使用自訂對話方塊。</span><span class="sxs-lookup"><span data-stu-id="399fe-176">0 - to use a custom dialog box.</span></span> <span data-ttu-id="399fe-177">如果使用一般對話方塊，則會由 [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) 方法設定認證。</span><span class="sxs-lookup"><span data-stu-id="399fe-177">If the generic dialog box is used, credentials are set by the [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span> |



 

### <a name="peerinvokeusernamedialog"></a><span data-ttu-id="399fe-178">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="399fe-178">PeerInvokeUsernameDialog</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="399fe-179">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-179">Constant Value</span></span></th>
<th><span data-ttu-id="399fe-180">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="399fe-180">PeerInvokeUsernameDialog</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="399fe-181">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-181">Type</span></span></td>
<td><span data-ttu-id="399fe-182">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="399fe-182">REG_DWORD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="399fe-183">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-183">Description</span></span></td>
<td><ul>
<li><span data-ttu-id="399fe-184">1-使用 [一般 EAPHost 使用者名稱] 對話方塊來取得認證。</span><span class="sxs-lookup"><span data-stu-id="399fe-184">1 - to get credentials using the generic EAPHost user name dialog box.</span></span></li>
<li><span data-ttu-id="399fe-185">0-使用自訂對話方塊。</span><span class="sxs-lookup"><span data-stu-id="399fe-185">0- to use a custom dialog box.</span></span></li>
</ul>
<span data-ttu-id="399fe-186">如果使用 [一般] 對話方塊，則認證會由 [<strong>EapPeerSetCredentials</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials]) 方法設定。</span><span class="sxs-lookup"><span data-stu-id="399fe-186">If the generic dialog box is used, credentials are set by the [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a><span data-ttu-id="399fe-187">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="399fe-187">PeerRequireConfigUI</span></span>



| <span data-ttu-id="399fe-188">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-188">Constant Value</span></span> | <span data-ttu-id="399fe-189">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="399fe-189">PeerRequireConfigUI</span></span>                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="399fe-190">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-190">Type</span></span>           | <span data-ttu-id="399fe-191">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="399fe-191">REG\_DWORD</span></span>                                                                                 |
| <span data-ttu-id="399fe-192">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-192">Description</span></span>    | <span data-ttu-id="399fe-193">如果此方法的設定使用者介面對話方塊已執行，則為0。如果不是，則為1。</span><span class="sxs-lookup"><span data-stu-id="399fe-193">0 if a configuration user interface dialog is implemented for this method; 1 if it is not.</span></span> |



 

### <a name="properties"></a><span data-ttu-id="399fe-194">屬性</span><span class="sxs-lookup"><span data-stu-id="399fe-194">Properties</span></span>



| <span data-ttu-id="399fe-195">常數值</span><span class="sxs-lookup"><span data-stu-id="399fe-195">Constant Value</span></span> | <span data-ttu-id="399fe-196">屬性</span><span class="sxs-lookup"><span data-stu-id="399fe-196">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399fe-197">類型</span><span class="sxs-lookup"><span data-stu-id="399fe-197">Type</span></span>           | <span data-ttu-id="399fe-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="399fe-198">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="399fe-199">Description</span><span class="sxs-lookup"><span data-stu-id="399fe-199">Description</span></span>    | <span data-ttu-id="399fe-200">DWORD 中的位會設定為指出屬性的支援。</span><span class="sxs-lookup"><span data-stu-id="399fe-200">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="399fe-201">如需支援值的清單，請參閱 [**EAP 方法屬性**](eap-method-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="399fe-201">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="399fe-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="399fe-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="399fe-203">EAP 驗證器方法登錄機碼</span><span class="sxs-lookup"><span data-stu-id="399fe-203">EAP Authenticator Method Registry Keys</span></span>](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="399fe-204">擴充的 EAP 類型的登錄設定</span><span class="sxs-lookup"><span data-stu-id="399fe-204">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="399fe-205">使用 EAPHost</span><span class="sxs-lookup"><span data-stu-id="399fe-205">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="399fe-206">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="399fe-206">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 