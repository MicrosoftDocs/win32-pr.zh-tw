---
description: CIM \_ ToDirectoryAction 關聯會識別檔案動作的目標目錄。
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: CIM_ToDirectoryAction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ed2f7c2e2b46e63e2cc02cc8e6ce09ab2688e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689203"
---
# <a name="cim_todirectoryaction-class"></a><span data-ttu-id="0140c-103">CIM \_ ToDirectoryAction 類別</span><span class="sxs-lookup"><span data-stu-id="0140c-103">CIM\_ToDirectoryAction class</span></span>

<span data-ttu-id="0140c-104">**CIM \_ ToDirectoryAction** 關聯會識別檔案動作的目標目錄。</span><span class="sxs-lookup"><span data-stu-id="0140c-104">The **CIM\_ToDirectoryAction** association identifies the target directory for the file action.</span></span> <span data-ttu-id="0140c-105">使用這個關聯時，會假設目標目錄是由先前的動作所建立。</span><span class="sxs-lookup"><span data-stu-id="0140c-105">When this association is used, it is assumed that the target directory was created by a previous action.</span></span> <span data-ttu-id="0140c-106">此關聯無法與 [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) 關聯存在，因為檔案動作只能包含單一目標目錄。</span><span class="sxs-lookup"><span data-stu-id="0140c-106">This association cannot exist with a [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0140c-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0140c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0140c-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0140c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0140c-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0140c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0140c-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0140c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0140c-111">語法</span><span class="sxs-lookup"><span data-stu-id="0140c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="0140c-112">成員</span><span class="sxs-lookup"><span data-stu-id="0140c-112">Members</span></span>

<span data-ttu-id="0140c-113">**CIM \_ ToDirectoryAction** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0140c-113">The **CIM\_ToDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="0140c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0140c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0140c-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0140c-115">Properties</span></span>

<span data-ttu-id="0140c-116">**CIM \_ ToDirectoryAction** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0140c-116">The **CIM\_ToDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0140c-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="0140c-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0140c-118">資料類型： **CIM \_ DirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="0140c-118">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="0140c-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0140c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0140c-120">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ， [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="0140c-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="0140c-121">目的地目錄的參考。</span><span class="sxs-lookup"><span data-stu-id="0140c-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="0140c-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="0140c-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0140c-123">資料類型： **CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="0140c-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="0140c-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0140c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0140c-125">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="0140c-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="0140c-126">檔案名的參考。</span><span class="sxs-lookup"><span data-stu-id="0140c-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0140c-127">備註</span><span class="sxs-lookup"><span data-stu-id="0140c-127">Remarks</span></span>

<span data-ttu-id="0140c-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0140c-128">WMI does not implement this class.</span></span>

<span data-ttu-id="0140c-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0140c-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0140c-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0140c-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0140c-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0140c-131">Requirements</span></span>



| <span data-ttu-id="0140c-132">需求</span><span class="sxs-lookup"><span data-stu-id="0140c-132">Requirement</span></span> | <span data-ttu-id="0140c-133">值</span><span class="sxs-lookup"><span data-stu-id="0140c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0140c-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0140c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0140c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0140c-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0140c-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0140c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0140c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0140c-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0140c-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="0140c-138">Namespace</span></span><br/>                | <span data-ttu-id="0140c-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0140c-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0140c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0140c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0140c-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0140c-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0140c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0140c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0140c-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0140c-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

