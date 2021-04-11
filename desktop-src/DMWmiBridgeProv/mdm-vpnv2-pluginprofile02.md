---
title: MDM_VPNv2_PluginProfile02 類別
description: MDM \_ >vpnv2 \_ PlugInProfile02 類別描述使用以 Windows 存放區為基礎的 VPN 外掛程式時所需的資訊。
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- MDM_VPNv2_PluginProfile02 類別
- MDM_VPNv2_PluginProfile02 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 008d60b28ec1d2cec9431cc63ac4d0c406d18060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934387"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a><span data-ttu-id="19559-105">MDM \_ >vpnv2 \_ PluginProfile02 類別</span><span class="sxs-lookup"><span data-stu-id="19559-105">MDM\_VPNv2\_PluginProfile02 class</span></span>

<span data-ttu-id="19559-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="19559-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="19559-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="19559-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="19559-108">**MDM \_ >vpnv2 \_ PlugInProfile02** 類別描述使用以 Windows 存放區為基礎的 VPN 外掛程式時所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="19559-108">The **MDM\_VPNv2\_PlugInProfile02** class describes the information needed when using a Windows Store based VPN plugin.</span></span>

<span data-ttu-id="19559-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="19559-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19559-110">語法</span><span class="sxs-lookup"><span data-stu-id="19559-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a><span data-ttu-id="19559-111">成員</span><span class="sxs-lookup"><span data-stu-id="19559-111">Members</span></span>

<span data-ttu-id="19559-112">**MDM \_ >vpnv2 \_ PluginProfile02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="19559-112">The **MDM\_VPNv2\_PluginProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="19559-113">屬性</span><span class="sxs-lookup"><span data-stu-id="19559-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19559-114">屬性</span><span class="sxs-lookup"><span data-stu-id="19559-114">Properties</span></span>

<span data-ttu-id="19559-115">**MDM \_ >vpnv2 \_ PluginProfile02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="19559-115">The **MDM\_VPNv2\_PluginProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="19559-116">CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="19559-116">CustomConfiguration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19559-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19559-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19559-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19559-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19559-119">CustomStoreUrl</span><span class="sxs-lookup"><span data-stu-id="19559-119">CustomStoreUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19559-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19559-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19559-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19559-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19559-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19559-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19559-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19559-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19559-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19559-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19559-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19559-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19559-126">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="19559-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="19559-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="19559-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19559-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19559-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19559-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19559-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19559-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19559-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19559-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="19559-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="19559-132">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="19559-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="19559-133">PluginPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="19559-133">PluginPackageFamilyName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19559-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19559-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19559-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19559-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19559-136">ServerUrlList</span><span class="sxs-lookup"><span data-stu-id="19559-136">ServerUrlList</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19559-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19559-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19559-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19559-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19559-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="19559-139">Requirements</span></span>



| <span data-ttu-id="19559-140">需求</span><span class="sxs-lookup"><span data-stu-id="19559-140">Requirement</span></span> | <span data-ttu-id="19559-141">值</span><span class="sxs-lookup"><span data-stu-id="19559-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19559-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19559-142">Minimum supported client</span></span><br/> | <span data-ttu-id="19559-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19559-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19559-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19559-144">Minimum supported server</span></span><br/> | <span data-ttu-id="19559-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="19559-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="19559-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="19559-146">Namespace</span></span><br/>                | <span data-ttu-id="19559-147">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="19559-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="19559-148">MOF</span><span class="sxs-lookup"><span data-stu-id="19559-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19559-149"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="19559-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="19559-150">DLL</span><span class="sxs-lookup"><span data-stu-id="19559-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19559-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19559-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19559-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19559-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19559-153">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="19559-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

