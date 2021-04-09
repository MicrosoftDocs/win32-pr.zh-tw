---
description: CIM \_ HostedFileSystem 關聯代表電腦系統與電腦系統上所裝載之檔案系統之間的連結。
ms.assetid: 1027fc6b-588b-4da8-8b3f-0c4c3328534a
ms.tgt_platform: multiple
title: CIM_HostedFileSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedFileSystem
- CIM_HostedFileSystem.PartComponent
- CIM_HostedFileSystem.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eef90ea3f1ed743ec5bee0eefa5afebc8c340077
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110849"
---
# <a name="cim_hostedfilesystem-class"></a><span data-ttu-id="32113-103">CIM \_ HostedFileSystem 類別</span><span class="sxs-lookup"><span data-stu-id="32113-103">CIM\_HostedFileSystem class</span></span>

<span data-ttu-id="32113-104">**CIM \_ HostedFileSystem** 關聯代表電腦系統與電腦系統上所裝載之檔案系統之間的連結。</span><span class="sxs-lookup"><span data-stu-id="32113-104">The **CIM\_HostedFileSystem** association represents a link between the computer system and the file system hosted on the computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32113-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="32113-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="32113-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="32113-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="32113-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="32113-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="32113-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="32113-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="32113-109">語法</span><span class="sxs-lookup"><span data-stu-id="32113-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC898-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_HostedFileSystem : CIM_SystemComponent
{
  CIM_FileSystem     REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="32113-110">成員</span><span class="sxs-lookup"><span data-stu-id="32113-110">Members</span></span>

<span data-ttu-id="32113-111">**CIM \_ HostedFileSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="32113-111">The **CIM\_HostedFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="32113-112">屬性</span><span class="sxs-lookup"><span data-stu-id="32113-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32113-113">屬性</span><span class="sxs-lookup"><span data-stu-id="32113-113">Properties</span></span>

<span data-ttu-id="32113-114">**CIM \_ HostedFileSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="32113-114">The **CIM\_HostedFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32113-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="32113-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32113-116">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="32113-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="32113-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32113-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32113-118">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="32113-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="32113-119">描述 [**電腦 \_ 系統的 CIM**](cim-computersystem.md) 系統。</span><span class="sxs-lookup"><span data-stu-id="32113-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="32113-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="32113-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32113-121">資料類型： **CIM \_ 檔案系統**</span><span class="sxs-lookup"><span data-stu-id="32113-121">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="32113-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32113-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32113-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="32113-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="32113-124">[**CIM 檔 \_ 系統**](cim-filesystem.md)，描述電腦系統所擁有的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="32113-124">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system owned by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32113-125">備註</span><span class="sxs-lookup"><span data-stu-id="32113-125">Remarks</span></span>

<span data-ttu-id="32113-126">**Cim \_ HostedFileSystem** 類別衍生自 [**cim \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="32113-126">The **CIM\_HostedFileSystem** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="32113-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="32113-127">WMI does not implement this class.</span></span>

<span data-ttu-id="32113-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="32113-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="32113-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="32113-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="32113-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="32113-130">Requirements</span></span>



| <span data-ttu-id="32113-131">需求</span><span class="sxs-lookup"><span data-stu-id="32113-131">Requirement</span></span> | <span data-ttu-id="32113-132">值</span><span class="sxs-lookup"><span data-stu-id="32113-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32113-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32113-133">Minimum supported client</span></span><br/> | <span data-ttu-id="32113-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32113-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32113-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32113-135">Minimum supported server</span></span><br/> | <span data-ttu-id="32113-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32113-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32113-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="32113-137">Namespace</span></span><br/>                | <span data-ttu-id="32113-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="32113-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32113-139">MOF</span><span class="sxs-lookup"><span data-stu-id="32113-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32113-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="32113-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32113-141">DLL</span><span class="sxs-lookup"><span data-stu-id="32113-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32113-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32113-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32113-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32113-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32113-144">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="32113-144">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

