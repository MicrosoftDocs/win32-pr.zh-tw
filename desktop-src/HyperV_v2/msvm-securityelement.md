---
description: 代表 CIM 的執行時間安全性設定 \_ 。
ms.assetid: fa4448dc-9353-475f-ac9b-5c50f36360d8
title: Msvm_SecurityElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityElement
- Msvm_SecurityElement.SystemCreationClassName
- Msvm_SecurityElement.SystemName
- Msvm_SecurityElement.CreationClassName
- Msvm_SecurityElement.Shielded
- Msvm_SecurityElement.EncryptStateAndVmMigrationTrafficEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f0de0fe1a515db0e7b1d8d49b96b61500703480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945505"
---
# <a name="msvm_securityelement-class"></a><span data-ttu-id="fdb00-103">Msvm \_ SecurityElement 類別</span><span class="sxs-lookup"><span data-stu-id="fdb00-103">Msvm\_SecurityElement class</span></span>

<span data-ttu-id="fdb00-104">代表 [**CIM \_**](cim-computersystem.md)的執行時間安全性設定。</span><span class="sxs-lookup"><span data-stu-id="fdb00-104">Represents the runtime security settings of a [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="fdb00-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fdb00-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb00-106">語法</span><span class="sxs-lookup"><span data-stu-id="fdb00-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityElement : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  boolean Shielded;
  boolean EncryptStateAndVmMigrationTrafficEnabled;
};
```

## <a name="members"></a><span data-ttu-id="fdb00-107">成員</span><span class="sxs-lookup"><span data-stu-id="fdb00-107">Members</span></span>

<span data-ttu-id="fdb00-108">**Msvm \_ SecurityElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fdb00-108">The **Msvm\_SecurityElement** class has these types of members:</span></span>

-   [<span data-ttu-id="fdb00-109">屬性</span><span class="sxs-lookup"><span data-stu-id="fdb00-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fdb00-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fdb00-110">Properties</span></span>

<span data-ttu-id="fdb00-111">**Msvm \_ SecurityElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fdb00-111">The **Msvm\_SecurityElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fdb00-112">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fdb00-112">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb00-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fdb00-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb00-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdb00-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb00-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="fdb00-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fdb00-116">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb00-116">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="fdb00-117">搭配這個類別的其他重要屬性使用時， **CreationClassName** 允許唯一識別此類別和其子類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="fdb00-117">When used with the other key properties of this class, **CreationClassName** allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="fdb00-118">**EncryptStateAndVmMigrationTrafficEnabled**</span><span class="sxs-lookup"><span data-stu-id="fdb00-118">**EncryptStateAndVmMigrationTrafficEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb00-119">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fdb00-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fdb00-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdb00-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb00-121">指出 VM 目前的狀態和遷移流量是否已加密。</span><span class="sxs-lookup"><span data-stu-id="fdb00-121">Indicates whether the VM is currently having its state and migration traffic encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="fdb00-122">**受防護**</span><span class="sxs-lookup"><span data-stu-id="fdb00-122">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb00-123">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fdb00-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fdb00-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdb00-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb00-125">指出 VM 目前是否受防護。</span><span class="sxs-lookup"><span data-stu-id="fdb00-125">Indicates whether the VM is currently shielded.</span></span>

</dd> <dt>

<span data-ttu-id="fdb00-126">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fdb00-126">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb00-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fdb00-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb00-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdb00-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb00-129">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="fdb00-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="fdb00-130">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb00-130">The creation class name of the scoping system.</span></span>

</dd> <dt>

<span data-ttu-id="fdb00-131">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fdb00-131">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb00-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fdb00-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb00-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fdb00-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb00-134">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**名稱**") </span><span class="sxs-lookup"><span data-stu-id="fdb00-134">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="fdb00-135">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb00-135">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fdb00-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdb00-136">Requirements</span></span>



| <span data-ttu-id="fdb00-137">需求</span><span class="sxs-lookup"><span data-stu-id="fdb00-137">Requirement</span></span> | <span data-ttu-id="fdb00-138">值</span><span class="sxs-lookup"><span data-stu-id="fdb00-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb00-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdb00-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fdb00-140">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdb00-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fdb00-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdb00-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fdb00-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fdb00-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fdb00-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="fdb00-143">Namespace</span></span><br/>                | <span data-ttu-id="fdb00-144">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="fdb00-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fdb00-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fdb00-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdb00-146"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fdb00-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdb00-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fdb00-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdb00-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fdb00-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fdb00-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdb00-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb00-150">**CIM \_ EnabledLogicalElement**</span><span class="sxs-lookup"><span data-stu-id="fdb00-150">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

