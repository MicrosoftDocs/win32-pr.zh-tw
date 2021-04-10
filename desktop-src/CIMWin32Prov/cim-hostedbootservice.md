---
description: CIM \_ HostedBootService 類別會將主機系統和開機服務產生關聯。 由於此關聯性是從 CIM HostedService 子類別化 \_ ，因此它會繼承為服務定義的範圍/命名配置，其中服務會延遲至其主機系統。
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: CIM_HostedBootService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12baa364653feda1400ad15d658e6739859b2521
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110853"
---
# <a name="cim_hostedbootservice-class"></a><span data-ttu-id="52f3f-104">CIM \_ HostedBootService 類別</span><span class="sxs-lookup"><span data-stu-id="52f3f-104">CIM\_HostedBootService class</span></span>

<span data-ttu-id="52f3f-105">**CIM \_ HostedBootService** 類別會將主機系統和開機服務產生關聯。</span><span class="sxs-lookup"><span data-stu-id="52f3f-105">The **CIM\_HostedBootService** class associates a hosting system and a boot service.</span></span> <span data-ttu-id="52f3f-106">由於此關聯性是從 [**CIM \_ HostedService**](cim-hostedservice.md)子類別化，因此它會繼承為服務定義的範圍/命名配置，其中服務會延遲至其主機系統。</span><span class="sxs-lookup"><span data-stu-id="52f3f-106">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52f3f-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="52f3f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="52f3f-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="52f3f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="52f3f-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="52f3f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="52f3f-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="52f3f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f3f-111">語法</span><span class="sxs-lookup"><span data-stu-id="52f3f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="52f3f-112">成員</span><span class="sxs-lookup"><span data-stu-id="52f3f-112">Members</span></span>

<span data-ttu-id="52f3f-113">**CIM \_ HostedBootService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="52f3f-113">The **CIM\_HostedBootService** class has these types of members:</span></span>

-   [<span data-ttu-id="52f3f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="52f3f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52f3f-115">屬性</span><span class="sxs-lookup"><span data-stu-id="52f3f-115">Properties</span></span>

<span data-ttu-id="52f3f-116">**CIM \_ HostedBootService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="52f3f-116">The **CIM\_HostedBootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52f3f-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="52f3f-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f3f-118">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="52f3f-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="52f3f-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="52f3f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f3f-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (前) </span><span class="sxs-lookup"><span data-stu-id="52f3f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="52f3f-121">描述裝載系統的 [**CIM \_ 系統**](cim-system.md) 。</span><span class="sxs-lookup"><span data-stu-id="52f3f-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="52f3f-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="52f3f-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f3f-123">資料類型： **CIM \_ BootService**</span><span class="sxs-lookup"><span data-stu-id="52f3f-123">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="52f3f-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="52f3f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f3f-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="52f3f-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="52f3f-126">[**CIM \_ BootService**](cim-bootservice.md) ，描述系統上裝載的開機服務。</span><span class="sxs-lookup"><span data-stu-id="52f3f-126">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52f3f-127">備註</span><span class="sxs-lookup"><span data-stu-id="52f3f-127">Remarks</span></span>

<span data-ttu-id="52f3f-128">**Cim \_ HostedBootService** 類別衍生自 [**cim \_ HostedService**](cim-hostedservice.md)。</span><span class="sxs-lookup"><span data-stu-id="52f3f-128">The **CIM\_HostedBootService** class is derived from [**CIM\_HostedService**](cim-hostedservice.md).</span></span>

<span data-ttu-id="52f3f-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="52f3f-129">WMI does not implement this class.</span></span>

<span data-ttu-id="52f3f-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="52f3f-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="52f3f-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="52f3f-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f3f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="52f3f-132">Requirements</span></span>



| <span data-ttu-id="52f3f-133">需求</span><span class="sxs-lookup"><span data-stu-id="52f3f-133">Requirement</span></span> | <span data-ttu-id="52f3f-134">值</span><span class="sxs-lookup"><span data-stu-id="52f3f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52f3f-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52f3f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="52f3f-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52f3f-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52f3f-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52f3f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="52f3f-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52f3f-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52f3f-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="52f3f-139">Namespace</span></span><br/>                | <span data-ttu-id="52f3f-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="52f3f-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="52f3f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="52f3f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52f3f-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="52f3f-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="52f3f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="52f3f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52f3f-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52f3f-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f3f-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52f3f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f3f-146">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="52f3f-146">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> </dl>

 

