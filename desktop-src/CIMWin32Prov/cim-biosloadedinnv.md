---
description: CIM \_ BIOSLoadedInNV 類別會將 BIOS 元素和載入它的非暫時性儲存區產生關聯。
ms.assetid: 11641616-e11d-49ff-bfe4-f95fe27f00b8
ms.tgt_platform: multiple
title: CIM_BIOSLoadedInNV 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSLoadedInNV
- CIM_BIOSLoadedInNV.Dependent
- CIM_BIOSLoadedInNV.Antecedent
- CIM_BIOSLoadedInNV.EndingAddress
- CIM_BIOSLoadedInNV.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de07e1d4b886ad14f6a7fd8dbb96c1c0f2d2079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936367"
---
# <a name="cim_biosloadedinnv-class"></a><span data-ttu-id="06abb-103">CIM \_ BIOSLoadedInNV 類別</span><span class="sxs-lookup"><span data-stu-id="06abb-103">CIM\_BIOSLoadedInNV class</span></span>

<span data-ttu-id="06abb-104">**CIM \_ BIOSLoadedInNV** 類別會將 BIOS 元素和載入它的非暫時性儲存區產生關聯。</span><span class="sxs-lookup"><span data-stu-id="06abb-104">The **CIM\_BIOSLoadedInNV** class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06abb-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="06abb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06abb-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="06abb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06abb-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="06abb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="06abb-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="06abb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06abb-109">語法</span><span class="sxs-lookup"><span data-stu-id="06abb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{524ED194-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BIOSLoadedInNV : CIM_Dependency
{
  CIM_BIOSElement        REF Dependent;
  CIM_NonVolatileStorage REF Antecedent;
  uint64                     EndingAddress;
  uint64                     StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="06abb-110">成員</span><span class="sxs-lookup"><span data-stu-id="06abb-110">Members</span></span>

<span data-ttu-id="06abb-111">**CIM \_ BIOSLoadedInNV** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06abb-111">The **CIM\_BIOSLoadedInNV** class has these types of members:</span></span>

-   [<span data-ttu-id="06abb-112">屬性</span><span class="sxs-lookup"><span data-stu-id="06abb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06abb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="06abb-113">Properties</span></span>

<span data-ttu-id="06abb-114">**CIM \_ BIOSLoadedInNV** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06abb-114">The **CIM\_BIOSLoadedInNV** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06abb-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="06abb-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06abb-116">資料類型： **CIM \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="06abb-116">Data type: **CIM\_NonVolatileStorage**</span></span>
</dt> <dt>

<span data-ttu-id="06abb-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06abb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06abb-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="06abb-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="06abb-119">描述非暫時性儲存的 [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) 。</span><span class="sxs-lookup"><span data-stu-id="06abb-119">A [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) that describes the non-volatile storage.</span></span>

</dd> <dt>

<span data-ttu-id="06abb-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="06abb-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06abb-121">資料類型： **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="06abb-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="06abb-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06abb-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06abb-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="06abb-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="06abb-124">[**CIM \_ BIOSElement**](cim-bioselement.md) ，描述儲存在非暫時性範圍中的 BIOS。</span><span class="sxs-lookup"><span data-stu-id="06abb-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS stored in the non-volatile extent.</span></span>

</dd> <dt>

<span data-ttu-id="06abb-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="06abb-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06abb-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06abb-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06abb-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06abb-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06abb-128">在非暫時性的儲存體中，BIOS 所在的結束位址。</span><span class="sxs-lookup"><span data-stu-id="06abb-128">Ending address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="06abb-129">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="06abb-129">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="06abb-130">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="06abb-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06abb-131">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06abb-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06abb-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06abb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06abb-133">在非暫時性的儲存體中，起始 BIOS 所在的起始位址。</span><span class="sxs-lookup"><span data-stu-id="06abb-133">Starting address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="06abb-134">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="06abb-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06abb-135">備註</span><span class="sxs-lookup"><span data-stu-id="06abb-135">Remarks</span></span>

<span data-ttu-id="06abb-136">**Cim \_ BIOSLoadedInNV** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="06abb-136">The **CIM\_BIOSLoadedInNV** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="06abb-137">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="06abb-137">WMI does not implement this class.</span></span>

<span data-ttu-id="06abb-138">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="06abb-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06abb-139">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="06abb-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06abb-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="06abb-140">Requirements</span></span>



| <span data-ttu-id="06abb-141">需求</span><span class="sxs-lookup"><span data-stu-id="06abb-141">Requirement</span></span> | <span data-ttu-id="06abb-142">值</span><span class="sxs-lookup"><span data-stu-id="06abb-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06abb-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06abb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="06abb-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06abb-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06abb-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06abb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="06abb-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06abb-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06abb-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="06abb-147">Namespace</span></span><br/>                | <span data-ttu-id="06abb-148">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="06abb-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06abb-149">MOF</span><span class="sxs-lookup"><span data-stu-id="06abb-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06abb-150"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="06abb-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06abb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="06abb-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06abb-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06abb-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06abb-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06abb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06abb-154">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="06abb-154">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

