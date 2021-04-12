---
title: MDM_VPNv2_Authentication03 類別
description: MDM \_ >vpnv2 \_ Authentication03 類別包含原生 VPN 設定檔的驗證資訊。
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- MDM_VPNv2_Authentication03 類別
- MDM_VPNv2_Authentication03 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ca50bcc83df01b4aa5e7ec900985cf15f7e67d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025114"
---
# <a name="mdm_vpnv2_authentication03-class"></a><span data-ttu-id="2110a-105">MDM \_ >vpnv2 \_ Authentication03 類別</span><span class="sxs-lookup"><span data-stu-id="2110a-105">MDM\_VPNv2\_Authentication03 class</span></span>

<span data-ttu-id="2110a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="2110a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2110a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="2110a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2110a-108">[**MDM \_ >vpnv2 \_ Authentication03**](mdm-vpnv2-01.md)類別包含原生 VPN 設定檔的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="2110a-108">The [**MDM\_VPNv2\_Authentication03**](mdm-vpnv2-01.md) class contains authentication information for the native VPN profile.</span></span>

<span data-ttu-id="2110a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2110a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2110a-110">語法</span><span class="sxs-lookup"><span data-stu-id="2110a-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a><span data-ttu-id="2110a-111">成員</span><span class="sxs-lookup"><span data-stu-id="2110a-111">Members</span></span>

<span data-ttu-id="2110a-112">**MDM \_ >vpnv2 \_ Authentication03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2110a-112">The **MDM\_VPNv2\_Authentication03** class has these types of members:</span></span>

-   [<span data-ttu-id="2110a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2110a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2110a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="2110a-114">Properties</span></span>

<span data-ttu-id="2110a-115">**MDM \_ >vpnv2 \_ Authentication03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2110a-115">The **MDM\_VPNv2\_Authentication03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2110a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2110a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2110a-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2110a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2110a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2110a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2110a-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2110a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2110a-120">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="2110a-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="2110a-121">MachineMethod</span><span class="sxs-lookup"><span data-stu-id="2110a-121">MachineMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2110a-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2110a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2110a-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2110a-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2110a-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2110a-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2110a-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2110a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2110a-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2110a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2110a-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2110a-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2110a-128">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2110a-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="2110a-129">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span><span class="sxs-lookup"><span data-stu-id="2110a-129">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="2110a-130">UserMethod</span><span class="sxs-lookup"><span data-stu-id="2110a-130">UserMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2110a-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2110a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2110a-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2110a-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2110a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2110a-133">Requirements</span></span>



| <span data-ttu-id="2110a-134">需求</span><span class="sxs-lookup"><span data-stu-id="2110a-134">Requirement</span></span> | <span data-ttu-id="2110a-135">值</span><span class="sxs-lookup"><span data-stu-id="2110a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2110a-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2110a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2110a-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2110a-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2110a-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2110a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2110a-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="2110a-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2110a-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="2110a-140">Namespace</span></span><br/>                | <span data-ttu-id="2110a-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2110a-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2110a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2110a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2110a-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="2110a-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2110a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2110a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2110a-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2110a-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2110a-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2110a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2110a-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="2110a-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

