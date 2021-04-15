---
description: 表示兩個服務存取點之間的關聯 (SAP) ，其中一個 SAP 相依于另一個可利用或與服務連接的 SAP。
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: 'CIM_SAPSAPDependency 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6888cbb74ea03b85bc9abfcea24e65660fd65953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511848"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a><span data-ttu-id="ec588-103">CIM_SAPSAPDependency 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="ec588-103">CIM_SAPSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="ec588-104">表示兩個服務存取點之間的關聯 (SAP) ，其中一個 SAP 相依于另一個可利用或與服務連接的 SAP。</span><span class="sxs-lookup"><span data-stu-id="ec588-104">Represents an association between two service access points (SAP), in which one SAP is dependant on the other to utilize or connect with a service.</span></span> <span data-ttu-id="ec588-105">例如，若要在網路印表機上列印，本機列印存取點必須利用基礎網路相關的 Sap 來傳送列印要求。</span><span class="sxs-lookup"><span data-stu-id="ec588-105">For example, to print on a network printer, local print access points must utilize underlying network-related SAPs to send the print request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec588-106">語法</span><span class="sxs-lookup"><span data-stu-id="ec588-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ec588-107">成員</span><span class="sxs-lookup"><span data-stu-id="ec588-107">Members</span></span>

<span data-ttu-id="ec588-108">**CIM \_ SAPSAPDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ec588-108">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="ec588-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ec588-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec588-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ec588-110">Properties</span></span>

<span data-ttu-id="ec588-111">**CIM \_ SAPSAPDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ec588-111">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec588-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="ec588-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-113">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="ec588-113">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec588-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec588-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="ec588-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ec588-116">必要 SAP 的參考。</span><span class="sxs-lookup"><span data-stu-id="ec588-116">A reference to the required SAP.</span></span>

</dd> <dt>

<span data-ttu-id="ec588-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="ec588-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-118">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="ec588-118">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec588-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec588-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="ec588-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ec588-121">依存 SAP 的參考。</span><span class="sxs-lookup"><span data-stu-id="ec588-121">A reference to the dependant SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec588-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec588-122">Requirements</span></span>



| <span data-ttu-id="ec588-123">需求</span><span class="sxs-lookup"><span data-stu-id="ec588-123">Requirement</span></span> | <span data-ttu-id="ec588-124">值</span><span class="sxs-lookup"><span data-stu-id="ec588-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec588-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec588-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ec588-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ec588-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ec588-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec588-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ec588-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec588-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ec588-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec588-129">Namespace</span></span><br/>                | <span data-ttu-id="ec588-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ec588-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec588-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ec588-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec588-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ec588-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec588-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ec588-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec588-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec588-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec588-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec588-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec588-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="ec588-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

