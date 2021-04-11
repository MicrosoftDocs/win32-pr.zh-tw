---
title: 'IBackgroundCopyJob GetDisplayName 方法 (>deliveryoptimization .h) '
description: 捕獲作業的顯示名稱。 一般而言，您會使用顯示名稱來識別使用者介面中的作業。
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName 方法
- GetDisplayName 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetDisplayName 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934856"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a><span data-ttu-id="1731c-107">IBackgroundCopyJob：： GetDisplayName 方法</span><span class="sxs-lookup"><span data-stu-id="1731c-107">IBackgroundCopyJob::GetDisplayName method</span></span>

<span data-ttu-id="1731c-108">捕獲作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1731c-108">Retrieves the display name for the job.</span></span> <span data-ttu-id="1731c-109">一般而言，您會使用顯示名稱來識別使用者介面中的作業。</span><span class="sxs-lookup"><span data-stu-id="1731c-109">Typically, you use the display name to identify the job in a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1731c-110">語法</span><span class="sxs-lookup"><span data-stu-id="1731c-110">Syntax</span></span>


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a><span data-ttu-id="1731c-111">參數</span><span class="sxs-lookup"><span data-stu-id="1731c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1731c-112">*ppDisplayName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1731c-112">*ppDisplayName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1731c-113">以 Null 終止的字串，其中包含識別作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1731c-113">Null-terminated string that contains the display name that identifies the job.</span></span> <span data-ttu-id="1731c-114">有一個以上的作業可以有相同的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1731c-114">More than one job can have the same display name.</span></span> <span data-ttu-id="1731c-115">完成時，呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式以釋放 *ppDisplayName* 。</span><span class="sxs-lookup"><span data-stu-id="1731c-115">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppDisplayName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1731c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1731c-116">Return value</span></span>

<span data-ttu-id="1731c-117">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="1731c-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="1731c-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1731c-118">Return code</span></span>                                                                                  | <span data-ttu-id="1731c-119">Description</span><span class="sxs-lookup"><span data-stu-id="1731c-119">Description</span></span>                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="1731c-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="1731c-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="1731c-121">已成功取出顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1731c-121">Display name was successfully retrieved.</span></span><br/>          |
| <dl> <span data-ttu-id="1731c-122"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1731c-122"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1731c-123">*PpDisplayName* 參數不可為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1731c-123">The *ppDisplayName* parameter cannot be **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1731c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1731c-124">Requirements</span></span>



| <span data-ttu-id="1731c-125">需求</span><span class="sxs-lookup"><span data-stu-id="1731c-125">Requirement</span></span> | <span data-ttu-id="1731c-126">值</span><span class="sxs-lookup"><span data-stu-id="1731c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1731c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1731c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1731c-128">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1731c-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1731c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1731c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1731c-130">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1731c-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1731c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="1731c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1731c-132"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="1731c-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="1731c-133">Idl</span><span class="sxs-lookup"><span data-stu-id="1731c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1731c-134"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1731c-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="1731c-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="1731c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="1731c-136"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1731c-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="1731c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1731c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1731c-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1731c-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="1731c-139">IID</span><span class="sxs-lookup"><span data-stu-id="1731c-139">IID</span></span><br/>                      | <span data-ttu-id="1731c-140">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="1731c-140">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1731c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1731c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1731c-142">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="1731c-142">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

