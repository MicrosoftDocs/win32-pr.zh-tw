---
title: MDM_VPNv2_NativeProfile02 類別
description: '\_ \_ 當使用 Windows 收件匣 VPN 通訊協定 (IKEV2、PPTP、L2TP) 時，MDM >vpnv2 NativeProfile2 類別會定義設定檔資訊。'
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- MDM_VPNv2_NativeProfile02 類別
- MDM_VPNv2_NativeProfile02 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8573975c488df6e5c759e719d5c687f6a71c505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844164"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a><span data-ttu-id="bc929-105">MDM \_ >vpnv2 \_ NativeProfile02 類別</span><span class="sxs-lookup"><span data-stu-id="bc929-105">MDM\_VPNv2\_NativeProfile02 class</span></span>

<span data-ttu-id="bc929-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="bc929-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc929-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="bc929-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc929-108">當使用 Windows 收件匣 VPN 通訊協定 (IKEv2、PPTP、L2TP) 時， **MDM \_ >vpnv2 \_ NativeProfile2** 類別會定義設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="bc929-108">The **MDM\_VPNv2\_NativeProfile2** class defines profile information when using a Windows Inbox VPN Protocol (IKEv2, PPTP, L2TP).</span></span>

<span data-ttu-id="bc929-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc929-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc929-110">語法</span><span class="sxs-lookup"><span data-stu-id="bc929-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a><span data-ttu-id="bc929-111">成員</span><span class="sxs-lookup"><span data-stu-id="bc929-111">Members</span></span>

<span data-ttu-id="bc929-112">**MDM \_ >vpnv2 \_ NativeProfile02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bc929-112">The **MDM\_VPNv2\_NativeProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="bc929-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bc929-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc929-114">屬性</span><span class="sxs-lookup"><span data-stu-id="bc929-114">Properties</span></span>

<span data-ttu-id="bc929-115">**MDM \_ >vpnv2 \_ NativeProfile02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bc929-115">The **MDM\_VPNv2\_NativeProfile02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc929-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc929-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc929-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc929-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc929-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc929-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc929-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc929-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc929-120">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc929-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="bc929-121">L2tpPsk</span><span class="sxs-lookup"><span data-stu-id="bc929-121">L2tpPsk</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc929-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc929-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc929-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bc929-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc929-124">NativeProtocolType</span><span class="sxs-lookup"><span data-stu-id="bc929-124">NativeProtocolType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc929-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc929-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc929-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bc929-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc929-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bc929-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc929-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc929-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc929-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc929-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc929-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc929-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc929-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="bc929-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="bc929-132">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="bc929-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="bc929-133">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="bc929-133">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc929-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc929-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc929-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bc929-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc929-136">伺服器</span><span class="sxs-lookup"><span data-stu-id="bc929-136">Servers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc929-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc929-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc929-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bc929-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc929-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc929-139">Requirements</span></span>



| <span data-ttu-id="bc929-140">需求</span><span class="sxs-lookup"><span data-stu-id="bc929-140">Requirement</span></span> | <span data-ttu-id="bc929-141">值</span><span class="sxs-lookup"><span data-stu-id="bc929-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc929-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc929-142">Minimum supported client</span></span><br/> | <span data-ttu-id="bc929-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc929-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc929-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc929-144">Minimum supported server</span></span><br/> | <span data-ttu-id="bc929-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="bc929-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bc929-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="bc929-146">Namespace</span></span><br/>                | <span data-ttu-id="bc929-147">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bc929-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bc929-148">MOF</span><span class="sxs-lookup"><span data-stu-id="bc929-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc929-149"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc929-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc929-150">DLL</span><span class="sxs-lookup"><span data-stu-id="bc929-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc929-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc929-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc929-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc929-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc929-153">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="bc929-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

