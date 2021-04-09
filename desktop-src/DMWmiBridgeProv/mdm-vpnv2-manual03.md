---
title: MDM_VPNv2_Manual03 類別
description: MDM \_ >vpnv2 \_ Manual03class 是選用節點，其中包含手動伺服器設定。
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- MDM_VPNv2_Manual03 類別
- MDM_VPNv2_Manual03 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934939"
---
# <a name="mdm_vpnv2_manual03-class"></a><span data-ttu-id="ecb9e-105">MDM \_ >vpnv2 \_ Manual03 類別</span><span class="sxs-lookup"><span data-stu-id="ecb9e-105">MDM\_VPNv2\_Manual03 class</span></span>

<span data-ttu-id="ecb9e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ecb9e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ecb9e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ecb9e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ecb9e-108">**MDM \_ >vpnv2 \_ Manual03** 類別是選擇性節點，其中包含手動伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="ecb9e-108">The **MDM\_VPNv2\_Manual03** class is an optional node containing the manual server settings.</span></span>

<span data-ttu-id="ecb9e-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ecb9e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb9e-110">語法</span><span class="sxs-lookup"><span data-stu-id="ecb9e-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a><span data-ttu-id="ecb9e-111">成員</span><span class="sxs-lookup"><span data-stu-id="ecb9e-111">Members</span></span>

<span data-ttu-id="ecb9e-112">**MDM \_ >vpnv2 \_ Manual03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ecb9e-112">The **MDM\_VPNv2\_Manual03** class has these types of members:</span></span>

-   [<span data-ttu-id="ecb9e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ecb9e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecb9e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ecb9e-114">Properties</span></span>

<span data-ttu-id="ecb9e-115">**MDM \_ >vpnv2 \_ Manual03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ecb9e-115">The **MDM\_VPNv2\_Manual03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ecb9e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ecb9e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb9e-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ecb9e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecb9e-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb9e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecb9e-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecb9e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ecb9e-120">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecb9e-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="ecb9e-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ecb9e-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb9e-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ecb9e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecb9e-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb9e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecb9e-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecb9e-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ecb9e-125">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ecb9e-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="ecb9e-126">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/Proxy/"</span><span class="sxs-lookup"><span data-stu-id="ecb9e-126">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/Proxy/"</span></span>

</dd> <dt>

[<span data-ttu-id="ecb9e-127">伺服器</span><span class="sxs-lookup"><span data-stu-id="ecb9e-127">Server</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb9e-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ecb9e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecb9e-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ecb9e-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecb9e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecb9e-130">Requirements</span></span>



| <span data-ttu-id="ecb9e-131">需求</span><span class="sxs-lookup"><span data-stu-id="ecb9e-131">Requirement</span></span> | <span data-ttu-id="ecb9e-132">值</span><span class="sxs-lookup"><span data-stu-id="ecb9e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb9e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecb9e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb9e-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecb9e-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ecb9e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ecb9e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb9e-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="ecb9e-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ecb9e-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="ecb9e-137">Namespace</span></span><br/>                | <span data-ttu-id="ecb9e-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ecb9e-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ecb9e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ecb9e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecb9e-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecb9e-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecb9e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb9e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecb9e-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecb9e-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb9e-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecb9e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb9e-144">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="ecb9e-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

