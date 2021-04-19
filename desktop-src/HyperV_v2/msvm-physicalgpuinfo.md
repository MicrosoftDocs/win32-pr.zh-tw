---
description: 包含 RemoteFX 實體圖形處理器 (GPU) 的相關資訊。
ms.assetid: 86B47AAE-DBFF-43EF-88C6-44836D6C3AFA
title: Msvm_PhysicalGPUInfo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PhysicalGPUInfo
- Msvm_PhysicalGPUInfo.InstanceID
- Msvm_PhysicalGPUInfo.Caption
- Msvm_PhysicalGPUInfo.Description
- Msvm_PhysicalGPUInfo.ElementName
- Msvm_PhysicalGPUInfo.Name
- Msvm_PhysicalGPUInfo.ID
- Msvm_PhysicalGPUInfo.TotalVideoMemory
- Msvm_PhysicalGPUInfo.AvailableVideoMemory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cd4ccf65b364620e84063ea6398c59dd0e467f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997961"
---
# <a name="msvm_physicalgpuinfo-class"></a><span data-ttu-id="a0d36-103">Msvm \_ PhysicalGPUInfo 類別</span><span class="sxs-lookup"><span data-stu-id="a0d36-103">Msvm\_PhysicalGPUInfo class</span></span>

<span data-ttu-id="a0d36-104">包含 RemoteFX 實體圖形處理器 (GPU) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0d36-104">Contains information about a RemoteFX physical graphics processing unit (GPU).</span></span>

<span data-ttu-id="a0d36-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a0d36-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d36-106">語法</span><span class="sxs-lookup"><span data-stu-id="a0d36-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PhysicalGPUInfo : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  string ID;
  uint64 TotalVideoMemory;
  uint64 AvailableVideoMemory;
};
```

## <a name="members"></a><span data-ttu-id="a0d36-107">成員</span><span class="sxs-lookup"><span data-stu-id="a0d36-107">Members</span></span>

<span data-ttu-id="a0d36-108">**Msvm \_ PhysicalGPUInfo** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a0d36-108">The **Msvm\_PhysicalGPUInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="a0d36-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a0d36-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0d36-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a0d36-110">Properties</span></span>

<span data-ttu-id="a0d36-111">**Msvm \_ PhysicalGPUInfo** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a0d36-111">The **Msvm\_PhysicalGPUInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0d36-112">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="a0d36-112">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d36-113">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a0d36-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0d36-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0d36-115">可供 RemoteFX 使用的實體 GPU 上未使用的視訊記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0d36-115">The amount of unused video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="a0d36-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="a0d36-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d36-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0d36-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0d36-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0d36-119">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a0d36-119">A short description of the object.</span></span> <span data-ttu-id="a0d36-120">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a0d36-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0d36-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="a0d36-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d36-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0d36-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0d36-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0d36-124">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a0d36-124">A description of the object.</span></span> <span data-ttu-id="a0d36-125">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a0d36-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0d36-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a0d36-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d36-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0d36-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0d36-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0d36-129">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a0d36-129">A display name for the object.</span></span> <span data-ttu-id="a0d36-130">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a0d36-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0d36-131">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="a0d36-131">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d36-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0d36-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0d36-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-134">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="a0d36-134">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="a0d36-135">實體 GPU 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0d36-135">The unique identifier of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="a0d36-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a0d36-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d36-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0d36-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0d36-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-139">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="a0d36-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a0d36-140">可唯一識別這個類別之實例的字串。</span><span class="sxs-lookup"><span data-stu-id="a0d36-140">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a0d36-141">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a0d36-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0d36-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a0d36-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d36-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0d36-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0d36-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-145">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="a0d36-145">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="a0d36-146">實體 GPU 的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a0d36-146">The display name of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="a0d36-147">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="a0d36-147">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d36-148">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a0d36-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0d36-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0d36-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0d36-150">可供 RemoteFX 使用之實體 GPU 的視訊記憶體總量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0d36-150">The total amount of video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0d36-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0d36-151">Requirements</span></span>



| <span data-ttu-id="a0d36-152">需求</span><span class="sxs-lookup"><span data-stu-id="a0d36-152">Requirement</span></span> | <span data-ttu-id="a0d36-153">值</span><span class="sxs-lookup"><span data-stu-id="a0d36-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d36-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0d36-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a0d36-155">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0d36-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a0d36-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0d36-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a0d36-157">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0d36-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0d36-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="a0d36-158">Namespace</span></span><br/>                | <span data-ttu-id="a0d36-159">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a0d36-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a0d36-160">MOF</span><span class="sxs-lookup"><span data-stu-id="a0d36-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0d36-161"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a0d36-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0d36-162">DLL</span><span class="sxs-lookup"><span data-stu-id="a0d36-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0d36-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0d36-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0d36-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0d36-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d36-165">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a0d36-165">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

