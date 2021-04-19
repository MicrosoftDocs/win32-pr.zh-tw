---
description: 代表父乙太網路交換器擴充功能與子乙太網路交換器擴充功能之間的關聯。
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Msvm_ParentEthernetSwitchExtension 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994536"
---
# <a name="msvm_parentethernetswitchextension-class"></a><span data-ttu-id="552d1-103">Msvm \_ ParentEthernetSwitchExtension 類別</span><span class="sxs-lookup"><span data-stu-id="552d1-103">Msvm\_ParentEthernetSwitchExtension class</span></span>

<span data-ttu-id="552d1-104">代表父乙太網路交換器擴充功能與子乙太網路交換器擴充功能之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="552d1-104">Represents the association between a parent Ethernet switch extension and a child Ethernet switch extension.</span></span>

<span data-ttu-id="552d1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="552d1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="552d1-106">語法</span><span class="sxs-lookup"><span data-stu-id="552d1-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="552d1-107">成員</span><span class="sxs-lookup"><span data-stu-id="552d1-107">Members</span></span>

<span data-ttu-id="552d1-108">**Msvm \_ ParentEthernetSwitchExtension** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="552d1-108">The **Msvm\_ParentEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="552d1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="552d1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="552d1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="552d1-110">Properties</span></span>

<span data-ttu-id="552d1-111">**Msvm \_ ParentEthernetSwitchExtension** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="552d1-111">The **Msvm\_ParentEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="552d1-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="552d1-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="552d1-113">資料類型： **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="552d1-113">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="552d1-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="552d1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="552d1-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="552d1-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="552d1-116">代表父 switch 擴充的 [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="552d1-116">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the parent switch extension.</span></span>

</dd> <dt>

<span data-ttu-id="552d1-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="552d1-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="552d1-118">資料類型： **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="552d1-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="552d1-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="552d1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="552d1-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="552d1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="552d1-121">代表子 switch 擴充的 [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) 類別之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="552d1-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the child switch extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="552d1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="552d1-122">Requirements</span></span>



| <span data-ttu-id="552d1-123">需求</span><span class="sxs-lookup"><span data-stu-id="552d1-123">Requirement</span></span> | <span data-ttu-id="552d1-124">值</span><span class="sxs-lookup"><span data-stu-id="552d1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552d1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="552d1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="552d1-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="552d1-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="552d1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="552d1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="552d1-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="552d1-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="552d1-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="552d1-129">Namespace</span></span><br/>                | <span data-ttu-id="552d1-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="552d1-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="552d1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="552d1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="552d1-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="552d1-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="552d1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="552d1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="552d1-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="552d1-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

