---
description: CIM \_ ToDirectorySpecification 關聯會識別檔案動作的目標目錄。
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: CIM_ToDirectorySpecification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0728f605e02195a6bf2bd4beb0ca67fe8744e12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111653"
---
# <a name="cim_todirectoryspecification-class"></a><span data-ttu-id="c33da-103">CIM \_ ToDirectorySpecification 類別</span><span class="sxs-lookup"><span data-stu-id="c33da-103">CIM\_ToDirectorySpecification class</span></span>

<span data-ttu-id="c33da-104">**CIM \_ ToDirectorySpecification** 關聯會識別檔案動作的目標目錄。</span><span class="sxs-lookup"><span data-stu-id="c33da-104">The **CIM\_ToDirectorySpecification** association identifies the target directory for the file action.</span></span> <span data-ttu-id="c33da-105">使用這個關聯時，會假設目標目錄已經存在。</span><span class="sxs-lookup"><span data-stu-id="c33da-105">When this association is used, it is assumed that the target directory already existed.</span></span> <span data-ttu-id="c33da-106">此關聯無法與 [**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) 關聯存在，因為檔案動作只能包含單一目標目錄。</span><span class="sxs-lookup"><span data-stu-id="c33da-106">This association cannot exist with a [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c33da-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c33da-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c33da-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="c33da-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c33da-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c33da-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c33da-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c33da-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33da-111">語法</span><span class="sxs-lookup"><span data-stu-id="c33da-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="c33da-112">成員</span><span class="sxs-lookup"><span data-stu-id="c33da-112">Members</span></span>

<span data-ttu-id="c33da-113">**CIM \_ ToDirectorySpecification** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c33da-113">The **CIM\_ToDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="c33da-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c33da-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c33da-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c33da-115">Properties</span></span>

<span data-ttu-id="c33da-116">**CIM \_ ToDirectorySpecification** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c33da-116">The **CIM\_ToDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c33da-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="c33da-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33da-118">資料類型： **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="c33da-118">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="c33da-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c33da-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33da-120">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ， [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="c33da-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c33da-121">目的地目錄的參考。</span><span class="sxs-lookup"><span data-stu-id="c33da-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="c33da-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="c33da-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33da-123">資料類型： **CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="c33da-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="c33da-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c33da-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33da-125">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="c33da-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c33da-126">檔案名的參考。</span><span class="sxs-lookup"><span data-stu-id="c33da-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c33da-127">備註</span><span class="sxs-lookup"><span data-stu-id="c33da-127">Remarks</span></span>

<span data-ttu-id="c33da-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="c33da-128">WMI does not implement this class.</span></span>

<span data-ttu-id="c33da-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="c33da-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c33da-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c33da-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33da-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c33da-131">Requirements</span></span>



| <span data-ttu-id="c33da-132">需求</span><span class="sxs-lookup"><span data-stu-id="c33da-132">Requirement</span></span> | <span data-ttu-id="c33da-133">值</span><span class="sxs-lookup"><span data-stu-id="c33da-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c33da-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c33da-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c33da-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c33da-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c33da-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c33da-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c33da-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c33da-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c33da-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="c33da-138">Namespace</span></span><br/>                | <span data-ttu-id="c33da-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c33da-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c33da-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c33da-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c33da-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c33da-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c33da-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c33da-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c33da-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c33da-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

