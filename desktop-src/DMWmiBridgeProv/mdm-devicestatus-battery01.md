---
title: MDM_DeviceStatus_Battery01 類別
description: '\_ \_ 企業使用 MDM DeviceStatus Battery01 類別，以其企業原則查詢裝置的電池合規性狀態。'
ms.assetid: f4e92e2a-e267-467a-9905-2539dcaf8d8c
keywords:
- MDM_DeviceStatus_Battery01 類別
- MDM_DeviceStatus_Battery01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01.InstanceID
- MDM_DeviceStatus_Battery01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b89cd709c4d0d3d5ad3490114bc82d36aa4ef0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965314"
---
# <a name="mdm_devicestatus_battery01-class"></a><span data-ttu-id="35a46-105">MDM \_ DeviceStatus \_ Battery01 類別</span><span class="sxs-lookup"><span data-stu-id="35a46-105">MDM\_DeviceStatus\_Battery01 class</span></span>

<span data-ttu-id="35a46-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="35a46-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="35a46-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="35a46-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="35a46-108">企業使用 **MDM \_ DeviceStatus \_ Battery01** 類別，以其企業原則查詢裝置的電池合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="35a46-108">The **MDM\_DeviceStatus\_Battery01** class is used by the enterprise to query the state of battery compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="35a46-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="35a46-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a46-110">語法</span><span class="sxs-lookup"><span data-stu-id="35a46-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Battery01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  sint32 EstimatedChargeRemaining;
  sint32 EstimatedRuntime;
};
```

## <a name="members"></a><span data-ttu-id="35a46-111">成員</span><span class="sxs-lookup"><span data-stu-id="35a46-111">Members</span></span>

<span data-ttu-id="35a46-112">**MDM \_ DeviceStatus \_ Battery01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="35a46-112">The **MDM\_DeviceStatus\_Battery01** class has these types of members:</span></span>

-   [<span data-ttu-id="35a46-113">屬性</span><span class="sxs-lookup"><span data-stu-id="35a46-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35a46-114">屬性</span><span class="sxs-lookup"><span data-stu-id="35a46-114">Properties</span></span>

<span data-ttu-id="35a46-115">**MDM \_ DeviceStatus \_ Battery01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="35a46-115">The **MDM\_DeviceStatus\_Battery01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="35a46-116">EstimatedChargeRemaining</span><span class="sxs-lookup"><span data-stu-id="35a46-116">EstimatedChargeRemaining</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedchargeremaining)
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a46-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="35a46-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35a46-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a46-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="35a46-119">EstimatedRuntime</span><span class="sxs-lookup"><span data-stu-id="35a46-119">EstimatedRuntime</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedruntime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a46-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="35a46-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35a46-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a46-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="35a46-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="35a46-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a46-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a46-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a46-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a46-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35a46-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35a46-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35a46-126">電池查詢的節點。</span><span class="sxs-lookup"><span data-stu-id="35a46-126">Node for the battery query.</span></span>

</dd> <dt>

<span data-ttu-id="35a46-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="35a46-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a46-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a46-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a46-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a46-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35a46-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35a46-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35a46-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="35a46-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="35a46-132">此類別的字串為 "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="35a46-132">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="35a46-133">狀態</span><span class="sxs-lookup"><span data-stu-id="35a46-133">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a46-134">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="35a46-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35a46-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a46-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35a46-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="35a46-136">Requirements</span></span>



| <span data-ttu-id="35a46-137">需求</span><span class="sxs-lookup"><span data-stu-id="35a46-137">Requirement</span></span> | <span data-ttu-id="35a46-138">值</span><span class="sxs-lookup"><span data-stu-id="35a46-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a46-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35a46-139">Minimum supported client</span></span><br/> | <span data-ttu-id="35a46-140">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35a46-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35a46-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35a46-141">Minimum supported server</span></span><br/> | <span data-ttu-id="35a46-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="35a46-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="35a46-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="35a46-143">Namespace</span></span><br/>                | <span data-ttu-id="35a46-144">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="35a46-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="35a46-145">MOF</span><span class="sxs-lookup"><span data-stu-id="35a46-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35a46-146"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="35a46-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="35a46-147">DLL</span><span class="sxs-lookup"><span data-stu-id="35a46-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a46-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a46-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

