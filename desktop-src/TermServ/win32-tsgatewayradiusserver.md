---
title: Win32_TSGatewayRADIUSServer 類別
description: 描述遠端驗證撥入消費者服務 (RADIUS) 伺服器，其具有一組遠端桌面服務連線授權原則 (RD \ 160;CAPs) 。
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer 類別遠端桌面服務
- Win32_TSGatewayRADIUSServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465088"
---
# <a name="win32_tsgatewayradiusserver-class"></a><span data-ttu-id="a1663-105">Win32 \_ TSGatewayRADIUSServer 類別</span><span class="sxs-lookup"><span data-stu-id="a1663-105">Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="a1663-106">描述遠端驗證撥入消費者服務 (RADIUS) 伺服器，其具有一組遠端桌面服務連線授權原則 (RD Cap) 。</span><span class="sxs-lookup"><span data-stu-id="a1663-106">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

<span data-ttu-id="a1663-107">RADIUS 是一種業界標準的通訊協定，可用來在伺服器電腦與驗證服務器（稱為 RADIUS 伺服器）之間傳輸驗證、授權和設定資訊，以及儲存使用者資訊的資料庫。</span><span class="sxs-lookup"><span data-stu-id="a1663-107">RADIUS is an industry-standard protocol that is used to transmit authentication, authorization, and configuration information between a server computer and an authenticating server, called a RADIUS server, with a database that stores user information.</span></span> <span data-ttu-id="a1663-108">如需詳細資訊，請參閱 [RADIUS 通訊協定](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="a1663-108">For more information, see [RADIUS Protocol](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1663-109">語法</span><span class="sxs-lookup"><span data-stu-id="a1663-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a><span data-ttu-id="a1663-110">成員</span><span class="sxs-lookup"><span data-stu-id="a1663-110">Members</span></span>

<span data-ttu-id="a1663-111">**Win32 \_ TSGatewayRADIUSServer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a1663-111">The **Win32\_TSGatewayRADIUSServer** class has these types of members:</span></span>

-   [<span data-ttu-id="a1663-112">方法</span><span class="sxs-lookup"><span data-stu-id="a1663-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a1663-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a1663-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a1663-114">方法</span><span class="sxs-lookup"><span data-stu-id="a1663-114">Methods</span></span>

<span data-ttu-id="a1663-115">**Win32 \_ TSGatewayRADIUSServer** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a1663-115">The **Win32\_TSGatewayRADIUSServer** class has these methods.</span></span>



| <span data-ttu-id="a1663-116">方法</span><span class="sxs-lookup"><span data-stu-id="a1663-116">Method</span></span>                                                                 | <span data-ttu-id="a1663-117">描述</span><span class="sxs-lookup"><span data-stu-id="a1663-117">Description</span></span>                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="a1663-118">**添加**</span><span class="sxs-lookup"><span data-stu-id="a1663-118">**Add**</span></span>](win32-tsgatewayradiusserver-add.md)                         | <span data-ttu-id="a1663-119">新增 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a1663-119">Adds a new RADIUS server.</span></span><br/>                                         |
| [<span data-ttu-id="a1663-120">**MoveDown**</span><span class="sxs-lookup"><span data-stu-id="a1663-120">**MoveDown**</span></span>](movedown-win32-tsgatewayradiusserver.md)               | <span data-ttu-id="a1663-121">以優先權順序將此 RADIUS 伺服器向下移動一個位置。</span><span class="sxs-lookup"><span data-stu-id="a1663-121">Moves this RADIUS server one position down in the priority order.</span></span><br/> |
| [<span data-ttu-id="a1663-122">**上移**</span><span class="sxs-lookup"><span data-stu-id="a1663-122">**MoveUp**</span></span>](moveup-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="a1663-123">以優先權順序將此 RADIUS 伺服器往上移動一個位置。</span><span class="sxs-lookup"><span data-stu-id="a1663-123">Moves this RADIUS server one position up in the priority order.</span></span><br/>   |
| [<span data-ttu-id="a1663-124">**移除**</span><span class="sxs-lookup"><span data-stu-id="a1663-124">**Remove**</span></span>](win32-tsgatewayradiusserver-remove.md)                   | <span data-ttu-id="a1663-125">移除目前的 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a1663-125">Removes the current RADIUS server.</span></span><br/>                                |
| [<span data-ttu-id="a1663-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="a1663-126">**SetName**</span></span>](setname-win32-tsgatewayradiusserver.md)                 | <span data-ttu-id="a1663-127">設定此 RADIUS 伺服器的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a1663-127">Sets the **Name** property for this RADIUS server.</span></span><br/>                |
| [<span data-ttu-id="a1663-128">**SetSharedSecret**</span><span class="sxs-lookup"><span data-stu-id="a1663-128">**SetSharedSecret**</span></span>](setsharedsecret-win32-tsgatewayradiusserver.md) | <span data-ttu-id="a1663-129">設定此 RADIUS 伺服器的 **SharedSecret** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a1663-129">Sets the **SharedSecret** property for this RADIUS server.</span></span><br/>        |
| [<span data-ttu-id="a1663-130">**更新**</span><span class="sxs-lookup"><span data-stu-id="a1663-130">**Update**</span></span>](update-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="a1663-131">更新目前的 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a1663-131">Updates the current RADIUS server.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="a1663-132">屬性</span><span class="sxs-lookup"><span data-stu-id="a1663-132">Properties</span></span>

<span data-ttu-id="a1663-133">**Win32 \_ TSGatewayRADIUSServer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a1663-133">The **Win32\_TSGatewayRADIUSServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1663-134">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a1663-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1663-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1663-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1663-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1663-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1663-137">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a1663-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a1663-138">RADIUS 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1663-138">Name of the RADIUS server.</span></span> <span data-ttu-id="a1663-139">這個屬性可以使用 [**SetName**](setname-win32-tsgatewayradiusserver.md) 方法來變更。</span><span class="sxs-lookup"><span data-stu-id="a1663-139">This property can be changed with the [**SetName**](setname-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="a1663-140">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="a1663-140">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1663-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a1663-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1663-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1663-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1663-143">RADIUS 伺服器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="a1663-143">Priority of the RADIUS server.</span></span> <span data-ttu-id="a1663-144">RD 閘道伺服器會根據優先順序在 RADIUS 伺服器上尋找 RD Cap。</span><span class="sxs-lookup"><span data-stu-id="a1663-144">The RD Gateway server looks for RD CAPs on RADIUS servers based on the priority.</span></span> <span data-ttu-id="a1663-145">您可以使用 [**上移**](moveup-win32-tsgatewayradiusserver.md)、 [**MoveDown**](movedown-win32-tsgatewayradiusserver.md)、 [**Add**](win32-tsgatewayradiusserver-add.md)和 [**Remove**](win32-tsgatewayradiusserver-remove.md) 方法來變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a1663-145">This property can be changed with the [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md), and [**Remove**](win32-tsgatewayradiusserver-remove.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="a1663-146">**SharedSecret**</span><span class="sxs-lookup"><span data-stu-id="a1663-146">**SharedSecret**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1663-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1663-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1663-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1663-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1663-149">RADIUS 伺服器的共用密碼。</span><span class="sxs-lookup"><span data-stu-id="a1663-149">Shared secret for the RADIUS server.</span></span> <span data-ttu-id="a1663-150">這個屬性可以使用 [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) 方法來變更。</span><span class="sxs-lookup"><span data-stu-id="a1663-150">This property can be changed with the [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1663-151">備註</span><span class="sxs-lookup"><span data-stu-id="a1663-151">Remarks</span></span>

<span data-ttu-id="a1663-152">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="a1663-152">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="a1663-153">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a1663-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a1663-154">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a1663-154">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a1663-155">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a1663-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a1663-156">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="a1663-156">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1663-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1663-157">Requirements</span></span>



| <span data-ttu-id="a1663-158">需求</span><span class="sxs-lookup"><span data-stu-id="a1663-158">Requirement</span></span> | <span data-ttu-id="a1663-159">值</span><span class="sxs-lookup"><span data-stu-id="a1663-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1663-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1663-160">Minimum supported client</span></span><br/> | <span data-ttu-id="a1663-161">都不支援</span><span class="sxs-lookup"><span data-stu-id="a1663-161">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a1663-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1663-162">Minimum supported server</span></span><br/> | <span data-ttu-id="a1663-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1663-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a1663-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1663-164">Namespace</span></span><br/>                | <span data-ttu-id="a1663-165">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a1663-165">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a1663-166">MOF</span><span class="sxs-lookup"><span data-stu-id="a1663-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1663-167"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1663-167"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1663-168">DLL</span><span class="sxs-lookup"><span data-stu-id="a1663-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1663-169"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1663-169"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a1663-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1663-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1663-171">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="a1663-171">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="a1663-172">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="a1663-172">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="a1663-173">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="a1663-173">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="a1663-174">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="a1663-174">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="a1663-175">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="a1663-175">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="a1663-176">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="a1663-176">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

