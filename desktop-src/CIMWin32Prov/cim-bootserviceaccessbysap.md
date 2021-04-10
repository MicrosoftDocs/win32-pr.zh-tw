---
description: CIM \_ BootServiceAccessBySAP 類別會將開機服務及其存取點產生關聯。
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: CIM_BootServiceAccessBySAP 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90548be52defbcf3419d6c7defc21395da5cfbfe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688987"
---
# <a name="cim_bootserviceaccessbysap-class"></a><span data-ttu-id="2840c-103">CIM \_ BootServiceAccessBySAP 類別</span><span class="sxs-lookup"><span data-stu-id="2840c-103">CIM\_BootServiceAccessBySAP class</span></span>

<span data-ttu-id="2840c-104">**CIM \_ BootServiceAccessBySAP** 類別會將開機服務及其存取點產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2840c-104">The **CIM\_BootServiceAccessBySAP** class associates a boot service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2840c-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2840c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2840c-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2840c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2840c-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2840c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2840c-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2840c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2840c-109">語法</span><span class="sxs-lookup"><span data-stu-id="2840c-109">Syntax</span></span>

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2840c-110">成員</span><span class="sxs-lookup"><span data-stu-id="2840c-110">Members</span></span>

<span data-ttu-id="2840c-111">**CIM \_ BootServiceAccessBySAP** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2840c-111">The **CIM\_BootServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="2840c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="2840c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2840c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2840c-113">Properties</span></span>

<span data-ttu-id="2840c-114">**CIM \_ BootServiceAccessBySAP** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2840c-114">The **CIM\_BootServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2840c-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="2840c-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2840c-116">資料類型： **CIM \_ BootService**</span><span class="sxs-lookup"><span data-stu-id="2840c-116">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="2840c-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2840c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2840c-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="2840c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2840c-119">描述開機服務的 [**CIM \_ BootService**](cim-bootservice.md) 。</span><span class="sxs-lookup"><span data-stu-id="2840c-119">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service.</span></span>

</dd> <dt>

<span data-ttu-id="2840c-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="2840c-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2840c-121">資料類型： **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="2840c-121">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="2840c-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2840c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2840c-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="2840c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2840c-124">描述開機服務存取點的 [**CIM \_ BootSAP**](cim-bootsap.md) 。</span><span class="sxs-lookup"><span data-stu-id="2840c-124">A [**CIM\_BootSAP**](cim-bootsap.md) that describes an access point for the boot service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2840c-125">備註</span><span class="sxs-lookup"><span data-stu-id="2840c-125">Remarks</span></span>

<span data-ttu-id="2840c-126">**Cim \_ BootServiceAccessBySAP** 類別衍生自 [**cim \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md)。</span><span class="sxs-lookup"><span data-stu-id="2840c-126">The **CIM\_BootServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="2840c-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="2840c-127">WMI does not implement this class.</span></span>

<span data-ttu-id="2840c-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2840c-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2840c-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2840c-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2840c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2840c-130">Requirements</span></span>



| <span data-ttu-id="2840c-131">需求</span><span class="sxs-lookup"><span data-stu-id="2840c-131">Requirement</span></span> | <span data-ttu-id="2840c-132">值</span><span class="sxs-lookup"><span data-stu-id="2840c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2840c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2840c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2840c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2840c-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2840c-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2840c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2840c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2840c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2840c-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="2840c-137">Namespace</span></span><br/>                | <span data-ttu-id="2840c-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2840c-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2840c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2840c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2840c-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2840c-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2840c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2840c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2840c-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2840c-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2840c-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2840c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2840c-144">**CIM \_ ServiceAccessBySAP**</span><span class="sxs-lookup"><span data-stu-id="2840c-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

