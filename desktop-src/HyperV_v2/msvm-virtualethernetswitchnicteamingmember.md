---
description: 表示小組 ExternalEthernetPort 與成員 ExternalEthernetPort 之間的關聯。
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Msvm_VirtualEthernetSwitchNicTeamingMember 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbf83f4605d6ab1b7bc9740b14c493393eb93163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195600"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a><span data-ttu-id="b78b5-103">Msvm \_ VirtualEthernetSwitchNicTeamingMember 類別</span><span class="sxs-lookup"><span data-stu-id="b78b5-103">Msvm\_VirtualEthernetSwitchNicTeamingMember class</span></span>

<span data-ttu-id="b78b5-104">表示小組 ExternalEthernetPort 與成員 ExternalEthernetPort 之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="b78b5-104">Represents the association between a team ExternalEthernetPort and a member ExternalEthernetPort.</span></span>

<span data-ttu-id="b78b5-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b78b5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b78b5-106">語法</span><span class="sxs-lookup"><span data-stu-id="b78b5-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b78b5-107">成員</span><span class="sxs-lookup"><span data-stu-id="b78b5-107">Members</span></span>

<span data-ttu-id="b78b5-108">**Msvm \_ VirtualEthernetSwitchNicTeamingMember** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b78b5-108">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these types of members:</span></span>

-   [<span data-ttu-id="b78b5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b78b5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b78b5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b78b5-110">Properties</span></span>

<span data-ttu-id="b78b5-111">**Msvm \_ VirtualEthernetSwitchNicTeamingMember** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b78b5-111">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b78b5-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="b78b5-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78b5-113">資料類型： **Msvm \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="b78b5-113">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="b78b5-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b78b5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78b5-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="b78b5-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b78b5-116">參考小組外部乙太網路埠實例的 [**Msvm \_ ExternalEthernetPort**](msvm-externalethernetport.md) 。</span><span class="sxs-lookup"><span data-stu-id="b78b5-116">An [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) that references the team external ethernet port instance.</span></span>

</dd> <dt>

<span data-ttu-id="b78b5-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="b78b5-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b78b5-118">資料類型： **Msvm \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="b78b5-118">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="b78b5-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b78b5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b78b5-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="b78b5-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b78b5-121">成員 [**Msvm \_ ExternalEthernetPort**](msvm-externalethernetport.md) 實例的參考。</span><span class="sxs-lookup"><span data-stu-id="b78b5-121">Reference to the member [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b78b5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b78b5-122">Requirements</span></span>



| <span data-ttu-id="b78b5-123">需求</span><span class="sxs-lookup"><span data-stu-id="b78b5-123">Requirement</span></span> | <span data-ttu-id="b78b5-124">值</span><span class="sxs-lookup"><span data-stu-id="b78b5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b78b5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b78b5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b78b5-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b78b5-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b78b5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b78b5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b78b5-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b78b5-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b78b5-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="b78b5-129">Namespace</span></span><br/>                | <span data-ttu-id="b78b5-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b78b5-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b78b5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b78b5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b78b5-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b78b5-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b78b5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b78b5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b78b5-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b78b5-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b78b5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b78b5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78b5-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="b78b5-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

