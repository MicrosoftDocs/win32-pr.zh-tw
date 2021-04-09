---
description: CIM \_ BIOSFeatureBIOSElements 類別會將 BIOS 功能和其匯總的 bios 專案產生關聯。
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: CIM_BIOSFeatureBIOSElements 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeatureBIOSElements
- CIM_BIOSFeatureBIOSElements.PartComponent
- CIM_BIOSFeatureBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a4eecea97b4d82fadcdc521d378b5b32d986b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111081"
---
# <a name="cim_biosfeaturebioselements-class"></a><span data-ttu-id="a0f7e-103">CIM \_ BIOSFeatureBIOSElements 類別</span><span class="sxs-lookup"><span data-stu-id="a0f7e-103">CIM\_BIOSFeatureBIOSElements class</span></span>

<span data-ttu-id="a0f7e-104">**CIM \_ BIOSFeatureBIOSElements** 類別會將 BIOS 功能和其匯總的 bios 專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-104">The **CIM\_BIOSFeatureBIOSElements** class associates a BIOS feature and its aggregated BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0f7e-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a0f7e-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a0f7e-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a0f7e-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f7e-109">語法</span><span class="sxs-lookup"><span data-stu-id="a0f7e-109">Syntax</span></span>

``` syntax
[UUID("{42B2EC5C-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeatureBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_BIOSElement REF PartComponent;
  CIM_BIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="a0f7e-110">成員</span><span class="sxs-lookup"><span data-stu-id="a0f7e-110">Members</span></span>

<span data-ttu-id="a0f7e-111">**CIM \_ BIOSFeatureBIOSElements** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a0f7e-111">The **CIM\_BIOSFeatureBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="a0f7e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a0f7e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0f7e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a0f7e-113">Properties</span></span>

<span data-ttu-id="a0f7e-114">**CIM \_ BIOSFeatureBIOSElements** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-114">The **CIM\_BIOSFeatureBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0f7e-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a0f7e-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0f7e-116">資料類型： **CIM \_ BIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="a0f7e-116">Data type: **CIM\_BIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="a0f7e-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0f7e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0f7e-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="a0f7e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a0f7e-119">描述 BIOS 功能的 [**CIM \_ BIOSFeature**](cim-biosfeature.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-119">A [**CIM\_BIOSFeature**](cim-biosfeature.md) that describes the BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="a0f7e-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a0f7e-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0f7e-121">資料類型： **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="a0f7e-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="a0f7e-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0f7e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0f7e-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="a0f7e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a0f7e-124">[**CIM \_ BIOSElement**](cim-bioselement.md) ，描述可執行 bios 功能所描述之功能的 bios 元素。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS element that implements the capabilities described by BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0f7e-125">備註</span><span class="sxs-lookup"><span data-stu-id="a0f7e-125">Remarks</span></span>

<span data-ttu-id="a0f7e-126">**Cim \_ BIOSFeatureBIOSElements** 類別衍生自 [**cim \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-126">The **CIM\_BIOSFeatureBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="a0f7e-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="a0f7e-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a0f7e-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a0f7e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f7e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0f7e-130">Requirements</span></span>



| <span data-ttu-id="a0f7e-131">需求</span><span class="sxs-lookup"><span data-stu-id="a0f7e-131">Requirement</span></span> | <span data-ttu-id="a0f7e-132">值</span><span class="sxs-lookup"><span data-stu-id="a0f7e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f7e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0f7e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f7e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0f7e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0f7e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0f7e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f7e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0f7e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0f7e-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="a0f7e-137">Namespace</span></span><br/>                | <span data-ttu-id="a0f7e-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a0f7e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a0f7e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a0f7e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0f7e-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0f7e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0f7e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a0f7e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0f7e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0f7e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f7e-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0f7e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f7e-144">**CIM \_ SoftwareFeatureSoftwareElements**</span><span class="sxs-lookup"><span data-stu-id="a0f7e-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

