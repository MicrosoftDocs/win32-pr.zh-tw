---
description: CIM \_ ServiceSAPDependency 類別代表服務與服務存取點之間的關聯 (SAP) ，這表示服務會使用參考的 SAP 來提供其功能。
ms.assetid: cf5a8b9b-a38e-4173-861c-e417fbea6016
ms.tgt_platform: multiple
title: 'CIM_ServiceSAPDependency 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Dependent
- CIM_ServiceSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e47283c962b377b70bc14efe998752d9009796df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110609"
---
# <a name="cim_servicesapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="0a39a-103">CIM_ServiceSAPDependency 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="0a39a-103">CIM_ServiceSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0a39a-104">**CIM \_ ServiceSAPDependency** 類別代表服務與服務存取點之間的關聯 (SAP) ，這表示服務會使用參考的 SAP 來提供其功能。</span><span class="sxs-lookup"><span data-stu-id="0a39a-104">The **CIM\_ServiceSAPDependency** class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span> <span data-ttu-id="0a39a-105">例如，開機服務可以叫用 BIOS 磁片服務 (中斷) 運作。</span><span class="sxs-lookup"><span data-stu-id="0a39a-105">For example, boot services can invoke BIOS disk services (interrupts) to function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a39a-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0a39a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0a39a-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0a39a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0a39a-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0a39a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0a39a-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0a39a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a39a-110">語法</span><span class="sxs-lookup"><span data-stu-id="0a39a-110">Syntax</span></span>

``` syntax
[UUID("{652E2D58-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_Service            REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0a39a-111">成員</span><span class="sxs-lookup"><span data-stu-id="0a39a-111">Members</span></span>

<span data-ttu-id="0a39a-112">**CIM \_ ServiceSAPDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0a39a-112">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="0a39a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0a39a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a39a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0a39a-114">Properties</span></span>

<span data-ttu-id="0a39a-115">**CIM \_ ServiceSAPDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0a39a-115">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a39a-116">**先行**</span><span class="sxs-lookup"><span data-stu-id="0a39a-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a39a-117">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="0a39a-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="0a39a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a39a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a39a-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="0a39a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0a39a-120">描述必要服務存取點的 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) 。</span><span class="sxs-lookup"><span data-stu-id="0a39a-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="0a39a-121">**依賴**</span><span class="sxs-lookup"><span data-stu-id="0a39a-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a39a-122">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="0a39a-122">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="0a39a-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a39a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a39a-124">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="0a39a-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0a39a-125">[**CIM \_ 服務**](cim-service.md)，描述相依于基礎 SAP 的服務。</span><span class="sxs-lookup"><span data-stu-id="0a39a-125">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a39a-126">備註</span><span class="sxs-lookup"><span data-stu-id="0a39a-126">Remarks</span></span>

<span data-ttu-id="0a39a-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0a39a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="0a39a-128">**Cim \_ ServiceSAPDependency** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="0a39a-128">The **CIM\_ServiceSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0a39a-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0a39a-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0a39a-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0a39a-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a39a-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a39a-131">Requirements</span></span>



| <span data-ttu-id="0a39a-132">需求</span><span class="sxs-lookup"><span data-stu-id="0a39a-132">Requirement</span></span> | <span data-ttu-id="0a39a-133">值</span><span class="sxs-lookup"><span data-stu-id="0a39a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a39a-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a39a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0a39a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a39a-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a39a-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a39a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0a39a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a39a-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a39a-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="0a39a-138">Namespace</span></span><br/>                | <span data-ttu-id="0a39a-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0a39a-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a39a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0a39a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a39a-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a39a-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a39a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0a39a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a39a-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a39a-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a39a-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a39a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a39a-145">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="0a39a-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

