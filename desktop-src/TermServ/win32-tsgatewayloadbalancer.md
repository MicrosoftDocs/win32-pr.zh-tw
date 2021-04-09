---
title: Win32_TSGatewayLoadBalancer 類別
description: 描述一組遠端桌面閘道 (RD 閘道) 負載平衡伺服器。 這些是用來在多部伺服器之間 RD 閘道連接之間進行負載平衡。
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer 類別遠端桌面服務
- Win32_TSGatewayLoadBalancer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685845"
---
# <a name="win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="8bd7d-106">Win32 \_ TSGatewayLoadBalancer 類別</span><span class="sxs-lookup"><span data-stu-id="8bd7d-106">Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="8bd7d-107">描述一組遠端桌面閘道 (RD 閘道) 負載平衡伺服器。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-107">Describes a set of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span> <span data-ttu-id="8bd7d-108">這些是用來在多部伺服器之間 RD 閘道連接之間進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-108">These are used to load balance RD Gateway connections across multiple servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd7d-109">語法</span><span class="sxs-lookup"><span data-stu-id="8bd7d-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a><span data-ttu-id="8bd7d-110">成員</span><span class="sxs-lookup"><span data-stu-id="8bd7d-110">Members</span></span>

<span data-ttu-id="8bd7d-111">**Win32 \_ TSGatewayLoadBalancer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8bd7d-111">The **Win32\_TSGatewayLoadBalancer** class has these types of members:</span></span>

-   [<span data-ttu-id="8bd7d-112">方法</span><span class="sxs-lookup"><span data-stu-id="8bd7d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8bd7d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8bd7d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8bd7d-114">方法</span><span class="sxs-lookup"><span data-stu-id="8bd7d-114">Methods</span></span>

<span data-ttu-id="8bd7d-115">**Win32 \_ TSGatewayLoadBalancer** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-115">The **Win32\_TSGatewayLoadBalancer** class has these methods.</span></span>



| <span data-ttu-id="8bd7d-116">方法</span><span class="sxs-lookup"><span data-stu-id="8bd7d-116">Method</span></span>                                                                             | <span data-ttu-id="8bd7d-117">描述</span><span class="sxs-lookup"><span data-stu-id="8bd7d-117">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bd7d-118">**AddServers**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-118">**AddServers**</span></span>](addservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="8bd7d-119">將伺服器新增至 [ **伺服器** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-119">Adds servers to the **Servers** property.</span></span><br/>                                                             |
| [<span data-ttu-id="8bd7d-120">**DeleteAllServers**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-120">**DeleteAllServers**</span></span>](deleteallservers-win32-tsgatewayloadbalancer.md)           | <span data-ttu-id="8bd7d-121">刪除參與負載平衡伺服器陣列的所有 RD 閘道負載平衡伺服器。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-121">Deletes all RD Gateway load-balancing servers participating in the load-balancing farm.</span></span><br/>               |
| [<span data-ttu-id="8bd7d-122">**DeleteServers**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-122">**DeleteServers**</span></span>](deleteservers-win32-tsgatewayloadbalancer.md)                 | <span data-ttu-id="8bd7d-123">從 **伺服器** 屬性刪除伺服器。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-123">Deletes servers from the **Servers** property.</span></span><br/>                                                        |
| [<span data-ttu-id="8bd7d-124">**IsLoadBalancingServer**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-124">**IsLoadBalancingServer**</span></span>](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | <span data-ttu-id="8bd7d-125">判斷伺服器是否可以執行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-125">Determines whether the server can perform load balancing.</span></span><br/>                                             |
| [<span data-ttu-id="8bd7d-126">**SetServers**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-126">**SetServers**</span></span>](setservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="8bd7d-127">以分號分隔的 RD 閘道負載平衡伺服器清單來設定 **伺服器** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-127">Sets the **Servers** property with the semicolon-separated list of RD Gateway load-balancing servers.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8bd7d-128">屬性</span><span class="sxs-lookup"><span data-stu-id="8bd7d-128">Properties</span></span>

<span data-ttu-id="8bd7d-129">**Win32 \_ TSGatewayLoadBalancer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-129">The **Win32\_TSGatewayLoadBalancer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bd7d-130">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-130">**Servers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bd7d-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bd7d-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8bd7d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bd7d-133">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8bd7d-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8bd7d-134">RD 閘道的負載平衡伺服器清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-134">Semicolon-separated list of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="8bd7d-135">您可以使用 [**SetServers**](setservers-win32-tsgatewayloadbalancer.md)、 [**AddServers**](addservers-win32-tsgatewayloadbalancer.md)、 [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)和 [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) 方法來變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-135">This property can be changed with the [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md), and [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bd7d-136">備註</span><span class="sxs-lookup"><span data-stu-id="8bd7d-136">Remarks</span></span>

<span data-ttu-id="8bd7d-137">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-137">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="8bd7d-138">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8bd7d-139">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8bd7d-140">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8bd7d-141">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="8bd7d-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd7d-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bd7d-142">Requirements</span></span>



| <span data-ttu-id="8bd7d-143">需求</span><span class="sxs-lookup"><span data-stu-id="8bd7d-143">Requirement</span></span> | <span data-ttu-id="8bd7d-144">值</span><span class="sxs-lookup"><span data-stu-id="8bd7d-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd7d-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bd7d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd7d-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="8bd7d-146">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8bd7d-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bd7d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd7d-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bd7d-148">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8bd7d-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="8bd7d-149">Namespace</span></span><br/>                | <span data-ttu-id="8bd7d-150">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="8bd7d-150">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8bd7d-151">MOF</span><span class="sxs-lookup"><span data-stu-id="8bd7d-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bd7d-152"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bd7d-152"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bd7d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="8bd7d-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bd7d-154"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bd7d-154"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8bd7d-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bd7d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd7d-156">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-156">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="8bd7d-157">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-157">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="8bd7d-158">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-158">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="8bd7d-159">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-159">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="8bd7d-160">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-160">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="8bd7d-161">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="8bd7d-161">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

