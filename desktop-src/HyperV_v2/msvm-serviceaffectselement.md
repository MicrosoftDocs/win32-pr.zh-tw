---
description: 將虛擬機器實例與控制其狀態的管理服務產生關聯。
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Msvm_ServiceAffectsElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113884"
---
# <a name="msvm_serviceaffectselement-class"></a><span data-ttu-id="123ee-103">Msvm \_ ServiceAffectsElement 類別</span><span class="sxs-lookup"><span data-stu-id="123ee-103">Msvm\_ServiceAffectsElement class</span></span>

<span data-ttu-id="123ee-104">將虛擬機器實例與控制其狀態的管理服務產生關聯。</span><span class="sxs-lookup"><span data-stu-id="123ee-104">Associates a virtual machine instance with the management service that controls its state.</span></span>

<span data-ttu-id="123ee-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="123ee-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="123ee-106">語法</span><span class="sxs-lookup"><span data-stu-id="123ee-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="123ee-107">成員</span><span class="sxs-lookup"><span data-stu-id="123ee-107">Members</span></span>

<span data-ttu-id="123ee-108">**Msvm \_ ServiceAffectsElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="123ee-108">The **Msvm\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="123ee-109">屬性</span><span class="sxs-lookup"><span data-stu-id="123ee-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="123ee-110">屬性</span><span class="sxs-lookup"><span data-stu-id="123ee-110">Properties</span></span>

<span data-ttu-id="123ee-111">**Msvm \_ ServiceAffectsElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="123ee-111">The **Msvm\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="123ee-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="123ee-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123ee-113">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="123ee-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="123ee-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="123ee-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123ee-115">虛擬機器的參考。</span><span class="sxs-lookup"><span data-stu-id="123ee-115">A reference to the virtual machine.</span></span> <span data-ttu-id="123ee-116">這個屬性繼承自 [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="123ee-116">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="123ee-117">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="123ee-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123ee-118">資料類型： **[ **CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="123ee-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="123ee-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="123ee-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123ee-120">控制虛擬機器的服務參考。</span><span class="sxs-lookup"><span data-stu-id="123ee-120">A reference to the service that controls the virtual machine.</span></span> <span data-ttu-id="123ee-121">這個屬性繼承自 [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="123ee-121">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="123ee-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="123ee-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123ee-123">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="123ee-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="123ee-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="123ee-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123ee-125">指定關聯表示的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="123ee-125">Specifies the type of control that the association represents.</span></span> <span data-ttu-id="123ee-126">這個屬性繼承自 [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))，而且一律設定為下列值。</span><span class="sxs-lookup"><span data-stu-id="123ee-126">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to the following value.</span></span>



| <span data-ttu-id="123ee-127">值</span><span class="sxs-lookup"><span data-stu-id="123ee-127">Value</span></span>                                                                        | <span data-ttu-id="123ee-128">意義</span><span class="sxs-lookup"><span data-stu-id="123ee-128">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="123ee-129"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="123ee-129"><dt>5</dt></span></span> </dl> | <span data-ttu-id="123ee-130">管理</span><span class="sxs-lookup"><span data-stu-id="123ee-130">Manages</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="123ee-131">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="123ee-131">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123ee-132">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="123ee-132">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="123ee-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="123ee-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123ee-134">**ElementAffects** 屬性陣列中對應陣列位置的關聯類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="123ee-134">The details for the type of association at the corresponding array position in the **ElementAffects** property array.</span></span> <span data-ttu-id="123ee-135">如果 **ElementAffects** 設定為 1 (其他) ，則需要這項資訊。</span><span class="sxs-lookup"><span data-stu-id="123ee-135">This information is required if **ElementAffects** is set to 1 (Other).</span></span> <span data-ttu-id="123ee-136">這個屬性繼承自 [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="123ee-136">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="123ee-137">備註</span><span class="sxs-lookup"><span data-stu-id="123ee-137">Remarks</span></span>

<span data-ttu-id="123ee-138">存取 **Msvm \_ ServiceAffectsElement** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="123ee-138">Access to the **Msvm\_ServiceAffectsElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="123ee-139">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="123ee-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="123ee-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="123ee-140">Requirements</span></span>



| <span data-ttu-id="123ee-141">需求</span><span class="sxs-lookup"><span data-stu-id="123ee-141">Requirement</span></span> | <span data-ttu-id="123ee-142">值</span><span class="sxs-lookup"><span data-stu-id="123ee-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="123ee-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="123ee-143">Minimum supported client</span></span><br/> | <span data-ttu-id="123ee-144">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="123ee-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="123ee-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="123ee-145">Minimum supported server</span></span><br/> | <span data-ttu-id="123ee-146">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="123ee-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="123ee-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="123ee-147">Namespace</span></span><br/>                | <span data-ttu-id="123ee-148">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="123ee-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="123ee-149">MOF</span><span class="sxs-lookup"><span data-stu-id="123ee-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="123ee-150"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="123ee-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="123ee-151">DLL</span><span class="sxs-lookup"><span data-stu-id="123ee-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="123ee-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="123ee-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="123ee-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="123ee-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123ee-154">**CIM \_ ServiceAffectsElement**</span><span class="sxs-lookup"><span data-stu-id="123ee-154">**CIM\_ServiceAffectsElement**</span></span>](cim-serviceaffectselement.md)
</dt> <dt>

<span data-ttu-id="123ee-155">[**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="123ee-155">[**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))</span></span>
</dt> </dl>

 

