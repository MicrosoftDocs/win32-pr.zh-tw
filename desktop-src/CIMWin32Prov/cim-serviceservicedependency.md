---
description: CIM \_ ServiceServiceDependency 類別代表兩個服務之間的關聯。
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: CIM_ServiceServiceDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981123"
---
# <a name="cim_serviceservicedependency-class"></a><span data-ttu-id="cd895-103">CIM \_ ServiceServiceDependency 類別</span><span class="sxs-lookup"><span data-stu-id="cd895-103">CIM\_ServiceServiceDependency class</span></span>

<span data-ttu-id="cd895-104">**CIM \_ ServiceServiceDependency** 類別代表兩個服務之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="cd895-104">The **CIM\_ServiceServiceDependency** class represents an association between two services.</span></span> <span data-ttu-id="cd895-105">相關聯的服務必須存在、必須已完成或不存在，其他服務才能運作。</span><span class="sxs-lookup"><span data-stu-id="cd895-105">The associated service must be present, must have completed, or must be absent for the other service to function.</span></span> <span data-ttu-id="cd895-106">例如，開機服務可相依于基礎 BIOS、磁片和初始化服務。</span><span class="sxs-lookup"><span data-stu-id="cd895-106">For example, boot services can be dependent on underlying BIOS, disk, and initialization services.</span></span> <span data-ttu-id="cd895-107">針對初始化服務，開機服務相依于正在完成的初始化服務。</span><span class="sxs-lookup"><span data-stu-id="cd895-107">For initialization services, the boot service is dependent on the initialization services completing.</span></span> <span data-ttu-id="cd895-108">若是磁片服務，開機服務實際上可以使用此服務的 Sap。</span><span class="sxs-lookup"><span data-stu-id="cd895-108">For disk services, boot services can actually use the SAPs of this service.</span></span> <span data-ttu-id="cd895-109">此使用相依性會在 [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) 關聯上建立模型。</span><span class="sxs-lookup"><span data-stu-id="cd895-109">This usage dependency is modeled on the [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd895-110">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="cd895-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cd895-111">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="cd895-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cd895-112">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cd895-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cd895-113">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cd895-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd895-114">語法</span><span class="sxs-lookup"><span data-stu-id="cd895-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="cd895-115">成員</span><span class="sxs-lookup"><span data-stu-id="cd895-115">Members</span></span>

<span data-ttu-id="cd895-116">**CIM \_ ServiceServiceDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cd895-116">The **CIM\_ServiceServiceDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="cd895-117">屬性</span><span class="sxs-lookup"><span data-stu-id="cd895-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd895-118">屬性</span><span class="sxs-lookup"><span data-stu-id="cd895-118">Properties</span></span>

<span data-ttu-id="cd895-119">**CIM \_ ServiceServiceDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cd895-119">The **CIM\_ServiceServiceDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd895-120">**先行**</span><span class="sxs-lookup"><span data-stu-id="cd895-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd895-121">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="cd895-121">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="cd895-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cd895-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd895-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="cd895-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cd895-124">描述所需服務的 [**CIM \_ 服務**](cim-service.md) 。</span><span class="sxs-lookup"><span data-stu-id="cd895-124">A [**CIM\_Service**](cim-service.md) that describes the required service.</span></span>

</dd> <dt>

<span data-ttu-id="cd895-125">**依賴**</span><span class="sxs-lookup"><span data-stu-id="cd895-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd895-126">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="cd895-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="cd895-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cd895-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd895-128">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="cd895-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cd895-129">[**CIM \_ 服務**](cim-service.md)，描述相依于基礎服務的服務。</span><span class="sxs-lookup"><span data-stu-id="cd895-129">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying service.</span></span>

</dd> <dt>

<span data-ttu-id="cd895-130">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="cd895-130">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd895-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cd895-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd895-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cd895-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd895-133">服務對服務相依性的本質。</span><span class="sxs-lookup"><span data-stu-id="cd895-133">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="cd895-134">這個屬性工作表示相關聯的服務必須已完成、必須啟動，或不能啟動，服務才能運作。</span><span class="sxs-lookup"><span data-stu-id="cd895-134">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd895-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="cd895-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cd895-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="cd895-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="cd895-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**服務必須已完成** (2) </span><span class="sxs-lookup"><span data-stu-id="cd895-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cd895-138">服務必須已完成。</span><span class="sxs-lookup"><span data-stu-id="cd895-138">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="cd895-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**服務必須啟動** (3) </span><span class="sxs-lookup"><span data-stu-id="cd895-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cd895-140">必須啟動服務。</span><span class="sxs-lookup"><span data-stu-id="cd895-140">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="cd895-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**服務不得啟動** (4) </span><span class="sxs-lookup"><span data-stu-id="cd895-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cd895-142">服務不得啟動。</span><span class="sxs-lookup"><span data-stu-id="cd895-142">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd895-143">備註</span><span class="sxs-lookup"><span data-stu-id="cd895-143">Remarks</span></span>

<span data-ttu-id="cd895-144">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="cd895-144">WMI does not implement this class.</span></span> <span data-ttu-id="cd895-145">針對衍生自 **CIM \_ SERVICESERVICEDEPENDENCY** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cd895-145">For WMI classes derived from **CIM\_ServiceServiceDependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cd895-146">**Cim \_ ServiceServiceDependency** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="cd895-146">The **CIM\_ServiceServiceDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="cd895-147">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="cd895-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cd895-148">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cd895-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd895-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd895-149">Requirements</span></span>



| <span data-ttu-id="cd895-150">需求</span><span class="sxs-lookup"><span data-stu-id="cd895-150">Requirement</span></span> | <span data-ttu-id="cd895-151">值</span><span class="sxs-lookup"><span data-stu-id="cd895-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd895-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd895-152">Minimum supported client</span></span><br/> | <span data-ttu-id="cd895-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd895-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd895-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd895-154">Minimum supported server</span></span><br/> | <span data-ttu-id="cd895-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd895-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd895-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="cd895-156">Namespace</span></span><br/>                | <span data-ttu-id="cd895-157">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cd895-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd895-158">MOF</span><span class="sxs-lookup"><span data-stu-id="cd895-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd895-159"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd895-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd895-160">DLL</span><span class="sxs-lookup"><span data-stu-id="cd895-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd895-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd895-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd895-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd895-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd895-163">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="cd895-163">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

