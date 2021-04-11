---
description: CIM \_ 匯出類別代表本機檔案系統與其目錄之間的關聯，這表示指定的目錄可供掛接。
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: CIM_Export 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936318"
---
# <a name="cim_export-class"></a><span data-ttu-id="2966d-103">CIM \_ 匯出類別</span><span class="sxs-lookup"><span data-stu-id="2966d-103">CIM\_Export class</span></span>

<span data-ttu-id="2966d-104">**CIM \_ 匯出** 類別代表本機檔案系統與其目錄之間的關聯，這表示指定的目錄可供掛接。</span><span class="sxs-lookup"><span data-stu-id="2966d-104">The **CIM\_Export** class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="2966d-105">匯出整個檔案系統時，目錄應該參考檔案系統的最上層目錄。</span><span class="sxs-lookup"><span data-stu-id="2966d-105">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2966d-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2966d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2966d-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2966d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2966d-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2966d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2966d-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2966d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2966d-110">語法</span><span class="sxs-lookup"><span data-stu-id="2966d-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a><span data-ttu-id="2966d-111">成員</span><span class="sxs-lookup"><span data-stu-id="2966d-111">Members</span></span>

<span data-ttu-id="2966d-112">**CIM \_ 匯出** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2966d-112">The **CIM\_Export** class has these types of members:</span></span>

-   [<span data-ttu-id="2966d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2966d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2966d-114">屬性</span><span class="sxs-lookup"><span data-stu-id="2966d-114">Properties</span></span>

<span data-ttu-id="2966d-115">**CIM \_ 匯出** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2966d-115">The **CIM\_Export** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2966d-116">**目錄**</span><span class="sxs-lookup"><span data-stu-id="2966d-116">**Directory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2966d-117">資料類型： **CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="2966d-117">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="2966d-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2966d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2966d-119">參考針對網路檔案系統匯出的目錄 (NFS) 掛接。</span><span class="sxs-lookup"><span data-stu-id="2966d-119">Reference to the directory exported for network file system (NFS) mount.</span></span>

</dd> <dt>

<span data-ttu-id="2966d-120">**ExportedDirectoryName**</span><span class="sxs-lookup"><span data-stu-id="2966d-120">**ExportedDirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2966d-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2966d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2966d-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2966d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2966d-123">匯出目錄時所用的名稱。</span><span class="sxs-lookup"><span data-stu-id="2966d-123">Name under which the directory is exported.</span></span>

</dd> <dt>

<span data-ttu-id="2966d-124">**LocalFS**</span><span class="sxs-lookup"><span data-stu-id="2966d-124">**LocalFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2966d-125">資料類型： **CIM \_ LocalFileSystem**</span><span class="sxs-lookup"><span data-stu-id="2966d-125">Data type: **CIM\_LocalFileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="2966d-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2966d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2966d-127">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="2966d-127">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2966d-128">本機檔案系統的參考。</span><span class="sxs-lookup"><span data-stu-id="2966d-128">Reference to the local file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2966d-129">備註</span><span class="sxs-lookup"><span data-stu-id="2966d-129">Remarks</span></span>

<span data-ttu-id="2966d-130">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="2966d-130">WMI does not implement this class.</span></span>

<span data-ttu-id="2966d-131">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2966d-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2966d-132">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2966d-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2966d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2966d-133">Requirements</span></span>



| <span data-ttu-id="2966d-134">需求</span><span class="sxs-lookup"><span data-stu-id="2966d-134">Requirement</span></span> | <span data-ttu-id="2966d-135">值</span><span class="sxs-lookup"><span data-stu-id="2966d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2966d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2966d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2966d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2966d-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2966d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2966d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2966d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2966d-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2966d-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="2966d-140">Namespace</span></span><br/>                | <span data-ttu-id="2966d-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2966d-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2966d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2966d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2966d-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2966d-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2966d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2966d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2966d-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2966d-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

