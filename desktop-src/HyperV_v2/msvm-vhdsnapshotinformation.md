---
description: 提供 VHD 設定檔案中快照集的相關資訊。
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Msvm_VHDSnapshotInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848375"
---
# <a name="msvm_vhdsnapshotinformation-class"></a><span data-ttu-id="36585-103">Msvm \_ VHDSnapshotInformation 類別</span><span class="sxs-lookup"><span data-stu-id="36585-103">Msvm\_VHDSnapshotInformation class</span></span>

<span data-ttu-id="36585-104">提供 VHD 設定檔案中快照集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="36585-104">Provides information about a snapshot within a VHD Set file</span></span>

<span data-ttu-id="36585-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="36585-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="36585-106">語法</span><span class="sxs-lookup"><span data-stu-id="36585-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a><span data-ttu-id="36585-107">成員</span><span class="sxs-lookup"><span data-stu-id="36585-107">Members</span></span>

<span data-ttu-id="36585-108">**Msvm \_ VHDSnapshotInformation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="36585-108">The **Msvm\_VHDSnapshotInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="36585-109">屬性</span><span class="sxs-lookup"><span data-stu-id="36585-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36585-110">屬性</span><span class="sxs-lookup"><span data-stu-id="36585-110">Properties</span></span>

<span data-ttu-id="36585-111">**Msvm \_ VHDSnapshotInformation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="36585-111">The **Msvm\_VHDSnapshotInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36585-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="36585-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36585-113">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="36585-113">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="36585-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36585-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36585-115">建立此快照集的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="36585-115">The date and time of this snapshot's creation.</span></span>

</dd> <dt>

<span data-ttu-id="36585-116">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="36585-116">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36585-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36585-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36585-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36585-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36585-119">VHD 設定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="36585-119">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="36585-120">**ParentPathsList**</span><span class="sxs-lookup"><span data-stu-id="36585-120">**ParentPathsList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36585-121">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="36585-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36585-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36585-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36585-123">檔案路徑的清單，代表這個快照相依的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="36585-123">A list of file paths representing all of the files on which this snapshot depends.</span></span> <span data-ttu-id="36585-124">除非特別要求，否則此欄位將是空的。</span><span class="sxs-lookup"><span data-stu-id="36585-124">This field will be empty unless specifically requested.</span></span> <span data-ttu-id="36585-125">第一個專案是檔案的直屬父系，最後一個專案是根目錄。</span><span class="sxs-lookup"><span data-stu-id="36585-125">The first entry is the file's immediate parent, with the last entry being the root.</span></span>

</dd> <dt>

<span data-ttu-id="36585-126">**ResilientChangeTrackingId**</span><span class="sxs-lookup"><span data-stu-id="36585-126">**ResilientChangeTrackingId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36585-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36585-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36585-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36585-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36585-129">與此快照集相關聯的復原變更追蹤識別碼（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="36585-129">The resilient change tracking ID, if any, associated with this snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="36585-130">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="36585-130">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36585-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36585-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36585-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36585-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36585-133">可在 VHD 設定檔案中唯一識別此快照集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="36585-133">A GUID that uniquely identifies this snapshot within the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="36585-134">**SnapshotPath**</span><span class="sxs-lookup"><span data-stu-id="36585-134">**SnapshotPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36585-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36585-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36585-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36585-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36585-137">此快照所表示之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="36585-137">The path of the file represented by this snapshot.</span></span> <span data-ttu-id="36585-138">如果沒有與此快照集相關聯的檔案，此欄位可能是空的。</span><span class="sxs-lookup"><span data-stu-id="36585-138">This field may be empty if there is no file associated with this snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36585-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="36585-139">Requirements</span></span>



| <span data-ttu-id="36585-140">需求</span><span class="sxs-lookup"><span data-stu-id="36585-140">Requirement</span></span> | <span data-ttu-id="36585-141">值</span><span class="sxs-lookup"><span data-stu-id="36585-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36585-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36585-142">Minimum supported client</span></span><br/> | <span data-ttu-id="36585-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36585-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="36585-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36585-144">Minimum supported server</span></span><br/> | <span data-ttu-id="36585-145">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="36585-145">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="36585-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="36585-146">Namespace</span></span><br/>                | <span data-ttu-id="36585-147">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="36585-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="36585-148">MOF</span><span class="sxs-lookup"><span data-stu-id="36585-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36585-149"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="36585-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36585-150">DLL</span><span class="sxs-lookup"><span data-stu-id="36585-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36585-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36585-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




