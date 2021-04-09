---
description: 代表 Msvm \_ GuestServiceInterfaceComponent 實例與 Msvm GuestService 實例之間的關聯 \_ ，代表在來賓中執行的服務。
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Msvm_RegisteredGuestService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693236"
---
# <a name="msvm_registeredguestservice-class"></a><span data-ttu-id="3f694-103">Msvm \_ RegisteredGuestService 類別</span><span class="sxs-lookup"><span data-stu-id="3f694-103">Msvm\_RegisteredGuestService class</span></span>

<span data-ttu-id="3f694-104">代表 [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) 實例與 [**Msvm \_ GuestService**](msvm-guestservice.md)實例之間的關聯，代表在來賓中執行的服務。</span><span class="sxs-lookup"><span data-stu-id="3f694-104">Represents an association between an instance of [**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) and an instance of [**Msvm\_GuestService**](msvm-guestservice.md), which represents a service running in the guest.</span></span> <span data-ttu-id="3f694-105">此類別衍生自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency) 性類別。</span><span class="sxs-lookup"><span data-stu-id="3f694-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="3f694-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3f694-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f694-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f694-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3f694-108">成員</span><span class="sxs-lookup"><span data-stu-id="3f694-108">Members</span></span>

<span data-ttu-id="3f694-109">**Msvm \_ RegisteredGuestService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3f694-109">The **Msvm\_RegisteredGuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="3f694-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3f694-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f694-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3f694-111">Properties</span></span>

<span data-ttu-id="3f694-112">**Msvm \_ RegisteredGuestService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3f694-112">The **Msvm\_RegisteredGuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f694-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="3f694-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f694-114">資料類型： **[ **Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="3f694-114">Data type: **[**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3f694-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f694-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f694-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) </span><span class="sxs-lookup"><span data-stu-id="3f694-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3f694-117">此關聯中 guest 服務介面元件的參考。</span><span class="sxs-lookup"><span data-stu-id="3f694-117">Reference to the guest service interface component in this association.</span></span>

</dd> <dt>

<span data-ttu-id="3f694-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="3f694-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f694-119">資料類型： **[ **Msvm \_ GuestService**](msvm-guestservice.md)**</span><span class="sxs-lookup"><span data-stu-id="3f694-119">Data type: **[**Msvm\_GuestService**](msvm-guestservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3f694-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f694-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f694-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="3f694-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3f694-122">參考相依于 **Antecedent** 屬性的已註冊來賓服務。</span><span class="sxs-lookup"><span data-stu-id="3f694-122">Reference to the registered guest service that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f694-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f694-123">Requirements</span></span>



| <span data-ttu-id="3f694-124">需求</span><span class="sxs-lookup"><span data-stu-id="3f694-124">Requirement</span></span> | <span data-ttu-id="3f694-125">值</span><span class="sxs-lookup"><span data-stu-id="3f694-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f694-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f694-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f694-127">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f694-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3f694-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f694-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f694-129">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f694-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3f694-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="3f694-130">Namespace</span></span><br/>                | <span data-ttu-id="3f694-131">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3f694-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f694-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3f694-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f694-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3f694-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f694-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3f694-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f694-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f694-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3f694-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f694-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f694-137">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="3f694-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="3f694-138">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="3f694-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

