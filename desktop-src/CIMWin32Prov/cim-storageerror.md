---
description: CIM \_ StorageError 類別代表因為錯誤而對應于使用中的媒體或記憶體空間區塊。 類別的索引鍵是錯誤中位元組的 StartingAddress 屬性。
ms.assetid: e786aa39-4718-416b-b659-bf4b8d3e2851
ms.tgt_platform: multiple
title: CIM_StorageError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageError
- CIM_StorageError.DeviceCreationClassName
- CIM_StorageError.DeviceID
- CIM_StorageError.EndingAddress
- CIM_StorageError.StartingAddress
- CIM_StorageError.SystemCreationClassName
- CIM_StorageError.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f5b197a5c82e61e054f5875fad466cac808ec38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972958"
---
# <a name="cim_storageerror-class"></a><span data-ttu-id="a2af2-104">CIM \_ StorageError 類別</span><span class="sxs-lookup"><span data-stu-id="a2af2-104">CIM\_StorageError class</span></span>

<span data-ttu-id="a2af2-105">**CIM \_ StorageError** 類別代表因為錯誤而對應于使用中的媒體或記憶體空間區塊。</span><span class="sxs-lookup"><span data-stu-id="a2af2-105">The **CIM\_StorageError** class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="a2af2-106">類別的索引鍵是錯誤中位元組的 **StartingAddress** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a2af2-106">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2af2-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a2af2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a2af2-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a2af2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a2af2-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2af2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a2af2-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a2af2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2af2-111">語法</span><span class="sxs-lookup"><span data-stu-id="a2af2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{71312AB6-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_StorageError
{
  string DeviceCreationClassName;
  string DeviceID;
  uint64 EndingAddress;
  uint64 StartingAddress;
  string SystemCreationClassName;
  string SystemName;
};
```

## <a name="members"></a><span data-ttu-id="a2af2-112">成員</span><span class="sxs-lookup"><span data-stu-id="a2af2-112">Members</span></span>

<span data-ttu-id="a2af2-113">**CIM \_ StorageError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a2af2-113">The **CIM\_StorageError** class has these types of members:</span></span>

-   [<span data-ttu-id="a2af2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a2af2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2af2-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a2af2-115">Properties</span></span>

<span data-ttu-id="a2af2-116">**CIM \_ StorageError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a2af2-116">The **CIM\_StorageError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2af2-117">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a2af2-117">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2af2-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2af2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2af2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageExtent**](cim-storageextent.md)。**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="a2af2-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="a2af2-121">設定存放區建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="a2af2-121">Scoping storage extent's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="a2af2-122">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a2af2-122">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2af2-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2af2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2af2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-125">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageExtent**](cim-storageextent.md)。**DeviceID**") </span><span class="sxs-lookup"><span data-stu-id="a2af2-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**DeviceID**")</span></span>
</dt> </dl>

<span data-ttu-id="a2af2-126">設定存放區裝置識別碼的範圍。</span><span class="sxs-lookup"><span data-stu-id="a2af2-126">Scoping storage extent's device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a2af2-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="a2af2-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2af2-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a2af2-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2af2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2af2-130">錯誤中位元組的結束位址。</span><span class="sxs-lookup"><span data-stu-id="a2af2-130">Ending address of the bytes in error.</span></span>

<span data-ttu-id="a2af2-131">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="a2af2-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a2af2-132">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="a2af2-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2af2-133">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a2af2-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2af2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-135">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a2af2-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a2af2-136">錯誤中位元組的起始位址。</span><span class="sxs-lookup"><span data-stu-id="a2af2-136">Starting address of the bytes in error.</span></span>

<span data-ttu-id="a2af2-137">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="a2af2-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a2af2-138">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a2af2-138">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2af2-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2af2-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2af2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-141">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageExtent**](cim-storageextent.md)。**SystemCreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="a2af2-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="a2af2-142">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="a2af2-142">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="a2af2-143">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a2af2-143">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2af2-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2af2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2af2-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2af2-146">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageExtent**](cim-storageextent.md)。**SystemName**") </span><span class="sxs-lookup"><span data-stu-id="a2af2-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemName**")</span></span>
</dt> </dl>

<span data-ttu-id="a2af2-147">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="a2af2-147">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2af2-148">備註</span><span class="sxs-lookup"><span data-stu-id="a2af2-148">Remarks</span></span>

<span data-ttu-id="a2af2-149">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a2af2-149">WMI does not implement this class.</span></span>

<span data-ttu-id="a2af2-150">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a2af2-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a2af2-151">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a2af2-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2af2-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2af2-152">Requirements</span></span>



| <span data-ttu-id="a2af2-153">需求</span><span class="sxs-lookup"><span data-stu-id="a2af2-153">Requirement</span></span> | <span data-ttu-id="a2af2-154">值</span><span class="sxs-lookup"><span data-stu-id="a2af2-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2af2-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2af2-155">Minimum supported client</span></span><br/> | <span data-ttu-id="a2af2-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2af2-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2af2-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2af2-157">Minimum supported server</span></span><br/> | <span data-ttu-id="a2af2-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2af2-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2af2-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="a2af2-159">Namespace</span></span><br/>                | <span data-ttu-id="a2af2-160">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2af2-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2af2-161">MOF</span><span class="sxs-lookup"><span data-stu-id="a2af2-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2af2-162"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2af2-162"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2af2-163">DLL</span><span class="sxs-lookup"><span data-stu-id="a2af2-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2af2-164"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2af2-164"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

