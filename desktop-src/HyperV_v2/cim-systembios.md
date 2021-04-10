---
description: 將 BIOS 與電腦系統產生關聯。
ms.assetid: a06af789-75c8-4d58-8a25-572dcf1091e2
title: CIM_SystemBIOS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemBIOS
- CIM_SystemBIOS.GroupComponent
- CIM_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: faa3130544fdb97bdf216fa266bc9e8cfe1815bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026563"
---
# <a name="cim_systembios-class"></a><span data-ttu-id="06522-103">CIM \_ SystemBIOS 類別</span><span class="sxs-lookup"><span data-stu-id="06522-103">CIM\_SystemBIOS class</span></span>

<span data-ttu-id="06522-104">將 BIOS 與電腦系統產生關聯。</span><span class="sxs-lookup"><span data-stu-id="06522-104">Associates a BIOS with a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="06522-105">語法</span><span class="sxs-lookup"><span data-stu-id="06522-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_SystemBIOS : CIM_SystemComponent
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_BIOSElement    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="06522-106">成員</span><span class="sxs-lookup"><span data-stu-id="06522-106">Members</span></span>

<span data-ttu-id="06522-107">**CIM \_ SystemBIOS** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06522-107">The **CIM\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="06522-108">屬性</span><span class="sxs-lookup"><span data-stu-id="06522-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06522-109">屬性</span><span class="sxs-lookup"><span data-stu-id="06522-109">Properties</span></span>

<span data-ttu-id="06522-110">**CIM \_ SystemBIOS** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06522-110">The **CIM\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06522-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="06522-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06522-112">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="06522-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="06522-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06522-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06522-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="06522-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="06522-115">從 BIOS 開機的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="06522-115">The computer system that boots from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="06522-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="06522-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06522-117">資料類型： **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="06522-117">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="06522-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06522-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06522-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="06522-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="06522-120">BIOS。</span><span class="sxs-lookup"><span data-stu-id="06522-120">The BIOS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06522-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="06522-121">Requirements</span></span>



| <span data-ttu-id="06522-122">需求</span><span class="sxs-lookup"><span data-stu-id="06522-122">Requirement</span></span> | <span data-ttu-id="06522-123">值</span><span class="sxs-lookup"><span data-stu-id="06522-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06522-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06522-124">Minimum supported client</span></span><br/> | <span data-ttu-id="06522-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06522-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="06522-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06522-126">Minimum supported server</span></span><br/> | <span data-ttu-id="06522-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06522-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="06522-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="06522-128">Namespace</span></span><br/>                | <span data-ttu-id="06522-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="06522-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="06522-130">MOF</span><span class="sxs-lookup"><span data-stu-id="06522-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06522-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="06522-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06522-132">DLL</span><span class="sxs-lookup"><span data-stu-id="06522-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06522-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06522-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06522-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06522-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06522-135">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="06522-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

