---
description: CIM \_ RunningOS 類別代表目前正在執行的作業系統。 電腦系統上的任何時間最多可以執行一個作業系統;電腦系統目前可能無法開機，或其作業系統可能不明。
ms.assetid: 93e3d425-d751-4252-aa81-7d6774c8f8c5
ms.tgt_platform: multiple
title: CIM_RunningOS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RunningOS
- CIM_RunningOS.Dependent
- CIM_RunningOS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ff86af88342a1b8f0147ecd9721765794faf39e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689152"
---
# <a name="cim_runningos-class"></a><span data-ttu-id="c7bdc-104">CIM \_ RunningOS 類別</span><span class="sxs-lookup"><span data-stu-id="c7bdc-104">CIM\_RunningOS class</span></span>

<span data-ttu-id="c7bdc-105">**CIM \_ RunningOS** 類別代表目前正在執行的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-105">The **CIM\_RunningOS** class represents the currently executing operating system.</span></span> <span data-ttu-id="c7bdc-106">電腦系統上的任何時間最多可以執行一個作業系統;電腦系統目前可能無法開機，或其作業系統可能不明。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-106">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7bdc-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c7bdc-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c7bdc-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c7bdc-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7bdc-111">語法</span><span class="sxs-lookup"><span data-stu-id="c7bdc-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1F2EA300-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RunningOS : CIM_Dependency
{
  CIM_ComputerSystem  REF Dependent;
  CIM_OperatingSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c7bdc-112">成員</span><span class="sxs-lookup"><span data-stu-id="c7bdc-112">Members</span></span>

<span data-ttu-id="c7bdc-113">**CIM \_ RunningOS** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c7bdc-113">The **CIM\_RunningOS** class has these types of members:</span></span>

-   [<span data-ttu-id="c7bdc-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c7bdc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7bdc-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c7bdc-115">Properties</span></span>

<span data-ttu-id="c7bdc-116">**CIM \_ RunningOS** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-116">The **CIM\_RunningOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7bdc-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="c7bdc-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7bdc-118">資料類型： **CIM \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="c7bdc-118">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="c7bdc-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7bdc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7bdc-120">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="c7bdc-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c7bdc-121">[**CIM 作業系統 \_**](cim-operatingsystem.md) ，描述電腦系統上目前正在執行的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-121">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system currently running on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c7bdc-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="c7bdc-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7bdc-123">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="c7bdc-123">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="c7bdc-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7bdc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7bdc-125">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="c7bdc-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c7bdc-126">描述 [**電腦 \_ 系統的 CIM**](cim-computersystem.md) 系統。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-126">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7bdc-127">備註</span><span class="sxs-lookup"><span data-stu-id="c7bdc-127">Remarks</span></span>

<span data-ttu-id="c7bdc-128">**Cim \_ RunningOS** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-128">The **CIM\_RunningOS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c7bdc-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-129">WMI does not implement this class.</span></span>

<span data-ttu-id="c7bdc-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c7bdc-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c7bdc-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7bdc-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7bdc-132">Requirements</span></span>



| <span data-ttu-id="c7bdc-133">需求</span><span class="sxs-lookup"><span data-stu-id="c7bdc-133">Requirement</span></span> | <span data-ttu-id="c7bdc-134">值</span><span class="sxs-lookup"><span data-stu-id="c7bdc-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7bdc-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7bdc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c7bdc-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7bdc-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7bdc-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7bdc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c7bdc-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7bdc-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7bdc-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7bdc-139">Namespace</span></span><br/>                | <span data-ttu-id="c7bdc-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c7bdc-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7bdc-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c7bdc-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7bdc-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7bdc-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7bdc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c7bdc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7bdc-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7bdc-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7bdc-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7bdc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7bdc-146">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="c7bdc-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

