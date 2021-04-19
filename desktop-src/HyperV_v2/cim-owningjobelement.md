---
description: 表示作業與建立作業的 managed 元素之間的關聯。
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: CIM_OwningJobElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987344"
---
# <a name="cim_owningjobelement-class"></a><span data-ttu-id="13728-103">CIM \_ OwningJobElement 類別</span><span class="sxs-lookup"><span data-stu-id="13728-103">CIM\_OwningJobElement class</span></span>

<span data-ttu-id="13728-104">表示作業與建立作業的 managed 元素之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="13728-104">Represents an association between a job and the managed element that created the job.</span></span> <span data-ttu-id="13728-105">因為作業可能會在系統之間移動，且 managed 元素可能不存在於整個作業期間，在某些情況下，這項關聯可能無法使用，或可能只存在於工作的一部分。</span><span class="sxs-lookup"><span data-stu-id="13728-105">Since a job might move between systems, and the managed element might not exist for the entire duration of the job, in some cases, this association might not be possible or might only exist for a portion of the existence of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="13728-106">語法</span><span class="sxs-lookup"><span data-stu-id="13728-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="13728-107">成員</span><span class="sxs-lookup"><span data-stu-id="13728-107">Members</span></span>

<span data-ttu-id="13728-108">**CIM \_ OwningJobElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13728-108">The **CIM\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="13728-109">屬性</span><span class="sxs-lookup"><span data-stu-id="13728-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13728-110">屬性</span><span class="sxs-lookup"><span data-stu-id="13728-110">Properties</span></span>

<span data-ttu-id="13728-111">**CIM \_ OwningJobElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="13728-111">The **CIM\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13728-112">**OwnedElement**</span><span class="sxs-lookup"><span data-stu-id="13728-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13728-113">資料類型： **CIM \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="13728-113">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="13728-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13728-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13728-115">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13728-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13728-116">Managed 元素所建立之作業的參考。</span><span class="sxs-lookup"><span data-stu-id="13728-116">A reference to the job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="13728-117">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="13728-117">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13728-118">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="13728-118">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="13728-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13728-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13728-120">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="13728-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="13728-121">建立作業之 managed 元素的參考。</span><span class="sxs-lookup"><span data-stu-id="13728-121">A reference to the managed element that created the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13728-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="13728-122">Requirements</span></span>



| <span data-ttu-id="13728-123">需求</span><span class="sxs-lookup"><span data-stu-id="13728-123">Requirement</span></span> | <span data-ttu-id="13728-124">值</span><span class="sxs-lookup"><span data-stu-id="13728-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13728-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13728-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13728-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="13728-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="13728-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13728-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13728-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13728-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="13728-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="13728-129">Namespace</span></span><br/>                | <span data-ttu-id="13728-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="13728-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13728-131">MOF</span><span class="sxs-lookup"><span data-stu-id="13728-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13728-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="13728-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13728-133">DLL</span><span class="sxs-lookup"><span data-stu-id="13728-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13728-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13728-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

