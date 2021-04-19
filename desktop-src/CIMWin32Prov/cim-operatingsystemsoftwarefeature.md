---
description: CIM \_ OperatingSystemSoftwareFeature 類別代表組成作業系統的軟體功能。
ms.assetid: 9ffc709c-213e-4252-9662-76f01e1685e5
ms.tgt_platform: multiple
title: CIM_OperatingSystemSoftwareFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystemSoftwareFeature
- CIM_OperatingSystemSoftwareFeature.PartComponent
- CIM_OperatingSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9d74478f211b23e103854cedb09a1e0186618b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972561"
---
# <a name="cim_operatingsystemsoftwarefeature-class"></a><span data-ttu-id="94259-103">CIM \_ OperatingSystemSoftwareFeature 類別</span><span class="sxs-lookup"><span data-stu-id="94259-103">CIM\_OperatingSystemSoftwareFeature class</span></span>

<span data-ttu-id="94259-104">**CIM \_ OperatingSystemSoftwareFeature** 類別代表組成作業系統的軟體功能。</span><span class="sxs-lookup"><span data-stu-id="94259-104">The **CIM\_OperatingSystemSoftwareFeature** class represents the software features that make up the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94259-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="94259-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94259-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="94259-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94259-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="94259-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="94259-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="94259-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94259-109">語法</span><span class="sxs-lookup"><span data-stu-id="94259-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{96B4C734-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OperatingSystemSoftwareFeature : CIM_Component
{
  CIM_SoftwareFeature REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="94259-110">成員</span><span class="sxs-lookup"><span data-stu-id="94259-110">Members</span></span>

<span data-ttu-id="94259-111">**CIM \_ OperatingSystemSoftwareFeature** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="94259-111">The **CIM\_OperatingSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="94259-112">屬性</span><span class="sxs-lookup"><span data-stu-id="94259-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94259-113">屬性</span><span class="sxs-lookup"><span data-stu-id="94259-113">Properties</span></span>

<span data-ttu-id="94259-114">**CIM \_ OperatingSystemSoftwareFeature** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="94259-114">The **CIM\_OperatingSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94259-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="94259-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94259-116">資料類型： **CIM \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="94259-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="94259-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94259-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94259-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="94259-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="94259-119">描述作業系統的 [**CIM \_ 作業系統**](cim-operatingsystem.md) 。</span><span class="sxs-lookup"><span data-stu-id="94259-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="94259-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="94259-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94259-121">資料類型： **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="94259-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="94259-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94259-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94259-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="94259-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="94259-124">[**CIM \_ SoftwareFeature**](cim-softwarefeature.md) ，描述構成作業系統的軟體功能。</span><span class="sxs-lookup"><span data-stu-id="94259-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) describing the software features that make up the operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94259-125">備註</span><span class="sxs-lookup"><span data-stu-id="94259-125">Remarks</span></span>

<span data-ttu-id="94259-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="94259-126">WMI does not implement this class.</span></span>

<span data-ttu-id="94259-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="94259-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94259-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="94259-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94259-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="94259-129">Requirements</span></span>



| <span data-ttu-id="94259-130">需求</span><span class="sxs-lookup"><span data-stu-id="94259-130">Requirement</span></span> | <span data-ttu-id="94259-131">值</span><span class="sxs-lookup"><span data-stu-id="94259-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94259-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94259-132">Minimum supported client</span></span><br/> | <span data-ttu-id="94259-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94259-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94259-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94259-134">Minimum supported server</span></span><br/> | <span data-ttu-id="94259-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94259-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94259-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="94259-136">Namespace</span></span><br/>                | <span data-ttu-id="94259-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="94259-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94259-138">MOF</span><span class="sxs-lookup"><span data-stu-id="94259-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94259-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="94259-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94259-140">DLL</span><span class="sxs-lookup"><span data-stu-id="94259-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94259-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94259-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94259-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94259-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94259-143">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="94259-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

