---
description: 此關聯會 (SAP) 來建立服務存取點，做為通訊協定端點的通訊協定服務要求者。
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Msvm_BindsToLANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945070"
---
# <a name="msvm_bindstolanendpoint-class"></a><span data-ttu-id="7dce0-103">Msvm \_ BindsToLANEndpoint 類別</span><span class="sxs-lookup"><span data-stu-id="7dce0-103">Msvm\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="7dce0-104">此關聯會 (SAP) 來建立服務存取點，做為通訊協定端點的通訊協定服務要求者。</span><span class="sxs-lookup"><span data-stu-id="7dce0-104">This association establishes a service access point (SAP) as a requester of protocol services from a protocol endpoint.</span></span> <span data-ttu-id="7dce0-105">此關聯通常會在單一系統上的 Sap 和端點之間執行。</span><span class="sxs-lookup"><span data-stu-id="7dce0-105">Typically, this association runs between SAPs and endpoints on a single system.</span></span> <span data-ttu-id="7dce0-106">因為通訊協定端點是一種 SAP，所以這個系結可用來建立兩個通訊協定的分層，其中的上層層是由 **相依** 性和較低 **層所表示。**</span><span class="sxs-lookup"><span data-stu-id="7dce0-106">Because a protocol endpoint is a kind of SAP, this binding can be used to establish a layering of two protocols, with the upper layer represented by the **Dependent** and the lower layer represented by the **Antecedent**.</span></span>

<span data-ttu-id="7dce0-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7dce0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dce0-108">語法</span><span class="sxs-lookup"><span data-stu-id="7dce0-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a><span data-ttu-id="7dce0-109">成員</span><span class="sxs-lookup"><span data-stu-id="7dce0-109">Members</span></span>

<span data-ttu-id="7dce0-110">**Msvm \_ BindsToLANEndpoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7dce0-110">The **Msvm\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="7dce0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7dce0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7dce0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7dce0-112">Properties</span></span>

<span data-ttu-id="7dce0-113">**Msvm \_ BindsToLANEndpoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7dce0-113">The **Msvm\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7dce0-114">**先行**</span><span class="sxs-lookup"><span data-stu-id="7dce0-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dce0-115">資料類型： **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="7dce0-115">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7dce0-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7dce0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7dce0-117">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="7dce0-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7dce0-118">代表切換埠之 [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) 類別的參考。</span><span class="sxs-lookup"><span data-stu-id="7dce0-118">A reference to an [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the switch port.</span></span> <span data-ttu-id="7dce0-119">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="7dce0-119">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7dce0-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="7dce0-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dce0-121">資料類型： **[ **Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="7dce0-121">Data type: **[**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7dce0-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7dce0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7dce0-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="7dce0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7dce0-124">與切換埠相關聯之 [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md) 的參考。</span><span class="sxs-lookup"><span data-stu-id="7dce0-124">A reference to the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) associated with the switch port.</span></span> <span data-ttu-id="7dce0-125">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="7dce0-125">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7dce0-126">**FrameType**</span><span class="sxs-lookup"><span data-stu-id="7dce0-126">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7dce0-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7dce0-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7dce0-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7dce0-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7dce0-129">描述系結至 LAN 端點的上層 SAP 或端點的框架方法。</span><span class="sxs-lookup"><span data-stu-id="7dce0-129">Describes the framing method for the upper layer SAP or endpoint that is bound to the LAN endpoint.</span></span> <span data-ttu-id="7dce0-130">這個屬性繼承自 **CIM \_ BindsToLANEndpoint**，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7dce0-130">This property is inherited from **CIM\_BindsToLANEndpoint**, and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dce0-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dce0-131">Requirements</span></span>



| <span data-ttu-id="7dce0-132">需求</span><span class="sxs-lookup"><span data-stu-id="7dce0-132">Requirement</span></span> | <span data-ttu-id="7dce0-133">值</span><span class="sxs-lookup"><span data-stu-id="7dce0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dce0-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7dce0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7dce0-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dce0-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7dce0-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7dce0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7dce0-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dce0-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7dce0-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="7dce0-138">Namespace</span></span><br/>                | <span data-ttu-id="7dce0-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7dce0-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7dce0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7dce0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7dce0-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7dce0-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7dce0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7dce0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dce0-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7dce0-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

