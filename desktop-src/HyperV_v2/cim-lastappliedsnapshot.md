---
description: 代表電腦系統與其最近套用的虛擬系統快照之間的關聯。
ms.assetid: 722491a3-1c46-4d37-8bd6-7c7d6648a806
title: CIM_LastAppliedSnapshot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSnapshot
- CIM_LastAppliedSnapshot.Antecedent
- CIM_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 38efa9c5f02cd0ea40d993cc39ba05ac0b6fde3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977114"
---
# <a name="cim_lastappliedsnapshot-class"></a><span data-ttu-id="51642-103">CIM \_ LastAppliedSnapshot 類別</span><span class="sxs-lookup"><span data-stu-id="51642-103">CIM\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="51642-104">代表電腦系統與其最近套用的虛擬系統快照之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="51642-104">Represents an association between a computer system and its most recently applied virtual system snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="51642-105">語法</span><span class="sxs-lookup"><span data-stu-id="51642-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_LastAppliedSnapshot : CIM_Dependency
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="51642-106">成員</span><span class="sxs-lookup"><span data-stu-id="51642-106">Members</span></span>

<span data-ttu-id="51642-107">**CIM \_ LastAppliedSnapshot** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="51642-107">The **CIM\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="51642-108">屬性</span><span class="sxs-lookup"><span data-stu-id="51642-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51642-109">屬性</span><span class="sxs-lookup"><span data-stu-id="51642-109">Properties</span></span>

<span data-ttu-id="51642-110">**CIM \_ LastAppliedSnapshot** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="51642-110">The **CIM\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51642-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="51642-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51642-112">資料類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="51642-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="51642-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="51642-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51642-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="51642-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="51642-115">上次套用至電腦系統的虛擬系統快照。</span><span class="sxs-lookup"><span data-stu-id="51642-115">The virtual system snapshot that was last applied to the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="51642-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="51642-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51642-117">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="51642-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="51642-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="51642-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51642-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="51642-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="51642-120">電腦系統。</span><span class="sxs-lookup"><span data-stu-id="51642-120">The computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51642-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="51642-121">Requirements</span></span>



| <span data-ttu-id="51642-122">需求</span><span class="sxs-lookup"><span data-stu-id="51642-122">Requirement</span></span> | <span data-ttu-id="51642-123">值</span><span class="sxs-lookup"><span data-stu-id="51642-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51642-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51642-124">Minimum supported client</span></span><br/> | <span data-ttu-id="51642-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="51642-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="51642-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51642-126">Minimum supported server</span></span><br/> | <span data-ttu-id="51642-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51642-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="51642-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="51642-128">Namespace</span></span><br/>                | <span data-ttu-id="51642-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="51642-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="51642-130">MOF</span><span class="sxs-lookup"><span data-stu-id="51642-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51642-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="51642-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51642-132">DLL</span><span class="sxs-lookup"><span data-stu-id="51642-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51642-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51642-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51642-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51642-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51642-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="51642-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

