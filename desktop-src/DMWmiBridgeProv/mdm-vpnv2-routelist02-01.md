---
title: MDM_VPNv2_RouteList02_01 類別
description: MDM \_ >vpnv2 \_ RouteList02 \_ 01 類別包含要新增至 VPN 介面路由表的選擇性路由清單。
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- MDM_VPNv2_RouteList02_01 類別
- MDM_VPNv2_RouteList02_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025315"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a><span data-ttu-id="256b0-105">MDM \_ >vpnv2 \_ RouteList02 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="256b0-105">MDM\_VPNv2\_RouteList02\_01 class</span></span>

<span data-ttu-id="256b0-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="256b0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="256b0-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="256b0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="256b0-108">**MDM \_ >vpnv2 \_ RouteList02 \_ 01** 類別包含要新增至 VPN 介面路由表的選擇性路由清單。</span><span class="sxs-lookup"><span data-stu-id="256b0-108">The **MDM\_VPNv2\_RouteList02\_01** class contains an optional list of routes to be added to the routing table for the VPN interface.</span></span>

<span data-ttu-id="256b0-109">這是分割通道案例的必要項，其中 VPN 伺服器網站有更多子網，預設子網是根據指派給介面的 IP。</span><span class="sxs-lookup"><span data-stu-id="256b0-109">This is required for split tunneling case where the VPN server site has more subnets that the default subnet based on the IP assigned to the interface.</span></span>

<span data-ttu-id="256b0-110">執行 TCP/IP 的每部電腦都要決定其路由。</span><span class="sxs-lookup"><span data-stu-id="256b0-110">Every computer that runs TCP/IP makes routing decisions.</span></span> <span data-ttu-id="256b0-111">這些決定由 IP 路由表控制。</span><span class="sxs-lookup"><span data-stu-id="256b0-111">These decisions are controlled by the IP routing table.</span></span> <span data-ttu-id="256b0-112">在此節點下新增值，就會使用 VPN 介面後置連線的路由來更新路由表。</span><span class="sxs-lookup"><span data-stu-id="256b0-112">Adding values under this node updates the routing table with routes for the VPN interface post connection.</span></span> <span data-ttu-id="256b0-113">此節點下的值代表 IP 路由的目的地前置詞。</span><span class="sxs-lookup"><span data-stu-id="256b0-113">The values under this node represent the destination prefix of IP routes.</span></span> <span data-ttu-id="256b0-114">目的地首碼包含 IP 位址首碼和前置長度。</span><span class="sxs-lookup"><span data-stu-id="256b0-114">A destination prefix consists of an IP address prefix and a prefix length.</span></span>

<span data-ttu-id="256b0-115">在這裡新增路由，可讓網路堆疊識別需要透過 VPN 介面進行分割通道 VPN 的流量。</span><span class="sxs-lookup"><span data-stu-id="256b0-115">Adding a route here allows the networking stack to identify the traffic that needs to go over the VPN interface for split tunnel VPN.</span></span> <span data-ttu-id="256b0-116">某些 VPN 伺服器可以在連線協商期間進行這項設定，而且在 VPN 設定檔中不需要這項資訊。</span><span class="sxs-lookup"><span data-stu-id="256b0-116">Some VPN servers can configure this during connect negotiation and do not need this information in the VPN Profile.</span></span> <span data-ttu-id="256b0-117">請洽詢您的 VPN 伺服器系統管理員，以判斷您是否需要在 VPN 設定檔中使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="256b0-117">Please check with your VPN server administrator to determine whether you need this information in the VPN profile.</span></span>

<span data-ttu-id="256b0-118">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="256b0-118">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="256b0-119">語法</span><span class="sxs-lookup"><span data-stu-id="256b0-119">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a><span data-ttu-id="256b0-120">成員</span><span class="sxs-lookup"><span data-stu-id="256b0-120">Members</span></span>

<span data-ttu-id="256b0-121">**MDM \_ >vpnv2 \_ RouteList02 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="256b0-121">The **MDM\_VPNv2\_RouteList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="256b0-122">屬性</span><span class="sxs-lookup"><span data-stu-id="256b0-122">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="256b0-123">屬性</span><span class="sxs-lookup"><span data-stu-id="256b0-123">Properties</span></span>

<span data-ttu-id="256b0-124">**MDM \_ >vpnv2 \_ RouteList02 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="256b0-124">The **MDM\_VPNv2\_RouteList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="256b0-125">位址</span><span class="sxs-lookup"><span data-stu-id="256b0-125">Address</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

<span data-ttu-id="256b0-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="256b0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256b0-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="256b0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="256b0-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="256b0-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256b0-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="256b0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256b0-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="256b0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256b0-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="256b0-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="256b0-132">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="256b0-132">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="256b0-133">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="256b0-133">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256b0-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="256b0-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256b0-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="256b0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256b0-136">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="256b0-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="256b0-137">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="256b0-137">Describes the full path to the parent node.</span></span> <span data-ttu-id="256b0-138">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span><span class="sxs-lookup"><span data-stu-id="256b0-138">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span></span>

</dd> <dt>

[<span data-ttu-id="256b0-139">PrefixSize</span><span class="sxs-lookup"><span data-stu-id="256b0-139">PrefixSize</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="256b0-140">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="256b0-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="256b0-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="256b0-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="256b0-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="256b0-142">Requirements</span></span>



| <span data-ttu-id="256b0-143">需求</span><span class="sxs-lookup"><span data-stu-id="256b0-143">Requirement</span></span> | <span data-ttu-id="256b0-144">值</span><span class="sxs-lookup"><span data-stu-id="256b0-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="256b0-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="256b0-145">Minimum supported client</span></span><br/> | <span data-ttu-id="256b0-146">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="256b0-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="256b0-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="256b0-147">Minimum supported server</span></span><br/> | <span data-ttu-id="256b0-148">都不支援</span><span class="sxs-lookup"><span data-stu-id="256b0-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="256b0-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="256b0-149">Namespace</span></span><br/>                | <span data-ttu-id="256b0-150">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="256b0-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="256b0-151">MOF</span><span class="sxs-lookup"><span data-stu-id="256b0-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="256b0-152"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="256b0-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="256b0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="256b0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="256b0-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="256b0-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="256b0-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="256b0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256b0-156">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="256b0-156">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

