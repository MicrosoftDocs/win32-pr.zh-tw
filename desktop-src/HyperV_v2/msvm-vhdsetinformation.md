---
description: 提供 VHD 設定檔案的相關資訊。
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Msvm_VHDSetInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 51f1371baea902627160c2c7a1fb31d156be8951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980954"
---
# <a name="msvm_vhdsetinformation-class"></a><span data-ttu-id="945c2-103">Msvm \_ VHDSetInformation 類別</span><span class="sxs-lookup"><span data-stu-id="945c2-103">Msvm\_VHDSetInformation class</span></span>

<span data-ttu-id="945c2-104">提供 VHD 設定檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="945c2-104">Provides information about a VHD Set file.</span></span>

<span data-ttu-id="945c2-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="945c2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="945c2-106">語法</span><span class="sxs-lookup"><span data-stu-id="945c2-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a><span data-ttu-id="945c2-107">成員</span><span class="sxs-lookup"><span data-stu-id="945c2-107">Members</span></span>

<span data-ttu-id="945c2-108">**Msvm \_ VHDSetInformation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="945c2-108">The **Msvm\_VHDSetInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="945c2-109">屬性</span><span class="sxs-lookup"><span data-stu-id="945c2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="945c2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="945c2-110">Properties</span></span>

<span data-ttu-id="945c2-111">**Msvm \_ VHDSetInformation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="945c2-111">The **Msvm\_VHDSetInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="945c2-112">**AllPaths**</span><span class="sxs-lookup"><span data-stu-id="945c2-112">**AllPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="945c2-113">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="945c2-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="945c2-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="945c2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="945c2-115">VHD 設定檔案包含的所有檔案的清單，包括任何未參考的檔案，以及根虛擬硬碟的任何父系。</span><span class="sxs-lookup"><span data-stu-id="945c2-115">A list of all files encompassed by the VHD Set file, including any unreferenced files and any parents of the root virtual hard disk.</span></span> <span data-ttu-id="945c2-116">根虛擬硬碟之後列出的所有檔案都不會由此 VHD 設定檔案來管理。</span><span class="sxs-lookup"><span data-stu-id="945c2-116">All files listed after the root virtual hard disk are unmanaged by this VHD Set file.</span></span> <span data-ttu-id="945c2-117">如果未特別要求此資訊，此欄位可能是空的。</span><span class="sxs-lookup"><span data-stu-id="945c2-117">This field may be empty if this information was not specifically requested.</span></span>

</dd> <dt>

<span data-ttu-id="945c2-118">**路徑**</span><span class="sxs-lookup"><span data-stu-id="945c2-118">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="945c2-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="945c2-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="945c2-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="945c2-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="945c2-121">VHD 設定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="945c2-121">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="945c2-122">**SnapshotIdList**</span><span class="sxs-lookup"><span data-stu-id="945c2-122">**SnapshotIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="945c2-123">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="945c2-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="945c2-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="945c2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="945c2-125">Guid 清單，代表這個 VHD 設定檔案所包含的所有快照集。</span><span class="sxs-lookup"><span data-stu-id="945c2-125">A list of GUIDs representing all of the snapshots contained by this VHD Set file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="945c2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="945c2-126">Requirements</span></span>



| <span data-ttu-id="945c2-127">需求</span><span class="sxs-lookup"><span data-stu-id="945c2-127">Requirement</span></span> | <span data-ttu-id="945c2-128">值</span><span class="sxs-lookup"><span data-stu-id="945c2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="945c2-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="945c2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="945c2-130">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="945c2-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="945c2-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="945c2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="945c2-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="945c2-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="945c2-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="945c2-133">Namespace</span></span><br/>                | <span data-ttu-id="945c2-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="945c2-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="945c2-135">MOF</span><span class="sxs-lookup"><span data-stu-id="945c2-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="945c2-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="945c2-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="945c2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="945c2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="945c2-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="945c2-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




