---
title: MDM_VPNv2_Proxy02 類別
description: MDM \_ >vpnv2 \_ Proxy02 類別會定義設定物件，以啟用 VPN 的連接後 proxy 支援。
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- MDM_VPNv2_Proxy02 類別
- MDM_VPNv2_Proxy02 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465341"
---
# <a name="mdm_vpnv2_proxy02-class"></a><span data-ttu-id="0309c-105">MDM \_ >vpnv2 \_ Proxy02 類別</span><span class="sxs-lookup"><span data-stu-id="0309c-105">MDM\_VPNv2\_Proxy02 class</span></span>

<span data-ttu-id="0309c-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="0309c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0309c-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="0309c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0309c-108">**MDM \_ >vpnv2 \_ Proxy02** 類別會定義設定物件，以啟用 VPN 的連接後 proxy 支援。</span><span class="sxs-lookup"><span data-stu-id="0309c-108">The **MDM\_VPNv2\_Proxy02** class defines a configuration object to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="0309c-109">當此設定檔為作用中且已連線時，會套用為此設定檔定義的 proxy。</span><span class="sxs-lookup"><span data-stu-id="0309c-109">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

<span data-ttu-id="0309c-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0309c-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0309c-111">語法</span><span class="sxs-lookup"><span data-stu-id="0309c-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a><span data-ttu-id="0309c-112">成員</span><span class="sxs-lookup"><span data-stu-id="0309c-112">Members</span></span>

<span data-ttu-id="0309c-113">**MDM \_ >vpnv2 \_ Proxy02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0309c-113">The **MDM\_VPNv2\_Proxy02** class has these types of members:</span></span>

-   [<span data-ttu-id="0309c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0309c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0309c-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0309c-115">Properties</span></span>

<span data-ttu-id="0309c-116">**MDM \_ >vpnv2 \_ Proxy02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0309c-116">The **MDM\_VPNv2\_Proxy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0309c-117">AutoConfigUrl</span><span class="sxs-lookup"><span data-stu-id="0309c-117">AutoConfigUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0309c-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0309c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0309c-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0309c-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0309c-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0309c-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0309c-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0309c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0309c-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0309c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0309c-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0309c-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0309c-124">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0309c-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="0309c-125">設定物件的集合，可啟用 VPN 的連線後 proxy 支援。</span><span class="sxs-lookup"><span data-stu-id="0309c-125">A collection of configuration objects to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="0309c-126">當此設定檔為作用中且已連線時，會套用為此設定檔定義的 proxy。</span><span class="sxs-lookup"><span data-stu-id="0309c-126">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

</dd> <dt>

<span data-ttu-id="0309c-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0309c-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0309c-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0309c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0309c-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0309c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0309c-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0309c-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0309c-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0309c-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="0309c-132">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="0309c-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0309c-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="0309c-133">Requirements</span></span>



| <span data-ttu-id="0309c-134">需求</span><span class="sxs-lookup"><span data-stu-id="0309c-134">Requirement</span></span> | <span data-ttu-id="0309c-135">值</span><span class="sxs-lookup"><span data-stu-id="0309c-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0309c-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0309c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0309c-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0309c-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0309c-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0309c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0309c-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="0309c-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0309c-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="0309c-140">Namespace</span></span><br/>                | <span data-ttu-id="0309c-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0309c-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0309c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0309c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0309c-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="0309c-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0309c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0309c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0309c-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0309c-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0309c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0309c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0309c-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="0309c-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

