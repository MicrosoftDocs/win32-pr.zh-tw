---
title: MDM_DeviceStatus 類別
description: '\_企業會使用 MDM DeviceStatus 類別來追蹤裝置清查，並使用其企業原則來查詢這些裝置的相容性狀態。'
ms.assetid: fceaaf36-8f33-410a-89b4-c824b10164d5
keywords:
- MDM_DeviceStatus 類別
- MDM_DeviceStatus 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus
- MDM_DeviceStatus.InstanceID
- MDM_DeviceStatus.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751a33553b4a00ac6719ce6e24c75a03444f0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104994"
---
# <a name="mdm_devicestatus-class"></a><span data-ttu-id="d7c5d-105">MDM \_ DeviceStatus 類別</span><span class="sxs-lookup"><span data-stu-id="d7c5d-105">MDM\_DeviceStatus class</span></span>

<span data-ttu-id="d7c5d-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d7c5d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d7c5d-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d7c5d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d7c5d-108">企業會使用 **MDM \_ DeviceStatus** 類別來追蹤裝置清查，並使用其企業原則來查詢這些裝置的相容性狀態。</span><span class="sxs-lookup"><span data-stu-id="d7c5d-108">The **MDM\_DeviceStatus** class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="d7c5d-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7c5d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c5d-110">語法</span><span class="sxs-lookup"><span data-stu-id="d7c5d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus
{
  string InstanceID;
  string ParentID;
  sint32 SecureBootState;
  string DomainName;
};
```

## <a name="members"></a><span data-ttu-id="d7c5d-111">成員</span><span class="sxs-lookup"><span data-stu-id="d7c5d-111">Members</span></span>

<span data-ttu-id="d7c5d-112">**MDM \_ DeviceStatus** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d7c5d-112">The **MDM\_DeviceStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="d7c5d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d7c5d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7c5d-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d7c5d-114">Properties</span></span>

<span data-ttu-id="d7c5d-115">**MDM \_ DeviceStatus** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d7c5d-115">The **MDM\_DeviceStatus** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d7c5d-116">DomainName</span><span class="sxs-lookup"><span data-stu-id="d7c5d-116">DomainName</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c5d-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7c5d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7c5d-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d7c5d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d7c5d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d7c5d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c5d-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7c5d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7c5d-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7c5d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7c5d-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d7c5d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d7c5d-123">DeviceStatus 設定服務提供者的根節點。</span><span class="sxs-lookup"><span data-stu-id="d7c5d-123">The root node for the DeviceStatus configuration service provider.</span></span>

</dd> <dt>

<span data-ttu-id="d7c5d-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d7c5d-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c5d-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7c5d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7c5d-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7c5d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7c5d-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d7c5d-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d7c5d-128">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="d7c5d-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="d7c5d-129">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="d7c5d-129">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="d7c5d-130">SecureBootState</span><span class="sxs-lookup"><span data-stu-id="d7c5d-130">SecureBootState</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-securebootstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c5d-131">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="d7c5d-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d7c5d-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d7c5d-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7c5d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7c5d-133">Requirements</span></span>



| <span data-ttu-id="d7c5d-134">需求</span><span class="sxs-lookup"><span data-stu-id="d7c5d-134">Requirement</span></span> | <span data-ttu-id="d7c5d-135">值</span><span class="sxs-lookup"><span data-stu-id="d7c5d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c5d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7c5d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d7c5d-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7c5d-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7c5d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7c5d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d7c5d-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="d7c5d-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d7c5d-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="d7c5d-140">Namespace</span></span><br/>                | <span data-ttu-id="d7c5d-141">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="d7c5d-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="d7c5d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d7c5d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7c5d-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7c5d-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7c5d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d7c5d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7c5d-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7c5d-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c5d-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7c5d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c5d-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="d7c5d-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

