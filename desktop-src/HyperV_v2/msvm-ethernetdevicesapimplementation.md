---
description: 代表服務存取點與執行它的邏輯裝置之間的關聯。
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Msvm_EthernetDeviceSAPImplementation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 96290eb0d572f4848fbf3805a44ce0ae173892c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319291"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a><span data-ttu-id="4f955-103">Msvm \_ EthernetDeviceSAPImplementation 類別</span><span class="sxs-lookup"><span data-stu-id="4f955-103">Msvm\_EthernetDeviceSAPImplementation class</span></span>

<span data-ttu-id="4f955-104">代表服務存取點與執行它的邏輯裝置之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4f955-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="4f955-105">此關聯的基數為多對多。</span><span class="sxs-lookup"><span data-stu-id="4f955-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="4f955-106"> (SAP) 的服務存取點可由一個以上的邏輯裝置提供，同時運作。</span><span class="sxs-lookup"><span data-stu-id="4f955-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="4f955-107">任何裝置都可以提供一個以上的 SAP。</span><span class="sxs-lookup"><span data-stu-id="4f955-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="4f955-108">當有許多邏輯裝置與單一 SAP 相關聯時，會假設這些專案會一起運作以提供存取點。</span><span class="sxs-lookup"><span data-stu-id="4f955-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="4f955-109">如果有不同的 SAP 執行，則每個執行都會導致 SAP 物件的個別具現化。</span><span class="sxs-lookup"><span data-stu-id="4f955-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="4f955-110">這些個別的具現化會與唯一的實作為關聯。</span><span class="sxs-lookup"><span data-stu-id="4f955-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="4f955-111">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4f955-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f955-112">語法</span><span class="sxs-lookup"><span data-stu-id="4f955-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4f955-113">成員</span><span class="sxs-lookup"><span data-stu-id="4f955-113">Members</span></span>

<span data-ttu-id="4f955-114">**Msvm \_ EthernetDeviceSAPImplementation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4f955-114">The **Msvm\_EthernetDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="4f955-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4f955-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f955-116">屬性</span><span class="sxs-lookup"><span data-stu-id="4f955-116">Properties</span></span>

<span data-ttu-id="4f955-117">**Msvm \_ EthernetDeviceSAPImplementation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4f955-117">The **Msvm\_EthernetDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f955-118">**先行**</span><span class="sxs-lookup"><span data-stu-id="4f955-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f955-119">資料類型： **[ **CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span><span class="sxs-lookup"><span data-stu-id="4f955-119">Data type: **[**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span></span>
</dt> <dt>

<span data-ttu-id="4f955-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f955-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f955-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="4f955-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4f955-122">衍生自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) （代表邏輯裝置）之類別的參考。</span><span class="sxs-lookup"><span data-stu-id="4f955-122">A reference to a class derived from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="4f955-123">**依賴**</span><span class="sxs-lookup"><span data-stu-id="4f955-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f955-124">資料類型： **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="4f955-124">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4f955-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f955-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f955-126">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="4f955-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4f955-127">[**Msvm \_ LANEndpoint**](msvm-lanendpoint.md)類別實例的參考，該類別代表 **使用中的 SAP。**</span><span class="sxs-lookup"><span data-stu-id="4f955-127">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f955-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f955-128">Requirements</span></span>



| <span data-ttu-id="4f955-129">需求</span><span class="sxs-lookup"><span data-stu-id="4f955-129">Requirement</span></span> | <span data-ttu-id="4f955-130">值</span><span class="sxs-lookup"><span data-stu-id="4f955-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f955-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f955-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4f955-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f955-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4f955-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f955-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4f955-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f955-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f955-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="4f955-135">Namespace</span></span><br/>                | <span data-ttu-id="4f955-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4f955-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4f955-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4f955-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f955-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4f955-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f955-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4f955-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f955-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f955-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

