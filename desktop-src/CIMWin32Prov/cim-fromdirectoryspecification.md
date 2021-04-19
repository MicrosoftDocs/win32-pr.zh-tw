---
description: CIM \_ FromDirectorySpecification 關聯會識別檔案動作的來原始目錄。
ms.assetid: 031ff95f-aa68-4b05-92a6-97a5e0d8956f
ms.tgt_platform: multiple
title: CIM_FromDirectorySpecification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectorySpecification
- CIM_FromDirectorySpecification.FileName
- CIM_FromDirectorySpecification.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7690514b46d89bdf1aa926438456c49598034700
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000049"
---
# <a name="cim_fromdirectoryspecification-class"></a><span data-ttu-id="a1e54-103">CIM \_ FromDirectorySpecification 類別</span><span class="sxs-lookup"><span data-stu-id="a1e54-103">CIM\_FromDirectorySpecification class</span></span>

<span data-ttu-id="a1e54-104">**CIM \_ FromDirectorySpecification** 關聯會識別檔案動作的來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="a1e54-104">The **CIM\_FromDirectorySpecification** association identifies the source directory for the file action.</span></span> <span data-ttu-id="a1e54-105">使用這個關聯時，假設來原始目錄已經存在。</span><span class="sxs-lookup"><span data-stu-id="a1e54-105">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="a1e54-106">此關聯無法與 [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) 關聯存在; 檔案動作只能包含單一來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="a1e54-106">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1e54-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a1e54-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a1e54-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a1e54-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a1e54-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a1e54-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a1e54-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a1e54-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e54-111">語法</span><span class="sxs-lookup"><span data-stu-id="a1e54-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6715375E-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectorySpecification
{
  CIM_FileAction             REF FileName;
  CIM_DirectorySpecification REF SourceDirectory;
};
```

## <a name="members"></a><span data-ttu-id="a1e54-112">成員</span><span class="sxs-lookup"><span data-stu-id="a1e54-112">Members</span></span>

<span data-ttu-id="a1e54-113">**CIM \_ FromDirectorySpecification** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a1e54-113">The **CIM\_FromDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="a1e54-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a1e54-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1e54-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a1e54-115">Properties</span></span>

<span data-ttu-id="a1e54-116">**CIM \_ FromDirectorySpecification** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a1e54-116">The **CIM\_FromDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1e54-117">**FileName**</span><span class="sxs-lookup"><span data-stu-id="a1e54-117">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1e54-118">資料類型： **CIM \_ FileAction**</span><span class="sxs-lookup"><span data-stu-id="a1e54-118">Data type: **CIM\_FileAction**</span></span>
</dt> <dt>

<span data-ttu-id="a1e54-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1e54-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1e54-120">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="a1e54-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="a1e54-121">檔案名的參考。</span><span class="sxs-lookup"><span data-stu-id="a1e54-121">Reference to the file name.</span></span>

</dd> <dt>

<span data-ttu-id="a1e54-122">**SourceDirectory**</span><span class="sxs-lookup"><span data-stu-id="a1e54-122">**SourceDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1e54-123">資料類型： **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="a1e54-123">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="a1e54-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1e54-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1e54-125">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ， [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="a1e54-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="a1e54-126">來原始目錄的參考。</span><span class="sxs-lookup"><span data-stu-id="a1e54-126">Reference to the source directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1e54-127">備註</span><span class="sxs-lookup"><span data-stu-id="a1e54-127">Remarks</span></span>

<span data-ttu-id="a1e54-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a1e54-128">WMI does not implement this class.</span></span>

<span data-ttu-id="a1e54-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a1e54-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a1e54-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a1e54-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e54-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1e54-131">Requirements</span></span>



| <span data-ttu-id="a1e54-132">需求</span><span class="sxs-lookup"><span data-stu-id="a1e54-132">Requirement</span></span> | <span data-ttu-id="a1e54-133">值</span><span class="sxs-lookup"><span data-stu-id="a1e54-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e54-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1e54-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e54-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1e54-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1e54-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1e54-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e54-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1e54-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1e54-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1e54-138">Namespace</span></span><br/>                | <span data-ttu-id="a1e54-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a1e54-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a1e54-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a1e54-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1e54-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1e54-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1e54-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a1e54-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1e54-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1e54-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

