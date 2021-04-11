---
description: CIM \_ DirectoryContainsFile 類別代表目錄和該目錄中包含的檔案之間的關聯。
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: CIM_DirectoryContainsFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847433"
---
# <a name="cim_directorycontainsfile-class"></a><span data-ttu-id="58d8d-103">CIM \_ DirectoryContainsFile 類別</span><span class="sxs-lookup"><span data-stu-id="58d8d-103">CIM\_DirectoryContainsFile class</span></span>

<span data-ttu-id="58d8d-104">**CIM \_ DirectoryContainsFile** 類別代表目錄和該目錄中包含的檔案之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="58d8d-104">The **CIM\_DirectoryContainsFile** class represents an association between a directory and files contained within that directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58d8d-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="58d8d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58d8d-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="58d8d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58d8d-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="58d8d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="58d8d-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="58d8d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d8d-109">語法</span><span class="sxs-lookup"><span data-stu-id="58d8d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="58d8d-110">成員</span><span class="sxs-lookup"><span data-stu-id="58d8d-110">Members</span></span>

<span data-ttu-id="58d8d-111">**CIM \_ DirectoryContainsFile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="58d8d-111">The **CIM\_DirectoryContainsFile** class has these types of members:</span></span>

-   [<span data-ttu-id="58d8d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="58d8d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58d8d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="58d8d-113">Properties</span></span>

<span data-ttu-id="58d8d-114">**CIM \_ DirectoryContainsFile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="58d8d-114">The **CIM\_DirectoryContainsFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58d8d-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="58d8d-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d8d-116">資料類型： **CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="58d8d-116">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="58d8d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58d8d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58d8d-118">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="58d8d-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="58d8d-119">描述目錄的 [**CIM \_ 目錄**](cim-directory.md) 。</span><span class="sxs-lookup"><span data-stu-id="58d8d-119">A [**CIM\_Directory**](cim-directory.md) that describes the directory.</span></span>

</dd> <dt>

<span data-ttu-id="58d8d-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="58d8d-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d8d-121">資料類型： **CIM 資料 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="58d8d-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="58d8d-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58d8d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58d8d-123">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="58d8d-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="58d8d-124">[**CIM \_ 資料檔案**](cim-datafile.md)，描述包含在目錄中的 LogicalFile。</span><span class="sxs-lookup"><span data-stu-id="58d8d-124">A [**CIM\_DataFile**](cim-datafile.md) that describes the LogicalFile contained within the directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58d8d-125">備註</span><span class="sxs-lookup"><span data-stu-id="58d8d-125">Remarks</span></span>

<span data-ttu-id="58d8d-126">WMI 會實作為動態類別的 **CIM \_ DirectoryContainsFile** 類別。</span><span class="sxs-lookup"><span data-stu-id="58d8d-126">WMI implements the **CIM\_DirectoryContainsFile** class, which is a dynamic class.</span></span>

<span data-ttu-id="58d8d-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="58d8d-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58d8d-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="58d8d-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d8d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="58d8d-129">Requirements</span></span>



| <span data-ttu-id="58d8d-130">需求</span><span class="sxs-lookup"><span data-stu-id="58d8d-130">Requirement</span></span> | <span data-ttu-id="58d8d-131">值</span><span class="sxs-lookup"><span data-stu-id="58d8d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58d8d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58d8d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="58d8d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58d8d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58d8d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58d8d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="58d8d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58d8d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58d8d-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="58d8d-136">Namespace</span></span><br/>                | <span data-ttu-id="58d8d-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58d8d-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58d8d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="58d8d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58d8d-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="58d8d-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58d8d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="58d8d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58d8d-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58d8d-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d8d-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58d8d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d8d-143">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="58d8d-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

