---
title: MDM_DeviceStatus_CellularIdentities01_01 類別
description: MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01 類別可讓您查詢裝置是否符合企業加密原則。
ms.assetid: e117ff72-48c0-4b25-8b09-c096851c18ac
keywords:
- MDM_DeviceStatus_CellularIdentities01_01 類別
- MDM_DeviceStatus_CellularIdentities01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01.InstanceID
- MDM_DeviceStatus_CellularIdentities01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d9d3fab514fbfb56d132fc20ba98ef8c2565eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843964"
---
# <a name="mdm_devicestatus_cellularidentities01_01-class"></a><span data-ttu-id="cb113-105">MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="cb113-105">MDM\_DeviceStatus\_CellularIdentities01\_01 class</span></span>

<span data-ttu-id="cb113-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="cb113-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cb113-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="cb113-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cb113-108">**MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** 類別可讓您查詢裝置是否符合企業加密原則。</span><span class="sxs-lookup"><span data-stu-id="cb113-108">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="cb113-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb113-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb113-110">語法</span><span class="sxs-lookup"><span data-stu-id="cb113-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_CellularIdentities01_01
{
  string  InstanceID;
  string  ParentID;
  string  IMSI;
  string  ICCID;
  string  PhoneNumber;
  string  CommercializationOperator;
  boolean RoamingStatus;
  boolean RoamingCompliance;
};
```

## <a name="members"></a><span data-ttu-id="cb113-111">成員</span><span class="sxs-lookup"><span data-stu-id="cb113-111">Members</span></span>

<span data-ttu-id="cb113-112">**MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cb113-112">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="cb113-113">屬性</span><span class="sxs-lookup"><span data-stu-id="cb113-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb113-114">屬性</span><span class="sxs-lookup"><span data-stu-id="cb113-114">Properties</span></span>

<span data-ttu-id="cb113-115">**MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cb113-115">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cb113-116">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="cb113-116">CommercializationOperator</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb113-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cb113-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb113-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cb113-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cb113-119">ICCID</span><span class="sxs-lookup"><span data-stu-id="cb113-119">ICCID</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb113-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cb113-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb113-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cb113-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cb113-122">IMSI</span><span class="sxs-lookup"><span data-stu-id="cb113-122">IMSI</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-imsi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb113-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cb113-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb113-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cb113-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb113-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cb113-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb113-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cb113-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb113-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cb113-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb113-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb113-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cb113-129">用於 SIM 卡上查詢的節點。</span><span class="sxs-lookup"><span data-stu-id="cb113-129">Node for queries on SIM cards.</span></span>

</dd> <dt>

<span data-ttu-id="cb113-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cb113-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb113-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cb113-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb113-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cb113-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb113-133">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb113-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cb113-134">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cb113-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="cb113-135">此類別的字串為 "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="cb113-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="cb113-136">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="cb113-136">PhoneNumber</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-phonenumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb113-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cb113-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb113-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cb113-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cb113-139">RoamingCompliance</span><span class="sxs-lookup"><span data-stu-id="cb113-139">RoamingCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingcompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb113-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cb113-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb113-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cb113-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cb113-142">RoamingStatus</span><span class="sxs-lookup"><span data-stu-id="cb113-142">RoamingStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb113-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cb113-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb113-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cb113-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb113-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb113-145">Requirements</span></span>



| <span data-ttu-id="cb113-146">需求</span><span class="sxs-lookup"><span data-stu-id="cb113-146">Requirement</span></span> | <span data-ttu-id="cb113-147">值</span><span class="sxs-lookup"><span data-stu-id="cb113-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb113-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb113-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cb113-149">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb113-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb113-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb113-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cb113-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="cb113-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cb113-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="cb113-152">Namespace</span></span><br/>                | <span data-ttu-id="cb113-153">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="cb113-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cb113-154">MOF</span><span class="sxs-lookup"><span data-stu-id="cb113-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb113-155"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb113-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb113-156">DLL</span><span class="sxs-lookup"><span data-stu-id="cb113-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb113-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb113-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb113-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb113-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb113-159">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="cb113-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

