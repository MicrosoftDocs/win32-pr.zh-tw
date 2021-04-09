---
description: CIM \_ HostedAccessPoint 類別代表服務存取點 (SAP) 和提供它的系統之間的關聯。 每個系統可能會裝載許多 Sap。
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: 'CIM_HostedAccessPoint 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110857"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="fecaa-104">CIM_HostedAccessPoint 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="fecaa-104">CIM_HostedAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="fecaa-105">**CIM \_ HostedAccessPoint** 類別代表服務存取點 (SAP) 和提供它的系統之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="fecaa-105">The **CIM\_HostedAccessPoint** class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="fecaa-106">每個系統可能會裝載許多 Sap。</span><span class="sxs-lookup"><span data-stu-id="fecaa-106">Each system may host many SAPs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fecaa-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="fecaa-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fecaa-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="fecaa-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fecaa-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fecaa-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fecaa-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="fecaa-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fecaa-111">語法</span><span class="sxs-lookup"><span data-stu-id="fecaa-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fecaa-112">成員</span><span class="sxs-lookup"><span data-stu-id="fecaa-112">Members</span></span>

<span data-ttu-id="fecaa-113">**CIM \_ HostedAccessPoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fecaa-113">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="fecaa-114">屬性</span><span class="sxs-lookup"><span data-stu-id="fecaa-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fecaa-115">屬性</span><span class="sxs-lookup"><span data-stu-id="fecaa-115">Properties</span></span>

<span data-ttu-id="fecaa-116">**CIM \_ HostedAccessPoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fecaa-116">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fecaa-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="fecaa-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fecaa-118">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="fecaa-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="fecaa-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fecaa-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fecaa-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="fecaa-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="fecaa-121">描述裝載系統的 [**CIM \_ 系統**](cim-system.md) 。</span><span class="sxs-lookup"><span data-stu-id="fecaa-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="fecaa-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="fecaa-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fecaa-123">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="fecaa-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="fecaa-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fecaa-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fecaa-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="fecaa-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fecaa-126">[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ，描述此系統上裝載的 SAP (s) 。</span><span class="sxs-lookup"><span data-stu-id="fecaa-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes The SAP(s) that are hosted on this system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fecaa-127">備註</span><span class="sxs-lookup"><span data-stu-id="fecaa-127">Remarks</span></span>

<span data-ttu-id="fecaa-128">**CIM \_HostedAccessPoint** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="fecaa-128">**CIM\_HostedAccessPoint** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fecaa-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="fecaa-129">WMI does not implement this class.</span></span>

<span data-ttu-id="fecaa-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="fecaa-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fecaa-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fecaa-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fecaa-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="fecaa-132">Requirements</span></span>



| <span data-ttu-id="fecaa-133">需求</span><span class="sxs-lookup"><span data-stu-id="fecaa-133">Requirement</span></span> | <span data-ttu-id="fecaa-134">值</span><span class="sxs-lookup"><span data-stu-id="fecaa-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fecaa-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fecaa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fecaa-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fecaa-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fecaa-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fecaa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fecaa-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fecaa-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fecaa-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="fecaa-139">Namespace</span></span><br/>                | <span data-ttu-id="fecaa-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fecaa-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fecaa-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fecaa-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fecaa-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fecaa-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fecaa-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fecaa-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fecaa-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fecaa-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fecaa-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fecaa-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fecaa-146">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="fecaa-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

