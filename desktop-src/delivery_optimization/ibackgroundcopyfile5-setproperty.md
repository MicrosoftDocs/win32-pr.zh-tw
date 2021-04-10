---
title: 'IBackgroundCopyFile5 SetProperty 方法 (>deliveryoptimization .h) '
description: 設定傳遞最佳化的泛型屬性 (是否) 檔案傳輸。
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty 方法
- SetProperty 方法，IBackgroundCopyFile5 介面
- IBackgroundCopyFile5 介面，SetProperty 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934283"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a><span data-ttu-id="3a4ee-106">IBackgroundCopyFile5：： SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="3a4ee-106">IBackgroundCopyFile5::SetProperty method</span></span>

<span data-ttu-id="3a4ee-107">設定傳遞最佳化的泛型屬性 (是否) 檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="3a4ee-107">Sets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4ee-108">語法</span><span class="sxs-lookup"><span data-stu-id="3a4ee-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="3a4ee-109">參數</span><span class="sxs-lookup"><span data-stu-id="3a4ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a4ee-110">*PropertyId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a4ee-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4ee-111">指定要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="3a4ee-111">Specifies the property to be set.</span></span>

</dd> <dt>

<span data-ttu-id="3a4ee-112">*ProertyValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3a4ee-112">*ProertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4ee-113">指定要設定之值的聯集指標。</span><span class="sxs-lookup"><span data-stu-id="3a4ee-113">A pointer to a union that specifies the value to be set.</span></span> <span data-ttu-id="3a4ee-114">使用適用于屬性識別碼的聯集成員。</span><span class="sxs-lookup"><span data-stu-id="3a4ee-114">The union member appropriate for the property ID is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a4ee-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a4ee-115">Return value</span></span>

<span data-ttu-id="3a4ee-116">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="3a4ee-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="3a4ee-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3a4ee-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4ee-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a4ee-118">Requirements</span></span>



| <span data-ttu-id="3a4ee-119">需求</span><span class="sxs-lookup"><span data-stu-id="3a4ee-119">Requirement</span></span> | <span data-ttu-id="3a4ee-120">值</span><span class="sxs-lookup"><span data-stu-id="3a4ee-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4ee-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a4ee-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4ee-122">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a4ee-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3a4ee-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a4ee-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4ee-124">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a4ee-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3a4ee-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3a4ee-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a4ee-126"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ee-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a4ee-127">Idl</span><span class="sxs-lookup"><span data-stu-id="3a4ee-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a4ee-128"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ee-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3a4ee-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="3a4ee-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a4ee-130"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ee-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3a4ee-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3a4ee-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a4ee-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ee-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3a4ee-133">IID</span><span class="sxs-lookup"><span data-stu-id="3a4ee-133">IID</span></span><br/>                      | <span data-ttu-id="3a4ee-134">IID_IBackgroundCopyFile5 定義為85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="3a4ee-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3a4ee-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a4ee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4ee-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="3a4ee-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="3a4ee-137">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="3a4ee-137">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





