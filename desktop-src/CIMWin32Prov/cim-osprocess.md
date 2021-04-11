---
description: CIM \_ OSProcess 類別會將作業系統以及在作業系統環境中執行的一或多個處理常式產生關聯。
ms.assetid: 59d52b29-9d97-464f-bbbc-4191305df8c7
ms.tgt_platform: multiple
title: CIM_OSProcess 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSProcess
- CIM_OSProcess.PartComponent
- CIM_OSProcess.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b11738669c87b402f12932ad65237a512360427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847107"
---
# <a name="cim_osprocess-class"></a><span data-ttu-id="354a8-103">CIM \_ OSProcess 類別</span><span class="sxs-lookup"><span data-stu-id="354a8-103">CIM\_OSProcess class</span></span>

<span data-ttu-id="354a8-104">**CIM \_ OSProcess** 類別會將作業系統以及在作業系統環境中執行的一或多個處理常式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="354a8-104">The **CIM\_OSProcess** class associates the operating system and one or more processes running in the context of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="354a8-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="354a8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="354a8-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="354a8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="354a8-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="354a8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="354a8-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="354a8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="354a8-109">語法</span><span class="sxs-lookup"><span data-stu-id="354a8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A361A7AE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OSProcess : CIM_Component
{
  CIM_Process         REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="354a8-110">成員</span><span class="sxs-lookup"><span data-stu-id="354a8-110">Members</span></span>

<span data-ttu-id="354a8-111">**CIM \_ OSProcess** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="354a8-111">The **CIM\_OSProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="354a8-112">屬性</span><span class="sxs-lookup"><span data-stu-id="354a8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="354a8-113">屬性</span><span class="sxs-lookup"><span data-stu-id="354a8-113">Properties</span></span>

<span data-ttu-id="354a8-114">**CIM \_ OSProcess** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="354a8-114">The **CIM\_OSProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="354a8-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="354a8-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="354a8-116">資料類型： **CIM \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="354a8-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="354a8-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="354a8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="354a8-118">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="354a8-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="354a8-119">描述作業系統的 [**CIM \_ 作業系統**](cim-operatingsystem.md) 。</span><span class="sxs-lookup"><span data-stu-id="354a8-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="354a8-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="354a8-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="354a8-121">資料類型： **CIM \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="354a8-121">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="354a8-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="354a8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="354a8-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="354a8-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="354a8-124">[**CIM \_ 進程**](cim-process.md)，描述在作業系統內容中執行的進程</span><span class="sxs-lookup"><span data-stu-id="354a8-124">A [**CIM\_Process**](cim-process.md) describing the process running in the context of the operating system</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="354a8-125">備註</span><span class="sxs-lookup"><span data-stu-id="354a8-125">Remarks</span></span>

<span data-ttu-id="354a8-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="354a8-126">WMI does not implement this class.</span></span>

<span data-ttu-id="354a8-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="354a8-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="354a8-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="354a8-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="354a8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="354a8-129">Requirements</span></span>



| <span data-ttu-id="354a8-130">需求</span><span class="sxs-lookup"><span data-stu-id="354a8-130">Requirement</span></span> | <span data-ttu-id="354a8-131">值</span><span class="sxs-lookup"><span data-stu-id="354a8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="354a8-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="354a8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="354a8-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="354a8-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="354a8-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="354a8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="354a8-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="354a8-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="354a8-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="354a8-136">Namespace</span></span><br/>                | <span data-ttu-id="354a8-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="354a8-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="354a8-138">MOF</span><span class="sxs-lookup"><span data-stu-id="354a8-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="354a8-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="354a8-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="354a8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="354a8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="354a8-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="354a8-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="354a8-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="354a8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354a8-143">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="354a8-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

