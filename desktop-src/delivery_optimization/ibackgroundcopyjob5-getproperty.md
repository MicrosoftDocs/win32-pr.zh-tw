---
title: 'IBackgroundCopyJob5 GetProperty 方法 (>deliveryoptimization .h) '
description: 取得傳遞最佳化 () 工作屬性的泛型方法。
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- GetProperty 方法
- GetProperty 方法，IBackgroundCopyJob5 介面
- IBackgroundCopyJob5 介面，GetProperty 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934465"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a><span data-ttu-id="4ac01-106">IBackgroundCopyJob5：： GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="4ac01-106">IBackgroundCopyJob5::GetProperty method</span></span>

<span data-ttu-id="4ac01-107">取得傳遞最佳化 () 工作屬性的泛型方法。</span><span class="sxs-lookup"><span data-stu-id="4ac01-107">A generic method for getting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ac01-108">語法</span><span class="sxs-lookup"><span data-stu-id="4ac01-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="4ac01-109">參數</span><span class="sxs-lookup"><span data-stu-id="4ac01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ac01-110">*PropertyId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ac01-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac01-111">取得指定為 [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) 列舉值之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ac01-111">The ID of the property that is being obtained specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="4ac01-112">*pPropertyValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4ac01-112">*pPropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac01-113">以 BITS_JOB_PROPERTY_VALUE 聯集傳回的屬性值。</span><span class="sxs-lookup"><span data-stu-id="4ac01-113">The property value returned as a BITS_JOB_PROPERTY_VALUE union.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ac01-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ac01-114">Return value</span></span>

<span data-ttu-id="4ac01-115">方法會傳回下列傳回值。</span><span class="sxs-lookup"><span data-stu-id="4ac01-115">The method returns the following return values.</span></span>



| <span data-ttu-id="4ac01-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4ac01-116">Return code</span></span>                                                                          | <span data-ttu-id="4ac01-117">Description</span><span class="sxs-lookup"><span data-stu-id="4ac01-117">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="4ac01-118"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4ac01-118"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="4ac01-119">Success</span><span class="sxs-lookup"><span data-stu-id="4ac01-119">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4ac01-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ac01-120">Requirements</span></span>



| <span data-ttu-id="4ac01-121">需求</span><span class="sxs-lookup"><span data-stu-id="4ac01-121">Requirement</span></span> | <span data-ttu-id="4ac01-122">值</span><span class="sxs-lookup"><span data-stu-id="4ac01-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac01-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ac01-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4ac01-124">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ac01-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ac01-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ac01-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4ac01-126">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ac01-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4ac01-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4ac01-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ac01-128"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ac01-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ac01-129">Idl</span><span class="sxs-lookup"><span data-stu-id="4ac01-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ac01-130"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ac01-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4ac01-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ac01-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ac01-132"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ac01-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4ac01-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4ac01-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ac01-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ac01-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4ac01-135">IID</span><span class="sxs-lookup"><span data-stu-id="4ac01-135">IID</span></span><br/>                      | <span data-ttu-id="4ac01-136">IID_IBackgroundCopyJob5 定義為 E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="4ac01-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="4ac01-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ac01-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac01-138">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="4ac01-138">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="4ac01-139">**IBackgroundCopyJob5：： SetProperty**</span><span class="sxs-lookup"><span data-stu-id="4ac01-139">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





