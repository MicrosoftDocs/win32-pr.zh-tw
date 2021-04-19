---
description: Msvm \_ EthernetSwitchPort 類別的實例與 Msvm EthernetPortData 類別的實例之間的關聯 \_ ，代表由交換器擴充功能所收集之埠的資料。
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Msvm_EthernetPortInfo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987566"
---
# <a name="msvm_ethernetportinfo-class"></a><span data-ttu-id="04746-103">Msvm \_ EthernetPortInfo 類別</span><span class="sxs-lookup"><span data-stu-id="04746-103">Msvm\_EthernetPortInfo class</span></span>

<span data-ttu-id="04746-104">[**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)類別的實例與 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)類別的實例之間的關聯，代表由交換器擴充功能所收集之埠的資料。</span><span class="sxs-lookup"><span data-stu-id="04746-104">An association between an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class and an instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents data gathered about the port by a switch extension.</span></span>

<span data-ttu-id="04746-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="04746-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04746-106">語法</span><span class="sxs-lookup"><span data-stu-id="04746-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="04746-107">成員</span><span class="sxs-lookup"><span data-stu-id="04746-107">Members</span></span>

<span data-ttu-id="04746-108">**Msvm \_ EthernetPortInfo** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="04746-108">The **Msvm\_EthernetPortInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="04746-109">屬性</span><span class="sxs-lookup"><span data-stu-id="04746-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04746-110">屬性</span><span class="sxs-lookup"><span data-stu-id="04746-110">Properties</span></span>

<span data-ttu-id="04746-111">**Msvm \_ EthernetPortInfo** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="04746-111">The **Msvm\_EthernetPortInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04746-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="04746-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04746-113">資料類型： **Msvm \_ EthernetSwitchPort**</span><span class="sxs-lookup"><span data-stu-id="04746-113">Data type: **Msvm\_EthernetSwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="04746-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04746-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04746-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) </span><span class="sxs-lookup"><span data-stu-id="04746-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="04746-116">代表切換埠之 [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="04746-116">An instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="04746-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="04746-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04746-118">資料類型： **Msvm \_ EthernetPortData**</span><span class="sxs-lookup"><span data-stu-id="04746-118">Data type: **Msvm\_EthernetPortData**</span></span>
</dt> <dt>

<span data-ttu-id="04746-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04746-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04746-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="04746-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="04746-121">表示埠資料之 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="04746-121">An instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents the port data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04746-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="04746-122">Requirements</span></span>



| <span data-ttu-id="04746-123">需求</span><span class="sxs-lookup"><span data-stu-id="04746-123">Requirement</span></span> | <span data-ttu-id="04746-124">值</span><span class="sxs-lookup"><span data-stu-id="04746-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04746-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04746-125">Minimum supported client</span></span><br/> | <span data-ttu-id="04746-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04746-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="04746-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04746-127">Minimum supported server</span></span><br/> | <span data-ttu-id="04746-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04746-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04746-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="04746-129">Namespace</span></span><br/>                | <span data-ttu-id="04746-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="04746-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="04746-131">MOF</span><span class="sxs-lookup"><span data-stu-id="04746-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04746-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="04746-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04746-133">DLL</span><span class="sxs-lookup"><span data-stu-id="04746-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04746-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04746-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

