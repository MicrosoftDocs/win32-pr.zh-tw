---
title: EAP 驗證器方法登錄值
description: 瞭解 EAP 驗證器方法登錄值。 EAP 驗證器方法需要這些特定的登錄值。
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933625"
---
# <a name="eap-authenticator-method-registry-values"></a><span data-ttu-id="668e5-104">EAP 驗證器方法登錄值</span><span class="sxs-lookup"><span data-stu-id="668e5-104">EAP Authenticator Method Registry Values</span></span>

<span data-ttu-id="668e5-105">EAP 驗證器方法需要特定的登錄值。</span><span class="sxs-lookup"><span data-stu-id="668e5-105">Specific registry values are required for EAP authenticator methods.</span></span>

## <a name="eap-authenticator-method-dll-paths"></a><span data-ttu-id="668e5-106">EAP 驗證器方法 DLL 路徑</span><span class="sxs-lookup"><span data-stu-id="668e5-106">EAP Authenticator Method DLL Paths</span></span>

<span data-ttu-id="668e5-107">下列路徑指定一般 EAP 驗證器方法 Dll 的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="668e5-107">The following path specifies the registry location for regular EAP authenticator method DLLs.</span></span>

<span data-ttu-id="668e5-108">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ *&lt; 作者 &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="668e5-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="668e5-109">例如，EAP 驗證器方法安裝註冊路徑 **指定了 "** 311" (表示 "Microsoft" 是作者) ，而 **EapTypeId** "40"，如下所示。</span><span class="sxs-lookup"><span data-stu-id="668e5-109">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="668e5-110">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="668e5-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="668e5-111">下列路徑指定擴充 EAP 驗證器方法 Dll 的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="668e5-111">The following path specifies the registry location for extended EAP authenticator method DLLs.</span></span>

<span data-ttu-id="668e5-112">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ *&lt; 作者 &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ \* &lt; VendorType&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="668e5-112">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;VendorType&gt;**\*</span></span>

<span data-ttu-id="668e5-113">例如，EAP 驗證器方法安裝註冊路徑 **指定了 "** 311" (表示 "Microsoft" 是作者) 、"311" 的 **VendorId** 和 "40" 的 **EapTypeId** ，如下所示。</span><span class="sxs-lookup"><span data-stu-id="668e5-113">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="668e5-114">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="668e5-114">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="668e5-115">如需 EAP 方法類型配置的詳細資訊，請參閱 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)的6.2 節。</span><span class="sxs-lookup"><span data-stu-id="668e5-115">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="668e5-116">登錄值</span><span class="sxs-lookup"><span data-stu-id="668e5-116">Registry Values</span></span>

<span data-ttu-id="668e5-117">以下是必要的驗證器方法登錄值。</span><span class="sxs-lookup"><span data-stu-id="668e5-117">The following authenticator method registry values are required.</span></span>

-   [<span data-ttu-id="668e5-118">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="668e5-118">AuthenticatorDllPath</span></span>](#authenticatordllpath)
-   [<span data-ttu-id="668e5-119">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="668e5-119">AuthenticatorFriendlyName</span></span>](#authenticatorfriendlyname)

<span data-ttu-id="668e5-120">除了上述的登錄值，建議使用下列驗證器方法登錄值。</span><span class="sxs-lookup"><span data-stu-id="668e5-120">Besides the above registry values, the following authenticator method registry value is recommended.</span></span>

-   [<span data-ttu-id="668e5-121">屬性</span><span class="sxs-lookup"><span data-stu-id="668e5-121">Properties</span></span>](#properties)

<span data-ttu-id="668e5-122">其餘的驗證器方法登錄值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="668e5-122">The remaining authenticator method registry values are optional.</span></span>

-   [<span data-ttu-id="668e5-123">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="668e5-123">ConfigCLSID</span></span>](#configclsid)
-   [<span data-ttu-id="668e5-124">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="668e5-124">StandaloneSupported</span></span>](#standalonesupported)

## <a name="authenticatordllpath"></a><span data-ttu-id="668e5-125">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="668e5-125">AuthenticatorDllPath</span></span>



| <span data-ttu-id="668e5-126">常數值</span><span class="sxs-lookup"><span data-stu-id="668e5-126">Constant Value</span></span> | <span data-ttu-id="668e5-127">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="668e5-127">AuthenticatorDllPath</span></span>                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668e5-128">類型</span><span class="sxs-lookup"><span data-stu-id="668e5-128">Type</span></span>           | <span data-ttu-id="668e5-129">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="668e5-129">REG\_EXPAND\_SZ</span></span>                                                                                               |
| <span data-ttu-id="668e5-130">Description</span><span class="sxs-lookup"><span data-stu-id="668e5-130">Description</span></span>    | <span data-ttu-id="668e5-131">EAP 驗證器方法 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="668e5-131">The path to the EAP authenticator method DLL.</span></span> <span data-ttu-id="668e5-132">例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。</span><span class="sxs-lookup"><span data-stu-id="668e5-132">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

## <a name="authenticatorfriendlyname"></a><span data-ttu-id="668e5-133">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="668e5-133">AuthenticatorFriendlyName</span></span>



| <span data-ttu-id="668e5-134">常數值</span><span class="sxs-lookup"><span data-stu-id="668e5-134">Constant Value</span></span> | <span data-ttu-id="668e5-135">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="668e5-135">AuthenticatorFriendlyName</span></span>                                                          |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="668e5-136">類型</span><span class="sxs-lookup"><span data-stu-id="668e5-136">Type</span></span>           | <span data-ttu-id="668e5-137">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="668e5-137">REG\_SZ</span></span>                                                                            |
| <span data-ttu-id="668e5-138">Description</span><span class="sxs-lookup"><span data-stu-id="668e5-138">Description</span></span>    | <span data-ttu-id="668e5-139">包含易記 (顯示 EAP 驗證器方法) 名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="668e5-139">String that contains the friendly (display) name for the EAP authenticator method.</span></span> |



 

## <a name="configclsid"></a><span data-ttu-id="668e5-140">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="668e5-140">ConfigCLSID</span></span>



| <span data-ttu-id="668e5-141">常數值</span><span class="sxs-lookup"><span data-stu-id="668e5-141">Constant Value</span></span> | <span data-ttu-id="668e5-142">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="668e5-142">ConfigCLSID</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668e5-143">類型</span><span class="sxs-lookup"><span data-stu-id="668e5-143">Type</span></span>           | <span data-ttu-id="668e5-144">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="668e5-144">REG\_SZ</span></span>                                                                                                                               |
| <span data-ttu-id="668e5-145">Description</span><span class="sxs-lookup"><span data-stu-id="668e5-145">Description</span></span>    | <span data-ttu-id="668e5-146">字串，其中包含此驗證器方法的設定類別 GUID，格式為 {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="668e5-146">String that contains the configuration class GUID for this authenticator method, in the format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span></span> |



 

## <a name="properties"></a><span data-ttu-id="668e5-147">屬性</span><span class="sxs-lookup"><span data-stu-id="668e5-147">Properties</span></span>



| <span data-ttu-id="668e5-148">常數值</span><span class="sxs-lookup"><span data-stu-id="668e5-148">Constant Value</span></span> | <span data-ttu-id="668e5-149">屬性</span><span class="sxs-lookup"><span data-stu-id="668e5-149">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668e5-150">類型</span><span class="sxs-lookup"><span data-stu-id="668e5-150">Type</span></span>           | <span data-ttu-id="668e5-151">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="668e5-151">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="668e5-152">Description</span><span class="sxs-lookup"><span data-stu-id="668e5-152">Description</span></span>    | <span data-ttu-id="668e5-153">DWORD 中的位會設定為指出屬性的支援。</span><span class="sxs-lookup"><span data-stu-id="668e5-153">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="668e5-154">如需支援值的清單，請參閱 [**EAP 方法屬性**](eap-method-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="668e5-154">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="standalonesupported"></a><span data-ttu-id="668e5-155">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="668e5-155">StandaloneSupported</span></span>



| <span data-ttu-id="668e5-156">常數值</span><span class="sxs-lookup"><span data-stu-id="668e5-156">Constant Value</span></span> | <span data-ttu-id="668e5-157">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="668e5-157">StandaloneSupported</span></span>                                             |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="668e5-158">類型</span><span class="sxs-lookup"><span data-stu-id="668e5-158">Type</span></span>           | <span data-ttu-id="668e5-159">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="668e5-159">REG\_DWORD</span></span>                                                      |
| <span data-ttu-id="668e5-160">Description</span><span class="sxs-lookup"><span data-stu-id="668e5-160">Description</span></span>    | <span data-ttu-id="668e5-161">如果這是獨立的驗證器方法，則為 0;如果不是，則為1。</span><span class="sxs-lookup"><span data-stu-id="668e5-161">0 if this is a standalone authenticator method; 1 if it is not.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="668e5-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="668e5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="668e5-163">EAP 對等方法登錄機碼</span><span class="sxs-lookup"><span data-stu-id="668e5-163">EAP Peer Method Registry Keys</span></span>](eap-peer-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="668e5-164">擴充的 EAP 類型的登錄設定</span><span class="sxs-lookup"><span data-stu-id="668e5-164">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="668e5-165">使用 EAPHost</span><span class="sxs-lookup"><span data-stu-id="668e5-165">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="668e5-166">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="668e5-166">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




