---
description: 代表服務與服務存取點之間的關聯， (可為服務提供功能的 SAP) 。
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: 'CIM_ServiceSAPDependency 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980349"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a><span data-ttu-id="87446-103">CIM_ServiceSAPDependency 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="87446-103">CIM_ServiceSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="87446-104">代表服務與服務存取點之間的關聯， (可為服務提供功能的 SAP) 。</span><span class="sxs-lookup"><span data-stu-id="87446-104">Represents an association between a service and a service access point (SAP) that provides the service with functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="87446-105">語法</span><span class="sxs-lookup"><span data-stu-id="87446-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="87446-106">成員</span><span class="sxs-lookup"><span data-stu-id="87446-106">Members</span></span>

<span data-ttu-id="87446-107">**CIM \_ ServiceSAPDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="87446-107">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="87446-108">屬性</span><span class="sxs-lookup"><span data-stu-id="87446-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87446-109">屬性</span><span class="sxs-lookup"><span data-stu-id="87446-109">Properties</span></span>

<span data-ttu-id="87446-110">**CIM \_ ServiceSAPDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="87446-110">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87446-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="87446-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87446-112">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="87446-112">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="87446-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87446-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87446-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="87446-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="87446-115">必要的服務存取點。</span><span class="sxs-lookup"><span data-stu-id="87446-115">The required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="87446-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="87446-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87446-117">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="87446-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="87446-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87446-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87446-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="87446-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="87446-120">相依于 SAP 的服務。</span><span class="sxs-lookup"><span data-stu-id="87446-120">The service that is dependent on the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87446-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="87446-121">Requirements</span></span>



| <span data-ttu-id="87446-122">需求</span><span class="sxs-lookup"><span data-stu-id="87446-122">Requirement</span></span> | <span data-ttu-id="87446-123">值</span><span class="sxs-lookup"><span data-stu-id="87446-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87446-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87446-124">Minimum supported client</span></span><br/> | <span data-ttu-id="87446-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="87446-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="87446-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87446-126">Minimum supported server</span></span><br/> | <span data-ttu-id="87446-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="87446-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="87446-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="87446-128">Namespace</span></span><br/>                | <span data-ttu-id="87446-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="87446-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="87446-130">MOF</span><span class="sxs-lookup"><span data-stu-id="87446-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87446-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="87446-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87446-132">DLL</span><span class="sxs-lookup"><span data-stu-id="87446-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87446-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87446-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87446-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87446-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87446-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="87446-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

