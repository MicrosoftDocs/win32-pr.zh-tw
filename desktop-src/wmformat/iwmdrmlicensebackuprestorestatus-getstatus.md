---
title: 'IWMDRMLicenseBackupRestoreStatus GetStatus 方法 (Wmdrmsdk .h) '
description: GetStatus 方法會抓取有關授權備份或還原作業的詳細狀態資訊。
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- GetStatus 方法 windows Media 格式
- GetStatus 方法 windows Media Format，IWMDRMLicenseBackupRestoreStatus 介面
- IWMDRMLicenseBackupRestoreStatus 介面 windows Media Format，GetStatus 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996267"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a><span data-ttu-id="1ac7b-106">IWMDRMLicenseBackupRestoreStatus：： GetStatus 方法</span><span class="sxs-lookup"><span data-stu-id="1ac7b-106">IWMDRMLicenseBackupRestoreStatus::GetStatus method</span></span>

<span data-ttu-id="1ac7b-107">**GetStatus** 方法會抓取有關授權備份或還原作業的詳細狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1ac7b-107">The **GetStatus** method retrieves detailed status information about a license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac7b-108">語法</span><span class="sxs-lookup"><span data-stu-id="1ac7b-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1ac7b-109">參數</span><span class="sxs-lookup"><span data-stu-id="1ac7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ac7b-110">*pStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1ac7b-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac7b-111">可接收狀態資訊之 [**WM \_ 備份 \_ 還原 \_ 狀態**](wm-backup-restore-status.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1ac7b-111">Pointer to a [**WM\_BACKUP\_RESTORE\_STATUS**](wm-backup-restore-status.md) structure that receives the status information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ac7b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ac7b-112">Return value</span></span>

<span data-ttu-id="1ac7b-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="1ac7b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1ac7b-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="1ac7b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1ac7b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1ac7b-115">Return code</span></span>                                                                          | <span data-ttu-id="1ac7b-116">Description</span><span class="sxs-lookup"><span data-stu-id="1ac7b-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1ac7b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1ac7b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1ac7b-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="1ac7b-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ac7b-119">備註</span><span class="sxs-lookup"><span data-stu-id="1ac7b-119">Remarks</span></span>

<span data-ttu-id="1ac7b-120">無。</span><span class="sxs-lookup"><span data-stu-id="1ac7b-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac7b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ac7b-121">Requirements</span></span>



| <span data-ttu-id="1ac7b-122">需求</span><span class="sxs-lookup"><span data-stu-id="1ac7b-122">Requirement</span></span> | <span data-ttu-id="1ac7b-123">值</span><span class="sxs-lookup"><span data-stu-id="1ac7b-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac7b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1ac7b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1ac7b-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ac7b-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ac7b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ac7b-126">Library</span></span><br/> | <dl> <span data-ttu-id="1ac7b-127"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ac7b-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ac7b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ac7b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac7b-129">**IWMDRMLicenseBackupRestoreStatus 介面**</span><span class="sxs-lookup"><span data-stu-id="1ac7b-129">**IWMDRMLicenseBackupRestoreStatus Interface**</span></span>](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





