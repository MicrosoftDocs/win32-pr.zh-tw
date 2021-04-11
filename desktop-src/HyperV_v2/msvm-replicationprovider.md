---
description: 表示可用的複寫提供者。
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Msvm_ReplicationProvider 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8cc821b6bdd5d6f5d1c1085a804799c662f9d62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849492"
---
# <a name="msvm_replicationprovider-class"></a><span data-ttu-id="d697a-103">Msvm \_ ReplicationProvider 類別</span><span class="sxs-lookup"><span data-stu-id="d697a-103">Msvm\_ReplicationProvider class</span></span>

<span data-ttu-id="d697a-104">表示可用的複寫提供者。</span><span class="sxs-lookup"><span data-stu-id="d697a-104">Represents the available providers for replication.</span></span>

<span data-ttu-id="d697a-105">下列語法已從 MOF 程式碼簡化，並包含這些繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d697a-105">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d697a-106">語法</span><span class="sxs-lookup"><span data-stu-id="d697a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a><span data-ttu-id="d697a-107">成員</span><span class="sxs-lookup"><span data-stu-id="d697a-107">Members</span></span>

<span data-ttu-id="d697a-108">**Msvm \_ ReplicationProvider** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d697a-108">The **Msvm\_ReplicationProvider** class has these types of members:</span></span>

-   [<span data-ttu-id="d697a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d697a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d697a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d697a-110">Properties</span></span>

<span data-ttu-id="d697a-111">**Msvm \_ ReplicationProvider** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d697a-111">The **Msvm\_ReplicationProvider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d697a-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="d697a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d697a-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d697a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d697a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d697a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d697a-115">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="d697a-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d697a-116">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d697a-116">A short description of the object.</span></span> <span data-ttu-id="d697a-117">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d697a-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="d697a-118">對於此物件，此值為：</span><span class="sxs-lookup"><span data-stu-id="d697a-118">For this object, the value is:</span></span>

<span data-ttu-id="d697a-119">「複寫提供者」</span><span class="sxs-lookup"><span data-stu-id="d697a-119">"Replication Provider"</span></span>

</dd> <dt>

<span data-ttu-id="d697a-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="d697a-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d697a-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d697a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d697a-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d697a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d697a-123">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d697a-123">A description of the object.</span></span> <span data-ttu-id="d697a-124">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d697a-124">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="d697a-125">若為外部提供者，則會提供值。</span><span class="sxs-lookup"><span data-stu-id="d697a-125">For external providers, the value is provided by them.</span></span> <span data-ttu-id="d697a-126">主機若要裝載內建提供者，其值為：</span><span class="sxs-lookup"><span data-stu-id="d697a-126">For host to host inbuilt provider, the value is:</span></span>

<span data-ttu-id="d697a-127">「虛擬機器複寫提供者對 Hyper-v 主機」</span><span class="sxs-lookup"><span data-stu-id="d697a-127">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="d697a-128">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d697a-128">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d697a-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d697a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d697a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d697a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d697a-131">端點提供者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d697a-131">A display name for the endpoint provider.</span></span> <span data-ttu-id="d697a-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d697a-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="d697a-133">主機若要裝載內建提供者，這個屬性一律設為：</span><span class="sxs-lookup"><span data-stu-id="d697a-133">For host to host inbuilt provider, this property is always set to:</span></span>

<span data-ttu-id="d697a-134">「虛擬機器複寫提供者對 Hyper-v 主機」</span><span class="sxs-lookup"><span data-stu-id="d697a-134">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="d697a-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d697a-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d697a-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d697a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d697a-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d697a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d697a-138">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="d697a-138">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d697a-139">識別提供者的 WMI 實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="d697a-139">The WMI instance ID, which identifies the provider.</span></span> <span data-ttu-id="d697a-140">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d697a-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="d697a-141">此屬性的格式為 "Microsoft： <主機名稱>\\ ReplicationProvider \\<提供者-名稱>」。</span><span class="sxs-lookup"><span data-stu-id="d697a-141">The format of this property is "Microsoft:<host-machine-name>\\ReplicationProvider\\<provider-Name>."</span></span>

</dd> <dt>

<span data-ttu-id="d697a-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d697a-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d697a-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d697a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d697a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d697a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d697a-145">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d697a-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d697a-146">識別端點提供者的提供者 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d697a-146">The globally unique identifier (GUID) of the provider that identifies the endpoint provider.</span></span> <span data-ttu-id="d697a-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d697a-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="d697a-148">如果是外部提供者，這個屬性就是提供者 COM 類別物件的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="d697a-148">In the case of an external provider, this property is the CLSID of the provider COM class object.</span></span> <span data-ttu-id="d697a-149">主機若要裝載內建提供者，這個屬性會固定為：</span><span class="sxs-lookup"><span data-stu-id="d697a-149">For host to host inbuilt provider, this property is fixed as:</span></span>

<span data-ttu-id="d697a-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span><span class="sxs-lookup"><span data-stu-id="d697a-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span></span>

</dd> <dt>

<span data-ttu-id="d697a-151">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d697a-151">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d697a-152">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d697a-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d697a-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d697a-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d697a-154">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d697a-154">The current statuses of the object.</span></span> <span data-ttu-id="d697a-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為：</span><span class="sxs-lookup"><span data-stu-id="d697a-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to:</span></span>

<dl> <dt>

<span data-ttu-id="d697a-156"><span id="S_OK"></span><span id="s_ok"></span>**S \_確定** (2) </span><span class="sxs-lookup"><span data-stu-id="d697a-156"><span id="S_OK"></span><span id="s_ok"></span>**S\_OK** (2)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d697a-157">備註</span><span class="sxs-lookup"><span data-stu-id="d697a-157">Remarks</span></span>

<span data-ttu-id="d697a-158">您可以使用任何可用的提供者和 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別來啟用複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="d697a-158">You can use any of available providers and the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to enable a replication relationship.</span></span> <span data-ttu-id="d697a-159">Hyper-v 預設會選擇可在建立複寫時變更的內建主機至主機服務提供者。</span><span class="sxs-lookup"><span data-stu-id="d697a-159">Hyper-V by default chooses the inbuilt host to host provider, which can be changed while creating the replication.</span></span> <span data-ttu-id="d697a-160">Hyper-v 管理服務會使用 COM 與外部提供者通訊。</span><span class="sxs-lookup"><span data-stu-id="d697a-160">Hyper-V management service communicates with an external provider by using COM.</span></span>

## <a name="requirements"></a><span data-ttu-id="d697a-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="d697a-161">Requirements</span></span>



| <span data-ttu-id="d697a-162">需求</span><span class="sxs-lookup"><span data-stu-id="d697a-162">Requirement</span></span> | <span data-ttu-id="d697a-163">值</span><span class="sxs-lookup"><span data-stu-id="d697a-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d697a-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d697a-164">Minimum supported client</span></span><br/> | <span data-ttu-id="d697a-165">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d697a-165">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d697a-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d697a-166">Minimum supported server</span></span><br/> | <span data-ttu-id="d697a-167">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d697a-167">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d697a-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="d697a-168">Namespace</span></span><br/>                | <span data-ttu-id="d697a-169">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d697a-169">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d697a-170">MOF</span><span class="sxs-lookup"><span data-stu-id="d697a-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d697a-171"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d697a-171"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d697a-172">DLL</span><span class="sxs-lookup"><span data-stu-id="d697a-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d697a-173"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d697a-173"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d697a-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d697a-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d697a-175">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="d697a-175">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="d697a-176">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="d697a-176">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

