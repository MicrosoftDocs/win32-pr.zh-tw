---
title: 'IDeliveryOptimizationFile GetStats 方法 (>deliveryoptimization .h) '
description: 傳回特定檔案的下載和上傳統計資料。
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats 方法
- GetStats 方法，IDeliveryOptimizationFile 介面
- IDeliveryOptimizationFile 介面，GetStats 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385089"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a><span data-ttu-id="e5104-106">IDeliveryOptimizationFile：： GetStats 方法</span><span class="sxs-lookup"><span data-stu-id="e5104-106">IDeliveryOptimizationFile::GetStats method</span></span>

<span data-ttu-id="e5104-107">傳回特定檔案的下載和上傳統計資料。</span><span class="sxs-lookup"><span data-stu-id="e5104-107">Returns download and upload stats for a specific file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5104-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5104-108">Syntax</span></span>


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a><span data-ttu-id="e5104-109">參數</span><span class="sxs-lookup"><span data-stu-id="e5104-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5104-110">*swarmStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e5104-110">*swarmStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5104-111">傳回特定檔案的下載和上傳統計資料。</span><span class="sxs-lookup"><span data-stu-id="e5104-111">Returns download and upload stats for a specific file.</span></span> <span data-ttu-id="e5104-112">如需詳細資訊，請參閱 [**DOSwarmStats**](doswarmstats.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="e5104-112">See the [**DOSwarmStats**](doswarmstats.md) structure for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5104-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5104-113">Return value</span></span>

<span data-ttu-id="e5104-114">這個方法應該會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="e5104-114">This method should return **S_OK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5104-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5104-115">Requirements</span></span>



| <span data-ttu-id="e5104-116">需求</span><span class="sxs-lookup"><span data-stu-id="e5104-116">Requirement</span></span> | <span data-ttu-id="e5104-117">值</span><span class="sxs-lookup"><span data-stu-id="e5104-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5104-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5104-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5104-119">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5104-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e5104-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5104-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5104-121">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5104-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e5104-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e5104-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5104-123"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5104-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5104-124">Idl</span><span class="sxs-lookup"><span data-stu-id="e5104-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5104-125"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5104-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5104-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e5104-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5104-127"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5104-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e5104-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e5104-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5104-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5104-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e5104-130">IID</span><span class="sxs-lookup"><span data-stu-id="e5104-130">IID</span></span><br/>                      | <span data-ttu-id="e5104-131">IID_IDeliveryOptimizationFile 定義為 B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="e5104-131">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e5104-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5104-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5104-133">**IDeliveryOptimizationFile**</span><span class="sxs-lookup"><span data-stu-id="e5104-133">**IDeliveryOptimizationFile**</span></span>](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





