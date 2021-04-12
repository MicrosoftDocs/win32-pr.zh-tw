---
description: CIM \_ ProcessExecutable 類別代表進程和資料檔之間的連結，表示檔案參與處理常式的執行。
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: CIM_ProcessExecutable 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aedb1e79ad842e4cb04746ff47bfab142a536f43
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026012"
---
# <a name="cim_processexecutable-class"></a><span data-ttu-id="8560b-103">CIM \_ ProcessExecutable 類別</span><span class="sxs-lookup"><span data-stu-id="8560b-103">CIM\_ProcessExecutable class</span></span>

<span data-ttu-id="8560b-104">**CIM \_ ProcessExecutable** 類別代表進程和資料檔之間的連結，表示檔案參與處理常式的執行。</span><span class="sxs-lookup"><span data-stu-id="8560b-104">The **CIM\_ProcessExecutable** class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8560b-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8560b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8560b-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8560b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8560b-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8560b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8560b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8560b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8560b-109">語法</span><span class="sxs-lookup"><span data-stu-id="8560b-109">Syntax</span></span>

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a><span data-ttu-id="8560b-110">成員</span><span class="sxs-lookup"><span data-stu-id="8560b-110">Members</span></span>

<span data-ttu-id="8560b-111">**CIM \_ ProcessExecutable** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8560b-111">The **CIM\_ProcessExecutable** class has these types of members:</span></span>

-   [<span data-ttu-id="8560b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8560b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8560b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8560b-113">Properties</span></span>

<span data-ttu-id="8560b-114">**CIM \_ ProcessExecutable** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8560b-114">The **CIM\_ProcessExecutable** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8560b-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="8560b-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8560b-116">資料類型： **CIM 資料 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="8560b-116">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="8560b-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8560b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8560b-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) () ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8560b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8560b-119">[**CIM 資料 \_ 檔**](cim-datafile.md)，描述參與進程執行的資料檔。</span><span class="sxs-lookup"><span data-stu-id="8560b-119">A [**CIM\_DataFile**](cim-datafile.md) that describes the data file participating in the execution of the process.</span></span>

</dd> <dt>

<span data-ttu-id="8560b-120">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="8560b-120">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8560b-121">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8560b-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8560b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8560b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8560b-123">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="8560b-123">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8560b-124">相關聯進程的位址空間中模組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="8560b-124">Base address of the module in the address space of the associated process.</span></span>

<span data-ttu-id="8560b-125">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="8560b-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8560b-126">**依賴**</span><span class="sxs-lookup"><span data-stu-id="8560b-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8560b-127">資料類型： **CIM \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="8560b-127">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="8560b-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8560b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8560b-129">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (相依) ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8560b-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8560b-130">描述進程的 [**CIM \_ 處理**](cim-process.md) 程式。</span><span class="sxs-lookup"><span data-stu-id="8560b-130">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="8560b-131">**GlobalProcessCount**</span><span class="sxs-lookup"><span data-stu-id="8560b-131">**GlobalProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8560b-132">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8560b-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8560b-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8560b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8560b-134">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="8560b-134">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8560b-135">目前已將檔案載入記憶體中的進程數目。</span><span class="sxs-lookup"><span data-stu-id="8560b-135">Current number of processes that have the file loaded in memory.</span></span>

</dd> <dt>

<span data-ttu-id="8560b-136">**ModuleInstance**</span><span class="sxs-lookup"><span data-stu-id="8560b-136">**ModuleInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8560b-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8560b-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8560b-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8560b-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8560b-139">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="8560b-139">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8560b-140">Win32 實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="8560b-140">Win32 instance handle.</span></span> <span data-ttu-id="8560b-141">這個屬性已過時，而且沒有取代值。</span><span class="sxs-lookup"><span data-stu-id="8560b-141">This property is obsolete, and there is no replacement value.</span></span>

</dd> <dt>

<span data-ttu-id="8560b-142">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="8560b-142">**ProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8560b-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8560b-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8560b-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8560b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8560b-145">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="8560b-145">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8560b-146">相關進程中檔案的參考計數。</span><span class="sxs-lookup"><span data-stu-id="8560b-146">Reference count of the file in the associated process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8560b-147">備註</span><span class="sxs-lookup"><span data-stu-id="8560b-147">Remarks</span></span>

<span data-ttu-id="8560b-148">**Cim \_ ProcessExecutable** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="8560b-148">The **CIM\_ProcessExecutable** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8560b-149">WMI 會實行 **CIM \_ ProcessExecutable** 類別。</span><span class="sxs-lookup"><span data-stu-id="8560b-149">WMI implements the **CIM\_ProcessExecutable** class.</span></span> <span data-ttu-id="8560b-150">**CIM \_ ProcessExecutable** 類別是動態類別。</span><span class="sxs-lookup"><span data-stu-id="8560b-150">The **CIM\_ProcessExecutable** class is a dynamic class.</span></span>

<span data-ttu-id="8560b-151">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8560b-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8560b-152">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8560b-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8560b-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="8560b-153">Requirements</span></span>



| <span data-ttu-id="8560b-154">需求</span><span class="sxs-lookup"><span data-stu-id="8560b-154">Requirement</span></span> | <span data-ttu-id="8560b-155">值</span><span class="sxs-lookup"><span data-stu-id="8560b-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8560b-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8560b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="8560b-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8560b-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8560b-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8560b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="8560b-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8560b-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8560b-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="8560b-160">Namespace</span></span><br/>                | <span data-ttu-id="8560b-161">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8560b-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8560b-162">MOF</span><span class="sxs-lookup"><span data-stu-id="8560b-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8560b-163"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8560b-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8560b-164">DLL</span><span class="sxs-lookup"><span data-stu-id="8560b-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8560b-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8560b-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8560b-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8560b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8560b-167">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="8560b-167">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

