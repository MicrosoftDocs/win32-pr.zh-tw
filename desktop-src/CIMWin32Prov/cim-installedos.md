---
description: CIM \_ InstalledOS 關聯類別代表電腦系統與已安裝作業系統之間的連結。
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: CIM_InstalledOS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53e01be6a87fa6e5ef91ad6e8a81dbbddff4a576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510602"
---
# <a name="cim_installedos-class"></a><span data-ttu-id="1b216-103">CIM \_ InstalledOS 類別</span><span class="sxs-lookup"><span data-stu-id="1b216-103">CIM\_InstalledOS class</span></span>

<span data-ttu-id="1b216-104">**CIM \_ InstalledOS** 關聯類別代表電腦系統與已安裝作業系統之間的連結。</span><span class="sxs-lookup"><span data-stu-id="1b216-104">The **CIM\_InstalledOS** association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="1b216-105">作業系統會在電腦系統的儲存範圍內安裝 (例如，複製到磁片磁碟機或下載至記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="1b216-105">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b216-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1b216-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1b216-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1b216-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1b216-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b216-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1b216-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1b216-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b216-110">語法</span><span class="sxs-lookup"><span data-stu-id="1b216-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a><span data-ttu-id="1b216-111">成員</span><span class="sxs-lookup"><span data-stu-id="1b216-111">Members</span></span>

<span data-ttu-id="1b216-112">**CIM \_ InstalledOS** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1b216-112">The **CIM\_InstalledOS** class has these types of members:</span></span>

-   [<span data-ttu-id="1b216-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1b216-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b216-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1b216-114">Properties</span></span>

<span data-ttu-id="1b216-115">**CIM \_ InstalledOS** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1b216-115">The **CIM\_InstalledOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b216-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1b216-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b216-117">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="1b216-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1b216-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1b216-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b216-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="1b216-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1b216-120">描述電腦系統的 [**CIM \_**](cim-computersystem.md) 系統。</span><span class="sxs-lookup"><span data-stu-id="1b216-120">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="1b216-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1b216-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b216-122">資料類型： **CIM \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="1b216-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1b216-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1b216-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b216-124">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="1b216-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1b216-125">[**CIM 作業系統 \_**](cim-operatingsystem.md) ，描述電腦系統上所安裝的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1b216-125">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="1b216-126">**PrimaryOS**</span><span class="sxs-lookup"><span data-stu-id="1b216-126">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b216-127">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1b216-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b216-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1b216-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b216-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 作業系統 \| 001.4」 ) </span><span class="sxs-lookup"><span data-stu-id="1b216-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="1b216-130">若 **為 TRUE**，則表示已安裝的作業系統是電腦系統的預設作業系統。</span><span class="sxs-lookup"><span data-stu-id="1b216-130">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b216-131">備註</span><span class="sxs-lookup"><span data-stu-id="1b216-131">Remarks</span></span>

<span data-ttu-id="1b216-132">**Cim \_ InstalledOS** 類別衍生自 [**cim \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="1b216-132">The **CIM\_InstalledOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="1b216-133">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="1b216-133">WMI does not implement this class.</span></span> <span data-ttu-id="1b216-134">針對衍生自 **CIM \_ InstalledOS** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="1b216-134">For classes derived from **CIM\_InstalledOS**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1b216-135">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1b216-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1b216-136">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1b216-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b216-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b216-137">Requirements</span></span>



| <span data-ttu-id="1b216-138">需求</span><span class="sxs-lookup"><span data-stu-id="1b216-138">Requirement</span></span> | <span data-ttu-id="1b216-139">值</span><span class="sxs-lookup"><span data-stu-id="1b216-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b216-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b216-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1b216-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b216-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b216-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b216-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1b216-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b216-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b216-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="1b216-144">Namespace</span></span><br/>                | <span data-ttu-id="1b216-145">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1b216-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b216-146">MOF</span><span class="sxs-lookup"><span data-stu-id="1b216-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b216-147"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b216-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b216-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1b216-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b216-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b216-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b216-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b216-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b216-151">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="1b216-151">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

