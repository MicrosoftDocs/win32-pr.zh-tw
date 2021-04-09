---
title: MDM_DeviceStatus_DeviceGuard01 類別
description: '\_ \_ 企業會使用 MDM DeviceStatus DeviceGuard01 類別來追蹤裝置清查，並使用其企業原則來查詢這些裝置的相容性狀態。'
ms.assetid: 267129f6-ec37-43ae-bba3-e21917012f27
keywords:
- MDM_DeviceStatus_DeviceGuard01 類別
- MDM_DeviceStatus_DeviceGuard01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01.InstanceID
- MDM_DeviceStatus_DeviceGuard01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5f4dffa67ad86b5486dce372018efd29e62620
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934776"
---
# <a name="mdm_devicestatus_deviceguard01-class"></a><span data-ttu-id="476d1-105">MDM \_ DeviceStatus \_ DeviceGuard01 類別</span><span class="sxs-lookup"><span data-stu-id="476d1-105">MDM\_DeviceStatus\_DeviceGuard01 class</span></span>

<span data-ttu-id="476d1-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="476d1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="476d1-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="476d1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="476d1-108">\_ \_ 企業會使用 MDM DeviceStatus DeviceGuard01 類別來追蹤裝置清查，並使用其企業原則來查詢這些裝置的相容性狀態。</span><span class="sxs-lookup"><span data-stu-id="476d1-108">The MDM\_DeviceStatus\_DeviceGuard01 class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="476d1-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="476d1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="476d1-110">語法</span><span class="sxs-lookup"><span data-stu-id="476d1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_DeviceGuard01
{
  string InstanceID;
  string ParentID;
  sint32 VirtualizationBasedSecurityHwReq;
  sint32 VirtualizationBasedSecurityStatus;
  sint32 LsaCfgCredGuardStatus;
};
```

## <a name="members"></a><span data-ttu-id="476d1-111">成員</span><span class="sxs-lookup"><span data-stu-id="476d1-111">Members</span></span>

<span data-ttu-id="476d1-112">**MDM \_ DeviceStatus \_ DeviceGuard01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="476d1-112">The **MDM\_DeviceStatus\_DeviceGuard01** class has these types of members:</span></span>

-   [<span data-ttu-id="476d1-113">屬性</span><span class="sxs-lookup"><span data-stu-id="476d1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="476d1-114">屬性</span><span class="sxs-lookup"><span data-stu-id="476d1-114">Properties</span></span>

<span data-ttu-id="476d1-115">**MDM \_ DeviceStatus \_ DeviceGuard01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="476d1-115">The **MDM\_DeviceStatus\_DeviceGuard01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="476d1-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="476d1-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="476d1-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="476d1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="476d1-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="476d1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="476d1-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="476d1-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="476d1-120">LsaCfgCredGuardStatus</span><span class="sxs-lookup"><span data-stu-id="476d1-120">LsaCfgCredGuardStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-lsacfgcredguardstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="476d1-121">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="476d1-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="476d1-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="476d1-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="476d1-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="476d1-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="476d1-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="476d1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="476d1-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="476d1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="476d1-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="476d1-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="476d1-127">VirtualizationBasedSecurityHwReq</span><span class="sxs-lookup"><span data-stu-id="476d1-127">VirtualizationBasedSecurityHwReq</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecurityhwreq)
</dt> <dd> <dl> <dt>

<span data-ttu-id="476d1-128">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="476d1-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="476d1-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="476d1-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="476d1-130">VirtualizationBasedSecurityStatus</span><span class="sxs-lookup"><span data-stu-id="476d1-130">VirtualizationBasedSecurityStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecuritystatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="476d1-131">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="476d1-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="476d1-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="476d1-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="476d1-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="476d1-133">Requirements</span></span>



| <span data-ttu-id="476d1-134">需求</span><span class="sxs-lookup"><span data-stu-id="476d1-134">Requirement</span></span> | <span data-ttu-id="476d1-135">值</span><span class="sxs-lookup"><span data-stu-id="476d1-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="476d1-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="476d1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="476d1-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="476d1-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="476d1-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="476d1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="476d1-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="476d1-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="476d1-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="476d1-140">Namespace</span></span><br/>                | <span data-ttu-id="476d1-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="476d1-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="476d1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="476d1-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="476d1-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="476d1-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="476d1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="476d1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="476d1-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="476d1-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

