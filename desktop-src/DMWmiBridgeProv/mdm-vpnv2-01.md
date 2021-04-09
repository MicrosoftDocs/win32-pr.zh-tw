---
title: MDM_VPNv2_01 類別
description: MDM \_ >vpnv2 \_ 01 類別允許設定裝置的 VPN 設定檔。
ms.assetid: cfef674b-880c-4c9f-a2c1-6c2cb03189da
keywords:
- MDM_VPNv2_01 類別
- MDM_VPNv2_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_01
- MDM_VPNv2_01.InstanceID
- MDM_VPNv2_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3457220c438d0143db90c1955d48352353fee29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934536"
---
# <a name="mdm_vpnv2_01-class"></a><span data-ttu-id="a021c-105">MDM \_ >vpnv2 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="a021c-105">MDM\_VPNv2\_01 class</span></span>

<span data-ttu-id="a021c-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a021c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a021c-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a021c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a021c-108">**MDM \_ >vpnv2 \_ 01** 類別允許設定裝置的 VPN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a021c-108">The **MDM\_VPNv2\_01** class allows configuration of the VPN profile of the device.</span></span>

<span data-ttu-id="a021c-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a021c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a021c-110">語法</span><span class="sxs-lookup"><span data-stu-id="a021c-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_01
{
  string  InstanceID;
  string  ParentID;
  string  EdpModeId;
  boolean RememberCredentials;
  boolean AlwaysOn;
  string  DnsSuffix;
  boolean ByPassForLocal;
  string  TrustedNetworkDetection;
  string  ProfileXML;
  boolean LockDown;
};
```

## <a name="members"></a><span data-ttu-id="a021c-111">成員</span><span class="sxs-lookup"><span data-stu-id="a021c-111">Members</span></span>

<span data-ttu-id="a021c-112">**MDM \_ >vpnv2 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a021c-112">The **MDM\_VPNv2\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="a021c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a021c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a021c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a021c-114">Properties</span></span>

<span data-ttu-id="a021c-115">**MDM \_ >vpnv2 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a021c-115">The **MDM\_VPNv2\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a021c-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="a021c-116">AlwaysOn</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-117">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a021c-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a021c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a021c-119">ByPassForLocal</span><span class="sxs-lookup"><span data-stu-id="a021c-119">ByPassForLocal</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-bypassforlocal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a021c-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a021c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a021c-122">DnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a021c-122">DnsSuffix</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-dnssuffix)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a021c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a021c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a021c-125">EdpModeId</span><span class="sxs-lookup"><span data-stu-id="a021c-125">EdpModeId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-edpmodeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a021c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a021c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a021c-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a021c-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a021c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a021c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a021c-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a021c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a021c-132">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a021c-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="a021c-133">針對此類別，此字串為 VPN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="a021c-133">For this class, the string is the VPN profile name.</span></span>

</dd> <dt>

[<span data-ttu-id="a021c-134">LockDown</span><span class="sxs-lookup"><span data-stu-id="a021c-134">LockDown</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-lockdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a021c-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a021c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a021c-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a021c-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a021c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a021c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a021c-140">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a021c-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a021c-141">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a021c-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="a021c-142">此類別的字串為 "./Vendor/MSFT/VPNv2"</span><span class="sxs-lookup"><span data-stu-id="a021c-142">For this class, the string is "./Vendor/MSFT/VPNv2"</span></span>

</dd> <dt>

[<span data-ttu-id="a021c-143">ProfileXML</span><span class="sxs-lookup"><span data-stu-id="a021c-143">ProfileXML</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-profilexml)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a021c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a021c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a021c-146">RememberCredentials</span><span class="sxs-lookup"><span data-stu-id="a021c-146">RememberCredentials</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-remembercredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-147">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a021c-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a021c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a021c-149">TrustedNetworkDetection</span><span class="sxs-lookup"><span data-stu-id="a021c-149">TrustedNetworkDetection</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trustednetworkdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a021c-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a021c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a021c-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a021c-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a021c-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="a021c-152">Requirements</span></span>



| <span data-ttu-id="a021c-153">需求</span><span class="sxs-lookup"><span data-stu-id="a021c-153">Requirement</span></span> | <span data-ttu-id="a021c-154">值</span><span class="sxs-lookup"><span data-stu-id="a021c-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a021c-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a021c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="a021c-156">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a021c-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a021c-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a021c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="a021c-158">都不支援</span><span class="sxs-lookup"><span data-stu-id="a021c-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a021c-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="a021c-159">Namespace</span></span><br/>                | <span data-ttu-id="a021c-160">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="a021c-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a021c-161">MOF</span><span class="sxs-lookup"><span data-stu-id="a021c-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a021c-162"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a021c-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a021c-163">DLL</span><span class="sxs-lookup"><span data-stu-id="a021c-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a021c-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a021c-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a021c-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a021c-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a021c-166">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a021c-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

