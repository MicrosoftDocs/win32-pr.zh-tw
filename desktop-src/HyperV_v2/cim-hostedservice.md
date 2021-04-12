---
description: 代表服務與裝載服務之系統之間的關聯。 系統可以裝載許多服務，不過這個類別並不代表跨多個系統裝載的服務。
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: 'CIM_HostedService 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 841c0e26898ed3baa4b4947779a395ee9ce870d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468689"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a><span data-ttu-id="bb1a9-104">CIM_HostedService 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="bb1a9-104">CIM_HostedService class (Hyper-V management)</span></span>

<span data-ttu-id="bb1a9-105">代表服務與裝載服務之系統之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="bb1a9-105">Represents an association between a service and the system that hosts the service.</span></span> <span data-ttu-id="bb1a9-106">系統可以裝載許多服務，不過這個類別並不代表跨多個系統裝載的服務。</span><span class="sxs-lookup"><span data-stu-id="bb1a9-106">A System can host many services, however this class does not represent services hosted across multiple systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1a9-107">語法</span><span class="sxs-lookup"><span data-stu-id="bb1a9-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bb1a9-108">成員</span><span class="sxs-lookup"><span data-stu-id="bb1a9-108">Members</span></span>

<span data-ttu-id="bb1a9-109">**CIM \_ HostedService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bb1a9-109">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="bb1a9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bb1a9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb1a9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bb1a9-111">Properties</span></span>

<span data-ttu-id="bb1a9-112">**CIM \_ HostedService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bb1a9-112">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb1a9-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="bb1a9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb1a9-114">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="bb1a9-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="bb1a9-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bb1a9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb1a9-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="bb1a9-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bb1a9-117">裝載系統。</span><span class="sxs-lookup"><span data-stu-id="bb1a9-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="bb1a9-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="bb1a9-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb1a9-119">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="bb1a9-119">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="bb1a9-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bb1a9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb1a9-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="bb1a9-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bb1a9-122">系統上託管的服務。</span><span class="sxs-lookup"><span data-stu-id="bb1a9-122">The Service hosted on the System.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb1a9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb1a9-123">Requirements</span></span>



| <span data-ttu-id="bb1a9-124">需求</span><span class="sxs-lookup"><span data-stu-id="bb1a9-124">Requirement</span></span> | <span data-ttu-id="bb1a9-125">值</span><span class="sxs-lookup"><span data-stu-id="bb1a9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1a9-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb1a9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bb1a9-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bb1a9-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bb1a9-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb1a9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bb1a9-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb1a9-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bb1a9-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="bb1a9-130">Namespace</span></span><br/>                | <span data-ttu-id="bb1a9-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="bb1a9-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bb1a9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="bb1a9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb1a9-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bb1a9-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb1a9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bb1a9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb1a9-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb1a9-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb1a9-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb1a9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb1a9-137">**CIM \_ HostedDependency**</span><span class="sxs-lookup"><span data-stu-id="bb1a9-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

