---
description: CIM \_ VideoBIOSFeatureVideoBIOSElements 類別會將影片 bios 功能與其匯總的影片 bios 專案產生關聯。
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: CIM_VideoBIOSFeatureVideoBIOSElements 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110604"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a><span data-ttu-id="cd210-103">CIM \_ VideoBIOSFeatureVideoBIOSElements 類別</span><span class="sxs-lookup"><span data-stu-id="cd210-103">CIM\_VideoBIOSFeatureVideoBIOSElements class</span></span>

<span data-ttu-id="cd210-104">**CIM \_ VideoBIOSFeatureVideoBIOSElements** 類別會將影片 bios 功能與其匯總的影片 bios 專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="cd210-104">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd210-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="cd210-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cd210-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="cd210-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cd210-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cd210-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cd210-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cd210-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd210-109">語法</span><span class="sxs-lookup"><span data-stu-id="cd210-109">Syntax</span></span>

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="cd210-110">成員</span><span class="sxs-lookup"><span data-stu-id="cd210-110">Members</span></span>

<span data-ttu-id="cd210-111">**CIM \_ VideoBIOSFeatureVideoBIOSElements** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cd210-111">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="cd210-112">屬性</span><span class="sxs-lookup"><span data-stu-id="cd210-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd210-113">屬性</span><span class="sxs-lookup"><span data-stu-id="cd210-113">Properties</span></span>

<span data-ttu-id="cd210-114">**CIM \_ VideoBIOSFeatureVideoBIOSElements** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cd210-114">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd210-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cd210-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd210-116">資料類型： **CIM \_ VideoBIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="cd210-116">Data type: **CIM\_VideoBIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="cd210-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cd210-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd210-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="cd210-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cd210-119">描述影片 BIOS 功能的 [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) 。</span><span class="sxs-lookup"><span data-stu-id="cd210-119">A [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) that describes the video BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="cd210-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cd210-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd210-121">資料類型： **CIM \_ VideoBIOSElement**</span><span class="sxs-lookup"><span data-stu-id="cd210-121">Data type: **CIM\_VideoBIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="cd210-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cd210-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd210-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="cd210-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cd210-124">[**CIM \_ VideoBIOSElement**](cim-videobioselement.md) ，描述可執行影片 bios 功能所描述之功能的影片 bios 元素。</span><span class="sxs-lookup"><span data-stu-id="cd210-124">A [**CIM\_VideoBIOSElement**](cim-videobioselement.md) that describes the video BIOS element that implements the capabilities described by video BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd210-125">備註</span><span class="sxs-lookup"><span data-stu-id="cd210-125">Remarks</span></span>

<span data-ttu-id="cd210-126">**Cim \_ VideoBIOSFeatureVideoBIOSElements** 類別衍生自 [**cim \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)。</span><span class="sxs-lookup"><span data-stu-id="cd210-126">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="cd210-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="cd210-127">WMI does not implement this class.</span></span>

<span data-ttu-id="cd210-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="cd210-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cd210-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cd210-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd210-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd210-130">Requirements</span></span>



| <span data-ttu-id="cd210-131">需求</span><span class="sxs-lookup"><span data-stu-id="cd210-131">Requirement</span></span> | <span data-ttu-id="cd210-132">值</span><span class="sxs-lookup"><span data-stu-id="cd210-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd210-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd210-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cd210-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd210-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd210-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd210-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cd210-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd210-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd210-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="cd210-137">Namespace</span></span><br/>                | <span data-ttu-id="cd210-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cd210-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd210-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cd210-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd210-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd210-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd210-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cd210-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd210-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd210-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd210-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd210-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd210-144">**CIM \_ SoftwareFeatureSoftwareElements**</span><span class="sxs-lookup"><span data-stu-id="cd210-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

