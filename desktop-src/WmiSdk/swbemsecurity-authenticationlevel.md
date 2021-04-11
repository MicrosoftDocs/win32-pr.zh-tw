---
description: AuthenticationLevel 屬性是一個整數，可定義指派給此物件的 COM 驗證層級。
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: SWbemSecurity. AuthenticationLevel 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318860"
---
# <a name="swbemsecurityauthenticationlevel-property"></a><span data-ttu-id="3103d-103">SWbemSecurity. AuthenticationLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="3103d-103">SWbemSecurity.AuthenticationLevel property</span></span>

<span data-ttu-id="3103d-104">**AuthenticationLevel** 屬性是一個整數，可定義指派給此物件的 COM 驗證層級。</span><span class="sxs-lookup"><span data-stu-id="3103d-104">The **AuthenticationLevel** property is an integer that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="3103d-105">此設定會決定您如何保護從 WMI 傳送的資訊。</span><span class="sxs-lookup"><span data-stu-id="3103d-105">This setting determines how you protect information sent from WMI.</span></span> <span data-ttu-id="3103d-106">如需驗證層級的詳細資訊，請參閱 [設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)。</span><span class="sxs-lookup"><span data-stu-id="3103d-106">For more information about authentication levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="3103d-107">一般情況下，不需要在進行 WMI API 呼叫時設定驗證層級。</span><span class="sxs-lookup"><span data-stu-id="3103d-107">In general, it is not necessary to set the authentication level when making WMI API calls.</span></span> <span data-ttu-id="3103d-108">如果您未設定此屬性，則會使用系統的預設 COM 驗證層級。</span><span class="sxs-lookup"><span data-stu-id="3103d-108">If you do not set this property, the default COM Authentication level for your system is used.</span></span>

<span data-ttu-id="3103d-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="3103d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3103d-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3103d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3103d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3103d-111">Syntax</span></span>


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="3103d-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="3103d-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3103d-113">備註</span><span class="sxs-lookup"><span data-stu-id="3103d-113">Remarks</span></span>

<span data-ttu-id="3103d-114">AuthenticationLevel 設定可讓您要求在整個連接中使用的 DCOM 驗證和隱私權層級。</span><span class="sxs-lookup"><span data-stu-id="3103d-114">The authenticationLevel setting enables you to request the level of DCOM authentication and privacy to be used throughout a connection.</span></span> <span data-ttu-id="3103d-115">設定的範圍從無驗證到每個封包加密驗證。</span><span class="sxs-lookup"><span data-stu-id="3103d-115">Settings range from no authentication to per-packet encrypted authentication.</span></span>



| <span data-ttu-id="3103d-116">值</span><span class="sxs-lookup"><span data-stu-id="3103d-116">Value</span></span>        | <span data-ttu-id="3103d-117">描述</span><span class="sxs-lookup"><span data-stu-id="3103d-117">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3103d-118">無</span><span class="sxs-lookup"><span data-stu-id="3103d-118">None</span></span>         | <span data-ttu-id="3103d-119">不使用任何驗證。</span><span class="sxs-lookup"><span data-stu-id="3103d-119">Does not use any authentication.</span></span> <span data-ttu-id="3103d-120">系統會忽略所有安全性設定。</span><span class="sxs-lookup"><span data-stu-id="3103d-120">All security settings are ignored.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="3103d-121">預設</span><span class="sxs-lookup"><span data-stu-id="3103d-121">Default</span></span>      | <span data-ttu-id="3103d-122">使用標準安全性協調來選取驗證等級。</span><span class="sxs-lookup"><span data-stu-id="3103d-122">Uses a standard security negotiation to select an authentication level.</span></span> <span data-ttu-id="3103d-123">這是建議的設定，因為牽涉到交易的用戶端將會與伺服器所指定的驗證層級進行協商。</span><span class="sxs-lookup"><span data-stu-id="3103d-123">This is the recommended setting because the client involved in the transaction will be negotiated to the authentication level specified by the server.</span></span><br/> <span data-ttu-id="3103d-124">DCOM 不會在協商會話期間選取 [無] 值。</span><span class="sxs-lookup"><span data-stu-id="3103d-124">DCOM will not select the value None during a negotiation session.</span></span><br/> |
| <span data-ttu-id="3103d-125">連線</span><span class="sxs-lookup"><span data-stu-id="3103d-125">Connect</span></span>      | <span data-ttu-id="3103d-126">只有當用戶端嘗試連接到伺服器時，才會驗證用戶端的認證。</span><span class="sxs-lookup"><span data-stu-id="3103d-126">Authenticates the credentials of the client only when the client tries to connect to the server.</span></span> <span data-ttu-id="3103d-127">建立連線之後，不會進行其他驗證檢查。</span><span class="sxs-lookup"><span data-stu-id="3103d-127">After a connection has been made, no additional authentication checks take place.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="3103d-128">呼叫</span><span class="sxs-lookup"><span data-stu-id="3103d-128">Call</span></span>         | <span data-ttu-id="3103d-129">當伺服器收到要求時，只會在每次呼叫的開頭驗證用戶端的認證。</span><span class="sxs-lookup"><span data-stu-id="3103d-129">Authenticates the credentials of the client only at the beginning of each call, when the server receives the request.</span></span> <span data-ttu-id="3103d-130">封包標頭已簽署，但在用戶端與伺服器之間交換的資料封包不會進行簽署或加密。</span><span class="sxs-lookup"><span data-stu-id="3103d-130">The packet headers are signed, but the data packets exchanged between the client and the server are neither signed nor encrypted.</span></span><br/>                                                     |
| <span data-ttu-id="3103d-131">Pkt</span><span class="sxs-lookup"><span data-stu-id="3103d-131">Pkt</span></span>          | <span data-ttu-id="3103d-132">驗證從預期的用戶端接收所有資料封包。</span><span class="sxs-lookup"><span data-stu-id="3103d-132">Authenticates that all data packets are received from the expected client.</span></span> <span data-ttu-id="3103d-133">類似于呼叫;封包標頭已簽署但未加密。</span><span class="sxs-lookup"><span data-stu-id="3103d-133">Similar to Call; packet headers are signed but not encrypted.</span></span> <span data-ttu-id="3103d-134">封包本身不會進行簽署或加密。</span><span class="sxs-lookup"><span data-stu-id="3103d-134">Packets themselves are neither signed nor encrypted.</span></span><br/>                                                                                                               |
| <span data-ttu-id="3103d-135">PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="3103d-135">PktIntegrity</span></span> | <span data-ttu-id="3103d-136">驗證並確認在用戶端與伺服器之間傳輸的資料封包都已修改。</span><span class="sxs-lookup"><span data-stu-id="3103d-136">Authenticates and verifies that none of the data packets transferred between the client and the server have been modified.</span></span> <span data-ttu-id="3103d-137">每個資料封包都會經過簽署，以確保在傳輸期間未修改封包。</span><span class="sxs-lookup"><span data-stu-id="3103d-137">Every data packet is signed, ensuring that the packets have not been modified during transit.</span></span> <span data-ttu-id="3103d-138">未加密任何資料封包。</span><span class="sxs-lookup"><span data-stu-id="3103d-138">None of the data packets are encrypted.</span></span><br/>                                            |
| <span data-ttu-id="3103d-139">PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="3103d-139">PktPrivacy</span></span>   | <span data-ttu-id="3103d-140">驗證所有先前的模擬等級，並簽署並加密每個資料封包。</span><span class="sxs-lookup"><span data-stu-id="3103d-140">Authenticates all previous impersonation levels and signs and encrypts each data packet.</span></span> <span data-ttu-id="3103d-141">這可確保用戶端與伺服器之間的所有通訊都是機密的。</span><span class="sxs-lookup"><span data-stu-id="3103d-141">This ensures that all communication between the client and the server is confidential.</span></span><br/>                                                                                                                             |



 

<span data-ttu-id="3103d-142">您可以設定 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObjectPath**](swbemobjectpath.md)和 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件的驗證層級，方法是將 **AuthenticationLevel** 屬性設定為所需的值。</span><span class="sxs-lookup"><span data-stu-id="3103d-142">You can set the authentication level of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by setting the **AuthenticationLevel** property to the desired value.</span></span>

<span data-ttu-id="3103d-143">下列範例顯示如何設定 **SwbemObject** 物件的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="3103d-143">The following example shows how to set the authentication level for an **SwbemObject** object.</span></span>


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



<span data-ttu-id="3103d-144">您也可以指定驗證層級做為標記的一部分。</span><span class="sxs-lookup"><span data-stu-id="3103d-144">You can also specify authentication levels as part of a moniker.</span></span> <span data-ttu-id="3103d-145">下列範例會設定驗證層級和模擬等級，並抓取 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的實例。</span><span class="sxs-lookup"><span data-stu-id="3103d-145">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a><span data-ttu-id="3103d-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="3103d-146">Requirements</span></span>



| <span data-ttu-id="3103d-147">需求</span><span class="sxs-lookup"><span data-stu-id="3103d-147">Requirement</span></span> | <span data-ttu-id="3103d-148">值</span><span class="sxs-lookup"><span data-stu-id="3103d-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3103d-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3103d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3103d-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3103d-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3103d-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3103d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3103d-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3103d-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3103d-153">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3103d-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="3103d-154"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3103d-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3103d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3103d-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3103d-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3103d-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3103d-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="3103d-157">CLSID</span></span><br/>                    | <span data-ttu-id="3103d-158">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="3103d-158">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="3103d-159">IID</span><span class="sxs-lookup"><span data-stu-id="3103d-159">IID</span></span><br/>                      | <span data-ttu-id="3103d-160">IID \_ ISWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="3103d-160">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3103d-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3103d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3103d-162">設定用戶端 \_ 應用程式 \_ 處理安全性</span><span class="sxs-lookup"><span data-stu-id="3103d-162">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="3103d-163">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="3103d-163">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="3103d-164">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="3103d-164">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> </dl>

 

