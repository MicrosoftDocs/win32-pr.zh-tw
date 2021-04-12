---
description: 代表服務存取點 (SAP) 和裝載它的系統之間的關聯。
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: 'CIM_HostedAccessPoint 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0684c2855e7966a0c01d1d9f9bfa0cbd71c2397a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468692"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a><span data-ttu-id="9a522-103">CIM_HostedAccessPoint 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="9a522-103">CIM_HostedAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="9a522-104">代表服務存取點 (SAP) 和裝載它的系統之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="9a522-104">Represents an association between a service access point (SAP) and the system that hosts it.</span></span> <span data-ttu-id="9a522-105">系統可以裝載多個存取點。</span><span class="sxs-lookup"><span data-stu-id="9a522-105">A system can host multiple access points.</span></span> <span data-ttu-id="9a522-106">若 SAP 的執行模型化，則必須由裝載 SAP 之系統一部分的裝置或軟體功能來執行。</span><span class="sxs-lookup"><span data-stu-id="9a522-106">If the implementation of the SAP is modeled, it must be implemented by a device or software feature that is part of the system that hosts the SAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a522-107">語法</span><span class="sxs-lookup"><span data-stu-id="9a522-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9a522-108">成員</span><span class="sxs-lookup"><span data-stu-id="9a522-108">Members</span></span>

<span data-ttu-id="9a522-109">**CIM \_ HostedAccessPoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9a522-109">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="9a522-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9a522-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a522-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9a522-111">Properties</span></span>

<span data-ttu-id="9a522-112">**CIM \_ HostedAccessPoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9a522-112">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a522-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="9a522-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a522-114">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="9a522-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="9a522-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a522-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a522-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="9a522-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9a522-117">裝載系統。</span><span class="sxs-lookup"><span data-stu-id="9a522-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="9a522-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="9a522-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a522-119">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="9a522-119">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="9a522-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a522-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a522-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="9a522-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9a522-122">系統上託管的 Sap。</span><span class="sxs-lookup"><span data-stu-id="9a522-122">The SAPs that are hosted on the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a522-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a522-123">Requirements</span></span>



| <span data-ttu-id="9a522-124">需求</span><span class="sxs-lookup"><span data-stu-id="9a522-124">Requirement</span></span> | <span data-ttu-id="9a522-125">值</span><span class="sxs-lookup"><span data-stu-id="9a522-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a522-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a522-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9a522-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9a522-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9a522-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a522-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9a522-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9a522-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9a522-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="9a522-130">Namespace</span></span><br/>                | <span data-ttu-id="9a522-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9a522-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9a522-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9a522-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a522-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9a522-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a522-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9a522-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a522-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9a522-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9a522-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a522-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a522-137">**CIM \_ HostedDependency**</span><span class="sxs-lookup"><span data-stu-id="9a522-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

