---
description: 將參考點集合匯出到檔案。 參考點集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Msvm_CollectionReferencePointService 類別的 ExportReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981883"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="64561-104">Msvm CollectionReferencePointService 類別的 ExportReferencePoint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="64561-104">ExportReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="64561-105">將參考點集合匯出到檔案。</span><span class="sxs-lookup"><span data-stu-id="64561-105">Exports a reference point collection to a file.</span></span> <span data-ttu-id="64561-106">參考點集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。</span><span class="sxs-lookup"><span data-stu-id="64561-106">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="64561-107">語法</span><span class="sxs-lookup"><span data-stu-id="64561-107">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="64561-108">參數</span><span class="sxs-lookup"><span data-stu-id="64561-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64561-109">*ReferencePointCollection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64561-109">*ReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64561-110">[**CIM \_ 集合**](cim-collection.md)的參考，代表要匯出的參考點集合。</span><span class="sxs-lookup"><span data-stu-id="64561-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the reference point collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="64561-111">*ExportDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64561-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64561-112">要匯出參考點集合之目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="64561-112">The fully-qualified path of the directory to which the reference point collection is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="64561-113">*ExportSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64561-113">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64561-114">[**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md)的實例，表示匯出作業的設定。</span><span class="sxs-lookup"><span data-stu-id="64561-114">An instance of [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="64561-115">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="64561-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64561-116">如果以非同步方式執行作業，則會傳回選擇性的參考。</span><span class="sxs-lookup"><span data-stu-id="64561-116">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="64561-117">如果有，則會使用 [**CIM \_ ConcreteJob**](cim-concretejob.md) 實例的傳回參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="64561-117">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64561-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="64561-118">Return value</span></span>

<span data-ttu-id="64561-119">如果這個方法是以同步方式執行，它會在成功時傳回0。</span><span class="sxs-lookup"><span data-stu-id="64561-119">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="64561-120">如果這個方法是以非同步方式執行，它會傳回4096，而作業輸出參數可以用來追蹤非同步作業的進度。</span><span class="sxs-lookup"><span data-stu-id="64561-120">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="64561-121">任何其他傳回值表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="64561-121">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="64561-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="64561-122">Requirements</span></span>



| <span data-ttu-id="64561-123">需求</span><span class="sxs-lookup"><span data-stu-id="64561-123">Requirement</span></span> | <span data-ttu-id="64561-124">值</span><span class="sxs-lookup"><span data-stu-id="64561-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64561-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64561-125">Minimum supported client</span></span><br/> | <span data-ttu-id="64561-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64561-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="64561-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64561-127">Minimum supported server</span></span><br/> | <span data-ttu-id="64561-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="64561-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="64561-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="64561-129">Namespace</span></span><br/>                | <span data-ttu-id="64561-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="64561-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="64561-131">MOF</span><span class="sxs-lookup"><span data-stu-id="64561-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64561-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="64561-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64561-133">DLL</span><span class="sxs-lookup"><span data-stu-id="64561-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64561-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64561-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64561-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64561-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64561-136">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="64561-136">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




