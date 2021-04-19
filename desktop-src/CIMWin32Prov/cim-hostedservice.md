---
description: CIM \_ HostedService 類別代表服務與功能所在系統之間的關聯。
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: 'CIM_HostedService 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999835"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a><span data-ttu-id="55e70-103">CIM_HostedService 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="55e70-103">CIM_HostedService class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="55e70-104">**CIM \_ HostedService** 類別代表服務與功能所在系統之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="55e70-104">The **CIM\_HostedService** class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="55e70-105">系統可能會裝載許多服務，而這些服務會延後到裝載系統。</span><span class="sxs-lookup"><span data-stu-id="55e70-105">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="55e70-106">此模型不代表跨多個系統裝載的服務。</span><span class="sxs-lookup"><span data-stu-id="55e70-106">The model does not represent services hosted across multiple systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55e70-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="55e70-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55e70-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="55e70-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55e70-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="55e70-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="55e70-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="55e70-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e70-111">語法</span><span class="sxs-lookup"><span data-stu-id="55e70-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="55e70-112">成員</span><span class="sxs-lookup"><span data-stu-id="55e70-112">Members</span></span>

<span data-ttu-id="55e70-113">**CIM \_ HostedService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="55e70-113">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="55e70-114">屬性</span><span class="sxs-lookup"><span data-stu-id="55e70-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55e70-115">屬性</span><span class="sxs-lookup"><span data-stu-id="55e70-115">Properties</span></span>

<span data-ttu-id="55e70-116">**CIM \_ HostedService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="55e70-116">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55e70-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="55e70-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55e70-118">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="55e70-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="55e70-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55e70-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55e70-120">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="55e70-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="55e70-121">描述裝載系統的 [**CIM \_ 系統**](cim-system.md) 。</span><span class="sxs-lookup"><span data-stu-id="55e70-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="55e70-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="55e70-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55e70-123">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="55e70-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="55e70-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55e70-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55e70-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="55e70-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="55e70-126">[**CIM \_ 服務**](cim-service.md)，描述系統上裝載的服務。</span><span class="sxs-lookup"><span data-stu-id="55e70-126">A [**CIM\_Service**](cim-service.md) that describes the service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55e70-127">備註</span><span class="sxs-lookup"><span data-stu-id="55e70-127">Remarks</span></span>

<span data-ttu-id="55e70-128">**CIM \_HostedService** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="55e70-128">**CIM\_HostedService** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="55e70-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="55e70-129">WMI does not implement this class.</span></span>

<span data-ttu-id="55e70-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="55e70-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55e70-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="55e70-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e70-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="55e70-132">Requirements</span></span>



| <span data-ttu-id="55e70-133">需求</span><span class="sxs-lookup"><span data-stu-id="55e70-133">Requirement</span></span> | <span data-ttu-id="55e70-134">值</span><span class="sxs-lookup"><span data-stu-id="55e70-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55e70-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55e70-135">Minimum supported client</span></span><br/> | <span data-ttu-id="55e70-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55e70-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55e70-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55e70-137">Minimum supported server</span></span><br/> | <span data-ttu-id="55e70-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55e70-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55e70-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="55e70-139">Namespace</span></span><br/>                | <span data-ttu-id="55e70-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55e70-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55e70-141">MOF</span><span class="sxs-lookup"><span data-stu-id="55e70-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55e70-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="55e70-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55e70-143">DLL</span><span class="sxs-lookup"><span data-stu-id="55e70-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55e70-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55e70-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e70-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55e70-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e70-146">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="55e70-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

