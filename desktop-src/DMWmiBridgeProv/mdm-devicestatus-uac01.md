---
title: MDM_DeviceStatus_UAC01 類別
description: '\_ \_ 企業會使用 MDM DeviceStatus UAC01 類別，以其企業原則查詢裝置的 UAC 狀態。'
ms.assetid: fb1ca1bb-229e-4eaa-a1e3-e790c1dab760
keywords:
- MDM_DeviceStatus_UAC01 類別
- MDM_DeviceStatus_UAC01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_UAC01
- MDM_DeviceStatus_UAC01.InstanceID
- MDM_DeviceStatus_UAC01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eecba42cd97bee660f66570e7f96c1ab2799f85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686187"
---
# <a name="mdm_devicestatus_uac01-class"></a><span data-ttu-id="ade39-105">MDM \_ DeviceStatus \_ UAC01 類別</span><span class="sxs-lookup"><span data-stu-id="ade39-105">MDM\_DeviceStatus\_UAC01 class</span></span>

<span data-ttu-id="ade39-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ade39-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ade39-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ade39-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ade39-108">企業會使用 **MDM \_ DeviceStatus \_ UAC01** 類別，以其企業原則查詢裝置的 UAC 狀態。</span><span class="sxs-lookup"><span data-stu-id="ade39-108">The **MDM\_DeviceStatus\_UAC01** class is used by the enterprise to query the UAC status of devices with their enterprise policies.</span></span>

<span data-ttu-id="ade39-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ade39-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade39-110">語法</span><span class="sxs-lookup"><span data-stu-id="ade39-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_UAC01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="ade39-111">成員</span><span class="sxs-lookup"><span data-stu-id="ade39-111">Members</span></span>

<span data-ttu-id="ade39-112">**MDM \_ DeviceStatus \_ UAC01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ade39-112">The **MDM\_DeviceStatus\_UAC01** class has these types of members:</span></span>

-   [<span data-ttu-id="ade39-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ade39-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ade39-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ade39-114">Properties</span></span>

<span data-ttu-id="ade39-115">**MDM \_ DeviceStatus \_ UAC01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ade39-115">The **MDM\_DeviceStatus\_UAC01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ade39-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ade39-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ade39-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ade39-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ade39-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ade39-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ade39-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ade39-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ade39-120">UAC 查詢的節點。</span><span class="sxs-lookup"><span data-stu-id="ade39-120">Node for the UAC query.</span></span>

</dd> <dt>

<span data-ttu-id="ade39-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ade39-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ade39-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ade39-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ade39-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ade39-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ade39-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ade39-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ade39-125">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ade39-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="ade39-126">此類別的字串為 "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="ade39-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="ade39-127">狀態</span><span class="sxs-lookup"><span data-stu-id="ade39-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ade39-128">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ade39-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ade39-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ade39-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ade39-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ade39-130">Requirements</span></span>



| <span data-ttu-id="ade39-131">需求</span><span class="sxs-lookup"><span data-stu-id="ade39-131">Requirement</span></span> | <span data-ttu-id="ade39-132">值</span><span class="sxs-lookup"><span data-stu-id="ade39-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ade39-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ade39-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ade39-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ade39-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ade39-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ade39-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ade39-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="ade39-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ade39-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="ade39-137">Namespace</span></span><br/>                | <span data-ttu-id="ade39-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ade39-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ade39-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ade39-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ade39-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="ade39-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ade39-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ade39-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ade39-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ade39-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

