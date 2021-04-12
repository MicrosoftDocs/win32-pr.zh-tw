---
description: 將虛擬電腦系統的快照集集合匯出到檔案。 快照集集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Msvm_CollectionSnapshotService 類別的 ExportSnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192121"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="1a62c-104">Msvm CollectionSnapshotService 類別的 ExportSnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1a62c-104">ExportSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="1a62c-105">將虛擬電腦系統的快照集集合匯出到檔案。</span><span class="sxs-lookup"><span data-stu-id="1a62c-105">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="1a62c-106">快照集集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。</span><span class="sxs-lookup"><span data-stu-id="1a62c-106">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a62c-107">語法</span><span class="sxs-lookup"><span data-stu-id="1a62c-107">Syntax</span></span>


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1a62c-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a62c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a62c-109">*SnapshotCollection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a62c-109">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a62c-110">[**CIM \_ 集合**](cim-collection.md)的參考，代表要匯出的快照集集合。</span><span class="sxs-lookup"><span data-stu-id="1a62c-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="1a62c-111">*ExportDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a62c-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a62c-112">要匯出虛擬系統集合之目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1a62c-112">The fully-qualified path of the directory to which the virtual system collection is to be exported.</span></span> <span data-ttu-id="1a62c-113">如果 *ExportSettingData* 參數中的 **CreateVmExportSubdirectory** 屬性設定為 **True** ，則可以重複使用此目錄來匯出多個虛擬系統集合，這個方法會將每個虛擬系統集合定義放在此路徑底下的個別子目錄中。</span><span class="sxs-lookup"><span data-stu-id="1a62c-113">If the **CreateVmExportSubdirectory** property in the *ExportSettingData* parameter is set to **True** then this directory can be reused for exporting multiple virtual system collections and this method places each virtual system collection definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="1a62c-114">*ExportSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a62c-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a62c-115">[**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)的實例，表示匯出作業的設定。</span><span class="sxs-lookup"><span data-stu-id="1a62c-115">An instance of [**Msvm\_CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="1a62c-116">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1a62c-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a62c-117">如果以非同步方式執行作業，則會傳回選擇性的參考。</span><span class="sxs-lookup"><span data-stu-id="1a62c-117">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="1a62c-118">如果有，則會使用 [**CIM \_ ConcreteJob**](cim-concretejob.md) 實例的傳回參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="1a62c-118">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a62c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a62c-119">Return value</span></span>

<span data-ttu-id="1a62c-120">如果這個方法是以同步方式執行，它會在成功時傳回0。</span><span class="sxs-lookup"><span data-stu-id="1a62c-120">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="1a62c-121">如果這個方法是以非同步方式執行，它會傳回4096，而作業輸出參數可以用來追蹤非同步作業的進度。</span><span class="sxs-lookup"><span data-stu-id="1a62c-121">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="1a62c-122">任何其他傳回值表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a62c-122">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a62c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a62c-123">Requirements</span></span>



| <span data-ttu-id="1a62c-124">需求</span><span class="sxs-lookup"><span data-stu-id="1a62c-124">Requirement</span></span> | <span data-ttu-id="1a62c-125">值</span><span class="sxs-lookup"><span data-stu-id="1a62c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a62c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a62c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1a62c-127">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a62c-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1a62c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a62c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1a62c-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1a62c-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1a62c-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="1a62c-130">Namespace</span></span><br/>                | <span data-ttu-id="1a62c-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1a62c-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1a62c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1a62c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a62c-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1a62c-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a62c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1a62c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a62c-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a62c-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a62c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a62c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a62c-137">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="1a62c-137">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




