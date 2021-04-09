---
title: 'IEnumBackgroundCopyFiles Next 方法 (>deliveryoptimization .h) '
description: 擷取列舉型別序列中指定的項目數目。 如果序列中剩餘的元素數目少於所要求的數目，則會抓取剩餘的元素。
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Next 方法
- Next 方法，IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，Next 方法
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934853"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a><span data-ttu-id="976b4-107">IEnumBackgroundCopyFiles：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="976b4-107">IEnumBackgroundCopyFiles::Next method</span></span>

<span data-ttu-id="976b4-108">擷取列舉型別序列中指定的項目數目。</span><span class="sxs-lookup"><span data-stu-id="976b4-108">Retrieves a specified number of items in the enumeration sequence.</span></span> <span data-ttu-id="976b4-109">如果序列中剩餘的元素數目少於所要求的數目，則會抓取剩餘的元素。</span><span class="sxs-lookup"><span data-stu-id="976b4-109">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="976b4-110">語法</span><span class="sxs-lookup"><span data-stu-id="976b4-110">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="976b4-111">參數</span><span class="sxs-lookup"><span data-stu-id="976b4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976b4-112">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="976b4-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="976b4-113">要求的元素數目。</span><span class="sxs-lookup"><span data-stu-id="976b4-113">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="976b4-114">*rgelt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="976b4-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="976b4-115">[**IBackgroundCopyFile**](ibackgroundcopyfile.md)物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="976b4-115">Array of [**IBackgroundCopyFile**](ibackgroundcopyfile.md) objects.</span></span> <span data-ttu-id="976b4-116">完成時，您必須釋放 *rgelt* 中的每個物件。</span><span class="sxs-lookup"><span data-stu-id="976b4-116">You must release each object in *rgelt* when done.</span></span>

</dd> <dt>

<span data-ttu-id="976b4-117">*pceltFetched* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="976b4-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="976b4-118">在 *rgelt* 中傳回的元素數目。</span><span class="sxs-lookup"><span data-stu-id="976b4-118">Number of elements returned in *rgelt*.</span></span> <span data-ttu-id="976b4-119">如果 *celt* 是一個，您可以將 *PceltFetched* 設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="976b4-119">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="976b4-120">否則，在呼叫這個方法之前，請先將 *pceltFetched* 的值初始化為0。</span><span class="sxs-lookup"><span data-stu-id="976b4-120">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976b4-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="976b4-121">Return value</span></span>

<span data-ttu-id="976b4-122">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="976b4-122">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="976b4-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="976b4-123">Return code</span></span>                                                                              | <span data-ttu-id="976b4-124">Description</span><span class="sxs-lookup"><span data-stu-id="976b4-124">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="976b4-125"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="976b4-125"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="976b4-126">已成功傳回要求的元素數目。</span><span class="sxs-lookup"><span data-stu-id="976b4-126">Successfully returned the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="976b4-127"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="976b4-127"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="976b4-128">傳回的數目小於要求的元素數目。</span><span class="sxs-lookup"><span data-stu-id="976b4-128">Returned less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="976b4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="976b4-129">Requirements</span></span>



| <span data-ttu-id="976b4-130">需求</span><span class="sxs-lookup"><span data-stu-id="976b4-130">Requirement</span></span> | <span data-ttu-id="976b4-131">值</span><span class="sxs-lookup"><span data-stu-id="976b4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="976b4-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="976b4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="976b4-133">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="976b4-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="976b4-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="976b4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="976b4-135">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="976b4-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="976b4-136">標頭</span><span class="sxs-lookup"><span data-stu-id="976b4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="976b4-137"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="976b4-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="976b4-138">Idl</span><span class="sxs-lookup"><span data-stu-id="976b4-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="976b4-139"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="976b4-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="976b4-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="976b4-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="976b4-141"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="976b4-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="976b4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="976b4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="976b4-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="976b4-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="976b4-144">IID</span><span class="sxs-lookup"><span data-stu-id="976b4-144">IID</span></span><br/>                      | <span data-ttu-id="976b4-145">IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="976b4-145">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="976b4-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="976b4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="976b4-147">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="976b4-147">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





