---
description: CIM \_ ServiceAccessBySAP 關聯類別代表服務的存取點。 例如，您可以透過 NetWare、Macintosh 或 Windows 服務存取點來存取印表機 (Sap) ，這些都可能裝載在不同的系統上。
ms.assetid: 68311a56-b034-4a30-a885-74a745a738d8
ms.tgt_platform: multiple
title: CIM_ServiceAccessBySAP 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessBySAP
- CIM_ServiceAccessBySAP.Dependent
- CIM_ServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e34b2af50a6475461ae4d39d156d26143fcb75f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936250"
---
# <a name="cim_serviceaccessbysap-class"></a><span data-ttu-id="8d929-104">CIM \_ ServiceAccessBySAP 類別</span><span class="sxs-lookup"><span data-stu-id="8d929-104">CIM\_ServiceAccessBySAP class</span></span>

<span data-ttu-id="8d929-105">**CIM \_ ServiceAccessBySAP** 關聯類別代表服務的存取點。</span><span class="sxs-lookup"><span data-stu-id="8d929-105">The **CIM\_ServiceAccessBySAP** association class represents the access points for a service.</span></span> <span data-ttu-id="8d929-106">例如，您可以透過 NetWare、Macintosh 或 Windows 服務存取點來存取印表機 (Sap) ，這些都可能裝載在不同的系統上。</span><span class="sxs-lookup"><span data-stu-id="8d929-106">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d929-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8d929-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d929-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8d929-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8d929-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8d929-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8d929-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8d929-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d929-111">語法</span><span class="sxs-lookup"><span data-stu-id="8d929-111">Syntax</span></span>

``` syntax
[UUID("{714C00BA-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessBySAP : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_Service            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8d929-112">成員</span><span class="sxs-lookup"><span data-stu-id="8d929-112">Members</span></span>

<span data-ttu-id="8d929-113">**CIM \_ ServiceAccessBySAP** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8d929-113">The **CIM\_ServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="8d929-114">屬性</span><span class="sxs-lookup"><span data-stu-id="8d929-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d929-115">屬性</span><span class="sxs-lookup"><span data-stu-id="8d929-115">Properties</span></span>

<span data-ttu-id="8d929-116">**CIM \_ ServiceAccessBySAP** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8d929-116">The **CIM\_ServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d929-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="8d929-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d929-118">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="8d929-118">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="8d929-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d929-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d929-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="8d929-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8d929-121">描述服務的 [**CIM \_ 服務**](cim-service.md) 。</span><span class="sxs-lookup"><span data-stu-id="8d929-121">A [**CIM\_Service**](cim-service.md) that describes the service.</span></span>

</dd> <dt>

<span data-ttu-id="8d929-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="8d929-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d929-123">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="8d929-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="8d929-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d929-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d929-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="8d929-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8d929-126">描述服務存取點的 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) 。</span><span class="sxs-lookup"><span data-stu-id="8d929-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes an access point for a service.</span></span> <span data-ttu-id="8d929-127">存取點相依于此關聯性，因為它們沒有沒有對應服務的函數。</span><span class="sxs-lookup"><span data-stu-id="8d929-127">Access points are dependent in this relationship since they have no function without a corresponding service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d929-128">備註</span><span class="sxs-lookup"><span data-stu-id="8d929-128">Remarks</span></span>

<span data-ttu-id="8d929-129">**Cim \_ ServiceAccessBySAP** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="8d929-129">The **CIM\_ServiceAccessBySAP** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8d929-130">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="8d929-130">WMI does not implement this class.</span></span> <span data-ttu-id="8d929-131">針對衍生自 **CIM \_ SERVICEACCESSBYSAP** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="8d929-131">For WMI classes that are derived from **CIM\_ServiceAccessBySAP**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8d929-132">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8d929-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d929-133">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8d929-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d929-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d929-134">Requirements</span></span>



| <span data-ttu-id="8d929-135">需求</span><span class="sxs-lookup"><span data-stu-id="8d929-135">Requirement</span></span> | <span data-ttu-id="8d929-136">值</span><span class="sxs-lookup"><span data-stu-id="8d929-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d929-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d929-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8d929-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d929-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d929-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d929-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8d929-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d929-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d929-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="8d929-141">Namespace</span></span><br/>                | <span data-ttu-id="8d929-142">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8d929-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d929-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8d929-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d929-144"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d929-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d929-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8d929-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d929-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d929-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d929-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d929-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d929-148">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="8d929-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

