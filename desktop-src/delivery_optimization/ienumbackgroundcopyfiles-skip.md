---
title: 'IEnumBackgroundCopyFiles Skip 方法 (>deliveryoptimization. h) '
description: 略過列舉順序中的下一個指定元素數目。 如果序列中剩餘的元素少於所要求的專案數，則會略過序列中的最後一個元素。
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip 方法
- Skip 方法，IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，Skip 方法
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024740"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a><span data-ttu-id="75435-107">IEnumBackgroundCopyFiles：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="75435-107">IEnumBackgroundCopyFiles::Skip method</span></span>

<span data-ttu-id="75435-108">略過列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="75435-108">Skips the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="75435-109">如果序列中剩餘的元素少於所要求的專案數，則會略過序列中的最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="75435-109">If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="75435-110">語法</span><span class="sxs-lookup"><span data-stu-id="75435-110">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="75435-111">參數</span><span class="sxs-lookup"><span data-stu-id="75435-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75435-112">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75435-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75435-113">要略過的元素數目。</span><span class="sxs-lookup"><span data-stu-id="75435-113">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75435-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="75435-114">Return value</span></span>

<span data-ttu-id="75435-115">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="75435-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="75435-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="75435-116">Return code</span></span>                                                                              | <span data-ttu-id="75435-117">Description</span><span class="sxs-lookup"><span data-stu-id="75435-117">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="75435-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="75435-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="75435-119">已成功跳過要求的元素數目。</span><span class="sxs-lookup"><span data-stu-id="75435-119">Successfully skipped the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="75435-120"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="75435-120"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="75435-121">略過小於要求的元素數目。</span><span class="sxs-lookup"><span data-stu-id="75435-121">Skipped less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="75435-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="75435-122">Requirements</span></span>



| <span data-ttu-id="75435-123">需求</span><span class="sxs-lookup"><span data-stu-id="75435-123">Requirement</span></span> | <span data-ttu-id="75435-124">值</span><span class="sxs-lookup"><span data-stu-id="75435-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75435-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75435-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75435-126">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75435-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="75435-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75435-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75435-128">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75435-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="75435-129">標頭</span><span class="sxs-lookup"><span data-stu-id="75435-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="75435-130"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="75435-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="75435-131">Idl</span><span class="sxs-lookup"><span data-stu-id="75435-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75435-132"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="75435-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="75435-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="75435-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="75435-134"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="75435-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="75435-135">DLL</span><span class="sxs-lookup"><span data-stu-id="75435-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75435-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75435-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="75435-137">IID</span><span class="sxs-lookup"><span data-stu-id="75435-137">IID</span></span><br/>                      | <span data-ttu-id="75435-138">IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="75435-138">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="75435-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75435-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75435-140">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="75435-140">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





