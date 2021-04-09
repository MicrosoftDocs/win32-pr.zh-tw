---
description: CIM \_ ResidesOnExtent 類別代表檔案系統與其所在儲存區之間的關聯。 一般而言，檔案系統位於邏輯磁片上。
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: CIM_ResidesOnExtent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 526023fbcc1c961ecaca068be8b0d4ce3e2f84f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111536"
---
# <a name="cim_residesonextent-class"></a><span data-ttu-id="198a9-104">CIM \_ ResidesOnExtent 類別</span><span class="sxs-lookup"><span data-stu-id="198a9-104">CIM\_ResidesOnExtent class</span></span>

<span data-ttu-id="198a9-105">**CIM \_ ResidesOnExtent** 類別代表檔案系統與其所在儲存區之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="198a9-105">The **CIM\_ResidesOnExtent** class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="198a9-106">一般而言，檔案系統位於邏輯磁片上。</span><span class="sxs-lookup"><span data-stu-id="198a9-106">Typically, a file system resides on a logical disk.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="198a9-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="198a9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="198a9-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="198a9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="198a9-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="198a9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="198a9-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="198a9-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="198a9-111">語法</span><span class="sxs-lookup"><span data-stu-id="198a9-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="198a9-112">成員</span><span class="sxs-lookup"><span data-stu-id="198a9-112">Members</span></span>

<span data-ttu-id="198a9-113">**CIM \_ ResidesOnExtent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="198a9-113">The **CIM\_ResidesOnExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="198a9-114">屬性</span><span class="sxs-lookup"><span data-stu-id="198a9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="198a9-115">屬性</span><span class="sxs-lookup"><span data-stu-id="198a9-115">Properties</span></span>

<span data-ttu-id="198a9-116">**CIM \_ ResidesOnExtent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="198a9-116">The **CIM\_ResidesOnExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="198a9-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="198a9-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="198a9-118">資料類型： **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="198a9-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="198a9-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="198a9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="198a9-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="198a9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="198a9-121">描述儲存區的 [**CIM \_ StorageExtent**](cim-storageextent.md) 。</span><span class="sxs-lookup"><span data-stu-id="198a9-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="198a9-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="198a9-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="198a9-123">資料類型： **CIM \_ 檔案系統**</span><span class="sxs-lookup"><span data-stu-id="198a9-123">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="198a9-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="198a9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="198a9-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="198a9-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="198a9-126">[**CIM 檔 \_ 系統**](cim-filesystem.md)，描述位於儲存區的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="198a9-126">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system that is located on the storage extent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="198a9-127">備註</span><span class="sxs-lookup"><span data-stu-id="198a9-127">Remarks</span></span>

<span data-ttu-id="198a9-128">**Cim \_ ResidesOnExtent** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="198a9-128">The **CIM\_ResidesOnExtent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="198a9-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="198a9-129">WMI does not implement this class.</span></span>

<span data-ttu-id="198a9-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="198a9-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="198a9-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="198a9-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="198a9-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="198a9-132">Requirements</span></span>



| <span data-ttu-id="198a9-133">需求</span><span class="sxs-lookup"><span data-stu-id="198a9-133">Requirement</span></span> | <span data-ttu-id="198a9-134">值</span><span class="sxs-lookup"><span data-stu-id="198a9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="198a9-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="198a9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="198a9-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="198a9-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="198a9-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="198a9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="198a9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="198a9-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="198a9-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="198a9-139">Namespace</span></span><br/>                | <span data-ttu-id="198a9-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="198a9-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="198a9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="198a9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="198a9-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="198a9-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="198a9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="198a9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="198a9-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="198a9-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="198a9-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="198a9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198a9-146">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="198a9-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

