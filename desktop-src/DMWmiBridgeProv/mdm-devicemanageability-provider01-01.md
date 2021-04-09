---
title: MDM_DeviceManageability_Provider01_01 類別
description: MDM \_ DeviceManageability \_ Provider01 \_ 01 類別可用來取得裝置上 mdm 設定功能的一般資訊。
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- MDM_DeviceManageability_Provider01_01 類別
- MDM_DeviceManageability_Provider01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1ef064bcffd5303a3ef820dc0b463a3b5e622b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843968"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a><span data-ttu-id="16d3f-105">MDM \_ DeviceManageability \_ Provider01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="16d3f-105">MDM\_DeviceManageability\_Provider01\_01 class</span></span>

<span data-ttu-id="16d3f-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="16d3f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="16d3f-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="16d3f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="16d3f-108">MDM \_ DeviceManageability \_ Provider01 \_ 01 類別可用來取得裝置上 mdm 設定功能的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="16d3f-108">The MDM\_DeviceManageability\_Provider01\_01 class is used retrieve the general information about MDM configuration capabilities on the device.</span></span>

<span data-ttu-id="16d3f-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="16d3f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16d3f-110">語法</span><span class="sxs-lookup"><span data-stu-id="16d3f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a><span data-ttu-id="16d3f-111">成員</span><span class="sxs-lookup"><span data-stu-id="16d3f-111">Members</span></span>

<span data-ttu-id="16d3f-112">**MDM \_ DeviceManageability \_ Provider01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16d3f-112">The **MDM\_DeviceManageability\_Provider01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="16d3f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="16d3f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16d3f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="16d3f-114">Properties</span></span>

<span data-ttu-id="16d3f-115">**MDM \_ DeviceManageability \_ Provider01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16d3f-115">The **MDM\_DeviceManageability\_Provider01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="16d3f-116">ConfigInfo</span><span class="sxs-lookup"><span data-stu-id="16d3f-116">ConfigInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d3f-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16d3f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16d3f-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="16d3f-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="16d3f-119">您必須將值設定為 [WMI \_ Bridge \_ 伺服器]。</span><span class="sxs-lookup"><span data-stu-id="16d3f-119">You must set the value to WMI\_Bridge\_Server.</span></span> <span data-ttu-id="16d3f-120">呼叫端無法動態設定提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="16d3f-120">The caller cannot dynamically set the Provider ID.</span></span>

</dd> <dt>

[<span data-ttu-id="16d3f-121">EnrollmentInfo</span><span class="sxs-lookup"><span data-stu-id="16d3f-121">EnrollmentInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d3f-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16d3f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16d3f-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="16d3f-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16d3f-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="16d3f-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d3f-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16d3f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16d3f-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16d3f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16d3f-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16d3f-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16d3f-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="16d3f-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d3f-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16d3f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16d3f-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16d3f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16d3f-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16d3f-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16d3f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="16d3f-132">Requirements</span></span>



| <span data-ttu-id="16d3f-133">需求</span><span class="sxs-lookup"><span data-stu-id="16d3f-133">Requirement</span></span> | <span data-ttu-id="16d3f-134">值</span><span class="sxs-lookup"><span data-stu-id="16d3f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16d3f-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16d3f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="16d3f-136">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16d3f-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16d3f-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16d3f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="16d3f-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="16d3f-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="16d3f-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="16d3f-139">Namespace</span></span><br/>                | <span data-ttu-id="16d3f-140">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="16d3f-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="16d3f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="16d3f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16d3f-142"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="16d3f-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="16d3f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="16d3f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16d3f-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16d3f-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

