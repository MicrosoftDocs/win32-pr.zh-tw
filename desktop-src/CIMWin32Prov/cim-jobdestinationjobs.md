---
description: CIM \_ JobDestinationJobs 關聯描述提交作業以進行處理的位置， (也就是工作目的地) 。
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: CIM_JobDestinationJobs 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e59e20f776c410db53294b6f6e98a1b13aef0de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187754"
---
# <a name="cim_jobdestinationjobs-class"></a><span data-ttu-id="f4ae2-103">CIM \_ JobDestinationJobs 類別</span><span class="sxs-lookup"><span data-stu-id="f4ae2-103">CIM\_JobDestinationJobs class</span></span>

<span data-ttu-id="f4ae2-104">**CIM \_ JobDestinationJobs** 關聯描述提交作業以進行處理的位置， (也就是工作目的地) 。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-104">The **CIM\_JobDestinationJobs** association describes where a job is submitted for processing (that is, to which job destination).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4ae2-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f4ae2-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f4ae2-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f4ae2-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ae2-109">語法</span><span class="sxs-lookup"><span data-stu-id="f4ae2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f4ae2-110">成員</span><span class="sxs-lookup"><span data-stu-id="f4ae2-110">Members</span></span>

<span data-ttu-id="f4ae2-111">**CIM \_ JobDestinationJobs** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f4ae2-111">The **CIM\_JobDestinationJobs** class has these types of members:</span></span>

-   [<span data-ttu-id="f4ae2-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f4ae2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4ae2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f4ae2-113">Properties</span></span>

<span data-ttu-id="f4ae2-114">**CIM \_ JobDestinationJobs** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-114">The **CIM\_JobDestinationJobs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4ae2-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="f4ae2-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4ae2-116">資料類型： **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="f4ae2-116">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="f4ae2-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4ae2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4ae2-118">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="f4ae2-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f4ae2-119">描述作業目的地的 [**CIM \_ JobDestination**](cim-jobdestination.md) ，可能是佇列。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-119">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination, possibly a queue.</span></span>

</dd> <dt>

<span data-ttu-id="f4ae2-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="f4ae2-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4ae2-121">資料類型： **CIM \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="f4ae2-121">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="f4ae2-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4ae2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4ae2-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="f4ae2-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f4ae2-124">[**CIM \_ 作業**](cim-job.md)，描述作業佇列/目的地中的作業。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-124">A [**CIM\_Job**](cim-job.md) describing the job that is in the job queue/Destination.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4ae2-125">備註</span><span class="sxs-lookup"><span data-stu-id="f4ae2-125">Remarks</span></span>

<span data-ttu-id="f4ae2-126">**CIM \_JobDestinationJobs** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-126">**CIM\_JobDestinationJobs** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f4ae2-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-127">WMI does not implement this class.</span></span>

<span data-ttu-id="f4ae2-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f4ae2-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f4ae2-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ae2-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4ae2-130">Requirements</span></span>



| <span data-ttu-id="f4ae2-131">需求</span><span class="sxs-lookup"><span data-stu-id="f4ae2-131">Requirement</span></span> | <span data-ttu-id="f4ae2-132">值</span><span class="sxs-lookup"><span data-stu-id="f4ae2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ae2-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4ae2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ae2-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4ae2-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4ae2-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4ae2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ae2-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4ae2-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4ae2-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="f4ae2-137">Namespace</span></span><br/>                | <span data-ttu-id="f4ae2-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f4ae2-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4ae2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f4ae2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4ae2-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4ae2-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4ae2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f4ae2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4ae2-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ae2-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ae2-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4ae2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ae2-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="f4ae2-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

