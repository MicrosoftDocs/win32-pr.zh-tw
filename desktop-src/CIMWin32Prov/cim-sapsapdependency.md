---
description: CIM \_ SAPSAPDependency 類別是 (sap) 的兩個服務存取點之間的關聯，這表示第一個 sap 需要第二個 sap 才能與其服務連接。
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: 'CIM_SAPSAPDependency 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b75cb397120ac2d4af041187f38f826e6b56be11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936178"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="24a7c-103">CIM_SAPSAPDependency 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="24a7c-103">CIM_SAPSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="24a7c-104">**CIM \_ SAPSAPDependency** 類別是 (sap) 的兩個服務存取點之間的關聯，這表示第一個 sap 需要第二個 sap 才能與其服務連接。</span><span class="sxs-lookup"><span data-stu-id="24a7c-104">The **CIM\_SAPSAPDependency** class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span> <span data-ttu-id="24a7c-105">例如，若要在網路印表機上列印，本機印表機存取點必須使用基礎網路相關的 Sap 或通訊協定端點來傳送列印要求。</span><span class="sxs-lookup"><span data-stu-id="24a7c-105">For example, to print on a network printer, local printer access points must use underlying network-related SAPs, or protocol endpoints, to send the print request.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24a7c-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="24a7c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="24a7c-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="24a7c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="24a7c-108">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="24a7c-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="24a7c-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="24a7c-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a7c-110">語法</span><span class="sxs-lookup"><span data-stu-id="24a7c-110">Syntax</span></span>

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="24a7c-111">成員</span><span class="sxs-lookup"><span data-stu-id="24a7c-111">Members</span></span>

<span data-ttu-id="24a7c-112">**CIM \_ SAPSAPDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="24a7c-112">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="24a7c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="24a7c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24a7c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="24a7c-114">Properties</span></span>

<span data-ttu-id="24a7c-115">**CIM \_ SAPSAPDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="24a7c-115">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24a7c-116">**先行**</span><span class="sxs-lookup"><span data-stu-id="24a7c-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a7c-117">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="24a7c-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="24a7c-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24a7c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24a7c-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="24a7c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="24a7c-120">描述必要服務存取點的 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) 。</span><span class="sxs-lookup"><span data-stu-id="24a7c-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="24a7c-121">**依賴**</span><span class="sxs-lookup"><span data-stu-id="24a7c-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a7c-122">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="24a7c-122">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="24a7c-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24a7c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24a7c-124">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="24a7c-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="24a7c-125">[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ，描述相依于基礎 SAP 的服務存取點。</span><span class="sxs-lookup"><span data-stu-id="24a7c-125">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24a7c-126">備註</span><span class="sxs-lookup"><span data-stu-id="24a7c-126">Remarks</span></span>

<span data-ttu-id="24a7c-127">**Cim \_ SAPSAPDependency** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="24a7c-127">The **CIM\_SAPSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="24a7c-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="24a7c-128">WMI does not implement this class.</span></span>

<span data-ttu-id="24a7c-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="24a7c-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="24a7c-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="24a7c-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a7c-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="24a7c-131">Requirements</span></span>



| <span data-ttu-id="24a7c-132">需求</span><span class="sxs-lookup"><span data-stu-id="24a7c-132">Requirement</span></span> | <span data-ttu-id="24a7c-133">值</span><span class="sxs-lookup"><span data-stu-id="24a7c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24a7c-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24a7c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="24a7c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24a7c-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24a7c-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24a7c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="24a7c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24a7c-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24a7c-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="24a7c-138">Namespace</span></span><br/>                | <span data-ttu-id="24a7c-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="24a7c-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24a7c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="24a7c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24a7c-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="24a7c-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24a7c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="24a7c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24a7c-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24a7c-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a7c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24a7c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a7c-145">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="24a7c-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

